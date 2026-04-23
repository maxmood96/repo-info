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
-	[`mysql:8.0.46`](#mysql8046)
-	[`mysql:8.0.46-bookworm`](#mysql8046-bookworm)
-	[`mysql:8.0.46-debian`](#mysql8046-debian)
-	[`mysql:8.0.46-oracle`](#mysql8046-oracle)
-	[`mysql:8.0.46-oraclelinux9`](#mysql8046-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.9`](#mysql849)
-	[`mysql:8.4.9-oracle`](#mysql849-oracle)
-	[`mysql:8.4.9-oraclelinux9`](#mysql849-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.7`](#mysql97)
-	[`mysql:9.7-oracle`](#mysql97-oracle)
-	[`mysql:9.7-oraclelinux9`](#mysql97-oraclelinux9)
-	[`mysql:9.7.0`](#mysql970)
-	[`mysql:9.7.0-oracle`](#mysql970-oracle)
-	[`mysql:9.7.0-oraclelinux9`](#mysql970-oraclelinux9)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:lts`](#mysqllts)
-	[`mysql:lts-oracle`](#mysqllts-oracle)
-	[`mysql:lts-oraclelinux9`](#mysqllts-oraclelinux9)
-	[`mysql:oracle`](#mysqloracle)
-	[`mysql:oraclelinux9`](#mysqloraclelinux9)

## `mysql:8`

```console
$ docker pull mysql@sha256:43bd9764df60666fb2ba2cf8217dd17b3d2414c150005d2fdd07a0cd73d3b7f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:8096dd88a82dad3741f292e282d36b577097926735aeee8960c9b8c759453bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238250587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c55658453cceab502e6a7f2d3abe7292180c6f71f463972bcae809304979c06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 23:18:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 20 Apr 2026 23:18:18 GMT
ENV GOSU_VERSION=1.19
# Mon, 20 Apr 2026 23:18:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 20 Apr 2026 23:18:44 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:19:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 20 Apr 2026 23:19:48 GMT
VOLUME [/var/lib/mysql]
# Mon, 20 Apr 2026 23:19:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:19:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 20 Apr 2026 23:19:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f035ba2a42b8a1b8f5674047539d50309c58d7c0bf025d946c8f93adad50a897`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9c5f1fb9544e1b87160680d79634b2756df9965406bd997d83f86b1d3f189c`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b565c834d59fd84b7e92785e9a9accffe3a2cbdbc7ebfb500176b62589acb11`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 6.2 MB (6170286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6e6468bcd71dd7e73c59c8ff211f3c3289b5689095efa58d80e7c7ccbfd766`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df58ba29e4716abfaa57ad92746073b6fdb2edc9ade56de9beacae40efc1ca54`  
		Last Modified: Mon, 20 Apr 2026 23:20:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506bcb676d56150811d81dfeecf8c775ce1d8e9e3e42fcaff4cebedef91e668d`  
		Last Modified: Mon, 20 Apr 2026 23:20:23 GMT  
		Size: 51.6 MB (51577760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a156be315d3009791029be3f35d7721f77d2f89b4c7c375fc21c6df01f33f5`  
		Last Modified: Mon, 20 Apr 2026 23:20:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b97080db618a59c7c1070d873c7676532d8130e4bd4abdc2b6da3010cad2ef1`  
		Last Modified: Mon, 20 Apr 2026 23:20:25 GMT  
		Size: 132.4 MB (132399697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182cd03161a6cc330cb3179e00ff03735060afe188a3c76b53de39ef68999458`  
		Last Modified: Mon, 20 Apr 2026 23:20:22 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:7223a3adb58c8156d99db3de7f6342b5147e32d330f3d08bc4ec098100c6f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15745116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc67f490818bb61b95b6408046b9c5243613c72188b7cf80013e7d060e813ba`

```dockerfile
```

-	Layers:
	-	`sha256:1201b5e782671f22800dff24fcf7729c366d7a8337fbf14c030bd213872a8460`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 15.7 MB (15710908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a530fb7783681a437b82d56d63db4aabe40bffb3f30296334a72c46875fd8b05`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b7ed149136988390cae1671eaf6b0697862623a9fa7ddc8777fc7722c0202895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233045862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56936cd75b2986359042279d478d41ddfdd00cd71cb130d68c61022db4707f9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 23:14:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 20 Apr 2026 23:14:58 GMT
ENV GOSU_VERSION=1.19
# Mon, 20 Apr 2026 23:14:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 20 Apr 2026 23:15:26 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:16:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 20 Apr 2026 23:16:36 GMT
VOLUME [/var/lib/mysql]
# Mon, 20 Apr 2026 23:16:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:16:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 20 Apr 2026 23:16:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a399ba9772226ad05fc45b09486adaff0390a7a25d9acda9819ecaa0f1e63d4f`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc07e22dc332f1680db8d5b4b7af4819586de6467b5f7f7f4c30ef46ed280d`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d41ef28c6723b46e3cab697745ea772e477b2518d13e301db151b61742345e0`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 5.8 MB (5793247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4f50cc254bbb68037b0d7fc835c251d31470f308ba8a2124c1d185b2c9f0a3`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c8ae92d35fb8a44794be7bb1ec22650ee3fb2f7903c8a966ade3af1fc80d83`  
		Last Modified: Mon, 20 Apr 2026 23:17:08 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757bc719f797504a0979fa4f8ce02238dd52823a0632c3bb6ed26bcc38ddecb1`  
		Last Modified: Mon, 20 Apr 2026 23:17:10 GMT  
		Size: 49.8 MB (49827767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca20ece91f44e5655427eed64840d8ef712de22c13f7a72775ab55dd659d36c`  
		Last Modified: Mon, 20 Apr 2026 23:17:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e8458c4ba6e54bce45741648c81c4a86874636c2131f149d2fde04115f2395`  
		Last Modified: Mon, 20 Apr 2026 23:17:13 GMT  
		Size: 130.8 MB (130778054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e967d5df3dfeddf636fe21b8267a213c56fb0101310ab536b03ec7ea673b659`  
		Last Modified: Mon, 20 Apr 2026 23:17:10 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:b68801a94249dca9abfa20e5adc37e05a40bba3101ccbf6af110f235234a17fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1486769bd3d1cc7c2392fe3ddbe873d685a118902324d049806adb91669f44e`

```dockerfile
```

-	Layers:
	-	`sha256:113cd58fe861869dadb0d755929aad301cb3ccc8489c76764c4181d8d9111035`  
		Last Modified: Mon, 20 Apr 2026 23:17:08 GMT  
		Size: 15.7 MB (15709328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dbe4130d194d2bd90f313c72d219b95b4b827ee15b2ff641c775b68ab304fa5`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:43bd9764df60666fb2ba2cf8217dd17b3d2414c150005d2fdd07a0cd73d3b7f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8096dd88a82dad3741f292e282d36b577097926735aeee8960c9b8c759453bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238250587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c55658453cceab502e6a7f2d3abe7292180c6f71f463972bcae809304979c06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 23:18:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 20 Apr 2026 23:18:18 GMT
ENV GOSU_VERSION=1.19
# Mon, 20 Apr 2026 23:18:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 20 Apr 2026 23:18:44 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:19:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 20 Apr 2026 23:19:48 GMT
VOLUME [/var/lib/mysql]
# Mon, 20 Apr 2026 23:19:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:19:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 20 Apr 2026 23:19:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f035ba2a42b8a1b8f5674047539d50309c58d7c0bf025d946c8f93adad50a897`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9c5f1fb9544e1b87160680d79634b2756df9965406bd997d83f86b1d3f189c`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b565c834d59fd84b7e92785e9a9accffe3a2cbdbc7ebfb500176b62589acb11`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 6.2 MB (6170286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6e6468bcd71dd7e73c59c8ff211f3c3289b5689095efa58d80e7c7ccbfd766`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df58ba29e4716abfaa57ad92746073b6fdb2edc9ade56de9beacae40efc1ca54`  
		Last Modified: Mon, 20 Apr 2026 23:20:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506bcb676d56150811d81dfeecf8c775ce1d8e9e3e42fcaff4cebedef91e668d`  
		Last Modified: Mon, 20 Apr 2026 23:20:23 GMT  
		Size: 51.6 MB (51577760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a156be315d3009791029be3f35d7721f77d2f89b4c7c375fc21c6df01f33f5`  
		Last Modified: Mon, 20 Apr 2026 23:20:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b97080db618a59c7c1070d873c7676532d8130e4bd4abdc2b6da3010cad2ef1`  
		Last Modified: Mon, 20 Apr 2026 23:20:25 GMT  
		Size: 132.4 MB (132399697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182cd03161a6cc330cb3179e00ff03735060afe188a3c76b53de39ef68999458`  
		Last Modified: Mon, 20 Apr 2026 23:20:22 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7223a3adb58c8156d99db3de7f6342b5147e32d330f3d08bc4ec098100c6f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15745116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc67f490818bb61b95b6408046b9c5243613c72188b7cf80013e7d060e813ba`

```dockerfile
```

-	Layers:
	-	`sha256:1201b5e782671f22800dff24fcf7729c366d7a8337fbf14c030bd213872a8460`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 15.7 MB (15710908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a530fb7783681a437b82d56d63db4aabe40bffb3f30296334a72c46875fd8b05`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b7ed149136988390cae1671eaf6b0697862623a9fa7ddc8777fc7722c0202895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233045862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56936cd75b2986359042279d478d41ddfdd00cd71cb130d68c61022db4707f9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 23:14:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 20 Apr 2026 23:14:58 GMT
ENV GOSU_VERSION=1.19
# Mon, 20 Apr 2026 23:14:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 20 Apr 2026 23:15:26 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:16:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 20 Apr 2026 23:16:36 GMT
VOLUME [/var/lib/mysql]
# Mon, 20 Apr 2026 23:16:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:16:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 20 Apr 2026 23:16:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a399ba9772226ad05fc45b09486adaff0390a7a25d9acda9819ecaa0f1e63d4f`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc07e22dc332f1680db8d5b4b7af4819586de6467b5f7f7f4c30ef46ed280d`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d41ef28c6723b46e3cab697745ea772e477b2518d13e301db151b61742345e0`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 5.8 MB (5793247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4f50cc254bbb68037b0d7fc835c251d31470f308ba8a2124c1d185b2c9f0a3`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c8ae92d35fb8a44794be7bb1ec22650ee3fb2f7903c8a966ade3af1fc80d83`  
		Last Modified: Mon, 20 Apr 2026 23:17:08 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757bc719f797504a0979fa4f8ce02238dd52823a0632c3bb6ed26bcc38ddecb1`  
		Last Modified: Mon, 20 Apr 2026 23:17:10 GMT  
		Size: 49.8 MB (49827767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca20ece91f44e5655427eed64840d8ef712de22c13f7a72775ab55dd659d36c`  
		Last Modified: Mon, 20 Apr 2026 23:17:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e8458c4ba6e54bce45741648c81c4a86874636c2131f149d2fde04115f2395`  
		Last Modified: Mon, 20 Apr 2026 23:17:13 GMT  
		Size: 130.8 MB (130778054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e967d5df3dfeddf636fe21b8267a213c56fb0101310ab536b03ec7ea673b659`  
		Last Modified: Mon, 20 Apr 2026 23:17:10 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b68801a94249dca9abfa20e5adc37e05a40bba3101ccbf6af110f235234a17fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1486769bd3d1cc7c2392fe3ddbe873d685a118902324d049806adb91669f44e`

```dockerfile
```

-	Layers:
	-	`sha256:113cd58fe861869dadb0d755929aad301cb3ccc8489c76764c4181d8d9111035`  
		Last Modified: Mon, 20 Apr 2026 23:17:08 GMT  
		Size: 15.7 MB (15709328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dbe4130d194d2bd90f313c72d219b95b4b827ee15b2ff641c775b68ab304fa5`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:43bd9764df60666fb2ba2cf8217dd17b3d2414c150005d2fdd07a0cd73d3b7f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:8096dd88a82dad3741f292e282d36b577097926735aeee8960c9b8c759453bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238250587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c55658453cceab502e6a7f2d3abe7292180c6f71f463972bcae809304979c06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 23:18:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 20 Apr 2026 23:18:18 GMT
ENV GOSU_VERSION=1.19
# Mon, 20 Apr 2026 23:18:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 20 Apr 2026 23:18:44 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:19:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 20 Apr 2026 23:19:48 GMT
VOLUME [/var/lib/mysql]
# Mon, 20 Apr 2026 23:19:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:19:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 20 Apr 2026 23:19:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f035ba2a42b8a1b8f5674047539d50309c58d7c0bf025d946c8f93adad50a897`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9c5f1fb9544e1b87160680d79634b2756df9965406bd997d83f86b1d3f189c`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b565c834d59fd84b7e92785e9a9accffe3a2cbdbc7ebfb500176b62589acb11`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 6.2 MB (6170286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6e6468bcd71dd7e73c59c8ff211f3c3289b5689095efa58d80e7c7ccbfd766`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df58ba29e4716abfaa57ad92746073b6fdb2edc9ade56de9beacae40efc1ca54`  
		Last Modified: Mon, 20 Apr 2026 23:20:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506bcb676d56150811d81dfeecf8c775ce1d8e9e3e42fcaff4cebedef91e668d`  
		Last Modified: Mon, 20 Apr 2026 23:20:23 GMT  
		Size: 51.6 MB (51577760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a156be315d3009791029be3f35d7721f77d2f89b4c7c375fc21c6df01f33f5`  
		Last Modified: Mon, 20 Apr 2026 23:20:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b97080db618a59c7c1070d873c7676532d8130e4bd4abdc2b6da3010cad2ef1`  
		Last Modified: Mon, 20 Apr 2026 23:20:25 GMT  
		Size: 132.4 MB (132399697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182cd03161a6cc330cb3179e00ff03735060afe188a3c76b53de39ef68999458`  
		Last Modified: Mon, 20 Apr 2026 23:20:22 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7223a3adb58c8156d99db3de7f6342b5147e32d330f3d08bc4ec098100c6f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15745116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc67f490818bb61b95b6408046b9c5243613c72188b7cf80013e7d060e813ba`

```dockerfile
```

-	Layers:
	-	`sha256:1201b5e782671f22800dff24fcf7729c366d7a8337fbf14c030bd213872a8460`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 15.7 MB (15710908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a530fb7783681a437b82d56d63db4aabe40bffb3f30296334a72c46875fd8b05`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b7ed149136988390cae1671eaf6b0697862623a9fa7ddc8777fc7722c0202895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233045862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56936cd75b2986359042279d478d41ddfdd00cd71cb130d68c61022db4707f9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 23:14:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 20 Apr 2026 23:14:58 GMT
ENV GOSU_VERSION=1.19
# Mon, 20 Apr 2026 23:14:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 20 Apr 2026 23:15:26 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:16:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 20 Apr 2026 23:16:36 GMT
VOLUME [/var/lib/mysql]
# Mon, 20 Apr 2026 23:16:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:16:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 20 Apr 2026 23:16:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a399ba9772226ad05fc45b09486adaff0390a7a25d9acda9819ecaa0f1e63d4f`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc07e22dc332f1680db8d5b4b7af4819586de6467b5f7f7f4c30ef46ed280d`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d41ef28c6723b46e3cab697745ea772e477b2518d13e301db151b61742345e0`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 5.8 MB (5793247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4f50cc254bbb68037b0d7fc835c251d31470f308ba8a2124c1d185b2c9f0a3`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c8ae92d35fb8a44794be7bb1ec22650ee3fb2f7903c8a966ade3af1fc80d83`  
		Last Modified: Mon, 20 Apr 2026 23:17:08 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757bc719f797504a0979fa4f8ce02238dd52823a0632c3bb6ed26bcc38ddecb1`  
		Last Modified: Mon, 20 Apr 2026 23:17:10 GMT  
		Size: 49.8 MB (49827767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca20ece91f44e5655427eed64840d8ef712de22c13f7a72775ab55dd659d36c`  
		Last Modified: Mon, 20 Apr 2026 23:17:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e8458c4ba6e54bce45741648c81c4a86874636c2131f149d2fde04115f2395`  
		Last Modified: Mon, 20 Apr 2026 23:17:13 GMT  
		Size: 130.8 MB (130778054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e967d5df3dfeddf636fe21b8267a213c56fb0101310ab536b03ec7ea673b659`  
		Last Modified: Mon, 20 Apr 2026 23:17:10 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b68801a94249dca9abfa20e5adc37e05a40bba3101ccbf6af110f235234a17fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1486769bd3d1cc7c2392fe3ddbe873d685a118902324d049806adb91669f44e`

```dockerfile
```

-	Layers:
	-	`sha256:113cd58fe861869dadb0d755929aad301cb3ccc8489c76764c4181d8d9111035`  
		Last Modified: Mon, 20 Apr 2026 23:17:08 GMT  
		Size: 15.7 MB (15709328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dbe4130d194d2bd90f313c72d219b95b4b827ee15b2ff641c775b68ab304fa5`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:d0304ed9fdb64a3f6c7ad11a5fb4f13abfc10e6dfa3f288d652e7320c34df7f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:b09c60e595de1f1ff13d25b1669999445c254d86e8c203f6e311b0ab0f8ec2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233580226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62ad261f3b62ee5f30c1841801f6edbc6104a9f39f1e3457fbcae69462589ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:12:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Apr 2026 23:12:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:12:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:12:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Apr 2026 23:12:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Apr 2026 23:12:30 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Apr 2026 23:12:30 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:12:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Apr 2026 23:12:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Apr 2026 23:12:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Apr 2026 23:12:58 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:13:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Apr 2026 23:13:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Apr 2026 23:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:13:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Apr 2026 23:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:13:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Apr 2026 23:13:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f1cc0a64cab12a54d6a77b8472ad3809c85088ee0f8778005743e539bc8055`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7cfd23b1113bed914c161f89482864faa8382a5102db2cd9df39114f129e2c`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c689d1836928c5a3cc38676953334a54069a73b7302210c2f281f207606461e5`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 6.2 MB (6170286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa784df8611230c5d24640df01a9e1e3c881b91c649fef3b4fd85d45491ab92`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe997c72f3e9c8dc35c23c2eacb22bb473ebef1f712226bb748ba499c6af165c`  
		Last Modified: Tue, 21 Apr 2026 23:14:00 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fe0e0986defcc3ee8b4755c308fa72fc28e1304a6f2f29a419549aa1e10be3`  
		Last Modified: Tue, 21 Apr 2026 23:14:02 GMT  
		Size: 49.9 MB (49933185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b552d7265316c8dfbffce20c4f8480c6c05d599dd5b19789904eb0b0f05b9e`  
		Last Modified: Tue, 21 Apr 2026 23:14:00 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0db31010df32f3e8b49a0764ea310afe93b6b3c5ab6f89359cb4695a9b0f636`  
		Last Modified: Tue, 21 Apr 2026 23:14:03 GMT  
		Size: 129.4 MB (129373791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b723faee7585ac532524b3f359fe7193ce4a64089855317848333d44196fcffa`  
		Last Modified: Tue, 21 Apr 2026 23:14:01 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139627f60883efc152aa6a64f01c1f9fdffd51792168ec3c324dd11f7444a3f0`  
		Last Modified: Tue, 21 Apr 2026 23:14:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:ff8230de6d2586a61a3f1f61bed13b681b1bd37fd4d22d628379523765b608aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15468997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70b738b0f5861ee3af6343b705ab76405be4a8f82c451f30b08571209a9adf3`

```dockerfile
```

-	Layers:
	-	`sha256:cc9a862b4c106da885d05859357699cd70a1c2461053d52a4cf5a6a3d1ae539b`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 15.4 MB (15434087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ea08437b3cfe3ec3ba4ebd279e2f843d71041fb22648bb7f1e614939a29ca53`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 34.9 KB (34910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a4d3554ff8dfcdd8132a565732425add1067336f7aa2284e7c36981731e1b801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229136291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b77f16c26869f999d0a2b0e2e41b4c6e50fd837001590aecdbad688e03d7ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:13:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Apr 2026 23:13:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:13:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:13:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Apr 2026 23:13:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Apr 2026 23:13:58 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Apr 2026 23:13:58 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:13:58 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Apr 2026 23:14:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Apr 2026 23:14:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Apr 2026 23:14:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:15:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Apr 2026 23:15:10 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Apr 2026 23:15:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:15:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Apr 2026 23:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:15:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Apr 2026 23:15:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683a26a7ab856dbdef4225b7c46be2ff85275e849f092e123567cce21726591f`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceca16716ebe9bd4ad74424a7773ca53912eab63fb06a56abeb0b0e9260f3553`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3dd2e3a57f1b87a3100a4fd35251d3862a30fc3b1ea1d9a53a22887aa74636`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 5.8 MB (5793307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0c1d42c4a42f3f4008e54c89d3031b4835d941eab6e1a461a028f299ad810b`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d389f2060259dfa514885ba625a0edfb7e70bece363fb5f3243af400c72373f`  
		Last Modified: Tue, 21 Apr 2026 23:15:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be6823e85fecd3d3bb0c8264186f7576cb2139921d7238b94c647f97562eff1`  
		Last Modified: Tue, 21 Apr 2026 23:15:44 GMT  
		Size: 48.8 MB (48786024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f563e75717ecb2d7eab3825f198b1f35b205ccef7d66d3b0b905837b7e2a6d`  
		Last Modified: Tue, 21 Apr 2026 23:15:42 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0801c66dbc2132daaf64530be5c5ddd9b924cd0516ebf3c6f3191feb67e7473`  
		Last Modified: Tue, 21 Apr 2026 23:15:47 GMT  
		Size: 127.9 MB (127910047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ae56e2fb1e4180cd486ae8678d88c8fcb54e46ed04eb2a583be1b401cb7fa`  
		Last Modified: Tue, 21 Apr 2026 23:15:43 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54c9d85f167881a10b2b079de66ec8de56067b597907e38f867e08d42d4701d`  
		Last Modified: Tue, 21 Apr 2026 23:15:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:859ab4c08ab26de26ae2f3a089715e994377ea0e139da62dfee2d05d53efd956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15467594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be309955ded5bc0806c8e176ed8b52a488cde394c4f6d2f3d81126e3cfd7785f`

```dockerfile
```

-	Layers:
	-	`sha256:bf65c6de1a6a6ee06273d6cf1f8eef17fea5dbe94e5a59b0735b0950be2f29aa`  
		Last Modified: Tue, 21 Apr 2026 23:15:41 GMT  
		Size: 15.4 MB (15432435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d38252b57a8ae864799f6927901dbf0c49092fd45cb1b59b7270dbc2b7ed87`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:9382e4f6f7f013231049ab854de9d0810594d028f4237b67102acc7ade8e3a99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:0845b57a4927c2e2e442b0c3c154ebf2bdede7d6e1cb3b5a4b3e8bc1d0e69e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183493846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecd5f2526848a17828c97ea713b778389f599988dc03bb40817bbd0f4e8cff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:41:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 22 Apr 2026 01:41:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:42:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:42:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 22 Apr 2026 01:42:07 GMT
ENV MYSQL_VERSION=8.0.46-1debian12
# Wed, 22 Apr 2026 01:42:07 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Apr 2026 01:42:17 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:42:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Apr 2026 01:42:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0855a4662f4674f4b2fa5b3319559ce3157688e702d8c2a79583f0da1351e556`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4e8a7b62f21cd8c4c97cd9f0ac47e47d244e51a06b6c9d503173911a5511e0`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 4.4 MB (4423340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9904ed9c36af76fad8fec577f30214c654ee4d5b049c97f3bf60a035c596e2`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 1.2 MB (1248703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5223423e03ce3b1462874ffb00ccf06b7d33ccdfaf4ab8d5267d4b1fcb2a3461`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffd0e9a8806dfb4190a5efb53b9068f1473ec79c114ae9acf64e04ae785cfd3`  
		Last Modified: Wed, 22 Apr 2026 01:42:42 GMT  
		Size: 15.3 MB (15295542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56737b600a7ed7a14d1e8410aa58f2c34e1a13828090dbb7dbd4fc8a60dba3d`  
		Last Modified: Wed, 22 Apr 2026 01:42:41 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c65b70c20a21019513cbc8a61d63aa4f5899645c90ecb9f3d2e2151267969e`  
		Last Modified: Wed, 22 Apr 2026 01:42:41 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b2450db828e1da3146b24825caf9ec6f014b7bd17c535dd6aea175bcab19d8`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 134.3 MB (134279198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31f61b0173611c4be67c102358804af4fbd8a1c40b8ac915470077320617e17`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7908b55f16b6979dab8bf2917860fefd90e59605fc97bf7c1df4914d6d231c81`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4531d449fbdc31a0aa3f36772fc8c521bfa962e70bab3a5abd4d3a4854ac79`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:c3a78f9613889dbaa4d0174c1b5fb8b5cbeb0582a4879cf79141c74c25fa3e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f692ec2a7da89ebf2bff1089e62c794c7272afcde68f5f5ad8983acf688d067c`

```dockerfile
```

-	Layers:
	-	`sha256:c864b878b36d1fbfaac5acc28598ccd96160e7d214da4131228041e666b25d0e`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f4d617789ef531659729800ee7388d1c1f154ba9399fae3bbd757f14b5dcc0`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:9382e4f6f7f013231049ab854de9d0810594d028f4237b67102acc7ade8e3a99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:0845b57a4927c2e2e442b0c3c154ebf2bdede7d6e1cb3b5a4b3e8bc1d0e69e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183493846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecd5f2526848a17828c97ea713b778389f599988dc03bb40817bbd0f4e8cff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:41:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 22 Apr 2026 01:41:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:42:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:42:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 22 Apr 2026 01:42:07 GMT
ENV MYSQL_VERSION=8.0.46-1debian12
# Wed, 22 Apr 2026 01:42:07 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Apr 2026 01:42:17 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:42:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Apr 2026 01:42:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0855a4662f4674f4b2fa5b3319559ce3157688e702d8c2a79583f0da1351e556`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4e8a7b62f21cd8c4c97cd9f0ac47e47d244e51a06b6c9d503173911a5511e0`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 4.4 MB (4423340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9904ed9c36af76fad8fec577f30214c654ee4d5b049c97f3bf60a035c596e2`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 1.2 MB (1248703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5223423e03ce3b1462874ffb00ccf06b7d33ccdfaf4ab8d5267d4b1fcb2a3461`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffd0e9a8806dfb4190a5efb53b9068f1473ec79c114ae9acf64e04ae785cfd3`  
		Last Modified: Wed, 22 Apr 2026 01:42:42 GMT  
		Size: 15.3 MB (15295542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56737b600a7ed7a14d1e8410aa58f2c34e1a13828090dbb7dbd4fc8a60dba3d`  
		Last Modified: Wed, 22 Apr 2026 01:42:41 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c65b70c20a21019513cbc8a61d63aa4f5899645c90ecb9f3d2e2151267969e`  
		Last Modified: Wed, 22 Apr 2026 01:42:41 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b2450db828e1da3146b24825caf9ec6f014b7bd17c535dd6aea175bcab19d8`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 134.3 MB (134279198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31f61b0173611c4be67c102358804af4fbd8a1c40b8ac915470077320617e17`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7908b55f16b6979dab8bf2917860fefd90e59605fc97bf7c1df4914d6d231c81`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4531d449fbdc31a0aa3f36772fc8c521bfa962e70bab3a5abd4d3a4854ac79`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:c3a78f9613889dbaa4d0174c1b5fb8b5cbeb0582a4879cf79141c74c25fa3e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f692ec2a7da89ebf2bff1089e62c794c7272afcde68f5f5ad8983acf688d067c`

```dockerfile
```

-	Layers:
	-	`sha256:c864b878b36d1fbfaac5acc28598ccd96160e7d214da4131228041e666b25d0e`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f4d617789ef531659729800ee7388d1c1f154ba9399fae3bbd757f14b5dcc0`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:d0304ed9fdb64a3f6c7ad11a5fb4f13abfc10e6dfa3f288d652e7320c34df7f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b09c60e595de1f1ff13d25b1669999445c254d86e8c203f6e311b0ab0f8ec2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233580226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62ad261f3b62ee5f30c1841801f6edbc6104a9f39f1e3457fbcae69462589ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:12:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Apr 2026 23:12:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:12:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:12:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Apr 2026 23:12:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Apr 2026 23:12:30 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Apr 2026 23:12:30 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:12:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Apr 2026 23:12:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Apr 2026 23:12:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Apr 2026 23:12:58 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:13:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Apr 2026 23:13:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Apr 2026 23:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:13:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Apr 2026 23:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:13:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Apr 2026 23:13:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f1cc0a64cab12a54d6a77b8472ad3809c85088ee0f8778005743e539bc8055`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7cfd23b1113bed914c161f89482864faa8382a5102db2cd9df39114f129e2c`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c689d1836928c5a3cc38676953334a54069a73b7302210c2f281f207606461e5`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 6.2 MB (6170286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa784df8611230c5d24640df01a9e1e3c881b91c649fef3b4fd85d45491ab92`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe997c72f3e9c8dc35c23c2eacb22bb473ebef1f712226bb748ba499c6af165c`  
		Last Modified: Tue, 21 Apr 2026 23:14:00 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fe0e0986defcc3ee8b4755c308fa72fc28e1304a6f2f29a419549aa1e10be3`  
		Last Modified: Tue, 21 Apr 2026 23:14:02 GMT  
		Size: 49.9 MB (49933185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b552d7265316c8dfbffce20c4f8480c6c05d599dd5b19789904eb0b0f05b9e`  
		Last Modified: Tue, 21 Apr 2026 23:14:00 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0db31010df32f3e8b49a0764ea310afe93b6b3c5ab6f89359cb4695a9b0f636`  
		Last Modified: Tue, 21 Apr 2026 23:14:03 GMT  
		Size: 129.4 MB (129373791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b723faee7585ac532524b3f359fe7193ce4a64089855317848333d44196fcffa`  
		Last Modified: Tue, 21 Apr 2026 23:14:01 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139627f60883efc152aa6a64f01c1f9fdffd51792168ec3c324dd11f7444a3f0`  
		Last Modified: Tue, 21 Apr 2026 23:14:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ff8230de6d2586a61a3f1f61bed13b681b1bd37fd4d22d628379523765b608aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15468997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70b738b0f5861ee3af6343b705ab76405be4a8f82c451f30b08571209a9adf3`

```dockerfile
```

-	Layers:
	-	`sha256:cc9a862b4c106da885d05859357699cd70a1c2461053d52a4cf5a6a3d1ae539b`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 15.4 MB (15434087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ea08437b3cfe3ec3ba4ebd279e2f843d71041fb22648bb7f1e614939a29ca53`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 34.9 KB (34910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a4d3554ff8dfcdd8132a565732425add1067336f7aa2284e7c36981731e1b801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229136291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b77f16c26869f999d0a2b0e2e41b4c6e50fd837001590aecdbad688e03d7ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:13:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Apr 2026 23:13:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:13:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:13:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Apr 2026 23:13:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Apr 2026 23:13:58 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Apr 2026 23:13:58 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:13:58 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Apr 2026 23:14:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Apr 2026 23:14:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Apr 2026 23:14:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:15:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Apr 2026 23:15:10 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Apr 2026 23:15:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:15:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Apr 2026 23:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:15:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Apr 2026 23:15:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683a26a7ab856dbdef4225b7c46be2ff85275e849f092e123567cce21726591f`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceca16716ebe9bd4ad74424a7773ca53912eab63fb06a56abeb0b0e9260f3553`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3dd2e3a57f1b87a3100a4fd35251d3862a30fc3b1ea1d9a53a22887aa74636`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 5.8 MB (5793307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0c1d42c4a42f3f4008e54c89d3031b4835d941eab6e1a461a028f299ad810b`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d389f2060259dfa514885ba625a0edfb7e70bece363fb5f3243af400c72373f`  
		Last Modified: Tue, 21 Apr 2026 23:15:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be6823e85fecd3d3bb0c8264186f7576cb2139921d7238b94c647f97562eff1`  
		Last Modified: Tue, 21 Apr 2026 23:15:44 GMT  
		Size: 48.8 MB (48786024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f563e75717ecb2d7eab3825f198b1f35b205ccef7d66d3b0b905837b7e2a6d`  
		Last Modified: Tue, 21 Apr 2026 23:15:42 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0801c66dbc2132daaf64530be5c5ddd9b924cd0516ebf3c6f3191feb67e7473`  
		Last Modified: Tue, 21 Apr 2026 23:15:47 GMT  
		Size: 127.9 MB (127910047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ae56e2fb1e4180cd486ae8678d88c8fcb54e46ed04eb2a583be1b401cb7fa`  
		Last Modified: Tue, 21 Apr 2026 23:15:43 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54c9d85f167881a10b2b079de66ec8de56067b597907e38f867e08d42d4701d`  
		Last Modified: Tue, 21 Apr 2026 23:15:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:859ab4c08ab26de26ae2f3a089715e994377ea0e139da62dfee2d05d53efd956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15467594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be309955ded5bc0806c8e176ed8b52a488cde394c4f6d2f3d81126e3cfd7785f`

```dockerfile
```

-	Layers:
	-	`sha256:bf65c6de1a6a6ee06273d6cf1f8eef17fea5dbe94e5a59b0735b0950be2f29aa`  
		Last Modified: Tue, 21 Apr 2026 23:15:41 GMT  
		Size: 15.4 MB (15432435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d38252b57a8ae864799f6927901dbf0c49092fd45cb1b59b7270dbc2b7ed87`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:d0304ed9fdb64a3f6c7ad11a5fb4f13abfc10e6dfa3f288d652e7320c34df7f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:b09c60e595de1f1ff13d25b1669999445c254d86e8c203f6e311b0ab0f8ec2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233580226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62ad261f3b62ee5f30c1841801f6edbc6104a9f39f1e3457fbcae69462589ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:12:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Apr 2026 23:12:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:12:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:12:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Apr 2026 23:12:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Apr 2026 23:12:30 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Apr 2026 23:12:30 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:12:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Apr 2026 23:12:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Apr 2026 23:12:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Apr 2026 23:12:58 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:13:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Apr 2026 23:13:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Apr 2026 23:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:13:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Apr 2026 23:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:13:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Apr 2026 23:13:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f1cc0a64cab12a54d6a77b8472ad3809c85088ee0f8778005743e539bc8055`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7cfd23b1113bed914c161f89482864faa8382a5102db2cd9df39114f129e2c`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c689d1836928c5a3cc38676953334a54069a73b7302210c2f281f207606461e5`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 6.2 MB (6170286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa784df8611230c5d24640df01a9e1e3c881b91c649fef3b4fd85d45491ab92`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe997c72f3e9c8dc35c23c2eacb22bb473ebef1f712226bb748ba499c6af165c`  
		Last Modified: Tue, 21 Apr 2026 23:14:00 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fe0e0986defcc3ee8b4755c308fa72fc28e1304a6f2f29a419549aa1e10be3`  
		Last Modified: Tue, 21 Apr 2026 23:14:02 GMT  
		Size: 49.9 MB (49933185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b552d7265316c8dfbffce20c4f8480c6c05d599dd5b19789904eb0b0f05b9e`  
		Last Modified: Tue, 21 Apr 2026 23:14:00 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0db31010df32f3e8b49a0764ea310afe93b6b3c5ab6f89359cb4695a9b0f636`  
		Last Modified: Tue, 21 Apr 2026 23:14:03 GMT  
		Size: 129.4 MB (129373791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b723faee7585ac532524b3f359fe7193ce4a64089855317848333d44196fcffa`  
		Last Modified: Tue, 21 Apr 2026 23:14:01 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139627f60883efc152aa6a64f01c1f9fdffd51792168ec3c324dd11f7444a3f0`  
		Last Modified: Tue, 21 Apr 2026 23:14:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ff8230de6d2586a61a3f1f61bed13b681b1bd37fd4d22d628379523765b608aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15468997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70b738b0f5861ee3af6343b705ab76405be4a8f82c451f30b08571209a9adf3`

```dockerfile
```

-	Layers:
	-	`sha256:cc9a862b4c106da885d05859357699cd70a1c2461053d52a4cf5a6a3d1ae539b`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 15.4 MB (15434087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ea08437b3cfe3ec3ba4ebd279e2f843d71041fb22648bb7f1e614939a29ca53`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 34.9 KB (34910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a4d3554ff8dfcdd8132a565732425add1067336f7aa2284e7c36981731e1b801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229136291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b77f16c26869f999d0a2b0e2e41b4c6e50fd837001590aecdbad688e03d7ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:13:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Apr 2026 23:13:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:13:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:13:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Apr 2026 23:13:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Apr 2026 23:13:58 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Apr 2026 23:13:58 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:13:58 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Apr 2026 23:14:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Apr 2026 23:14:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Apr 2026 23:14:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:15:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Apr 2026 23:15:10 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Apr 2026 23:15:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:15:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Apr 2026 23:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:15:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Apr 2026 23:15:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683a26a7ab856dbdef4225b7c46be2ff85275e849f092e123567cce21726591f`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceca16716ebe9bd4ad74424a7773ca53912eab63fb06a56abeb0b0e9260f3553`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3dd2e3a57f1b87a3100a4fd35251d3862a30fc3b1ea1d9a53a22887aa74636`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 5.8 MB (5793307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0c1d42c4a42f3f4008e54c89d3031b4835d941eab6e1a461a028f299ad810b`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d389f2060259dfa514885ba625a0edfb7e70bece363fb5f3243af400c72373f`  
		Last Modified: Tue, 21 Apr 2026 23:15:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be6823e85fecd3d3bb0c8264186f7576cb2139921d7238b94c647f97562eff1`  
		Last Modified: Tue, 21 Apr 2026 23:15:44 GMT  
		Size: 48.8 MB (48786024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f563e75717ecb2d7eab3825f198b1f35b205ccef7d66d3b0b905837b7e2a6d`  
		Last Modified: Tue, 21 Apr 2026 23:15:42 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0801c66dbc2132daaf64530be5c5ddd9b924cd0516ebf3c6f3191feb67e7473`  
		Last Modified: Tue, 21 Apr 2026 23:15:47 GMT  
		Size: 127.9 MB (127910047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ae56e2fb1e4180cd486ae8678d88c8fcb54e46ed04eb2a583be1b401cb7fa`  
		Last Modified: Tue, 21 Apr 2026 23:15:43 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54c9d85f167881a10b2b079de66ec8de56067b597907e38f867e08d42d4701d`  
		Last Modified: Tue, 21 Apr 2026 23:15:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:859ab4c08ab26de26ae2f3a089715e994377ea0e139da62dfee2d05d53efd956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15467594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be309955ded5bc0806c8e176ed8b52a488cde394c4f6d2f3d81126e3cfd7785f`

```dockerfile
```

-	Layers:
	-	`sha256:bf65c6de1a6a6ee06273d6cf1f8eef17fea5dbe94e5a59b0735b0950be2f29aa`  
		Last Modified: Tue, 21 Apr 2026 23:15:41 GMT  
		Size: 15.4 MB (15432435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d38252b57a8ae864799f6927901dbf0c49092fd45cb1b59b7270dbc2b7ed87`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.46`

```console
$ docker pull mysql@sha256:d0304ed9fdb64a3f6c7ad11a5fb4f13abfc10e6dfa3f288d652e7320c34df7f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.46` - linux; amd64

```console
$ docker pull mysql@sha256:b09c60e595de1f1ff13d25b1669999445c254d86e8c203f6e311b0ab0f8ec2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233580226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62ad261f3b62ee5f30c1841801f6edbc6104a9f39f1e3457fbcae69462589ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:12:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Apr 2026 23:12:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:12:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:12:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Apr 2026 23:12:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Apr 2026 23:12:30 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Apr 2026 23:12:30 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:12:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Apr 2026 23:12:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Apr 2026 23:12:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Apr 2026 23:12:58 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:13:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Apr 2026 23:13:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Apr 2026 23:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:13:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Apr 2026 23:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:13:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Apr 2026 23:13:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f1cc0a64cab12a54d6a77b8472ad3809c85088ee0f8778005743e539bc8055`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7cfd23b1113bed914c161f89482864faa8382a5102db2cd9df39114f129e2c`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c689d1836928c5a3cc38676953334a54069a73b7302210c2f281f207606461e5`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 6.2 MB (6170286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa784df8611230c5d24640df01a9e1e3c881b91c649fef3b4fd85d45491ab92`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe997c72f3e9c8dc35c23c2eacb22bb473ebef1f712226bb748ba499c6af165c`  
		Last Modified: Tue, 21 Apr 2026 23:14:00 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fe0e0986defcc3ee8b4755c308fa72fc28e1304a6f2f29a419549aa1e10be3`  
		Last Modified: Tue, 21 Apr 2026 23:14:02 GMT  
		Size: 49.9 MB (49933185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b552d7265316c8dfbffce20c4f8480c6c05d599dd5b19789904eb0b0f05b9e`  
		Last Modified: Tue, 21 Apr 2026 23:14:00 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0db31010df32f3e8b49a0764ea310afe93b6b3c5ab6f89359cb4695a9b0f636`  
		Last Modified: Tue, 21 Apr 2026 23:14:03 GMT  
		Size: 129.4 MB (129373791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b723faee7585ac532524b3f359fe7193ce4a64089855317848333d44196fcffa`  
		Last Modified: Tue, 21 Apr 2026 23:14:01 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139627f60883efc152aa6a64f01c1f9fdffd51792168ec3c324dd11f7444a3f0`  
		Last Modified: Tue, 21 Apr 2026 23:14:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.46` - unknown; unknown

```console
$ docker pull mysql@sha256:ff8230de6d2586a61a3f1f61bed13b681b1bd37fd4d22d628379523765b608aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15468997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70b738b0f5861ee3af6343b705ab76405be4a8f82c451f30b08571209a9adf3`

```dockerfile
```

-	Layers:
	-	`sha256:cc9a862b4c106da885d05859357699cd70a1c2461053d52a4cf5a6a3d1ae539b`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 15.4 MB (15434087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ea08437b3cfe3ec3ba4ebd279e2f843d71041fb22648bb7f1e614939a29ca53`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 34.9 KB (34910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.46` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a4d3554ff8dfcdd8132a565732425add1067336f7aa2284e7c36981731e1b801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229136291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b77f16c26869f999d0a2b0e2e41b4c6e50fd837001590aecdbad688e03d7ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:13:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Apr 2026 23:13:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:13:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:13:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Apr 2026 23:13:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Apr 2026 23:13:58 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Apr 2026 23:13:58 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:13:58 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Apr 2026 23:14:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Apr 2026 23:14:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Apr 2026 23:14:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:15:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Apr 2026 23:15:10 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Apr 2026 23:15:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:15:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Apr 2026 23:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:15:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Apr 2026 23:15:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683a26a7ab856dbdef4225b7c46be2ff85275e849f092e123567cce21726591f`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceca16716ebe9bd4ad74424a7773ca53912eab63fb06a56abeb0b0e9260f3553`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3dd2e3a57f1b87a3100a4fd35251d3862a30fc3b1ea1d9a53a22887aa74636`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 5.8 MB (5793307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0c1d42c4a42f3f4008e54c89d3031b4835d941eab6e1a461a028f299ad810b`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d389f2060259dfa514885ba625a0edfb7e70bece363fb5f3243af400c72373f`  
		Last Modified: Tue, 21 Apr 2026 23:15:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be6823e85fecd3d3bb0c8264186f7576cb2139921d7238b94c647f97562eff1`  
		Last Modified: Tue, 21 Apr 2026 23:15:44 GMT  
		Size: 48.8 MB (48786024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f563e75717ecb2d7eab3825f198b1f35b205ccef7d66d3b0b905837b7e2a6d`  
		Last Modified: Tue, 21 Apr 2026 23:15:42 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0801c66dbc2132daaf64530be5c5ddd9b924cd0516ebf3c6f3191feb67e7473`  
		Last Modified: Tue, 21 Apr 2026 23:15:47 GMT  
		Size: 127.9 MB (127910047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ae56e2fb1e4180cd486ae8678d88c8fcb54e46ed04eb2a583be1b401cb7fa`  
		Last Modified: Tue, 21 Apr 2026 23:15:43 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54c9d85f167881a10b2b079de66ec8de56067b597907e38f867e08d42d4701d`  
		Last Modified: Tue, 21 Apr 2026 23:15:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.46` - unknown; unknown

```console
$ docker pull mysql@sha256:859ab4c08ab26de26ae2f3a089715e994377ea0e139da62dfee2d05d53efd956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15467594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be309955ded5bc0806c8e176ed8b52a488cde394c4f6d2f3d81126e3cfd7785f`

```dockerfile
```

-	Layers:
	-	`sha256:bf65c6de1a6a6ee06273d6cf1f8eef17fea5dbe94e5a59b0735b0950be2f29aa`  
		Last Modified: Tue, 21 Apr 2026 23:15:41 GMT  
		Size: 15.4 MB (15432435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d38252b57a8ae864799f6927901dbf0c49092fd45cb1b59b7270dbc2b7ed87`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.46-bookworm`

```console
$ docker pull mysql@sha256:9382e4f6f7f013231049ab854de9d0810594d028f4237b67102acc7ade8e3a99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.46-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:0845b57a4927c2e2e442b0c3c154ebf2bdede7d6e1cb3b5a4b3e8bc1d0e69e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183493846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecd5f2526848a17828c97ea713b778389f599988dc03bb40817bbd0f4e8cff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:41:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 22 Apr 2026 01:41:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:42:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:42:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 22 Apr 2026 01:42:07 GMT
ENV MYSQL_VERSION=8.0.46-1debian12
# Wed, 22 Apr 2026 01:42:07 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Apr 2026 01:42:17 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:42:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Apr 2026 01:42:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0855a4662f4674f4b2fa5b3319559ce3157688e702d8c2a79583f0da1351e556`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4e8a7b62f21cd8c4c97cd9f0ac47e47d244e51a06b6c9d503173911a5511e0`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 4.4 MB (4423340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9904ed9c36af76fad8fec577f30214c654ee4d5b049c97f3bf60a035c596e2`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 1.2 MB (1248703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5223423e03ce3b1462874ffb00ccf06b7d33ccdfaf4ab8d5267d4b1fcb2a3461`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffd0e9a8806dfb4190a5efb53b9068f1473ec79c114ae9acf64e04ae785cfd3`  
		Last Modified: Wed, 22 Apr 2026 01:42:42 GMT  
		Size: 15.3 MB (15295542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56737b600a7ed7a14d1e8410aa58f2c34e1a13828090dbb7dbd4fc8a60dba3d`  
		Last Modified: Wed, 22 Apr 2026 01:42:41 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c65b70c20a21019513cbc8a61d63aa4f5899645c90ecb9f3d2e2151267969e`  
		Last Modified: Wed, 22 Apr 2026 01:42:41 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b2450db828e1da3146b24825caf9ec6f014b7bd17c535dd6aea175bcab19d8`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 134.3 MB (134279198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31f61b0173611c4be67c102358804af4fbd8a1c40b8ac915470077320617e17`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7908b55f16b6979dab8bf2917860fefd90e59605fc97bf7c1df4914d6d231c81`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4531d449fbdc31a0aa3f36772fc8c521bfa962e70bab3a5abd4d3a4854ac79`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.46-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:c3a78f9613889dbaa4d0174c1b5fb8b5cbeb0582a4879cf79141c74c25fa3e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f692ec2a7da89ebf2bff1089e62c794c7272afcde68f5f5ad8983acf688d067c`

```dockerfile
```

-	Layers:
	-	`sha256:c864b878b36d1fbfaac5acc28598ccd96160e7d214da4131228041e666b25d0e`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f4d617789ef531659729800ee7388d1c1f154ba9399fae3bbd757f14b5dcc0`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.46-debian`

```console
$ docker pull mysql@sha256:9382e4f6f7f013231049ab854de9d0810594d028f4237b67102acc7ade8e3a99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.46-debian` - linux; amd64

```console
$ docker pull mysql@sha256:0845b57a4927c2e2e442b0c3c154ebf2bdede7d6e1cb3b5a4b3e8bc1d0e69e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183493846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecd5f2526848a17828c97ea713b778389f599988dc03bb40817bbd0f4e8cff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:41:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 22 Apr 2026 01:41:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:42:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:42:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 22 Apr 2026 01:42:07 GMT
ENV MYSQL_VERSION=8.0.46-1debian12
# Wed, 22 Apr 2026 01:42:07 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Apr 2026 01:42:17 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:42:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Apr 2026 01:42:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0855a4662f4674f4b2fa5b3319559ce3157688e702d8c2a79583f0da1351e556`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4e8a7b62f21cd8c4c97cd9f0ac47e47d244e51a06b6c9d503173911a5511e0`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 4.4 MB (4423340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9904ed9c36af76fad8fec577f30214c654ee4d5b049c97f3bf60a035c596e2`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 1.2 MB (1248703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5223423e03ce3b1462874ffb00ccf06b7d33ccdfaf4ab8d5267d4b1fcb2a3461`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffd0e9a8806dfb4190a5efb53b9068f1473ec79c114ae9acf64e04ae785cfd3`  
		Last Modified: Wed, 22 Apr 2026 01:42:42 GMT  
		Size: 15.3 MB (15295542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56737b600a7ed7a14d1e8410aa58f2c34e1a13828090dbb7dbd4fc8a60dba3d`  
		Last Modified: Wed, 22 Apr 2026 01:42:41 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c65b70c20a21019513cbc8a61d63aa4f5899645c90ecb9f3d2e2151267969e`  
		Last Modified: Wed, 22 Apr 2026 01:42:41 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b2450db828e1da3146b24825caf9ec6f014b7bd17c535dd6aea175bcab19d8`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 134.3 MB (134279198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31f61b0173611c4be67c102358804af4fbd8a1c40b8ac915470077320617e17`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7908b55f16b6979dab8bf2917860fefd90e59605fc97bf7c1df4914d6d231c81`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4531d449fbdc31a0aa3f36772fc8c521bfa962e70bab3a5abd4d3a4854ac79`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.46-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:c3a78f9613889dbaa4d0174c1b5fb8b5cbeb0582a4879cf79141c74c25fa3e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f692ec2a7da89ebf2bff1089e62c794c7272afcde68f5f5ad8983acf688d067c`

```dockerfile
```

-	Layers:
	-	`sha256:c864b878b36d1fbfaac5acc28598ccd96160e7d214da4131228041e666b25d0e`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f4d617789ef531659729800ee7388d1c1f154ba9399fae3bbd757f14b5dcc0`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.46-oracle`

```console
$ docker pull mysql@sha256:d0304ed9fdb64a3f6c7ad11a5fb4f13abfc10e6dfa3f288d652e7320c34df7f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.46-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b09c60e595de1f1ff13d25b1669999445c254d86e8c203f6e311b0ab0f8ec2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233580226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62ad261f3b62ee5f30c1841801f6edbc6104a9f39f1e3457fbcae69462589ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:12:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Apr 2026 23:12:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:12:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:12:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Apr 2026 23:12:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Apr 2026 23:12:30 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Apr 2026 23:12:30 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:12:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Apr 2026 23:12:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Apr 2026 23:12:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Apr 2026 23:12:58 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:13:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Apr 2026 23:13:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Apr 2026 23:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:13:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Apr 2026 23:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:13:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Apr 2026 23:13:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f1cc0a64cab12a54d6a77b8472ad3809c85088ee0f8778005743e539bc8055`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7cfd23b1113bed914c161f89482864faa8382a5102db2cd9df39114f129e2c`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c689d1836928c5a3cc38676953334a54069a73b7302210c2f281f207606461e5`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 6.2 MB (6170286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa784df8611230c5d24640df01a9e1e3c881b91c649fef3b4fd85d45491ab92`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe997c72f3e9c8dc35c23c2eacb22bb473ebef1f712226bb748ba499c6af165c`  
		Last Modified: Tue, 21 Apr 2026 23:14:00 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fe0e0986defcc3ee8b4755c308fa72fc28e1304a6f2f29a419549aa1e10be3`  
		Last Modified: Tue, 21 Apr 2026 23:14:02 GMT  
		Size: 49.9 MB (49933185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b552d7265316c8dfbffce20c4f8480c6c05d599dd5b19789904eb0b0f05b9e`  
		Last Modified: Tue, 21 Apr 2026 23:14:00 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0db31010df32f3e8b49a0764ea310afe93b6b3c5ab6f89359cb4695a9b0f636`  
		Last Modified: Tue, 21 Apr 2026 23:14:03 GMT  
		Size: 129.4 MB (129373791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b723faee7585ac532524b3f359fe7193ce4a64089855317848333d44196fcffa`  
		Last Modified: Tue, 21 Apr 2026 23:14:01 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139627f60883efc152aa6a64f01c1f9fdffd51792168ec3c324dd11f7444a3f0`  
		Last Modified: Tue, 21 Apr 2026 23:14:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.46-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ff8230de6d2586a61a3f1f61bed13b681b1bd37fd4d22d628379523765b608aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15468997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70b738b0f5861ee3af6343b705ab76405be4a8f82c451f30b08571209a9adf3`

```dockerfile
```

-	Layers:
	-	`sha256:cc9a862b4c106da885d05859357699cd70a1c2461053d52a4cf5a6a3d1ae539b`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 15.4 MB (15434087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ea08437b3cfe3ec3ba4ebd279e2f843d71041fb22648bb7f1e614939a29ca53`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 34.9 KB (34910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.46-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a4d3554ff8dfcdd8132a565732425add1067336f7aa2284e7c36981731e1b801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229136291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b77f16c26869f999d0a2b0e2e41b4c6e50fd837001590aecdbad688e03d7ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:13:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Apr 2026 23:13:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:13:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:13:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Apr 2026 23:13:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Apr 2026 23:13:58 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Apr 2026 23:13:58 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:13:58 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Apr 2026 23:14:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Apr 2026 23:14:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Apr 2026 23:14:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:15:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Apr 2026 23:15:10 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Apr 2026 23:15:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:15:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Apr 2026 23:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:15:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Apr 2026 23:15:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683a26a7ab856dbdef4225b7c46be2ff85275e849f092e123567cce21726591f`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceca16716ebe9bd4ad74424a7773ca53912eab63fb06a56abeb0b0e9260f3553`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3dd2e3a57f1b87a3100a4fd35251d3862a30fc3b1ea1d9a53a22887aa74636`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 5.8 MB (5793307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0c1d42c4a42f3f4008e54c89d3031b4835d941eab6e1a461a028f299ad810b`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d389f2060259dfa514885ba625a0edfb7e70bece363fb5f3243af400c72373f`  
		Last Modified: Tue, 21 Apr 2026 23:15:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be6823e85fecd3d3bb0c8264186f7576cb2139921d7238b94c647f97562eff1`  
		Last Modified: Tue, 21 Apr 2026 23:15:44 GMT  
		Size: 48.8 MB (48786024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f563e75717ecb2d7eab3825f198b1f35b205ccef7d66d3b0b905837b7e2a6d`  
		Last Modified: Tue, 21 Apr 2026 23:15:42 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0801c66dbc2132daaf64530be5c5ddd9b924cd0516ebf3c6f3191feb67e7473`  
		Last Modified: Tue, 21 Apr 2026 23:15:47 GMT  
		Size: 127.9 MB (127910047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ae56e2fb1e4180cd486ae8678d88c8fcb54e46ed04eb2a583be1b401cb7fa`  
		Last Modified: Tue, 21 Apr 2026 23:15:43 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54c9d85f167881a10b2b079de66ec8de56067b597907e38f867e08d42d4701d`  
		Last Modified: Tue, 21 Apr 2026 23:15:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.46-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:859ab4c08ab26de26ae2f3a089715e994377ea0e139da62dfee2d05d53efd956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15467594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be309955ded5bc0806c8e176ed8b52a488cde394c4f6d2f3d81126e3cfd7785f`

```dockerfile
```

-	Layers:
	-	`sha256:bf65c6de1a6a6ee06273d6cf1f8eef17fea5dbe94e5a59b0735b0950be2f29aa`  
		Last Modified: Tue, 21 Apr 2026 23:15:41 GMT  
		Size: 15.4 MB (15432435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d38252b57a8ae864799f6927901dbf0c49092fd45cb1b59b7270dbc2b7ed87`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.46-oraclelinux9`

```console
$ docker pull mysql@sha256:d0304ed9fdb64a3f6c7ad11a5fb4f13abfc10e6dfa3f288d652e7320c34df7f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.46-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:b09c60e595de1f1ff13d25b1669999445c254d86e8c203f6e311b0ab0f8ec2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233580226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62ad261f3b62ee5f30c1841801f6edbc6104a9f39f1e3457fbcae69462589ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:12:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Apr 2026 23:12:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:12:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:12:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Apr 2026 23:12:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Apr 2026 23:12:30 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Apr 2026 23:12:30 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:12:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Apr 2026 23:12:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Apr 2026 23:12:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Apr 2026 23:12:58 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:13:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Apr 2026 23:13:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Apr 2026 23:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:13:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Apr 2026 23:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:13:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Apr 2026 23:13:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f1cc0a64cab12a54d6a77b8472ad3809c85088ee0f8778005743e539bc8055`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7cfd23b1113bed914c161f89482864faa8382a5102db2cd9df39114f129e2c`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c689d1836928c5a3cc38676953334a54069a73b7302210c2f281f207606461e5`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 6.2 MB (6170286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa784df8611230c5d24640df01a9e1e3c881b91c649fef3b4fd85d45491ab92`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe997c72f3e9c8dc35c23c2eacb22bb473ebef1f712226bb748ba499c6af165c`  
		Last Modified: Tue, 21 Apr 2026 23:14:00 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fe0e0986defcc3ee8b4755c308fa72fc28e1304a6f2f29a419549aa1e10be3`  
		Last Modified: Tue, 21 Apr 2026 23:14:02 GMT  
		Size: 49.9 MB (49933185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b552d7265316c8dfbffce20c4f8480c6c05d599dd5b19789904eb0b0f05b9e`  
		Last Modified: Tue, 21 Apr 2026 23:14:00 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0db31010df32f3e8b49a0764ea310afe93b6b3c5ab6f89359cb4695a9b0f636`  
		Last Modified: Tue, 21 Apr 2026 23:14:03 GMT  
		Size: 129.4 MB (129373791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b723faee7585ac532524b3f359fe7193ce4a64089855317848333d44196fcffa`  
		Last Modified: Tue, 21 Apr 2026 23:14:01 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139627f60883efc152aa6a64f01c1f9fdffd51792168ec3c324dd11f7444a3f0`  
		Last Modified: Tue, 21 Apr 2026 23:14:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.46-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ff8230de6d2586a61a3f1f61bed13b681b1bd37fd4d22d628379523765b608aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15468997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70b738b0f5861ee3af6343b705ab76405be4a8f82c451f30b08571209a9adf3`

```dockerfile
```

-	Layers:
	-	`sha256:cc9a862b4c106da885d05859357699cd70a1c2461053d52a4cf5a6a3d1ae539b`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 15.4 MB (15434087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ea08437b3cfe3ec3ba4ebd279e2f843d71041fb22648bb7f1e614939a29ca53`  
		Last Modified: Tue, 21 Apr 2026 23:13:59 GMT  
		Size: 34.9 KB (34910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.46-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a4d3554ff8dfcdd8132a565732425add1067336f7aa2284e7c36981731e1b801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229136291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b77f16c26869f999d0a2b0e2e41b4c6e50fd837001590aecdbad688e03d7ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:13:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Apr 2026 23:13:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:13:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:13:57 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Apr 2026 23:13:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Apr 2026 23:13:58 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Apr 2026 23:13:58 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:13:58 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Apr 2026 23:14:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Apr 2026 23:14:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Apr 2026 23:14:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Tue, 21 Apr 2026 23:15:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Apr 2026 23:15:10 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Apr 2026 23:15:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:15:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Apr 2026 23:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:15:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Apr 2026 23:15:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683a26a7ab856dbdef4225b7c46be2ff85275e849f092e123567cce21726591f`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceca16716ebe9bd4ad74424a7773ca53912eab63fb06a56abeb0b0e9260f3553`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3dd2e3a57f1b87a3100a4fd35251d3862a30fc3b1ea1d9a53a22887aa74636`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 5.8 MB (5793307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0c1d42c4a42f3f4008e54c89d3031b4835d941eab6e1a461a028f299ad810b`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d389f2060259dfa514885ba625a0edfb7e70bece363fb5f3243af400c72373f`  
		Last Modified: Tue, 21 Apr 2026 23:15:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be6823e85fecd3d3bb0c8264186f7576cb2139921d7238b94c647f97562eff1`  
		Last Modified: Tue, 21 Apr 2026 23:15:44 GMT  
		Size: 48.8 MB (48786024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f563e75717ecb2d7eab3825f198b1f35b205ccef7d66d3b0b905837b7e2a6d`  
		Last Modified: Tue, 21 Apr 2026 23:15:42 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0801c66dbc2132daaf64530be5c5ddd9b924cd0516ebf3c6f3191feb67e7473`  
		Last Modified: Tue, 21 Apr 2026 23:15:47 GMT  
		Size: 127.9 MB (127910047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ae56e2fb1e4180cd486ae8678d88c8fcb54e46ed04eb2a583be1b401cb7fa`  
		Last Modified: Tue, 21 Apr 2026 23:15:43 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54c9d85f167881a10b2b079de66ec8de56067b597907e38f867e08d42d4701d`  
		Last Modified: Tue, 21 Apr 2026 23:15:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.46-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:859ab4c08ab26de26ae2f3a089715e994377ea0e139da62dfee2d05d53efd956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15467594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be309955ded5bc0806c8e176ed8b52a488cde394c4f6d2f3d81126e3cfd7785f`

```dockerfile
```

-	Layers:
	-	`sha256:bf65c6de1a6a6ee06273d6cf1f8eef17fea5dbe94e5a59b0735b0950be2f29aa`  
		Last Modified: Tue, 21 Apr 2026 23:15:41 GMT  
		Size: 15.4 MB (15432435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d38252b57a8ae864799f6927901dbf0c49092fd45cb1b59b7270dbc2b7ed87`  
		Last Modified: Tue, 21 Apr 2026 23:15:40 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:43bd9764df60666fb2ba2cf8217dd17b3d2414c150005d2fdd07a0cd73d3b7f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:8096dd88a82dad3741f292e282d36b577097926735aeee8960c9b8c759453bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238250587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c55658453cceab502e6a7f2d3abe7292180c6f71f463972bcae809304979c06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 23:18:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 20 Apr 2026 23:18:18 GMT
ENV GOSU_VERSION=1.19
# Mon, 20 Apr 2026 23:18:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 20 Apr 2026 23:18:44 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:19:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 20 Apr 2026 23:19:48 GMT
VOLUME [/var/lib/mysql]
# Mon, 20 Apr 2026 23:19:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:19:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 20 Apr 2026 23:19:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f035ba2a42b8a1b8f5674047539d50309c58d7c0bf025d946c8f93adad50a897`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9c5f1fb9544e1b87160680d79634b2756df9965406bd997d83f86b1d3f189c`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b565c834d59fd84b7e92785e9a9accffe3a2cbdbc7ebfb500176b62589acb11`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 6.2 MB (6170286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6e6468bcd71dd7e73c59c8ff211f3c3289b5689095efa58d80e7c7ccbfd766`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df58ba29e4716abfaa57ad92746073b6fdb2edc9ade56de9beacae40efc1ca54`  
		Last Modified: Mon, 20 Apr 2026 23:20:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506bcb676d56150811d81dfeecf8c775ce1d8e9e3e42fcaff4cebedef91e668d`  
		Last Modified: Mon, 20 Apr 2026 23:20:23 GMT  
		Size: 51.6 MB (51577760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a156be315d3009791029be3f35d7721f77d2f89b4c7c375fc21c6df01f33f5`  
		Last Modified: Mon, 20 Apr 2026 23:20:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b97080db618a59c7c1070d873c7676532d8130e4bd4abdc2b6da3010cad2ef1`  
		Last Modified: Mon, 20 Apr 2026 23:20:25 GMT  
		Size: 132.4 MB (132399697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182cd03161a6cc330cb3179e00ff03735060afe188a3c76b53de39ef68999458`  
		Last Modified: Mon, 20 Apr 2026 23:20:22 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:7223a3adb58c8156d99db3de7f6342b5147e32d330f3d08bc4ec098100c6f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15745116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc67f490818bb61b95b6408046b9c5243613c72188b7cf80013e7d060e813ba`

```dockerfile
```

-	Layers:
	-	`sha256:1201b5e782671f22800dff24fcf7729c366d7a8337fbf14c030bd213872a8460`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 15.7 MB (15710908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a530fb7783681a437b82d56d63db4aabe40bffb3f30296334a72c46875fd8b05`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b7ed149136988390cae1671eaf6b0697862623a9fa7ddc8777fc7722c0202895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233045862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56936cd75b2986359042279d478d41ddfdd00cd71cb130d68c61022db4707f9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 23:14:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 20 Apr 2026 23:14:58 GMT
ENV GOSU_VERSION=1.19
# Mon, 20 Apr 2026 23:14:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 20 Apr 2026 23:15:26 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:16:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 20 Apr 2026 23:16:36 GMT
VOLUME [/var/lib/mysql]
# Mon, 20 Apr 2026 23:16:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:16:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 20 Apr 2026 23:16:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a399ba9772226ad05fc45b09486adaff0390a7a25d9acda9819ecaa0f1e63d4f`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc07e22dc332f1680db8d5b4b7af4819586de6467b5f7f7f4c30ef46ed280d`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d41ef28c6723b46e3cab697745ea772e477b2518d13e301db151b61742345e0`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 5.8 MB (5793247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4f50cc254bbb68037b0d7fc835c251d31470f308ba8a2124c1d185b2c9f0a3`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c8ae92d35fb8a44794be7bb1ec22650ee3fb2f7903c8a966ade3af1fc80d83`  
		Last Modified: Mon, 20 Apr 2026 23:17:08 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757bc719f797504a0979fa4f8ce02238dd52823a0632c3bb6ed26bcc38ddecb1`  
		Last Modified: Mon, 20 Apr 2026 23:17:10 GMT  
		Size: 49.8 MB (49827767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca20ece91f44e5655427eed64840d8ef712de22c13f7a72775ab55dd659d36c`  
		Last Modified: Mon, 20 Apr 2026 23:17:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e8458c4ba6e54bce45741648c81c4a86874636c2131f149d2fde04115f2395`  
		Last Modified: Mon, 20 Apr 2026 23:17:13 GMT  
		Size: 130.8 MB (130778054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e967d5df3dfeddf636fe21b8267a213c56fb0101310ab536b03ec7ea673b659`  
		Last Modified: Mon, 20 Apr 2026 23:17:10 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:b68801a94249dca9abfa20e5adc37e05a40bba3101ccbf6af110f235234a17fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1486769bd3d1cc7c2392fe3ddbe873d685a118902324d049806adb91669f44e`

```dockerfile
```

-	Layers:
	-	`sha256:113cd58fe861869dadb0d755929aad301cb3ccc8489c76764c4181d8d9111035`  
		Last Modified: Mon, 20 Apr 2026 23:17:08 GMT  
		Size: 15.7 MB (15709328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dbe4130d194d2bd90f313c72d219b95b4b827ee15b2ff641c775b68ab304fa5`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:43bd9764df60666fb2ba2cf8217dd17b3d2414c150005d2fdd07a0cd73d3b7f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8096dd88a82dad3741f292e282d36b577097926735aeee8960c9b8c759453bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238250587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c55658453cceab502e6a7f2d3abe7292180c6f71f463972bcae809304979c06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 23:18:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 20 Apr 2026 23:18:18 GMT
ENV GOSU_VERSION=1.19
# Mon, 20 Apr 2026 23:18:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 20 Apr 2026 23:18:44 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:19:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 20 Apr 2026 23:19:48 GMT
VOLUME [/var/lib/mysql]
# Mon, 20 Apr 2026 23:19:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:19:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 20 Apr 2026 23:19:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f035ba2a42b8a1b8f5674047539d50309c58d7c0bf025d946c8f93adad50a897`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9c5f1fb9544e1b87160680d79634b2756df9965406bd997d83f86b1d3f189c`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b565c834d59fd84b7e92785e9a9accffe3a2cbdbc7ebfb500176b62589acb11`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 6.2 MB (6170286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6e6468bcd71dd7e73c59c8ff211f3c3289b5689095efa58d80e7c7ccbfd766`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df58ba29e4716abfaa57ad92746073b6fdb2edc9ade56de9beacae40efc1ca54`  
		Last Modified: Mon, 20 Apr 2026 23:20:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506bcb676d56150811d81dfeecf8c775ce1d8e9e3e42fcaff4cebedef91e668d`  
		Last Modified: Mon, 20 Apr 2026 23:20:23 GMT  
		Size: 51.6 MB (51577760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a156be315d3009791029be3f35d7721f77d2f89b4c7c375fc21c6df01f33f5`  
		Last Modified: Mon, 20 Apr 2026 23:20:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b97080db618a59c7c1070d873c7676532d8130e4bd4abdc2b6da3010cad2ef1`  
		Last Modified: Mon, 20 Apr 2026 23:20:25 GMT  
		Size: 132.4 MB (132399697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182cd03161a6cc330cb3179e00ff03735060afe188a3c76b53de39ef68999458`  
		Last Modified: Mon, 20 Apr 2026 23:20:22 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7223a3adb58c8156d99db3de7f6342b5147e32d330f3d08bc4ec098100c6f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15745116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc67f490818bb61b95b6408046b9c5243613c72188b7cf80013e7d060e813ba`

```dockerfile
```

-	Layers:
	-	`sha256:1201b5e782671f22800dff24fcf7729c366d7a8337fbf14c030bd213872a8460`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 15.7 MB (15710908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a530fb7783681a437b82d56d63db4aabe40bffb3f30296334a72c46875fd8b05`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b7ed149136988390cae1671eaf6b0697862623a9fa7ddc8777fc7722c0202895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233045862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56936cd75b2986359042279d478d41ddfdd00cd71cb130d68c61022db4707f9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 23:14:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 20 Apr 2026 23:14:58 GMT
ENV GOSU_VERSION=1.19
# Mon, 20 Apr 2026 23:14:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 20 Apr 2026 23:15:26 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:16:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 20 Apr 2026 23:16:36 GMT
VOLUME [/var/lib/mysql]
# Mon, 20 Apr 2026 23:16:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:16:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 20 Apr 2026 23:16:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a399ba9772226ad05fc45b09486adaff0390a7a25d9acda9819ecaa0f1e63d4f`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc07e22dc332f1680db8d5b4b7af4819586de6467b5f7f7f4c30ef46ed280d`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d41ef28c6723b46e3cab697745ea772e477b2518d13e301db151b61742345e0`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 5.8 MB (5793247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4f50cc254bbb68037b0d7fc835c251d31470f308ba8a2124c1d185b2c9f0a3`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c8ae92d35fb8a44794be7bb1ec22650ee3fb2f7903c8a966ade3af1fc80d83`  
		Last Modified: Mon, 20 Apr 2026 23:17:08 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757bc719f797504a0979fa4f8ce02238dd52823a0632c3bb6ed26bcc38ddecb1`  
		Last Modified: Mon, 20 Apr 2026 23:17:10 GMT  
		Size: 49.8 MB (49827767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca20ece91f44e5655427eed64840d8ef712de22c13f7a72775ab55dd659d36c`  
		Last Modified: Mon, 20 Apr 2026 23:17:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e8458c4ba6e54bce45741648c81c4a86874636c2131f149d2fde04115f2395`  
		Last Modified: Mon, 20 Apr 2026 23:17:13 GMT  
		Size: 130.8 MB (130778054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e967d5df3dfeddf636fe21b8267a213c56fb0101310ab536b03ec7ea673b659`  
		Last Modified: Mon, 20 Apr 2026 23:17:10 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b68801a94249dca9abfa20e5adc37e05a40bba3101ccbf6af110f235234a17fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1486769bd3d1cc7c2392fe3ddbe873d685a118902324d049806adb91669f44e`

```dockerfile
```

-	Layers:
	-	`sha256:113cd58fe861869dadb0d755929aad301cb3ccc8489c76764c4181d8d9111035`  
		Last Modified: Mon, 20 Apr 2026 23:17:08 GMT  
		Size: 15.7 MB (15709328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dbe4130d194d2bd90f313c72d219b95b4b827ee15b2ff641c775b68ab304fa5`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:43bd9764df60666fb2ba2cf8217dd17b3d2414c150005d2fdd07a0cd73d3b7f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:8096dd88a82dad3741f292e282d36b577097926735aeee8960c9b8c759453bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238250587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c55658453cceab502e6a7f2d3abe7292180c6f71f463972bcae809304979c06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 23:18:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 20 Apr 2026 23:18:18 GMT
ENV GOSU_VERSION=1.19
# Mon, 20 Apr 2026 23:18:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 20 Apr 2026 23:18:44 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:19:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 20 Apr 2026 23:19:48 GMT
VOLUME [/var/lib/mysql]
# Mon, 20 Apr 2026 23:19:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:19:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 20 Apr 2026 23:19:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f035ba2a42b8a1b8f5674047539d50309c58d7c0bf025d946c8f93adad50a897`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9c5f1fb9544e1b87160680d79634b2756df9965406bd997d83f86b1d3f189c`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b565c834d59fd84b7e92785e9a9accffe3a2cbdbc7ebfb500176b62589acb11`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 6.2 MB (6170286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6e6468bcd71dd7e73c59c8ff211f3c3289b5689095efa58d80e7c7ccbfd766`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df58ba29e4716abfaa57ad92746073b6fdb2edc9ade56de9beacae40efc1ca54`  
		Last Modified: Mon, 20 Apr 2026 23:20:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506bcb676d56150811d81dfeecf8c775ce1d8e9e3e42fcaff4cebedef91e668d`  
		Last Modified: Mon, 20 Apr 2026 23:20:23 GMT  
		Size: 51.6 MB (51577760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a156be315d3009791029be3f35d7721f77d2f89b4c7c375fc21c6df01f33f5`  
		Last Modified: Mon, 20 Apr 2026 23:20:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b97080db618a59c7c1070d873c7676532d8130e4bd4abdc2b6da3010cad2ef1`  
		Last Modified: Mon, 20 Apr 2026 23:20:25 GMT  
		Size: 132.4 MB (132399697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182cd03161a6cc330cb3179e00ff03735060afe188a3c76b53de39ef68999458`  
		Last Modified: Mon, 20 Apr 2026 23:20:22 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7223a3adb58c8156d99db3de7f6342b5147e32d330f3d08bc4ec098100c6f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15745116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc67f490818bb61b95b6408046b9c5243613c72188b7cf80013e7d060e813ba`

```dockerfile
```

-	Layers:
	-	`sha256:1201b5e782671f22800dff24fcf7729c366d7a8337fbf14c030bd213872a8460`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 15.7 MB (15710908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a530fb7783681a437b82d56d63db4aabe40bffb3f30296334a72c46875fd8b05`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b7ed149136988390cae1671eaf6b0697862623a9fa7ddc8777fc7722c0202895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233045862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56936cd75b2986359042279d478d41ddfdd00cd71cb130d68c61022db4707f9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 23:14:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 20 Apr 2026 23:14:58 GMT
ENV GOSU_VERSION=1.19
# Mon, 20 Apr 2026 23:14:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 20 Apr 2026 23:15:26 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:16:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 20 Apr 2026 23:16:36 GMT
VOLUME [/var/lib/mysql]
# Mon, 20 Apr 2026 23:16:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:16:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 20 Apr 2026 23:16:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a399ba9772226ad05fc45b09486adaff0390a7a25d9acda9819ecaa0f1e63d4f`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc07e22dc332f1680db8d5b4b7af4819586de6467b5f7f7f4c30ef46ed280d`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d41ef28c6723b46e3cab697745ea772e477b2518d13e301db151b61742345e0`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 5.8 MB (5793247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4f50cc254bbb68037b0d7fc835c251d31470f308ba8a2124c1d185b2c9f0a3`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c8ae92d35fb8a44794be7bb1ec22650ee3fb2f7903c8a966ade3af1fc80d83`  
		Last Modified: Mon, 20 Apr 2026 23:17:08 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757bc719f797504a0979fa4f8ce02238dd52823a0632c3bb6ed26bcc38ddecb1`  
		Last Modified: Mon, 20 Apr 2026 23:17:10 GMT  
		Size: 49.8 MB (49827767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca20ece91f44e5655427eed64840d8ef712de22c13f7a72775ab55dd659d36c`  
		Last Modified: Mon, 20 Apr 2026 23:17:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e8458c4ba6e54bce45741648c81c4a86874636c2131f149d2fde04115f2395`  
		Last Modified: Mon, 20 Apr 2026 23:17:13 GMT  
		Size: 130.8 MB (130778054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e967d5df3dfeddf636fe21b8267a213c56fb0101310ab536b03ec7ea673b659`  
		Last Modified: Mon, 20 Apr 2026 23:17:10 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b68801a94249dca9abfa20e5adc37e05a40bba3101ccbf6af110f235234a17fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1486769bd3d1cc7c2392fe3ddbe873d685a118902324d049806adb91669f44e`

```dockerfile
```

-	Layers:
	-	`sha256:113cd58fe861869dadb0d755929aad301cb3ccc8489c76764c4181d8d9111035`  
		Last Modified: Mon, 20 Apr 2026 23:17:08 GMT  
		Size: 15.7 MB (15709328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dbe4130d194d2bd90f313c72d219b95b4b827ee15b2ff641c775b68ab304fa5`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.9`

```console
$ docker pull mysql@sha256:43bd9764df60666fb2ba2cf8217dd17b3d2414c150005d2fdd07a0cd73d3b7f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.9` - linux; amd64

```console
$ docker pull mysql@sha256:8096dd88a82dad3741f292e282d36b577097926735aeee8960c9b8c759453bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238250587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c55658453cceab502e6a7f2d3abe7292180c6f71f463972bcae809304979c06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 23:18:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 20 Apr 2026 23:18:18 GMT
ENV GOSU_VERSION=1.19
# Mon, 20 Apr 2026 23:18:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 20 Apr 2026 23:18:44 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:19:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 20 Apr 2026 23:19:48 GMT
VOLUME [/var/lib/mysql]
# Mon, 20 Apr 2026 23:19:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:19:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 20 Apr 2026 23:19:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f035ba2a42b8a1b8f5674047539d50309c58d7c0bf025d946c8f93adad50a897`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9c5f1fb9544e1b87160680d79634b2756df9965406bd997d83f86b1d3f189c`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b565c834d59fd84b7e92785e9a9accffe3a2cbdbc7ebfb500176b62589acb11`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 6.2 MB (6170286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6e6468bcd71dd7e73c59c8ff211f3c3289b5689095efa58d80e7c7ccbfd766`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df58ba29e4716abfaa57ad92746073b6fdb2edc9ade56de9beacae40efc1ca54`  
		Last Modified: Mon, 20 Apr 2026 23:20:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506bcb676d56150811d81dfeecf8c775ce1d8e9e3e42fcaff4cebedef91e668d`  
		Last Modified: Mon, 20 Apr 2026 23:20:23 GMT  
		Size: 51.6 MB (51577760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a156be315d3009791029be3f35d7721f77d2f89b4c7c375fc21c6df01f33f5`  
		Last Modified: Mon, 20 Apr 2026 23:20:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b97080db618a59c7c1070d873c7676532d8130e4bd4abdc2b6da3010cad2ef1`  
		Last Modified: Mon, 20 Apr 2026 23:20:25 GMT  
		Size: 132.4 MB (132399697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182cd03161a6cc330cb3179e00ff03735060afe188a3c76b53de39ef68999458`  
		Last Modified: Mon, 20 Apr 2026 23:20:22 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.9` - unknown; unknown

```console
$ docker pull mysql@sha256:7223a3adb58c8156d99db3de7f6342b5147e32d330f3d08bc4ec098100c6f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15745116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc67f490818bb61b95b6408046b9c5243613c72188b7cf80013e7d060e813ba`

```dockerfile
```

-	Layers:
	-	`sha256:1201b5e782671f22800dff24fcf7729c366d7a8337fbf14c030bd213872a8460`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 15.7 MB (15710908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a530fb7783681a437b82d56d63db4aabe40bffb3f30296334a72c46875fd8b05`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b7ed149136988390cae1671eaf6b0697862623a9fa7ddc8777fc7722c0202895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233045862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56936cd75b2986359042279d478d41ddfdd00cd71cb130d68c61022db4707f9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 23:14:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 20 Apr 2026 23:14:58 GMT
ENV GOSU_VERSION=1.19
# Mon, 20 Apr 2026 23:14:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 20 Apr 2026 23:15:26 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:16:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 20 Apr 2026 23:16:36 GMT
VOLUME [/var/lib/mysql]
# Mon, 20 Apr 2026 23:16:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:16:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 20 Apr 2026 23:16:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a399ba9772226ad05fc45b09486adaff0390a7a25d9acda9819ecaa0f1e63d4f`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc07e22dc332f1680db8d5b4b7af4819586de6467b5f7f7f4c30ef46ed280d`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d41ef28c6723b46e3cab697745ea772e477b2518d13e301db151b61742345e0`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 5.8 MB (5793247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4f50cc254bbb68037b0d7fc835c251d31470f308ba8a2124c1d185b2c9f0a3`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c8ae92d35fb8a44794be7bb1ec22650ee3fb2f7903c8a966ade3af1fc80d83`  
		Last Modified: Mon, 20 Apr 2026 23:17:08 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757bc719f797504a0979fa4f8ce02238dd52823a0632c3bb6ed26bcc38ddecb1`  
		Last Modified: Mon, 20 Apr 2026 23:17:10 GMT  
		Size: 49.8 MB (49827767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca20ece91f44e5655427eed64840d8ef712de22c13f7a72775ab55dd659d36c`  
		Last Modified: Mon, 20 Apr 2026 23:17:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e8458c4ba6e54bce45741648c81c4a86874636c2131f149d2fde04115f2395`  
		Last Modified: Mon, 20 Apr 2026 23:17:13 GMT  
		Size: 130.8 MB (130778054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e967d5df3dfeddf636fe21b8267a213c56fb0101310ab536b03ec7ea673b659`  
		Last Modified: Mon, 20 Apr 2026 23:17:10 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.9` - unknown; unknown

```console
$ docker pull mysql@sha256:b68801a94249dca9abfa20e5adc37e05a40bba3101ccbf6af110f235234a17fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1486769bd3d1cc7c2392fe3ddbe873d685a118902324d049806adb91669f44e`

```dockerfile
```

-	Layers:
	-	`sha256:113cd58fe861869dadb0d755929aad301cb3ccc8489c76764c4181d8d9111035`  
		Last Modified: Mon, 20 Apr 2026 23:17:08 GMT  
		Size: 15.7 MB (15709328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dbe4130d194d2bd90f313c72d219b95b4b827ee15b2ff641c775b68ab304fa5`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.9-oracle`

```console
$ docker pull mysql@sha256:43bd9764df60666fb2ba2cf8217dd17b3d2414c150005d2fdd07a0cd73d3b7f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8096dd88a82dad3741f292e282d36b577097926735aeee8960c9b8c759453bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238250587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c55658453cceab502e6a7f2d3abe7292180c6f71f463972bcae809304979c06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 23:18:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 20 Apr 2026 23:18:18 GMT
ENV GOSU_VERSION=1.19
# Mon, 20 Apr 2026 23:18:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 20 Apr 2026 23:18:44 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:19:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 20 Apr 2026 23:19:48 GMT
VOLUME [/var/lib/mysql]
# Mon, 20 Apr 2026 23:19:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:19:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 20 Apr 2026 23:19:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f035ba2a42b8a1b8f5674047539d50309c58d7c0bf025d946c8f93adad50a897`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9c5f1fb9544e1b87160680d79634b2756df9965406bd997d83f86b1d3f189c`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b565c834d59fd84b7e92785e9a9accffe3a2cbdbc7ebfb500176b62589acb11`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 6.2 MB (6170286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6e6468bcd71dd7e73c59c8ff211f3c3289b5689095efa58d80e7c7ccbfd766`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df58ba29e4716abfaa57ad92746073b6fdb2edc9ade56de9beacae40efc1ca54`  
		Last Modified: Mon, 20 Apr 2026 23:20:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506bcb676d56150811d81dfeecf8c775ce1d8e9e3e42fcaff4cebedef91e668d`  
		Last Modified: Mon, 20 Apr 2026 23:20:23 GMT  
		Size: 51.6 MB (51577760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a156be315d3009791029be3f35d7721f77d2f89b4c7c375fc21c6df01f33f5`  
		Last Modified: Mon, 20 Apr 2026 23:20:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b97080db618a59c7c1070d873c7676532d8130e4bd4abdc2b6da3010cad2ef1`  
		Last Modified: Mon, 20 Apr 2026 23:20:25 GMT  
		Size: 132.4 MB (132399697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182cd03161a6cc330cb3179e00ff03735060afe188a3c76b53de39ef68999458`  
		Last Modified: Mon, 20 Apr 2026 23:20:22 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7223a3adb58c8156d99db3de7f6342b5147e32d330f3d08bc4ec098100c6f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15745116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc67f490818bb61b95b6408046b9c5243613c72188b7cf80013e7d060e813ba`

```dockerfile
```

-	Layers:
	-	`sha256:1201b5e782671f22800dff24fcf7729c366d7a8337fbf14c030bd213872a8460`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 15.7 MB (15710908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a530fb7783681a437b82d56d63db4aabe40bffb3f30296334a72c46875fd8b05`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b7ed149136988390cae1671eaf6b0697862623a9fa7ddc8777fc7722c0202895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233045862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56936cd75b2986359042279d478d41ddfdd00cd71cb130d68c61022db4707f9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 23:14:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 20 Apr 2026 23:14:58 GMT
ENV GOSU_VERSION=1.19
# Mon, 20 Apr 2026 23:14:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 20 Apr 2026 23:15:26 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:16:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 20 Apr 2026 23:16:36 GMT
VOLUME [/var/lib/mysql]
# Mon, 20 Apr 2026 23:16:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:16:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 20 Apr 2026 23:16:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a399ba9772226ad05fc45b09486adaff0390a7a25d9acda9819ecaa0f1e63d4f`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc07e22dc332f1680db8d5b4b7af4819586de6467b5f7f7f4c30ef46ed280d`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d41ef28c6723b46e3cab697745ea772e477b2518d13e301db151b61742345e0`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 5.8 MB (5793247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4f50cc254bbb68037b0d7fc835c251d31470f308ba8a2124c1d185b2c9f0a3`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c8ae92d35fb8a44794be7bb1ec22650ee3fb2f7903c8a966ade3af1fc80d83`  
		Last Modified: Mon, 20 Apr 2026 23:17:08 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757bc719f797504a0979fa4f8ce02238dd52823a0632c3bb6ed26bcc38ddecb1`  
		Last Modified: Mon, 20 Apr 2026 23:17:10 GMT  
		Size: 49.8 MB (49827767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca20ece91f44e5655427eed64840d8ef712de22c13f7a72775ab55dd659d36c`  
		Last Modified: Mon, 20 Apr 2026 23:17:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e8458c4ba6e54bce45741648c81c4a86874636c2131f149d2fde04115f2395`  
		Last Modified: Mon, 20 Apr 2026 23:17:13 GMT  
		Size: 130.8 MB (130778054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e967d5df3dfeddf636fe21b8267a213c56fb0101310ab536b03ec7ea673b659`  
		Last Modified: Mon, 20 Apr 2026 23:17:10 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b68801a94249dca9abfa20e5adc37e05a40bba3101ccbf6af110f235234a17fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1486769bd3d1cc7c2392fe3ddbe873d685a118902324d049806adb91669f44e`

```dockerfile
```

-	Layers:
	-	`sha256:113cd58fe861869dadb0d755929aad301cb3ccc8489c76764c4181d8d9111035`  
		Last Modified: Mon, 20 Apr 2026 23:17:08 GMT  
		Size: 15.7 MB (15709328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dbe4130d194d2bd90f313c72d219b95b4b827ee15b2ff641c775b68ab304fa5`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.9-oraclelinux9`

```console
$ docker pull mysql@sha256:43bd9764df60666fb2ba2cf8217dd17b3d2414c150005d2fdd07a0cd73d3b7f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:8096dd88a82dad3741f292e282d36b577097926735aeee8960c9b8c759453bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238250587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c55658453cceab502e6a7f2d3abe7292180c6f71f463972bcae809304979c06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 23:18:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 20 Apr 2026 23:18:18 GMT
ENV GOSU_VERSION=1.19
# Mon, 20 Apr 2026 23:18:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 20 Apr 2026 23:18:44 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 20 Apr 2026 23:18:44 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:18:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 20 Apr 2026 23:19:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:19:48 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 20 Apr 2026 23:19:48 GMT
VOLUME [/var/lib/mysql]
# Mon, 20 Apr 2026 23:19:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:19:48 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 20 Apr 2026 23:19:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f035ba2a42b8a1b8f5674047539d50309c58d7c0bf025d946c8f93adad50a897`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9c5f1fb9544e1b87160680d79634b2756df9965406bd997d83f86b1d3f189c`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b565c834d59fd84b7e92785e9a9accffe3a2cbdbc7ebfb500176b62589acb11`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 6.2 MB (6170286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6e6468bcd71dd7e73c59c8ff211f3c3289b5689095efa58d80e7c7ccbfd766`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df58ba29e4716abfaa57ad92746073b6fdb2edc9ade56de9beacae40efc1ca54`  
		Last Modified: Mon, 20 Apr 2026 23:20:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506bcb676d56150811d81dfeecf8c775ce1d8e9e3e42fcaff4cebedef91e668d`  
		Last Modified: Mon, 20 Apr 2026 23:20:23 GMT  
		Size: 51.6 MB (51577760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a156be315d3009791029be3f35d7721f77d2f89b4c7c375fc21c6df01f33f5`  
		Last Modified: Mon, 20 Apr 2026 23:20:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b97080db618a59c7c1070d873c7676532d8130e4bd4abdc2b6da3010cad2ef1`  
		Last Modified: Mon, 20 Apr 2026 23:20:25 GMT  
		Size: 132.4 MB (132399697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182cd03161a6cc330cb3179e00ff03735060afe188a3c76b53de39ef68999458`  
		Last Modified: Mon, 20 Apr 2026 23:20:22 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7223a3adb58c8156d99db3de7f6342b5147e32d330f3d08bc4ec098100c6f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15745116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc67f490818bb61b95b6408046b9c5243613c72188b7cf80013e7d060e813ba`

```dockerfile
```

-	Layers:
	-	`sha256:1201b5e782671f22800dff24fcf7729c366d7a8337fbf14c030bd213872a8460`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 15.7 MB (15710908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a530fb7783681a437b82d56d63db4aabe40bffb3f30296334a72c46875fd8b05`  
		Last Modified: Mon, 20 Apr 2026 23:20:20 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b7ed149136988390cae1671eaf6b0697862623a9fa7ddc8777fc7722c0202895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233045862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56936cd75b2986359042279d478d41ddfdd00cd71cb130d68c61022db4707f9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 23:14:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 20 Apr 2026 23:14:58 GMT
ENV GOSU_VERSION=1.19
# Mon, 20 Apr 2026 23:14:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 20 Apr 2026 23:15:26 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 20 Apr 2026 23:15:26 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:15:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 20 Apr 2026 23:16:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 20 Apr 2026 23:16:36 GMT
VOLUME [/var/lib/mysql]
# Mon, 20 Apr 2026 23:16:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:16:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 20 Apr 2026 23:16:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a399ba9772226ad05fc45b09486adaff0390a7a25d9acda9819ecaa0f1e63d4f`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc07e22dc332f1680db8d5b4b7af4819586de6467b5f7f7f4c30ef46ed280d`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d41ef28c6723b46e3cab697745ea772e477b2518d13e301db151b61742345e0`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 5.8 MB (5793247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4f50cc254bbb68037b0d7fc835c251d31470f308ba8a2124c1d185b2c9f0a3`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c8ae92d35fb8a44794be7bb1ec22650ee3fb2f7903c8a966ade3af1fc80d83`  
		Last Modified: Mon, 20 Apr 2026 23:17:08 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757bc719f797504a0979fa4f8ce02238dd52823a0632c3bb6ed26bcc38ddecb1`  
		Last Modified: Mon, 20 Apr 2026 23:17:10 GMT  
		Size: 49.8 MB (49827767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca20ece91f44e5655427eed64840d8ef712de22c13f7a72775ab55dd659d36c`  
		Last Modified: Mon, 20 Apr 2026 23:17:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e8458c4ba6e54bce45741648c81c4a86874636c2131f149d2fde04115f2395`  
		Last Modified: Mon, 20 Apr 2026 23:17:13 GMT  
		Size: 130.8 MB (130778054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e967d5df3dfeddf636fe21b8267a213c56fb0101310ab536b03ec7ea673b659`  
		Last Modified: Mon, 20 Apr 2026 23:17:10 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b68801a94249dca9abfa20e5adc37e05a40bba3101ccbf6af110f235234a17fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1486769bd3d1cc7c2392fe3ddbe873d685a118902324d049806adb91669f44e`

```dockerfile
```

-	Layers:
	-	`sha256:113cd58fe861869dadb0d755929aad301cb3ccc8489c76764c4181d8d9111035`  
		Last Modified: Mon, 20 Apr 2026 23:17:08 GMT  
		Size: 15.7 MB (15709328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dbe4130d194d2bd90f313c72d219b95b4b827ee15b2ff641c775b68ab304fa5`  
		Last Modified: Mon, 20 Apr 2026 23:17:07 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:c9e48b0c008f1936d4139d1c0dcd5950a9dbe57d4d40f383013cde432fa6d6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:537a1944f2b8623b55a74cde949488d3c46c0068d8eca6f7f54c5310f0a5c72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273451129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac34d07e4eeaa812627077a1ef6fdd881b747bb4dbe03f1742604c84535976b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191b09bcaa2f4b6ceac8d0a092752d710c7cb8c158f109fb44b0bc219d315f3e`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9f281a64d5f7c1adee5dd7d5e1c894de430238a10d0c4a41a73e306887b51`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae6deebd2fa83f366083d49c617bc812907f63192a98f714f794a563be07cc6`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 6.2 MB (6170254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b513c0ae344ea5695be1a37fd68ec9245479e1450059015c7d1a2c7be6012be`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9248317979a45744ddcebf6dc864e5b8ef351da623a270a7adbc6829b74b88bd`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7d368319daf4fe7b958b04f96c2a9c60e4359dd4cc134020e22825b4da75be`  
		Last Modified: Thu, 23 Apr 2026 01:01:48 GMT  
		Size: 57.0 MB (56969256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9dca007c40c7e33d142c2e4e063839d976b09a0057b1cf95803a237736a7f8`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf1cab22f6a5b111f8a0cbf806b16fdb585114a1cf370a9279286a548e1e77`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 162.2 MB (162208769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb28e454875147702a01891683ce3520e6e0d48aa0c75e2d9f6d7f3c6bf310b`  
		Last Modified: Thu, 23 Apr 2026 01:01:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:35400cf8c23d435d257eb41f611d1cbadde191808588fbfba36f36894ad952d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750613bae6e60c9ed24bac0793e629d92ac14959c02ea82f91346b3438010c8e`

```dockerfile
```

-	Layers:
	-	`sha256:48f6cb45c1a8becbdcbe9a814cea4e8823d670cb435eb4891b6859e25d9bc057`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 16.8 MB (16788746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd260c630db9c35d2f8cc5ceb01ca6a6be0ef9889e54015d3f126fe1b0212e86`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:89233db66310e90199c157a406ad8c670a8d7c7e80bb5814ce71657690447586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269914928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0392683984d253ce62ad4c0c7993a799564ac9655c2b7d600a5141b4cb819cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958292599b7314ec7dd613f8549b5316c9977b962863d3c2b71d3abef29ea931`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83bdb5799a03fed707127b8f442e590582d15b49e9b1ab921bbbf200fb66f06`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a146dbeb68544928a894500f7c80df9a5044c39cd48e20af21b5bcbd5e53a`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 5.8 MB (5793344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23eef2559d8c101ee648abd2a7ae553da5ad5c2349ad7bc57d794b135015fbb`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4a0bc67efe10e1bccf7f1d6ea0c6cd7db94beef9f7f3df6aa6f3bb63563e2`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9111beb1a028839fb654a5eaca276b63337ece9bc8300fa789d281155ab2a1`  
		Last Modified: Thu, 23 Apr 2026 01:01:54 GMT  
		Size: 57.0 MB (56983366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bce26e215509641f3dc484376219e784da8f9627435df6484a025872393461`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099716a3250a98c8616cea216e9bf1b08f369c62e5a0ee2ead1e2b04b5ac20f1`  
		Last Modified: Thu, 23 Apr 2026 01:01:57 GMT  
		Size: 160.5 MB (160491427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cfcef095841975363f6c03c416fe3b7f0f60d27900506f265dcdfadfc0136e`  
		Last Modified: Thu, 23 Apr 2026 01:01:53 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:777289978011ac1954f64074d705df42cfad749e83e68bd3c3b3742f9293cd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670354434e7ddc06769e6429b04e37b0e2613b16e4a25acf32640229c3cff5e5`

```dockerfile
```

-	Layers:
	-	`sha256:d7835c0dfd73722ed4a8affec245a3250b191f4c16b65dfccc0a39fc05c38914`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 16.8 MB (16787202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e86b702bce28d1e8390a520c6fcdcaafe60a0b70c0aadfeba3da1650449170d`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:c9e48b0c008f1936d4139d1c0dcd5950a9dbe57d4d40f383013cde432fa6d6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:537a1944f2b8623b55a74cde949488d3c46c0068d8eca6f7f54c5310f0a5c72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273451129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac34d07e4eeaa812627077a1ef6fdd881b747bb4dbe03f1742604c84535976b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191b09bcaa2f4b6ceac8d0a092752d710c7cb8c158f109fb44b0bc219d315f3e`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9f281a64d5f7c1adee5dd7d5e1c894de430238a10d0c4a41a73e306887b51`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae6deebd2fa83f366083d49c617bc812907f63192a98f714f794a563be07cc6`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 6.2 MB (6170254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b513c0ae344ea5695be1a37fd68ec9245479e1450059015c7d1a2c7be6012be`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9248317979a45744ddcebf6dc864e5b8ef351da623a270a7adbc6829b74b88bd`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7d368319daf4fe7b958b04f96c2a9c60e4359dd4cc134020e22825b4da75be`  
		Last Modified: Thu, 23 Apr 2026 01:01:48 GMT  
		Size: 57.0 MB (56969256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9dca007c40c7e33d142c2e4e063839d976b09a0057b1cf95803a237736a7f8`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf1cab22f6a5b111f8a0cbf806b16fdb585114a1cf370a9279286a548e1e77`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 162.2 MB (162208769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb28e454875147702a01891683ce3520e6e0d48aa0c75e2d9f6d7f3c6bf310b`  
		Last Modified: Thu, 23 Apr 2026 01:01:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:35400cf8c23d435d257eb41f611d1cbadde191808588fbfba36f36894ad952d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750613bae6e60c9ed24bac0793e629d92ac14959c02ea82f91346b3438010c8e`

```dockerfile
```

-	Layers:
	-	`sha256:48f6cb45c1a8becbdcbe9a814cea4e8823d670cb435eb4891b6859e25d9bc057`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 16.8 MB (16788746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd260c630db9c35d2f8cc5ceb01ca6a6be0ef9889e54015d3f126fe1b0212e86`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:89233db66310e90199c157a406ad8c670a8d7c7e80bb5814ce71657690447586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269914928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0392683984d253ce62ad4c0c7993a799564ac9655c2b7d600a5141b4cb819cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958292599b7314ec7dd613f8549b5316c9977b962863d3c2b71d3abef29ea931`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83bdb5799a03fed707127b8f442e590582d15b49e9b1ab921bbbf200fb66f06`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a146dbeb68544928a894500f7c80df9a5044c39cd48e20af21b5bcbd5e53a`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 5.8 MB (5793344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23eef2559d8c101ee648abd2a7ae553da5ad5c2349ad7bc57d794b135015fbb`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4a0bc67efe10e1bccf7f1d6ea0c6cd7db94beef9f7f3df6aa6f3bb63563e2`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9111beb1a028839fb654a5eaca276b63337ece9bc8300fa789d281155ab2a1`  
		Last Modified: Thu, 23 Apr 2026 01:01:54 GMT  
		Size: 57.0 MB (56983366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bce26e215509641f3dc484376219e784da8f9627435df6484a025872393461`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099716a3250a98c8616cea216e9bf1b08f369c62e5a0ee2ead1e2b04b5ac20f1`  
		Last Modified: Thu, 23 Apr 2026 01:01:57 GMT  
		Size: 160.5 MB (160491427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cfcef095841975363f6c03c416fe3b7f0f60d27900506f265dcdfadfc0136e`  
		Last Modified: Thu, 23 Apr 2026 01:01:53 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:777289978011ac1954f64074d705df42cfad749e83e68bd3c3b3742f9293cd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670354434e7ddc06769e6429b04e37b0e2613b16e4a25acf32640229c3cff5e5`

```dockerfile
```

-	Layers:
	-	`sha256:d7835c0dfd73722ed4a8affec245a3250b191f4c16b65dfccc0a39fc05c38914`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 16.8 MB (16787202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e86b702bce28d1e8390a520c6fcdcaafe60a0b70c0aadfeba3da1650449170d`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:c9e48b0c008f1936d4139d1c0dcd5950a9dbe57d4d40f383013cde432fa6d6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:537a1944f2b8623b55a74cde949488d3c46c0068d8eca6f7f54c5310f0a5c72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273451129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac34d07e4eeaa812627077a1ef6fdd881b747bb4dbe03f1742604c84535976b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191b09bcaa2f4b6ceac8d0a092752d710c7cb8c158f109fb44b0bc219d315f3e`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9f281a64d5f7c1adee5dd7d5e1c894de430238a10d0c4a41a73e306887b51`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae6deebd2fa83f366083d49c617bc812907f63192a98f714f794a563be07cc6`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 6.2 MB (6170254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b513c0ae344ea5695be1a37fd68ec9245479e1450059015c7d1a2c7be6012be`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9248317979a45744ddcebf6dc864e5b8ef351da623a270a7adbc6829b74b88bd`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7d368319daf4fe7b958b04f96c2a9c60e4359dd4cc134020e22825b4da75be`  
		Last Modified: Thu, 23 Apr 2026 01:01:48 GMT  
		Size: 57.0 MB (56969256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9dca007c40c7e33d142c2e4e063839d976b09a0057b1cf95803a237736a7f8`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf1cab22f6a5b111f8a0cbf806b16fdb585114a1cf370a9279286a548e1e77`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 162.2 MB (162208769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb28e454875147702a01891683ce3520e6e0d48aa0c75e2d9f6d7f3c6bf310b`  
		Last Modified: Thu, 23 Apr 2026 01:01:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:35400cf8c23d435d257eb41f611d1cbadde191808588fbfba36f36894ad952d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750613bae6e60c9ed24bac0793e629d92ac14959c02ea82f91346b3438010c8e`

```dockerfile
```

-	Layers:
	-	`sha256:48f6cb45c1a8becbdcbe9a814cea4e8823d670cb435eb4891b6859e25d9bc057`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 16.8 MB (16788746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd260c630db9c35d2f8cc5ceb01ca6a6be0ef9889e54015d3f126fe1b0212e86`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:89233db66310e90199c157a406ad8c670a8d7c7e80bb5814ce71657690447586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269914928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0392683984d253ce62ad4c0c7993a799564ac9655c2b7d600a5141b4cb819cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958292599b7314ec7dd613f8549b5316c9977b962863d3c2b71d3abef29ea931`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83bdb5799a03fed707127b8f442e590582d15b49e9b1ab921bbbf200fb66f06`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a146dbeb68544928a894500f7c80df9a5044c39cd48e20af21b5bcbd5e53a`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 5.8 MB (5793344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23eef2559d8c101ee648abd2a7ae553da5ad5c2349ad7bc57d794b135015fbb`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4a0bc67efe10e1bccf7f1d6ea0c6cd7db94beef9f7f3df6aa6f3bb63563e2`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9111beb1a028839fb654a5eaca276b63337ece9bc8300fa789d281155ab2a1`  
		Last Modified: Thu, 23 Apr 2026 01:01:54 GMT  
		Size: 57.0 MB (56983366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bce26e215509641f3dc484376219e784da8f9627435df6484a025872393461`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099716a3250a98c8616cea216e9bf1b08f369c62e5a0ee2ead1e2b04b5ac20f1`  
		Last Modified: Thu, 23 Apr 2026 01:01:57 GMT  
		Size: 160.5 MB (160491427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cfcef095841975363f6c03c416fe3b7f0f60d27900506f265dcdfadfc0136e`  
		Last Modified: Thu, 23 Apr 2026 01:01:53 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:777289978011ac1954f64074d705df42cfad749e83e68bd3c3b3742f9293cd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670354434e7ddc06769e6429b04e37b0e2613b16e4a25acf32640229c3cff5e5`

```dockerfile
```

-	Layers:
	-	`sha256:d7835c0dfd73722ed4a8affec245a3250b191f4c16b65dfccc0a39fc05c38914`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 16.8 MB (16787202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e86b702bce28d1e8390a520c6fcdcaafe60a0b70c0aadfeba3da1650449170d`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7`

```console
$ docker pull mysql@sha256:c9e48b0c008f1936d4139d1c0dcd5950a9dbe57d4d40f383013cde432fa6d6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7` - linux; amd64

```console
$ docker pull mysql@sha256:537a1944f2b8623b55a74cde949488d3c46c0068d8eca6f7f54c5310f0a5c72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273451129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac34d07e4eeaa812627077a1ef6fdd881b747bb4dbe03f1742604c84535976b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191b09bcaa2f4b6ceac8d0a092752d710c7cb8c158f109fb44b0bc219d315f3e`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9f281a64d5f7c1adee5dd7d5e1c894de430238a10d0c4a41a73e306887b51`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae6deebd2fa83f366083d49c617bc812907f63192a98f714f794a563be07cc6`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 6.2 MB (6170254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b513c0ae344ea5695be1a37fd68ec9245479e1450059015c7d1a2c7be6012be`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9248317979a45744ddcebf6dc864e5b8ef351da623a270a7adbc6829b74b88bd`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7d368319daf4fe7b958b04f96c2a9c60e4359dd4cc134020e22825b4da75be`  
		Last Modified: Thu, 23 Apr 2026 01:01:48 GMT  
		Size: 57.0 MB (56969256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9dca007c40c7e33d142c2e4e063839d976b09a0057b1cf95803a237736a7f8`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf1cab22f6a5b111f8a0cbf806b16fdb585114a1cf370a9279286a548e1e77`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 162.2 MB (162208769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb28e454875147702a01891683ce3520e6e0d48aa0c75e2d9f6d7f3c6bf310b`  
		Last Modified: Thu, 23 Apr 2026 01:01:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7` - unknown; unknown

```console
$ docker pull mysql@sha256:35400cf8c23d435d257eb41f611d1cbadde191808588fbfba36f36894ad952d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750613bae6e60c9ed24bac0793e629d92ac14959c02ea82f91346b3438010c8e`

```dockerfile
```

-	Layers:
	-	`sha256:48f6cb45c1a8becbdcbe9a814cea4e8823d670cb435eb4891b6859e25d9bc057`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 16.8 MB (16788746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd260c630db9c35d2f8cc5ceb01ca6a6be0ef9889e54015d3f126fe1b0212e86`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:89233db66310e90199c157a406ad8c670a8d7c7e80bb5814ce71657690447586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269914928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0392683984d253ce62ad4c0c7993a799564ac9655c2b7d600a5141b4cb819cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958292599b7314ec7dd613f8549b5316c9977b962863d3c2b71d3abef29ea931`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83bdb5799a03fed707127b8f442e590582d15b49e9b1ab921bbbf200fb66f06`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a146dbeb68544928a894500f7c80df9a5044c39cd48e20af21b5bcbd5e53a`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 5.8 MB (5793344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23eef2559d8c101ee648abd2a7ae553da5ad5c2349ad7bc57d794b135015fbb`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4a0bc67efe10e1bccf7f1d6ea0c6cd7db94beef9f7f3df6aa6f3bb63563e2`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9111beb1a028839fb654a5eaca276b63337ece9bc8300fa789d281155ab2a1`  
		Last Modified: Thu, 23 Apr 2026 01:01:54 GMT  
		Size: 57.0 MB (56983366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bce26e215509641f3dc484376219e784da8f9627435df6484a025872393461`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099716a3250a98c8616cea216e9bf1b08f369c62e5a0ee2ead1e2b04b5ac20f1`  
		Last Modified: Thu, 23 Apr 2026 01:01:57 GMT  
		Size: 160.5 MB (160491427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cfcef095841975363f6c03c416fe3b7f0f60d27900506f265dcdfadfc0136e`  
		Last Modified: Thu, 23 Apr 2026 01:01:53 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7` - unknown; unknown

```console
$ docker pull mysql@sha256:777289978011ac1954f64074d705df42cfad749e83e68bd3c3b3742f9293cd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670354434e7ddc06769e6429b04e37b0e2613b16e4a25acf32640229c3cff5e5`

```dockerfile
```

-	Layers:
	-	`sha256:d7835c0dfd73722ed4a8affec245a3250b191f4c16b65dfccc0a39fc05c38914`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 16.8 MB (16787202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e86b702bce28d1e8390a520c6fcdcaafe60a0b70c0aadfeba3da1650449170d`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7-oracle`

```console
$ docker pull mysql@sha256:c9e48b0c008f1936d4139d1c0dcd5950a9dbe57d4d40f383013cde432fa6d6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:537a1944f2b8623b55a74cde949488d3c46c0068d8eca6f7f54c5310f0a5c72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273451129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac34d07e4eeaa812627077a1ef6fdd881b747bb4dbe03f1742604c84535976b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191b09bcaa2f4b6ceac8d0a092752d710c7cb8c158f109fb44b0bc219d315f3e`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9f281a64d5f7c1adee5dd7d5e1c894de430238a10d0c4a41a73e306887b51`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae6deebd2fa83f366083d49c617bc812907f63192a98f714f794a563be07cc6`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 6.2 MB (6170254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b513c0ae344ea5695be1a37fd68ec9245479e1450059015c7d1a2c7be6012be`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9248317979a45744ddcebf6dc864e5b8ef351da623a270a7adbc6829b74b88bd`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7d368319daf4fe7b958b04f96c2a9c60e4359dd4cc134020e22825b4da75be`  
		Last Modified: Thu, 23 Apr 2026 01:01:48 GMT  
		Size: 57.0 MB (56969256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9dca007c40c7e33d142c2e4e063839d976b09a0057b1cf95803a237736a7f8`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf1cab22f6a5b111f8a0cbf806b16fdb585114a1cf370a9279286a548e1e77`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 162.2 MB (162208769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb28e454875147702a01891683ce3520e6e0d48aa0c75e2d9f6d7f3c6bf310b`  
		Last Modified: Thu, 23 Apr 2026 01:01:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:35400cf8c23d435d257eb41f611d1cbadde191808588fbfba36f36894ad952d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750613bae6e60c9ed24bac0793e629d92ac14959c02ea82f91346b3438010c8e`

```dockerfile
```

-	Layers:
	-	`sha256:48f6cb45c1a8becbdcbe9a814cea4e8823d670cb435eb4891b6859e25d9bc057`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 16.8 MB (16788746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd260c630db9c35d2f8cc5ceb01ca6a6be0ef9889e54015d3f126fe1b0212e86`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:89233db66310e90199c157a406ad8c670a8d7c7e80bb5814ce71657690447586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269914928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0392683984d253ce62ad4c0c7993a799564ac9655c2b7d600a5141b4cb819cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958292599b7314ec7dd613f8549b5316c9977b962863d3c2b71d3abef29ea931`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83bdb5799a03fed707127b8f442e590582d15b49e9b1ab921bbbf200fb66f06`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a146dbeb68544928a894500f7c80df9a5044c39cd48e20af21b5bcbd5e53a`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 5.8 MB (5793344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23eef2559d8c101ee648abd2a7ae553da5ad5c2349ad7bc57d794b135015fbb`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4a0bc67efe10e1bccf7f1d6ea0c6cd7db94beef9f7f3df6aa6f3bb63563e2`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9111beb1a028839fb654a5eaca276b63337ece9bc8300fa789d281155ab2a1`  
		Last Modified: Thu, 23 Apr 2026 01:01:54 GMT  
		Size: 57.0 MB (56983366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bce26e215509641f3dc484376219e784da8f9627435df6484a025872393461`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099716a3250a98c8616cea216e9bf1b08f369c62e5a0ee2ead1e2b04b5ac20f1`  
		Last Modified: Thu, 23 Apr 2026 01:01:57 GMT  
		Size: 160.5 MB (160491427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cfcef095841975363f6c03c416fe3b7f0f60d27900506f265dcdfadfc0136e`  
		Last Modified: Thu, 23 Apr 2026 01:01:53 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:777289978011ac1954f64074d705df42cfad749e83e68bd3c3b3742f9293cd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670354434e7ddc06769e6429b04e37b0e2613b16e4a25acf32640229c3cff5e5`

```dockerfile
```

-	Layers:
	-	`sha256:d7835c0dfd73722ed4a8affec245a3250b191f4c16b65dfccc0a39fc05c38914`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 16.8 MB (16787202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e86b702bce28d1e8390a520c6fcdcaafe60a0b70c0aadfeba3da1650449170d`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7-oraclelinux9`

```console
$ docker pull mysql@sha256:c9e48b0c008f1936d4139d1c0dcd5950a9dbe57d4d40f383013cde432fa6d6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:537a1944f2b8623b55a74cde949488d3c46c0068d8eca6f7f54c5310f0a5c72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273451129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac34d07e4eeaa812627077a1ef6fdd881b747bb4dbe03f1742604c84535976b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191b09bcaa2f4b6ceac8d0a092752d710c7cb8c158f109fb44b0bc219d315f3e`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9f281a64d5f7c1adee5dd7d5e1c894de430238a10d0c4a41a73e306887b51`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae6deebd2fa83f366083d49c617bc812907f63192a98f714f794a563be07cc6`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 6.2 MB (6170254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b513c0ae344ea5695be1a37fd68ec9245479e1450059015c7d1a2c7be6012be`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9248317979a45744ddcebf6dc864e5b8ef351da623a270a7adbc6829b74b88bd`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7d368319daf4fe7b958b04f96c2a9c60e4359dd4cc134020e22825b4da75be`  
		Last Modified: Thu, 23 Apr 2026 01:01:48 GMT  
		Size: 57.0 MB (56969256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9dca007c40c7e33d142c2e4e063839d976b09a0057b1cf95803a237736a7f8`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf1cab22f6a5b111f8a0cbf806b16fdb585114a1cf370a9279286a548e1e77`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 162.2 MB (162208769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb28e454875147702a01891683ce3520e6e0d48aa0c75e2d9f6d7f3c6bf310b`  
		Last Modified: Thu, 23 Apr 2026 01:01:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:35400cf8c23d435d257eb41f611d1cbadde191808588fbfba36f36894ad952d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750613bae6e60c9ed24bac0793e629d92ac14959c02ea82f91346b3438010c8e`

```dockerfile
```

-	Layers:
	-	`sha256:48f6cb45c1a8becbdcbe9a814cea4e8823d670cb435eb4891b6859e25d9bc057`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 16.8 MB (16788746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd260c630db9c35d2f8cc5ceb01ca6a6be0ef9889e54015d3f126fe1b0212e86`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:89233db66310e90199c157a406ad8c670a8d7c7e80bb5814ce71657690447586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269914928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0392683984d253ce62ad4c0c7993a799564ac9655c2b7d600a5141b4cb819cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958292599b7314ec7dd613f8549b5316c9977b962863d3c2b71d3abef29ea931`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83bdb5799a03fed707127b8f442e590582d15b49e9b1ab921bbbf200fb66f06`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a146dbeb68544928a894500f7c80df9a5044c39cd48e20af21b5bcbd5e53a`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 5.8 MB (5793344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23eef2559d8c101ee648abd2a7ae553da5ad5c2349ad7bc57d794b135015fbb`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4a0bc67efe10e1bccf7f1d6ea0c6cd7db94beef9f7f3df6aa6f3bb63563e2`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9111beb1a028839fb654a5eaca276b63337ece9bc8300fa789d281155ab2a1`  
		Last Modified: Thu, 23 Apr 2026 01:01:54 GMT  
		Size: 57.0 MB (56983366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bce26e215509641f3dc484376219e784da8f9627435df6484a025872393461`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099716a3250a98c8616cea216e9bf1b08f369c62e5a0ee2ead1e2b04b5ac20f1`  
		Last Modified: Thu, 23 Apr 2026 01:01:57 GMT  
		Size: 160.5 MB (160491427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cfcef095841975363f6c03c416fe3b7f0f60d27900506f265dcdfadfc0136e`  
		Last Modified: Thu, 23 Apr 2026 01:01:53 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:777289978011ac1954f64074d705df42cfad749e83e68bd3c3b3742f9293cd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670354434e7ddc06769e6429b04e37b0e2613b16e4a25acf32640229c3cff5e5`

```dockerfile
```

-	Layers:
	-	`sha256:d7835c0dfd73722ed4a8affec245a3250b191f4c16b65dfccc0a39fc05c38914`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 16.8 MB (16787202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e86b702bce28d1e8390a520c6fcdcaafe60a0b70c0aadfeba3da1650449170d`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7.0`

```console
$ docker pull mysql@sha256:c9e48b0c008f1936d4139d1c0dcd5950a9dbe57d4d40f383013cde432fa6d6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7.0` - linux; amd64

```console
$ docker pull mysql@sha256:537a1944f2b8623b55a74cde949488d3c46c0068d8eca6f7f54c5310f0a5c72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273451129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac34d07e4eeaa812627077a1ef6fdd881b747bb4dbe03f1742604c84535976b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191b09bcaa2f4b6ceac8d0a092752d710c7cb8c158f109fb44b0bc219d315f3e`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9f281a64d5f7c1adee5dd7d5e1c894de430238a10d0c4a41a73e306887b51`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae6deebd2fa83f366083d49c617bc812907f63192a98f714f794a563be07cc6`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 6.2 MB (6170254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b513c0ae344ea5695be1a37fd68ec9245479e1450059015c7d1a2c7be6012be`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9248317979a45744ddcebf6dc864e5b8ef351da623a270a7adbc6829b74b88bd`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7d368319daf4fe7b958b04f96c2a9c60e4359dd4cc134020e22825b4da75be`  
		Last Modified: Thu, 23 Apr 2026 01:01:48 GMT  
		Size: 57.0 MB (56969256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9dca007c40c7e33d142c2e4e063839d976b09a0057b1cf95803a237736a7f8`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf1cab22f6a5b111f8a0cbf806b16fdb585114a1cf370a9279286a548e1e77`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 162.2 MB (162208769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb28e454875147702a01891683ce3520e6e0d48aa0c75e2d9f6d7f3c6bf310b`  
		Last Modified: Thu, 23 Apr 2026 01:01:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7.0` - unknown; unknown

```console
$ docker pull mysql@sha256:35400cf8c23d435d257eb41f611d1cbadde191808588fbfba36f36894ad952d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750613bae6e60c9ed24bac0793e629d92ac14959c02ea82f91346b3438010c8e`

```dockerfile
```

-	Layers:
	-	`sha256:48f6cb45c1a8becbdcbe9a814cea4e8823d670cb435eb4891b6859e25d9bc057`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 16.8 MB (16788746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd260c630db9c35d2f8cc5ceb01ca6a6be0ef9889e54015d3f126fe1b0212e86`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:89233db66310e90199c157a406ad8c670a8d7c7e80bb5814ce71657690447586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269914928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0392683984d253ce62ad4c0c7993a799564ac9655c2b7d600a5141b4cb819cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958292599b7314ec7dd613f8549b5316c9977b962863d3c2b71d3abef29ea931`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83bdb5799a03fed707127b8f442e590582d15b49e9b1ab921bbbf200fb66f06`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a146dbeb68544928a894500f7c80df9a5044c39cd48e20af21b5bcbd5e53a`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 5.8 MB (5793344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23eef2559d8c101ee648abd2a7ae553da5ad5c2349ad7bc57d794b135015fbb`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4a0bc67efe10e1bccf7f1d6ea0c6cd7db94beef9f7f3df6aa6f3bb63563e2`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9111beb1a028839fb654a5eaca276b63337ece9bc8300fa789d281155ab2a1`  
		Last Modified: Thu, 23 Apr 2026 01:01:54 GMT  
		Size: 57.0 MB (56983366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bce26e215509641f3dc484376219e784da8f9627435df6484a025872393461`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099716a3250a98c8616cea216e9bf1b08f369c62e5a0ee2ead1e2b04b5ac20f1`  
		Last Modified: Thu, 23 Apr 2026 01:01:57 GMT  
		Size: 160.5 MB (160491427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cfcef095841975363f6c03c416fe3b7f0f60d27900506f265dcdfadfc0136e`  
		Last Modified: Thu, 23 Apr 2026 01:01:53 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7.0` - unknown; unknown

```console
$ docker pull mysql@sha256:777289978011ac1954f64074d705df42cfad749e83e68bd3c3b3742f9293cd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670354434e7ddc06769e6429b04e37b0e2613b16e4a25acf32640229c3cff5e5`

```dockerfile
```

-	Layers:
	-	`sha256:d7835c0dfd73722ed4a8affec245a3250b191f4c16b65dfccc0a39fc05c38914`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 16.8 MB (16787202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e86b702bce28d1e8390a520c6fcdcaafe60a0b70c0aadfeba3da1650449170d`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7.0-oracle`

```console
$ docker pull mysql@sha256:c9e48b0c008f1936d4139d1c0dcd5950a9dbe57d4d40f383013cde432fa6d6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:537a1944f2b8623b55a74cde949488d3c46c0068d8eca6f7f54c5310f0a5c72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273451129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac34d07e4eeaa812627077a1ef6fdd881b747bb4dbe03f1742604c84535976b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191b09bcaa2f4b6ceac8d0a092752d710c7cb8c158f109fb44b0bc219d315f3e`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9f281a64d5f7c1adee5dd7d5e1c894de430238a10d0c4a41a73e306887b51`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae6deebd2fa83f366083d49c617bc812907f63192a98f714f794a563be07cc6`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 6.2 MB (6170254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b513c0ae344ea5695be1a37fd68ec9245479e1450059015c7d1a2c7be6012be`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9248317979a45744ddcebf6dc864e5b8ef351da623a270a7adbc6829b74b88bd`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7d368319daf4fe7b958b04f96c2a9c60e4359dd4cc134020e22825b4da75be`  
		Last Modified: Thu, 23 Apr 2026 01:01:48 GMT  
		Size: 57.0 MB (56969256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9dca007c40c7e33d142c2e4e063839d976b09a0057b1cf95803a237736a7f8`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf1cab22f6a5b111f8a0cbf806b16fdb585114a1cf370a9279286a548e1e77`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 162.2 MB (162208769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb28e454875147702a01891683ce3520e6e0d48aa0c75e2d9f6d7f3c6bf310b`  
		Last Modified: Thu, 23 Apr 2026 01:01:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:35400cf8c23d435d257eb41f611d1cbadde191808588fbfba36f36894ad952d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750613bae6e60c9ed24bac0793e629d92ac14959c02ea82f91346b3438010c8e`

```dockerfile
```

-	Layers:
	-	`sha256:48f6cb45c1a8becbdcbe9a814cea4e8823d670cb435eb4891b6859e25d9bc057`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 16.8 MB (16788746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd260c630db9c35d2f8cc5ceb01ca6a6be0ef9889e54015d3f126fe1b0212e86`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:89233db66310e90199c157a406ad8c670a8d7c7e80bb5814ce71657690447586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269914928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0392683984d253ce62ad4c0c7993a799564ac9655c2b7d600a5141b4cb819cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958292599b7314ec7dd613f8549b5316c9977b962863d3c2b71d3abef29ea931`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83bdb5799a03fed707127b8f442e590582d15b49e9b1ab921bbbf200fb66f06`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a146dbeb68544928a894500f7c80df9a5044c39cd48e20af21b5bcbd5e53a`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 5.8 MB (5793344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23eef2559d8c101ee648abd2a7ae553da5ad5c2349ad7bc57d794b135015fbb`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4a0bc67efe10e1bccf7f1d6ea0c6cd7db94beef9f7f3df6aa6f3bb63563e2`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9111beb1a028839fb654a5eaca276b63337ece9bc8300fa789d281155ab2a1`  
		Last Modified: Thu, 23 Apr 2026 01:01:54 GMT  
		Size: 57.0 MB (56983366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bce26e215509641f3dc484376219e784da8f9627435df6484a025872393461`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099716a3250a98c8616cea216e9bf1b08f369c62e5a0ee2ead1e2b04b5ac20f1`  
		Last Modified: Thu, 23 Apr 2026 01:01:57 GMT  
		Size: 160.5 MB (160491427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cfcef095841975363f6c03c416fe3b7f0f60d27900506f265dcdfadfc0136e`  
		Last Modified: Thu, 23 Apr 2026 01:01:53 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:777289978011ac1954f64074d705df42cfad749e83e68bd3c3b3742f9293cd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670354434e7ddc06769e6429b04e37b0e2613b16e4a25acf32640229c3cff5e5`

```dockerfile
```

-	Layers:
	-	`sha256:d7835c0dfd73722ed4a8affec245a3250b191f4c16b65dfccc0a39fc05c38914`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 16.8 MB (16787202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e86b702bce28d1e8390a520c6fcdcaafe60a0b70c0aadfeba3da1650449170d`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7.0-oraclelinux9`

```console
$ docker pull mysql@sha256:c9e48b0c008f1936d4139d1c0dcd5950a9dbe57d4d40f383013cde432fa6d6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:537a1944f2b8623b55a74cde949488d3c46c0068d8eca6f7f54c5310f0a5c72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273451129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac34d07e4eeaa812627077a1ef6fdd881b747bb4dbe03f1742604c84535976b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191b09bcaa2f4b6ceac8d0a092752d710c7cb8c158f109fb44b0bc219d315f3e`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9f281a64d5f7c1adee5dd7d5e1c894de430238a10d0c4a41a73e306887b51`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae6deebd2fa83f366083d49c617bc812907f63192a98f714f794a563be07cc6`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 6.2 MB (6170254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b513c0ae344ea5695be1a37fd68ec9245479e1450059015c7d1a2c7be6012be`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9248317979a45744ddcebf6dc864e5b8ef351da623a270a7adbc6829b74b88bd`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7d368319daf4fe7b958b04f96c2a9c60e4359dd4cc134020e22825b4da75be`  
		Last Modified: Thu, 23 Apr 2026 01:01:48 GMT  
		Size: 57.0 MB (56969256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9dca007c40c7e33d142c2e4e063839d976b09a0057b1cf95803a237736a7f8`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf1cab22f6a5b111f8a0cbf806b16fdb585114a1cf370a9279286a548e1e77`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 162.2 MB (162208769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb28e454875147702a01891683ce3520e6e0d48aa0c75e2d9f6d7f3c6bf310b`  
		Last Modified: Thu, 23 Apr 2026 01:01:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:35400cf8c23d435d257eb41f611d1cbadde191808588fbfba36f36894ad952d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750613bae6e60c9ed24bac0793e629d92ac14959c02ea82f91346b3438010c8e`

```dockerfile
```

-	Layers:
	-	`sha256:48f6cb45c1a8becbdcbe9a814cea4e8823d670cb435eb4891b6859e25d9bc057`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 16.8 MB (16788746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd260c630db9c35d2f8cc5ceb01ca6a6be0ef9889e54015d3f126fe1b0212e86`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:89233db66310e90199c157a406ad8c670a8d7c7e80bb5814ce71657690447586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269914928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0392683984d253ce62ad4c0c7993a799564ac9655c2b7d600a5141b4cb819cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958292599b7314ec7dd613f8549b5316c9977b962863d3c2b71d3abef29ea931`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83bdb5799a03fed707127b8f442e590582d15b49e9b1ab921bbbf200fb66f06`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a146dbeb68544928a894500f7c80df9a5044c39cd48e20af21b5bcbd5e53a`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 5.8 MB (5793344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23eef2559d8c101ee648abd2a7ae553da5ad5c2349ad7bc57d794b135015fbb`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4a0bc67efe10e1bccf7f1d6ea0c6cd7db94beef9f7f3df6aa6f3bb63563e2`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9111beb1a028839fb654a5eaca276b63337ece9bc8300fa789d281155ab2a1`  
		Last Modified: Thu, 23 Apr 2026 01:01:54 GMT  
		Size: 57.0 MB (56983366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bce26e215509641f3dc484376219e784da8f9627435df6484a025872393461`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099716a3250a98c8616cea216e9bf1b08f369c62e5a0ee2ead1e2b04b5ac20f1`  
		Last Modified: Thu, 23 Apr 2026 01:01:57 GMT  
		Size: 160.5 MB (160491427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cfcef095841975363f6c03c416fe3b7f0f60d27900506f265dcdfadfc0136e`  
		Last Modified: Thu, 23 Apr 2026 01:01:53 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:777289978011ac1954f64074d705df42cfad749e83e68bd3c3b3742f9293cd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670354434e7ddc06769e6429b04e37b0e2613b16e4a25acf32640229c3cff5e5`

```dockerfile
```

-	Layers:
	-	`sha256:d7835c0dfd73722ed4a8affec245a3250b191f4c16b65dfccc0a39fc05c38914`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 16.8 MB (16787202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e86b702bce28d1e8390a520c6fcdcaafe60a0b70c0aadfeba3da1650449170d`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:c9e48b0c008f1936d4139d1c0dcd5950a9dbe57d4d40f383013cde432fa6d6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:537a1944f2b8623b55a74cde949488d3c46c0068d8eca6f7f54c5310f0a5c72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273451129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac34d07e4eeaa812627077a1ef6fdd881b747bb4dbe03f1742604c84535976b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191b09bcaa2f4b6ceac8d0a092752d710c7cb8c158f109fb44b0bc219d315f3e`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9f281a64d5f7c1adee5dd7d5e1c894de430238a10d0c4a41a73e306887b51`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae6deebd2fa83f366083d49c617bc812907f63192a98f714f794a563be07cc6`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 6.2 MB (6170254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b513c0ae344ea5695be1a37fd68ec9245479e1450059015c7d1a2c7be6012be`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9248317979a45744ddcebf6dc864e5b8ef351da623a270a7adbc6829b74b88bd`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7d368319daf4fe7b958b04f96c2a9c60e4359dd4cc134020e22825b4da75be`  
		Last Modified: Thu, 23 Apr 2026 01:01:48 GMT  
		Size: 57.0 MB (56969256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9dca007c40c7e33d142c2e4e063839d976b09a0057b1cf95803a237736a7f8`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf1cab22f6a5b111f8a0cbf806b16fdb585114a1cf370a9279286a548e1e77`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 162.2 MB (162208769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb28e454875147702a01891683ce3520e6e0d48aa0c75e2d9f6d7f3c6bf310b`  
		Last Modified: Thu, 23 Apr 2026 01:01:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:35400cf8c23d435d257eb41f611d1cbadde191808588fbfba36f36894ad952d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750613bae6e60c9ed24bac0793e629d92ac14959c02ea82f91346b3438010c8e`

```dockerfile
```

-	Layers:
	-	`sha256:48f6cb45c1a8becbdcbe9a814cea4e8823d670cb435eb4891b6859e25d9bc057`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 16.8 MB (16788746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd260c630db9c35d2f8cc5ceb01ca6a6be0ef9889e54015d3f126fe1b0212e86`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:89233db66310e90199c157a406ad8c670a8d7c7e80bb5814ce71657690447586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269914928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0392683984d253ce62ad4c0c7993a799564ac9655c2b7d600a5141b4cb819cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958292599b7314ec7dd613f8549b5316c9977b962863d3c2b71d3abef29ea931`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83bdb5799a03fed707127b8f442e590582d15b49e9b1ab921bbbf200fb66f06`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a146dbeb68544928a894500f7c80df9a5044c39cd48e20af21b5bcbd5e53a`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 5.8 MB (5793344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23eef2559d8c101ee648abd2a7ae553da5ad5c2349ad7bc57d794b135015fbb`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4a0bc67efe10e1bccf7f1d6ea0c6cd7db94beef9f7f3df6aa6f3bb63563e2`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9111beb1a028839fb654a5eaca276b63337ece9bc8300fa789d281155ab2a1`  
		Last Modified: Thu, 23 Apr 2026 01:01:54 GMT  
		Size: 57.0 MB (56983366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bce26e215509641f3dc484376219e784da8f9627435df6484a025872393461`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099716a3250a98c8616cea216e9bf1b08f369c62e5a0ee2ead1e2b04b5ac20f1`  
		Last Modified: Thu, 23 Apr 2026 01:01:57 GMT  
		Size: 160.5 MB (160491427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cfcef095841975363f6c03c416fe3b7f0f60d27900506f265dcdfadfc0136e`  
		Last Modified: Thu, 23 Apr 2026 01:01:53 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:777289978011ac1954f64074d705df42cfad749e83e68bd3c3b3742f9293cd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670354434e7ddc06769e6429b04e37b0e2613b16e4a25acf32640229c3cff5e5`

```dockerfile
```

-	Layers:
	-	`sha256:d7835c0dfd73722ed4a8affec245a3250b191f4c16b65dfccc0a39fc05c38914`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 16.8 MB (16787202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e86b702bce28d1e8390a520c6fcdcaafe60a0b70c0aadfeba3da1650449170d`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:c9e48b0c008f1936d4139d1c0dcd5950a9dbe57d4d40f383013cde432fa6d6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:537a1944f2b8623b55a74cde949488d3c46c0068d8eca6f7f54c5310f0a5c72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273451129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac34d07e4eeaa812627077a1ef6fdd881b747bb4dbe03f1742604c84535976b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191b09bcaa2f4b6ceac8d0a092752d710c7cb8c158f109fb44b0bc219d315f3e`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9f281a64d5f7c1adee5dd7d5e1c894de430238a10d0c4a41a73e306887b51`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae6deebd2fa83f366083d49c617bc812907f63192a98f714f794a563be07cc6`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 6.2 MB (6170254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b513c0ae344ea5695be1a37fd68ec9245479e1450059015c7d1a2c7be6012be`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9248317979a45744ddcebf6dc864e5b8ef351da623a270a7adbc6829b74b88bd`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7d368319daf4fe7b958b04f96c2a9c60e4359dd4cc134020e22825b4da75be`  
		Last Modified: Thu, 23 Apr 2026 01:01:48 GMT  
		Size: 57.0 MB (56969256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9dca007c40c7e33d142c2e4e063839d976b09a0057b1cf95803a237736a7f8`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf1cab22f6a5b111f8a0cbf806b16fdb585114a1cf370a9279286a548e1e77`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 162.2 MB (162208769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb28e454875147702a01891683ce3520e6e0d48aa0c75e2d9f6d7f3c6bf310b`  
		Last Modified: Thu, 23 Apr 2026 01:01:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:35400cf8c23d435d257eb41f611d1cbadde191808588fbfba36f36894ad952d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750613bae6e60c9ed24bac0793e629d92ac14959c02ea82f91346b3438010c8e`

```dockerfile
```

-	Layers:
	-	`sha256:48f6cb45c1a8becbdcbe9a814cea4e8823d670cb435eb4891b6859e25d9bc057`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 16.8 MB (16788746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd260c630db9c35d2f8cc5ceb01ca6a6be0ef9889e54015d3f126fe1b0212e86`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:89233db66310e90199c157a406ad8c670a8d7c7e80bb5814ce71657690447586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269914928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0392683984d253ce62ad4c0c7993a799564ac9655c2b7d600a5141b4cb819cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958292599b7314ec7dd613f8549b5316c9977b962863d3c2b71d3abef29ea931`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83bdb5799a03fed707127b8f442e590582d15b49e9b1ab921bbbf200fb66f06`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a146dbeb68544928a894500f7c80df9a5044c39cd48e20af21b5bcbd5e53a`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 5.8 MB (5793344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23eef2559d8c101ee648abd2a7ae553da5ad5c2349ad7bc57d794b135015fbb`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4a0bc67efe10e1bccf7f1d6ea0c6cd7db94beef9f7f3df6aa6f3bb63563e2`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9111beb1a028839fb654a5eaca276b63337ece9bc8300fa789d281155ab2a1`  
		Last Modified: Thu, 23 Apr 2026 01:01:54 GMT  
		Size: 57.0 MB (56983366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bce26e215509641f3dc484376219e784da8f9627435df6484a025872393461`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099716a3250a98c8616cea216e9bf1b08f369c62e5a0ee2ead1e2b04b5ac20f1`  
		Last Modified: Thu, 23 Apr 2026 01:01:57 GMT  
		Size: 160.5 MB (160491427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cfcef095841975363f6c03c416fe3b7f0f60d27900506f265dcdfadfc0136e`  
		Last Modified: Thu, 23 Apr 2026 01:01:53 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:777289978011ac1954f64074d705df42cfad749e83e68bd3c3b3742f9293cd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670354434e7ddc06769e6429b04e37b0e2613b16e4a25acf32640229c3cff5e5`

```dockerfile
```

-	Layers:
	-	`sha256:d7835c0dfd73722ed4a8affec245a3250b191f4c16b65dfccc0a39fc05c38914`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 16.8 MB (16787202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e86b702bce28d1e8390a520c6fcdcaafe60a0b70c0aadfeba3da1650449170d`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:c9e48b0c008f1936d4139d1c0dcd5950a9dbe57d4d40f383013cde432fa6d6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:537a1944f2b8623b55a74cde949488d3c46c0068d8eca6f7f54c5310f0a5c72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273451129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac34d07e4eeaa812627077a1ef6fdd881b747bb4dbe03f1742604c84535976b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191b09bcaa2f4b6ceac8d0a092752d710c7cb8c158f109fb44b0bc219d315f3e`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9f281a64d5f7c1adee5dd7d5e1c894de430238a10d0c4a41a73e306887b51`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae6deebd2fa83f366083d49c617bc812907f63192a98f714f794a563be07cc6`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 6.2 MB (6170254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b513c0ae344ea5695be1a37fd68ec9245479e1450059015c7d1a2c7be6012be`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9248317979a45744ddcebf6dc864e5b8ef351da623a270a7adbc6829b74b88bd`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7d368319daf4fe7b958b04f96c2a9c60e4359dd4cc134020e22825b4da75be`  
		Last Modified: Thu, 23 Apr 2026 01:01:48 GMT  
		Size: 57.0 MB (56969256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9dca007c40c7e33d142c2e4e063839d976b09a0057b1cf95803a237736a7f8`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf1cab22f6a5b111f8a0cbf806b16fdb585114a1cf370a9279286a548e1e77`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 162.2 MB (162208769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb28e454875147702a01891683ce3520e6e0d48aa0c75e2d9f6d7f3c6bf310b`  
		Last Modified: Thu, 23 Apr 2026 01:01:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:35400cf8c23d435d257eb41f611d1cbadde191808588fbfba36f36894ad952d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750613bae6e60c9ed24bac0793e629d92ac14959c02ea82f91346b3438010c8e`

```dockerfile
```

-	Layers:
	-	`sha256:48f6cb45c1a8becbdcbe9a814cea4e8823d670cb435eb4891b6859e25d9bc057`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 16.8 MB (16788746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd260c630db9c35d2f8cc5ceb01ca6a6be0ef9889e54015d3f126fe1b0212e86`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:89233db66310e90199c157a406ad8c670a8d7c7e80bb5814ce71657690447586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269914928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0392683984d253ce62ad4c0c7993a799564ac9655c2b7d600a5141b4cb819cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958292599b7314ec7dd613f8549b5316c9977b962863d3c2b71d3abef29ea931`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83bdb5799a03fed707127b8f442e590582d15b49e9b1ab921bbbf200fb66f06`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a146dbeb68544928a894500f7c80df9a5044c39cd48e20af21b5bcbd5e53a`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 5.8 MB (5793344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23eef2559d8c101ee648abd2a7ae553da5ad5c2349ad7bc57d794b135015fbb`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4a0bc67efe10e1bccf7f1d6ea0c6cd7db94beef9f7f3df6aa6f3bb63563e2`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9111beb1a028839fb654a5eaca276b63337ece9bc8300fa789d281155ab2a1`  
		Last Modified: Thu, 23 Apr 2026 01:01:54 GMT  
		Size: 57.0 MB (56983366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bce26e215509641f3dc484376219e784da8f9627435df6484a025872393461`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099716a3250a98c8616cea216e9bf1b08f369c62e5a0ee2ead1e2b04b5ac20f1`  
		Last Modified: Thu, 23 Apr 2026 01:01:57 GMT  
		Size: 160.5 MB (160491427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cfcef095841975363f6c03c416fe3b7f0f60d27900506f265dcdfadfc0136e`  
		Last Modified: Thu, 23 Apr 2026 01:01:53 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:777289978011ac1954f64074d705df42cfad749e83e68bd3c3b3742f9293cd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670354434e7ddc06769e6429b04e37b0e2613b16e4a25acf32640229c3cff5e5`

```dockerfile
```

-	Layers:
	-	`sha256:d7835c0dfd73722ed4a8affec245a3250b191f4c16b65dfccc0a39fc05c38914`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 16.8 MB (16787202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e86b702bce28d1e8390a520c6fcdcaafe60a0b70c0aadfeba3da1650449170d`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:c9e48b0c008f1936d4139d1c0dcd5950a9dbe57d4d40f383013cde432fa6d6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:537a1944f2b8623b55a74cde949488d3c46c0068d8eca6f7f54c5310f0a5c72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273451129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac34d07e4eeaa812627077a1ef6fdd881b747bb4dbe03f1742604c84535976b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191b09bcaa2f4b6ceac8d0a092752d710c7cb8c158f109fb44b0bc219d315f3e`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9f281a64d5f7c1adee5dd7d5e1c894de430238a10d0c4a41a73e306887b51`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae6deebd2fa83f366083d49c617bc812907f63192a98f714f794a563be07cc6`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 6.2 MB (6170254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b513c0ae344ea5695be1a37fd68ec9245479e1450059015c7d1a2c7be6012be`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9248317979a45744ddcebf6dc864e5b8ef351da623a270a7adbc6829b74b88bd`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7d368319daf4fe7b958b04f96c2a9c60e4359dd4cc134020e22825b4da75be`  
		Last Modified: Thu, 23 Apr 2026 01:01:48 GMT  
		Size: 57.0 MB (56969256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9dca007c40c7e33d142c2e4e063839d976b09a0057b1cf95803a237736a7f8`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf1cab22f6a5b111f8a0cbf806b16fdb585114a1cf370a9279286a548e1e77`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 162.2 MB (162208769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb28e454875147702a01891683ce3520e6e0d48aa0c75e2d9f6d7f3c6bf310b`  
		Last Modified: Thu, 23 Apr 2026 01:01:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:35400cf8c23d435d257eb41f611d1cbadde191808588fbfba36f36894ad952d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750613bae6e60c9ed24bac0793e629d92ac14959c02ea82f91346b3438010c8e`

```dockerfile
```

-	Layers:
	-	`sha256:48f6cb45c1a8becbdcbe9a814cea4e8823d670cb435eb4891b6859e25d9bc057`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 16.8 MB (16788746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd260c630db9c35d2f8cc5ceb01ca6a6be0ef9889e54015d3f126fe1b0212e86`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:89233db66310e90199c157a406ad8c670a8d7c7e80bb5814ce71657690447586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269914928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0392683984d253ce62ad4c0c7993a799564ac9655c2b7d600a5141b4cb819cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958292599b7314ec7dd613f8549b5316c9977b962863d3c2b71d3abef29ea931`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83bdb5799a03fed707127b8f442e590582d15b49e9b1ab921bbbf200fb66f06`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a146dbeb68544928a894500f7c80df9a5044c39cd48e20af21b5bcbd5e53a`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 5.8 MB (5793344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23eef2559d8c101ee648abd2a7ae553da5ad5c2349ad7bc57d794b135015fbb`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4a0bc67efe10e1bccf7f1d6ea0c6cd7db94beef9f7f3df6aa6f3bb63563e2`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9111beb1a028839fb654a5eaca276b63337ece9bc8300fa789d281155ab2a1`  
		Last Modified: Thu, 23 Apr 2026 01:01:54 GMT  
		Size: 57.0 MB (56983366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bce26e215509641f3dc484376219e784da8f9627435df6484a025872393461`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099716a3250a98c8616cea216e9bf1b08f369c62e5a0ee2ead1e2b04b5ac20f1`  
		Last Modified: Thu, 23 Apr 2026 01:01:57 GMT  
		Size: 160.5 MB (160491427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cfcef095841975363f6c03c416fe3b7f0f60d27900506f265dcdfadfc0136e`  
		Last Modified: Thu, 23 Apr 2026 01:01:53 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:777289978011ac1954f64074d705df42cfad749e83e68bd3c3b3742f9293cd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670354434e7ddc06769e6429b04e37b0e2613b16e4a25acf32640229c3cff5e5`

```dockerfile
```

-	Layers:
	-	`sha256:d7835c0dfd73722ed4a8affec245a3250b191f4c16b65dfccc0a39fc05c38914`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 16.8 MB (16787202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e86b702bce28d1e8390a520c6fcdcaafe60a0b70c0aadfeba3da1650449170d`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:c9e48b0c008f1936d4139d1c0dcd5950a9dbe57d4d40f383013cde432fa6d6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:537a1944f2b8623b55a74cde949488d3c46c0068d8eca6f7f54c5310f0a5c72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273451129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac34d07e4eeaa812627077a1ef6fdd881b747bb4dbe03f1742604c84535976b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191b09bcaa2f4b6ceac8d0a092752d710c7cb8c158f109fb44b0bc219d315f3e`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9f281a64d5f7c1adee5dd7d5e1c894de430238a10d0c4a41a73e306887b51`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae6deebd2fa83f366083d49c617bc812907f63192a98f714f794a563be07cc6`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 6.2 MB (6170254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b513c0ae344ea5695be1a37fd68ec9245479e1450059015c7d1a2c7be6012be`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9248317979a45744ddcebf6dc864e5b8ef351da623a270a7adbc6829b74b88bd`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7d368319daf4fe7b958b04f96c2a9c60e4359dd4cc134020e22825b4da75be`  
		Last Modified: Thu, 23 Apr 2026 01:01:48 GMT  
		Size: 57.0 MB (56969256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9dca007c40c7e33d142c2e4e063839d976b09a0057b1cf95803a237736a7f8`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf1cab22f6a5b111f8a0cbf806b16fdb585114a1cf370a9279286a548e1e77`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 162.2 MB (162208769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb28e454875147702a01891683ce3520e6e0d48aa0c75e2d9f6d7f3c6bf310b`  
		Last Modified: Thu, 23 Apr 2026 01:01:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:35400cf8c23d435d257eb41f611d1cbadde191808588fbfba36f36894ad952d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750613bae6e60c9ed24bac0793e629d92ac14959c02ea82f91346b3438010c8e`

```dockerfile
```

-	Layers:
	-	`sha256:48f6cb45c1a8becbdcbe9a814cea4e8823d670cb435eb4891b6859e25d9bc057`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 16.8 MB (16788746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd260c630db9c35d2f8cc5ceb01ca6a6be0ef9889e54015d3f126fe1b0212e86`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:89233db66310e90199c157a406ad8c670a8d7c7e80bb5814ce71657690447586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269914928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0392683984d253ce62ad4c0c7993a799564ac9655c2b7d600a5141b4cb819cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958292599b7314ec7dd613f8549b5316c9977b962863d3c2b71d3abef29ea931`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83bdb5799a03fed707127b8f442e590582d15b49e9b1ab921bbbf200fb66f06`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a146dbeb68544928a894500f7c80df9a5044c39cd48e20af21b5bcbd5e53a`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 5.8 MB (5793344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23eef2559d8c101ee648abd2a7ae553da5ad5c2349ad7bc57d794b135015fbb`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4a0bc67efe10e1bccf7f1d6ea0c6cd7db94beef9f7f3df6aa6f3bb63563e2`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9111beb1a028839fb654a5eaca276b63337ece9bc8300fa789d281155ab2a1`  
		Last Modified: Thu, 23 Apr 2026 01:01:54 GMT  
		Size: 57.0 MB (56983366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bce26e215509641f3dc484376219e784da8f9627435df6484a025872393461`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099716a3250a98c8616cea216e9bf1b08f369c62e5a0ee2ead1e2b04b5ac20f1`  
		Last Modified: Thu, 23 Apr 2026 01:01:57 GMT  
		Size: 160.5 MB (160491427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cfcef095841975363f6c03c416fe3b7f0f60d27900506f265dcdfadfc0136e`  
		Last Modified: Thu, 23 Apr 2026 01:01:53 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:777289978011ac1954f64074d705df42cfad749e83e68bd3c3b3742f9293cd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670354434e7ddc06769e6429b04e37b0e2613b16e4a25acf32640229c3cff5e5`

```dockerfile
```

-	Layers:
	-	`sha256:d7835c0dfd73722ed4a8affec245a3250b191f4c16b65dfccc0a39fc05c38914`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 16.8 MB (16787202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e86b702bce28d1e8390a520c6fcdcaafe60a0b70c0aadfeba3da1650449170d`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:c9e48b0c008f1936d4139d1c0dcd5950a9dbe57d4d40f383013cde432fa6d6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:537a1944f2b8623b55a74cde949488d3c46c0068d8eca6f7f54c5310f0a5c72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273451129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac34d07e4eeaa812627077a1ef6fdd881b747bb4dbe03f1742604c84535976b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191b09bcaa2f4b6ceac8d0a092752d710c7cb8c158f109fb44b0bc219d315f3e`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9f281a64d5f7c1adee5dd7d5e1c894de430238a10d0c4a41a73e306887b51`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae6deebd2fa83f366083d49c617bc812907f63192a98f714f794a563be07cc6`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 6.2 MB (6170254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b513c0ae344ea5695be1a37fd68ec9245479e1450059015c7d1a2c7be6012be`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9248317979a45744ddcebf6dc864e5b8ef351da623a270a7adbc6829b74b88bd`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7d368319daf4fe7b958b04f96c2a9c60e4359dd4cc134020e22825b4da75be`  
		Last Modified: Thu, 23 Apr 2026 01:01:48 GMT  
		Size: 57.0 MB (56969256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9dca007c40c7e33d142c2e4e063839d976b09a0057b1cf95803a237736a7f8`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf1cab22f6a5b111f8a0cbf806b16fdb585114a1cf370a9279286a548e1e77`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 162.2 MB (162208769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb28e454875147702a01891683ce3520e6e0d48aa0c75e2d9f6d7f3c6bf310b`  
		Last Modified: Thu, 23 Apr 2026 01:01:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:35400cf8c23d435d257eb41f611d1cbadde191808588fbfba36f36894ad952d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750613bae6e60c9ed24bac0793e629d92ac14959c02ea82f91346b3438010c8e`

```dockerfile
```

-	Layers:
	-	`sha256:48f6cb45c1a8becbdcbe9a814cea4e8823d670cb435eb4891b6859e25d9bc057`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 16.8 MB (16788746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd260c630db9c35d2f8cc5ceb01ca6a6be0ef9889e54015d3f126fe1b0212e86`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:89233db66310e90199c157a406ad8c670a8d7c7e80bb5814ce71657690447586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269914928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0392683984d253ce62ad4c0c7993a799564ac9655c2b7d600a5141b4cb819cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:50 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:50 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:26 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958292599b7314ec7dd613f8549b5316c9977b962863d3c2b71d3abef29ea931`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83bdb5799a03fed707127b8f442e590582d15b49e9b1ab921bbbf200fb66f06`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a146dbeb68544928a894500f7c80df9a5044c39cd48e20af21b5bcbd5e53a`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 5.8 MB (5793344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23eef2559d8c101ee648abd2a7ae553da5ad5c2349ad7bc57d794b135015fbb`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4a0bc67efe10e1bccf7f1d6ea0c6cd7db94beef9f7f3df6aa6f3bb63563e2`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9111beb1a028839fb654a5eaca276b63337ece9bc8300fa789d281155ab2a1`  
		Last Modified: Thu, 23 Apr 2026 01:01:54 GMT  
		Size: 57.0 MB (56983366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bce26e215509641f3dc484376219e784da8f9627435df6484a025872393461`  
		Last Modified: Thu, 23 Apr 2026 01:01:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099716a3250a98c8616cea216e9bf1b08f369c62e5a0ee2ead1e2b04b5ac20f1`  
		Last Modified: Thu, 23 Apr 2026 01:01:57 GMT  
		Size: 160.5 MB (160491427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cfcef095841975363f6c03c416fe3b7f0f60d27900506f265dcdfadfc0136e`  
		Last Modified: Thu, 23 Apr 2026 01:01:53 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:777289978011ac1954f64074d705df42cfad749e83e68bd3c3b3742f9293cd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670354434e7ddc06769e6429b04e37b0e2613b16e4a25acf32640229c3cff5e5`

```dockerfile
```

-	Layers:
	-	`sha256:d7835c0dfd73722ed4a8affec245a3250b191f4c16b65dfccc0a39fc05c38914`  
		Last Modified: Thu, 23 Apr 2026 01:01:51 GMT  
		Size: 16.8 MB (16787202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e86b702bce28d1e8390a520c6fcdcaafe60a0b70c0aadfeba3da1650449170d`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json
