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
$ docker pull mysql@sha256:4af1f8815716546f5b12410f7621f37f93db8dd11a184706ef59111930b8c2ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:bcfecfdd2f8c2988c0db7335dfeed0dc336defe7007e98c5308f58168d808a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232278067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9272481a67f6ca40b0b29b2e102d29fa86b54c69e969883ce4705ece06bbf3d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:12:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:12:16 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:12:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:43 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 18 Apr 2026 00:12:43 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Sat, 18 Apr 2026 00:12:43 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:13:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:13:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:13:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Sat, 18 Apr 2026 00:13:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:50 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 18 Apr 2026 00:13:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:50 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a1a4fb3367dc55623389a4502dafe5c4b80a28e63533023c41bfb0eedfa356`  
		Last Modified: Sat, 18 Apr 2026 00:14:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69c68c7dd2162edcd7163732030b25dfd837c756bd5a183d6c77e98c793d469`  
		Last Modified: Sat, 18 Apr 2026 00:14:21 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6126bf990b9d25ee02468abf80406b6b2a9aefaf88bc6099d3e85031ee008ae`  
		Last Modified: Sat, 18 Apr 2026 00:14:21 GMT  
		Size: 6.2 MB (6170273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77ecc122bf40cbbcf5f49b8436f4f32753dc6d34c305c854ccea4fc5576c664`  
		Last Modified: Sat, 18 Apr 2026 00:14:21 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a966b78a59e9f2903466c252de71fa15162f6e6f03d2981a85657e6228696898`  
		Last Modified: Sat, 18 Apr 2026 00:14:22 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc827b16c7b9253c14abed3d8ef38216db3af30db2e948772ad83330b2a0751`  
		Last Modified: Sat, 18 Apr 2026 00:14:24 GMT  
		Size: 49.9 MB (49909952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ccadc91b4fa2f47fa562c638aa8d4e80e9a5b2cb8b12bab4d1f7aea0f83586`  
		Last Modified: Sat, 18 Apr 2026 00:14:22 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496eb3815f35004486146355aa0a146ac1810270cefb3967e904c07fa657d8ed`  
		Last Modified: Sat, 18 Apr 2026 00:14:26 GMT  
		Size: 128.1 MB (128094881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c350fcbc37b3909736eeb896c96b6cf30cd3c99cc5a0e4937c61ea3ab0c1b47e`  
		Last Modified: Sat, 18 Apr 2026 00:14:24 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e72ef22e056678f0d595eda7f04328a16be5c81ddb98f155f8d91f17462c8b`  
		Last Modified: Sat, 18 Apr 2026 00:14:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:37fcd1dc5bd7019a9d9557c5a579451e80279d0ffce7880ac5e7ee92718d3f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424d7d9564a58a14fa9b2691bef5436cc3a39107f77739d0a26327065b1f4a33`

```dockerfile
```

-	Layers:
	-	`sha256:0faffc9d5b7858fc1a118f35a0cd1444d253be2a6019a8159bd8503c52aa2197`  
		Last Modified: Sat, 18 Apr 2026 00:14:21 GMT  
		Size: 15.0 MB (14957541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0f0e180252c7e9db2e2d4dc137e3281a4f581d4c482257c90c8e0d2a17f1417`  
		Last Modified: Sat, 18 Apr 2026 00:14:21 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0e7040b532c0f2ac8cb822695d33025522acd5252175cb104a5929aa66b40222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227884633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9cc8fab569ceb806ffb83b5b91e0b953e84c096c87b31a36b5d1355c72633c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:12:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:12:04 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:12:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:33 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 18 Apr 2026 00:12:33 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Sat, 18 Apr 2026 00:12:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Sat, 18 Apr 2026 00:13:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:43 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 18 Apr 2026 00:13:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc94f9e40e97c93301716a04c45844be8892d60aa3dfbd672f58e274033719ee`  
		Last Modified: Sat, 18 Apr 2026 00:14:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8295d92b87f72abe5bf6a9b85af5ed9c2a022af1c74d2f5c7471ebdadd6561e9`  
		Last Modified: Sat, 18 Apr 2026 00:14:13 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a574c190fa744079fa99dd400c0c66c5e897e866021ef68859ad78d6216474`  
		Last Modified: Sat, 18 Apr 2026 00:14:13 GMT  
		Size: 5.8 MB (5793308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8312482523a97383fa4e1988cf357e22ab500a7532b038ac78364fd1002d7142`  
		Last Modified: Sat, 18 Apr 2026 00:14:13 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c793807e067a08cdd43ebf772868409b33cf69cbd77a40097303ee1e29aeed`  
		Last Modified: Sat, 18 Apr 2026 00:14:14 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f4b4c46fca3d35c547c3e8e4238eca72b22e1d9962ea3a7c08c2b3351710ab`  
		Last Modified: Sat, 18 Apr 2026 00:14:16 GMT  
		Size: 48.8 MB (48770063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e00e08c28e154b72643b3fef054432fd0e10b43b043ffd82e6c1860117ff6b5`  
		Last Modified: Sat, 18 Apr 2026 00:14:14 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0101c6b71549aedabcd194182fe24f62da1f064fbc08a0b9ef02d3982112a6`  
		Last Modified: Sat, 18 Apr 2026 00:14:18 GMT  
		Size: 126.7 MB (126674353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e378b78be7830395461fb53df8a4bce4542c83d6f417de8c71e5ad4e4cb0dd`  
		Last Modified: Sat, 18 Apr 2026 00:14:15 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daae491d7aa8f4a5f24a4524c1a96fedee9f6bc4a29b16784081cfd8665e123`  
		Last Modified: Sat, 18 Apr 2026 00:14:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:af2fdb46c41cef58075546847e4895cd4a6a4c1a4dc3734979ab65f0c889eb0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a7ad1e0c79e1d476f5d2ea5a4ab371aaf9a70398040f7200a03e83909d808d`

```dockerfile
```

-	Layers:
	-	`sha256:2a92b97db0e510e80bb672ec11a1f76ee83101afef3a4fd5676a911a3c673cfb`  
		Last Modified: Sat, 18 Apr 2026 00:14:14 GMT  
		Size: 15.0 MB (14955889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4881c0709ab3ddbf4c6b9c2b525c4cb6dc674ebb81fcbfaa29675b586b222a80`  
		Last Modified: Sat, 18 Apr 2026 00:14:13 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:224bcb427d70a54ea2a5c8f47dfcf697ae4baefedd02ecf8d4229dd7b061293d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:7521b58cc03468b664c5de690241b6dc9d2364006d10597d97397a212120c15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183456328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab885ab385edfa53da4203990bd761a77fccf33769800fc2df501f565be7905f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:59:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 07 Apr 2026 01:59:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:59:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 01:59:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:59:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 01:59:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:59:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:59:55 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 07 Apr 2026 01:59:55 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Tue, 07 Apr 2026 01:59:56 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Apr 2026 02:00:06 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:00:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 07 Apr 2026 02:00:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fda07a196ca664a0f0b4ba877bb68ecd33fb55d4acd555541d78e60f372c25`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a558eb92c31fa6ed8922542f00a556fb55d34be3844dce7870c1f748d62211`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 4.4 MB (4423376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4107c155f335fd6d61b205342a30de2da9681199addc501554263b40952a8dd7`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 1.2 MB (1248693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afa9ec7b1fb9d9efa60c61bf1224a7fd8447a4609ec4d760499e6236f2e526e`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfed2d5964a29cda9920b9d8d726321f4bbc4deb439c23dd23eb38b9d7dc5467`  
		Last Modified: Tue, 07 Apr 2026 02:00:40 GMT  
		Size: 15.3 MB (15295827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dfe214ed17391380f7bed0882214598bc23cdec7b41fca921a3f260062a0db`  
		Last Modified: Tue, 07 Apr 2026 02:00:39 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30da1beffde5ddafe325eee749594b751bdeed3a824049a2cef238a761e6d78`  
		Last Modified: Tue, 07 Apr 2026 02:00:40 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6382d97cd590366bacb4cbebb1c515954df251ac4788aeb486badd5abc34f395`  
		Last Modified: Tue, 07 Apr 2026 02:00:42 GMT  
		Size: 134.2 MB (134241282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079ebea3eb2c27b2a8aba90c38e57dbf32e799ff4db45a7803fe3270a70b72c0`  
		Last Modified: Tue, 07 Apr 2026 02:00:40 GMT  
		Size: 842.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60b15b193b9a2d16800e39a3be5e8b4828b3b19adc4402134a01dbfb48bafb9`  
		Last Modified: Tue, 07 Apr 2026 02:00:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c93804bc588485f466357f7fa8c54f81bb3c41276ae7c48702b13020750ffa`  
		Last Modified: Tue, 07 Apr 2026 02:00:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:849ae264000eb5e71d9f92f986024806dcab8997858f33b7b88744479550da1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc5cc8c1f3fb474b99bb524787301a873e854047c3e144bb81f791a37ccca31`

```dockerfile
```

-	Layers:
	-	`sha256:e2635946ae306c7821e1ae58324b3bcc78143e87d2cc4888c2f737ea7fe3e848`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d1be7c7aaaf7d4d279088cc41f1eb94b13d126f0e42b380b719df22e2f58378`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:224bcb427d70a54ea2a5c8f47dfcf697ae4baefedd02ecf8d4229dd7b061293d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:7521b58cc03468b664c5de690241b6dc9d2364006d10597d97397a212120c15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183456328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab885ab385edfa53da4203990bd761a77fccf33769800fc2df501f565be7905f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:59:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 07 Apr 2026 01:59:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:59:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 01:59:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:59:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 01:59:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:59:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:59:55 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 07 Apr 2026 01:59:55 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Tue, 07 Apr 2026 01:59:56 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
VOLUME [/var/lib/mysql]
# Tue, 07 Apr 2026 02:00:06 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 02:00:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:00:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 07 Apr 2026 02:00:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fda07a196ca664a0f0b4ba877bb68ecd33fb55d4acd555541d78e60f372c25`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a558eb92c31fa6ed8922542f00a556fb55d34be3844dce7870c1f748d62211`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 4.4 MB (4423376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4107c155f335fd6d61b205342a30de2da9681199addc501554263b40952a8dd7`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 1.2 MB (1248693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afa9ec7b1fb9d9efa60c61bf1224a7fd8447a4609ec4d760499e6236f2e526e`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfed2d5964a29cda9920b9d8d726321f4bbc4deb439c23dd23eb38b9d7dc5467`  
		Last Modified: Tue, 07 Apr 2026 02:00:40 GMT  
		Size: 15.3 MB (15295827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dfe214ed17391380f7bed0882214598bc23cdec7b41fca921a3f260062a0db`  
		Last Modified: Tue, 07 Apr 2026 02:00:39 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30da1beffde5ddafe325eee749594b751bdeed3a824049a2cef238a761e6d78`  
		Last Modified: Tue, 07 Apr 2026 02:00:40 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6382d97cd590366bacb4cbebb1c515954df251ac4788aeb486badd5abc34f395`  
		Last Modified: Tue, 07 Apr 2026 02:00:42 GMT  
		Size: 134.2 MB (134241282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079ebea3eb2c27b2a8aba90c38e57dbf32e799ff4db45a7803fe3270a70b72c0`  
		Last Modified: Tue, 07 Apr 2026 02:00:40 GMT  
		Size: 842.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60b15b193b9a2d16800e39a3be5e8b4828b3b19adc4402134a01dbfb48bafb9`  
		Last Modified: Tue, 07 Apr 2026 02:00:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c93804bc588485f466357f7fa8c54f81bb3c41276ae7c48702b13020750ffa`  
		Last Modified: Tue, 07 Apr 2026 02:00:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:849ae264000eb5e71d9f92f986024806dcab8997858f33b7b88744479550da1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc5cc8c1f3fb474b99bb524787301a873e854047c3e144bb81f791a37ccca31`

```dockerfile
```

-	Layers:
	-	`sha256:e2635946ae306c7821e1ae58324b3bcc78143e87d2cc4888c2f737ea7fe3e848`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d1be7c7aaaf7d4d279088cc41f1eb94b13d126f0e42b380b719df22e2f58378`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:4af1f8815716546f5b12410f7621f37f93db8dd11a184706ef59111930b8c2ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:bcfecfdd2f8c2988c0db7335dfeed0dc336defe7007e98c5308f58168d808a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232278067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9272481a67f6ca40b0b29b2e102d29fa86b54c69e969883ce4705ece06bbf3d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:12:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:12:16 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:12:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:43 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 18 Apr 2026 00:12:43 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Sat, 18 Apr 2026 00:12:43 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:13:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:13:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:13:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Sat, 18 Apr 2026 00:13:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:50 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 18 Apr 2026 00:13:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:50 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a1a4fb3367dc55623389a4502dafe5c4b80a28e63533023c41bfb0eedfa356`  
		Last Modified: Sat, 18 Apr 2026 00:14:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69c68c7dd2162edcd7163732030b25dfd837c756bd5a183d6c77e98c793d469`  
		Last Modified: Sat, 18 Apr 2026 00:14:21 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6126bf990b9d25ee02468abf80406b6b2a9aefaf88bc6099d3e85031ee008ae`  
		Last Modified: Sat, 18 Apr 2026 00:14:21 GMT  
		Size: 6.2 MB (6170273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77ecc122bf40cbbcf5f49b8436f4f32753dc6d34c305c854ccea4fc5576c664`  
		Last Modified: Sat, 18 Apr 2026 00:14:21 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a966b78a59e9f2903466c252de71fa15162f6e6f03d2981a85657e6228696898`  
		Last Modified: Sat, 18 Apr 2026 00:14:22 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc827b16c7b9253c14abed3d8ef38216db3af30db2e948772ad83330b2a0751`  
		Last Modified: Sat, 18 Apr 2026 00:14:24 GMT  
		Size: 49.9 MB (49909952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ccadc91b4fa2f47fa562c638aa8d4e80e9a5b2cb8b12bab4d1f7aea0f83586`  
		Last Modified: Sat, 18 Apr 2026 00:14:22 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496eb3815f35004486146355aa0a146ac1810270cefb3967e904c07fa657d8ed`  
		Last Modified: Sat, 18 Apr 2026 00:14:26 GMT  
		Size: 128.1 MB (128094881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c350fcbc37b3909736eeb896c96b6cf30cd3c99cc5a0e4937c61ea3ab0c1b47e`  
		Last Modified: Sat, 18 Apr 2026 00:14:24 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e72ef22e056678f0d595eda7f04328a16be5c81ddb98f155f8d91f17462c8b`  
		Last Modified: Sat, 18 Apr 2026 00:14:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:37fcd1dc5bd7019a9d9557c5a579451e80279d0ffce7880ac5e7ee92718d3f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424d7d9564a58a14fa9b2691bef5436cc3a39107f77739d0a26327065b1f4a33`

```dockerfile
```

-	Layers:
	-	`sha256:0faffc9d5b7858fc1a118f35a0cd1444d253be2a6019a8159bd8503c52aa2197`  
		Last Modified: Sat, 18 Apr 2026 00:14:21 GMT  
		Size: 15.0 MB (14957541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0f0e180252c7e9db2e2d4dc137e3281a4f581d4c482257c90c8e0d2a17f1417`  
		Last Modified: Sat, 18 Apr 2026 00:14:21 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0e7040b532c0f2ac8cb822695d33025522acd5252175cb104a5929aa66b40222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227884633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9cc8fab569ceb806ffb83b5b91e0b953e84c096c87b31a36b5d1355c72633c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:12:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:12:04 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:12:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:33 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 18 Apr 2026 00:12:33 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Sat, 18 Apr 2026 00:12:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Sat, 18 Apr 2026 00:13:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:43 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 18 Apr 2026 00:13:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc94f9e40e97c93301716a04c45844be8892d60aa3dfbd672f58e274033719ee`  
		Last Modified: Sat, 18 Apr 2026 00:14:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8295d92b87f72abe5bf6a9b85af5ed9c2a022af1c74d2f5c7471ebdadd6561e9`  
		Last Modified: Sat, 18 Apr 2026 00:14:13 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a574c190fa744079fa99dd400c0c66c5e897e866021ef68859ad78d6216474`  
		Last Modified: Sat, 18 Apr 2026 00:14:13 GMT  
		Size: 5.8 MB (5793308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8312482523a97383fa4e1988cf357e22ab500a7532b038ac78364fd1002d7142`  
		Last Modified: Sat, 18 Apr 2026 00:14:13 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c793807e067a08cdd43ebf772868409b33cf69cbd77a40097303ee1e29aeed`  
		Last Modified: Sat, 18 Apr 2026 00:14:14 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f4b4c46fca3d35c547c3e8e4238eca72b22e1d9962ea3a7c08c2b3351710ab`  
		Last Modified: Sat, 18 Apr 2026 00:14:16 GMT  
		Size: 48.8 MB (48770063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e00e08c28e154b72643b3fef054432fd0e10b43b043ffd82e6c1860117ff6b5`  
		Last Modified: Sat, 18 Apr 2026 00:14:14 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0101c6b71549aedabcd194182fe24f62da1f064fbc08a0b9ef02d3982112a6`  
		Last Modified: Sat, 18 Apr 2026 00:14:18 GMT  
		Size: 126.7 MB (126674353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e378b78be7830395461fb53df8a4bce4542c83d6f417de8c71e5ad4e4cb0dd`  
		Last Modified: Sat, 18 Apr 2026 00:14:15 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daae491d7aa8f4a5f24a4524c1a96fedee9f6bc4a29b16784081cfd8665e123`  
		Last Modified: Sat, 18 Apr 2026 00:14:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:af2fdb46c41cef58075546847e4895cd4a6a4c1a4dc3734979ab65f0c889eb0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a7ad1e0c79e1d476f5d2ea5a4ab371aaf9a70398040f7200a03e83909d808d`

```dockerfile
```

-	Layers:
	-	`sha256:2a92b97db0e510e80bb672ec11a1f76ee83101afef3a4fd5676a911a3c673cfb`  
		Last Modified: Sat, 18 Apr 2026 00:14:14 GMT  
		Size: 15.0 MB (14955889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4881c0709ab3ddbf4c6b9c2b525c4cb6dc674ebb81fcbfaa29675b586b222a80`  
		Last Modified: Sat, 18 Apr 2026 00:14:13 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:4af1f8815716546f5b12410f7621f37f93db8dd11a184706ef59111930b8c2ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:bcfecfdd2f8c2988c0db7335dfeed0dc336defe7007e98c5308f58168d808a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232278067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9272481a67f6ca40b0b29b2e102d29fa86b54c69e969883ce4705ece06bbf3d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:12:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:12:16 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:12:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:43 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 18 Apr 2026 00:12:43 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Sat, 18 Apr 2026 00:12:43 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:13:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:13:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:13:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Sat, 18 Apr 2026 00:13:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:50 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 18 Apr 2026 00:13:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:50 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a1a4fb3367dc55623389a4502dafe5c4b80a28e63533023c41bfb0eedfa356`  
		Last Modified: Sat, 18 Apr 2026 00:14:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69c68c7dd2162edcd7163732030b25dfd837c756bd5a183d6c77e98c793d469`  
		Last Modified: Sat, 18 Apr 2026 00:14:21 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6126bf990b9d25ee02468abf80406b6b2a9aefaf88bc6099d3e85031ee008ae`  
		Last Modified: Sat, 18 Apr 2026 00:14:21 GMT  
		Size: 6.2 MB (6170273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77ecc122bf40cbbcf5f49b8436f4f32753dc6d34c305c854ccea4fc5576c664`  
		Last Modified: Sat, 18 Apr 2026 00:14:21 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a966b78a59e9f2903466c252de71fa15162f6e6f03d2981a85657e6228696898`  
		Last Modified: Sat, 18 Apr 2026 00:14:22 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc827b16c7b9253c14abed3d8ef38216db3af30db2e948772ad83330b2a0751`  
		Last Modified: Sat, 18 Apr 2026 00:14:24 GMT  
		Size: 49.9 MB (49909952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ccadc91b4fa2f47fa562c638aa8d4e80e9a5b2cb8b12bab4d1f7aea0f83586`  
		Last Modified: Sat, 18 Apr 2026 00:14:22 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496eb3815f35004486146355aa0a146ac1810270cefb3967e904c07fa657d8ed`  
		Last Modified: Sat, 18 Apr 2026 00:14:26 GMT  
		Size: 128.1 MB (128094881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c350fcbc37b3909736eeb896c96b6cf30cd3c99cc5a0e4937c61ea3ab0c1b47e`  
		Last Modified: Sat, 18 Apr 2026 00:14:24 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e72ef22e056678f0d595eda7f04328a16be5c81ddb98f155f8d91f17462c8b`  
		Last Modified: Sat, 18 Apr 2026 00:14:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:37fcd1dc5bd7019a9d9557c5a579451e80279d0ffce7880ac5e7ee92718d3f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424d7d9564a58a14fa9b2691bef5436cc3a39107f77739d0a26327065b1f4a33`

```dockerfile
```

-	Layers:
	-	`sha256:0faffc9d5b7858fc1a118f35a0cd1444d253be2a6019a8159bd8503c52aa2197`  
		Last Modified: Sat, 18 Apr 2026 00:14:21 GMT  
		Size: 15.0 MB (14957541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0f0e180252c7e9db2e2d4dc137e3281a4f581d4c482257c90c8e0d2a17f1417`  
		Last Modified: Sat, 18 Apr 2026 00:14:21 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0e7040b532c0f2ac8cb822695d33025522acd5252175cb104a5929aa66b40222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227884633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9cc8fab569ceb806ffb83b5b91e0b953e84c096c87b31a36b5d1355c72633c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:12:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:12:04 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:12:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:33 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 18 Apr 2026 00:12:33 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Sat, 18 Apr 2026 00:12:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Sat, 18 Apr 2026 00:13:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:43 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 18 Apr 2026 00:13:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc94f9e40e97c93301716a04c45844be8892d60aa3dfbd672f58e274033719ee`  
		Last Modified: Sat, 18 Apr 2026 00:14:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8295d92b87f72abe5bf6a9b85af5ed9c2a022af1c74d2f5c7471ebdadd6561e9`  
		Last Modified: Sat, 18 Apr 2026 00:14:13 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a574c190fa744079fa99dd400c0c66c5e897e866021ef68859ad78d6216474`  
		Last Modified: Sat, 18 Apr 2026 00:14:13 GMT  
		Size: 5.8 MB (5793308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8312482523a97383fa4e1988cf357e22ab500a7532b038ac78364fd1002d7142`  
		Last Modified: Sat, 18 Apr 2026 00:14:13 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c793807e067a08cdd43ebf772868409b33cf69cbd77a40097303ee1e29aeed`  
		Last Modified: Sat, 18 Apr 2026 00:14:14 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f4b4c46fca3d35c547c3e8e4238eca72b22e1d9962ea3a7c08c2b3351710ab`  
		Last Modified: Sat, 18 Apr 2026 00:14:16 GMT  
		Size: 48.8 MB (48770063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e00e08c28e154b72643b3fef054432fd0e10b43b043ffd82e6c1860117ff6b5`  
		Last Modified: Sat, 18 Apr 2026 00:14:14 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0101c6b71549aedabcd194182fe24f62da1f064fbc08a0b9ef02d3982112a6`  
		Last Modified: Sat, 18 Apr 2026 00:14:18 GMT  
		Size: 126.7 MB (126674353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e378b78be7830395461fb53df8a4bce4542c83d6f417de8c71e5ad4e4cb0dd`  
		Last Modified: Sat, 18 Apr 2026 00:14:15 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daae491d7aa8f4a5f24a4524c1a96fedee9f6bc4a29b16784081cfd8665e123`  
		Last Modified: Sat, 18 Apr 2026 00:14:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:af2fdb46c41cef58075546847e4895cd4a6a4c1a4dc3734979ab65f0c889eb0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a7ad1e0c79e1d476f5d2ea5a4ab371aaf9a70398040f7200a03e83909d808d`

```dockerfile
```

-	Layers:
	-	`sha256:2a92b97db0e510e80bb672ec11a1f76ee83101afef3a4fd5676a911a3c673cfb`  
		Last Modified: Sat, 18 Apr 2026 00:14:14 GMT  
		Size: 15.0 MB (14955889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4881c0709ab3ddbf4c6b9c2b525c4cb6dc674ebb81fcbfaa29675b586b222a80`  
		Last Modified: Sat, 18 Apr 2026 00:14:13 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.46`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.0.46-bookworm`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.0.46-debian`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.0.46-oracle`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.0.46-oraclelinux9`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

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
$ docker pull mysql@sha256:c5df04bee1a42b74a5841c6409e669cf62126cd0416f00c1cea8ab933b9361b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:da26407911eac4c4fcff99ef11b9ae975540ff3ad9b5677c4d85a347c14b188d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266343873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bf110498531f91e80936e0181b8b63bac636481065a63df2e63e1aac2b1548`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:49 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e639cd467a9761616d6de8a409cb209d411f2f7ac84577b64566973d75ac5fa2`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e79c47b3010a916b04df087a57f16c399eec48d8080cb50a0f45d889323471`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 783.6 KB (783562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28152004afeb0fef135bc7f72c9c3f8605fa7f970ed9b908d8304af3ea29244`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 6.2 MB (6170281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c97bec1a3486df0287c44424237160304e8efa58d3d1ee5a191ccb45fa25303`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e885080b838ed1c6b7b5a9cb5427937014dee091f74f7371b01d9b538b636dbe`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6497d062da4fa91bf366b76e736a978762cb698b9ff1e12230118d43b124c820`  
		Last Modified: Sat, 18 Apr 2026 00:14:08 GMT  
		Size: 51.4 MB (51442459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d6178a9105eb0d5e61411f96f39c4d6500b46654be8fd130bd3bfbc6432eb`  
		Last Modified: Sat, 18 Apr 2026 00:14:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664c1f1ffcc8492f4c05894e234ba3577253cfa08919ad60b2a3323d52e7cac8`  
		Last Modified: Sat, 18 Apr 2026 00:14:10 GMT  
		Size: 160.6 MB (160628269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faff6d2a6d2f55b7cf1230e6b98303036b47e0817dfce3c5ca8ff65fd996cb5`  
		Last Modified: Sat, 18 Apr 2026 00:14:07 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:200c99f4fd2adb80e59f9b5ddde5cc8b3b7e2c90fa4b568da17a87f05c43841a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2f9dca420dd5d35f90a57ddc98c3bad21d241f0fc6c7f274c4debffda4d610`

```dockerfile
```

-	Layers:
	-	`sha256:6b65aba3f1f64e1d29ed5c0f839788403aeaec80bd07e669614ad67d695642d0`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b038cfc7980164d5219693a0827211109ac800244906ce3b65d883686d6612c`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d36eff8bce9626a30d9a53067fbc3f3929b3406fe4548c296ce2990585e58abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261447241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ca5ab30bf4ee9e428b79662b2e440e93912fc72f6408f1c5243dab5d554460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:18 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd414fac5cad07f393cbace2273171bff2f71ff6228b9118e8b6b72d195055f`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fde8c58f5021cf570a07a88e4dc7b3a2c01c772e5af1d20bbfd4cfcc8e3db9`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175ca4a36287d2506f12dd65b36c1e5269084cfd865815c70e4c09f94382745c`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 5.8 MB (5793264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f921be051e0c6462756bb035889736e272fd01828a8abdd1f13e16dcf3de3297`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1167dd93878509d66f2e3f08528ea12ceb9a823e45d5bca27e20199873a05`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb5786475529b351b067fec5c959deb8b048266b7885b434b176c782ac478d0`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 50.1 MB (50080397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d295fbc6d41d027458ae9f6b9479c90a58c714db1c208f57b5ef7f8a8ab282`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e994635adec80593755e571049efab4ba4bc1a7468498702e56bda9b84da85b`  
		Last Modified: Sat, 18 Apr 2026 00:13:51 GMT  
		Size: 158.9 MB (158926780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1274e1258c8e15a7c0aed082b7ac4f47dd327dabcc6774f39ae591e419f117b3`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:9c82cc9b29ee178010cb60478cfea7696743e49f94710329120952b3e45f45f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f26768fe11299baa6669694b24d81a2b0d67daa498a46903111e1eedeefab6`

```dockerfile
```

-	Layers:
	-	`sha256:c06da225b9122f111fb64ccd9c8441b8c4aee1f59835b3be6673afa2b0296105`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a03073ece591c34e951f68d29baf88f8e7dcc3ca40235a0df3b02e2d9029ec1`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:c5df04bee1a42b74a5841c6409e669cf62126cd0416f00c1cea8ab933b9361b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:da26407911eac4c4fcff99ef11b9ae975540ff3ad9b5677c4d85a347c14b188d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266343873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bf110498531f91e80936e0181b8b63bac636481065a63df2e63e1aac2b1548`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:49 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e639cd467a9761616d6de8a409cb209d411f2f7ac84577b64566973d75ac5fa2`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e79c47b3010a916b04df087a57f16c399eec48d8080cb50a0f45d889323471`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 783.6 KB (783562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28152004afeb0fef135bc7f72c9c3f8605fa7f970ed9b908d8304af3ea29244`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 6.2 MB (6170281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c97bec1a3486df0287c44424237160304e8efa58d3d1ee5a191ccb45fa25303`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e885080b838ed1c6b7b5a9cb5427937014dee091f74f7371b01d9b538b636dbe`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6497d062da4fa91bf366b76e736a978762cb698b9ff1e12230118d43b124c820`  
		Last Modified: Sat, 18 Apr 2026 00:14:08 GMT  
		Size: 51.4 MB (51442459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d6178a9105eb0d5e61411f96f39c4d6500b46654be8fd130bd3bfbc6432eb`  
		Last Modified: Sat, 18 Apr 2026 00:14:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664c1f1ffcc8492f4c05894e234ba3577253cfa08919ad60b2a3323d52e7cac8`  
		Last Modified: Sat, 18 Apr 2026 00:14:10 GMT  
		Size: 160.6 MB (160628269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faff6d2a6d2f55b7cf1230e6b98303036b47e0817dfce3c5ca8ff65fd996cb5`  
		Last Modified: Sat, 18 Apr 2026 00:14:07 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:200c99f4fd2adb80e59f9b5ddde5cc8b3b7e2c90fa4b568da17a87f05c43841a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2f9dca420dd5d35f90a57ddc98c3bad21d241f0fc6c7f274c4debffda4d610`

```dockerfile
```

-	Layers:
	-	`sha256:6b65aba3f1f64e1d29ed5c0f839788403aeaec80bd07e669614ad67d695642d0`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b038cfc7980164d5219693a0827211109ac800244906ce3b65d883686d6612c`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d36eff8bce9626a30d9a53067fbc3f3929b3406fe4548c296ce2990585e58abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261447241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ca5ab30bf4ee9e428b79662b2e440e93912fc72f6408f1c5243dab5d554460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:18 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd414fac5cad07f393cbace2273171bff2f71ff6228b9118e8b6b72d195055f`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fde8c58f5021cf570a07a88e4dc7b3a2c01c772e5af1d20bbfd4cfcc8e3db9`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175ca4a36287d2506f12dd65b36c1e5269084cfd865815c70e4c09f94382745c`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 5.8 MB (5793264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f921be051e0c6462756bb035889736e272fd01828a8abdd1f13e16dcf3de3297`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1167dd93878509d66f2e3f08528ea12ceb9a823e45d5bca27e20199873a05`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb5786475529b351b067fec5c959deb8b048266b7885b434b176c782ac478d0`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 50.1 MB (50080397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d295fbc6d41d027458ae9f6b9479c90a58c714db1c208f57b5ef7f8a8ab282`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e994635adec80593755e571049efab4ba4bc1a7468498702e56bda9b84da85b`  
		Last Modified: Sat, 18 Apr 2026 00:13:51 GMT  
		Size: 158.9 MB (158926780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1274e1258c8e15a7c0aed082b7ac4f47dd327dabcc6774f39ae591e419f117b3`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9c82cc9b29ee178010cb60478cfea7696743e49f94710329120952b3e45f45f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f26768fe11299baa6669694b24d81a2b0d67daa498a46903111e1eedeefab6`

```dockerfile
```

-	Layers:
	-	`sha256:c06da225b9122f111fb64ccd9c8441b8c4aee1f59835b3be6673afa2b0296105`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a03073ece591c34e951f68d29baf88f8e7dcc3ca40235a0df3b02e2d9029ec1`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:c5df04bee1a42b74a5841c6409e669cf62126cd0416f00c1cea8ab933b9361b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:da26407911eac4c4fcff99ef11b9ae975540ff3ad9b5677c4d85a347c14b188d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266343873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bf110498531f91e80936e0181b8b63bac636481065a63df2e63e1aac2b1548`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:49 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e639cd467a9761616d6de8a409cb209d411f2f7ac84577b64566973d75ac5fa2`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e79c47b3010a916b04df087a57f16c399eec48d8080cb50a0f45d889323471`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 783.6 KB (783562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28152004afeb0fef135bc7f72c9c3f8605fa7f970ed9b908d8304af3ea29244`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 6.2 MB (6170281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c97bec1a3486df0287c44424237160304e8efa58d3d1ee5a191ccb45fa25303`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e885080b838ed1c6b7b5a9cb5427937014dee091f74f7371b01d9b538b636dbe`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6497d062da4fa91bf366b76e736a978762cb698b9ff1e12230118d43b124c820`  
		Last Modified: Sat, 18 Apr 2026 00:14:08 GMT  
		Size: 51.4 MB (51442459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d6178a9105eb0d5e61411f96f39c4d6500b46654be8fd130bd3bfbc6432eb`  
		Last Modified: Sat, 18 Apr 2026 00:14:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664c1f1ffcc8492f4c05894e234ba3577253cfa08919ad60b2a3323d52e7cac8`  
		Last Modified: Sat, 18 Apr 2026 00:14:10 GMT  
		Size: 160.6 MB (160628269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faff6d2a6d2f55b7cf1230e6b98303036b47e0817dfce3c5ca8ff65fd996cb5`  
		Last Modified: Sat, 18 Apr 2026 00:14:07 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:200c99f4fd2adb80e59f9b5ddde5cc8b3b7e2c90fa4b568da17a87f05c43841a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2f9dca420dd5d35f90a57ddc98c3bad21d241f0fc6c7f274c4debffda4d610`

```dockerfile
```

-	Layers:
	-	`sha256:6b65aba3f1f64e1d29ed5c0f839788403aeaec80bd07e669614ad67d695642d0`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b038cfc7980164d5219693a0827211109ac800244906ce3b65d883686d6612c`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d36eff8bce9626a30d9a53067fbc3f3929b3406fe4548c296ce2990585e58abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261447241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ca5ab30bf4ee9e428b79662b2e440e93912fc72f6408f1c5243dab5d554460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:18 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd414fac5cad07f393cbace2273171bff2f71ff6228b9118e8b6b72d195055f`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fde8c58f5021cf570a07a88e4dc7b3a2c01c772e5af1d20bbfd4cfcc8e3db9`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175ca4a36287d2506f12dd65b36c1e5269084cfd865815c70e4c09f94382745c`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 5.8 MB (5793264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f921be051e0c6462756bb035889736e272fd01828a8abdd1f13e16dcf3de3297`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1167dd93878509d66f2e3f08528ea12ceb9a823e45d5bca27e20199873a05`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb5786475529b351b067fec5c959deb8b048266b7885b434b176c782ac478d0`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 50.1 MB (50080397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d295fbc6d41d027458ae9f6b9479c90a58c714db1c208f57b5ef7f8a8ab282`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e994635adec80593755e571049efab4ba4bc1a7468498702e56bda9b84da85b`  
		Last Modified: Sat, 18 Apr 2026 00:13:51 GMT  
		Size: 158.9 MB (158926780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1274e1258c8e15a7c0aed082b7ac4f47dd327dabcc6774f39ae591e419f117b3`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9c82cc9b29ee178010cb60478cfea7696743e49f94710329120952b3e45f45f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f26768fe11299baa6669694b24d81a2b0d67daa498a46903111e1eedeefab6`

```dockerfile
```

-	Layers:
	-	`sha256:c06da225b9122f111fb64ccd9c8441b8c4aee1f59835b3be6673afa2b0296105`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a03073ece591c34e951f68d29baf88f8e7dcc3ca40235a0df3b02e2d9029ec1`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6`

```console
$ docker pull mysql@sha256:c5df04bee1a42b74a5841c6409e669cf62126cd0416f00c1cea8ab933b9361b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6` - linux; amd64

```console
$ docker pull mysql@sha256:da26407911eac4c4fcff99ef11b9ae975540ff3ad9b5677c4d85a347c14b188d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266343873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bf110498531f91e80936e0181b8b63bac636481065a63df2e63e1aac2b1548`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:49 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e639cd467a9761616d6de8a409cb209d411f2f7ac84577b64566973d75ac5fa2`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e79c47b3010a916b04df087a57f16c399eec48d8080cb50a0f45d889323471`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 783.6 KB (783562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28152004afeb0fef135bc7f72c9c3f8605fa7f970ed9b908d8304af3ea29244`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 6.2 MB (6170281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c97bec1a3486df0287c44424237160304e8efa58d3d1ee5a191ccb45fa25303`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e885080b838ed1c6b7b5a9cb5427937014dee091f74f7371b01d9b538b636dbe`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6497d062da4fa91bf366b76e736a978762cb698b9ff1e12230118d43b124c820`  
		Last Modified: Sat, 18 Apr 2026 00:14:08 GMT  
		Size: 51.4 MB (51442459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d6178a9105eb0d5e61411f96f39c4d6500b46654be8fd130bd3bfbc6432eb`  
		Last Modified: Sat, 18 Apr 2026 00:14:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664c1f1ffcc8492f4c05894e234ba3577253cfa08919ad60b2a3323d52e7cac8`  
		Last Modified: Sat, 18 Apr 2026 00:14:10 GMT  
		Size: 160.6 MB (160628269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faff6d2a6d2f55b7cf1230e6b98303036b47e0817dfce3c5ca8ff65fd996cb5`  
		Last Modified: Sat, 18 Apr 2026 00:14:07 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6` - unknown; unknown

```console
$ docker pull mysql@sha256:200c99f4fd2adb80e59f9b5ddde5cc8b3b7e2c90fa4b568da17a87f05c43841a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2f9dca420dd5d35f90a57ddc98c3bad21d241f0fc6c7f274c4debffda4d610`

```dockerfile
```

-	Layers:
	-	`sha256:6b65aba3f1f64e1d29ed5c0f839788403aeaec80bd07e669614ad67d695642d0`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b038cfc7980164d5219693a0827211109ac800244906ce3b65d883686d6612c`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d36eff8bce9626a30d9a53067fbc3f3929b3406fe4548c296ce2990585e58abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261447241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ca5ab30bf4ee9e428b79662b2e440e93912fc72f6408f1c5243dab5d554460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:18 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd414fac5cad07f393cbace2273171bff2f71ff6228b9118e8b6b72d195055f`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fde8c58f5021cf570a07a88e4dc7b3a2c01c772e5af1d20bbfd4cfcc8e3db9`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175ca4a36287d2506f12dd65b36c1e5269084cfd865815c70e4c09f94382745c`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 5.8 MB (5793264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f921be051e0c6462756bb035889736e272fd01828a8abdd1f13e16dcf3de3297`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1167dd93878509d66f2e3f08528ea12ceb9a823e45d5bca27e20199873a05`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb5786475529b351b067fec5c959deb8b048266b7885b434b176c782ac478d0`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 50.1 MB (50080397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d295fbc6d41d027458ae9f6b9479c90a58c714db1c208f57b5ef7f8a8ab282`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e994635adec80593755e571049efab4ba4bc1a7468498702e56bda9b84da85b`  
		Last Modified: Sat, 18 Apr 2026 00:13:51 GMT  
		Size: 158.9 MB (158926780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1274e1258c8e15a7c0aed082b7ac4f47dd327dabcc6774f39ae591e419f117b3`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6` - unknown; unknown

```console
$ docker pull mysql@sha256:9c82cc9b29ee178010cb60478cfea7696743e49f94710329120952b3e45f45f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f26768fe11299baa6669694b24d81a2b0d67daa498a46903111e1eedeefab6`

```dockerfile
```

-	Layers:
	-	`sha256:c06da225b9122f111fb64ccd9c8441b8c4aee1f59835b3be6673afa2b0296105`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a03073ece591c34e951f68d29baf88f8e7dcc3ca40235a0df3b02e2d9029ec1`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6-oracle`

```console
$ docker pull mysql@sha256:c5df04bee1a42b74a5841c6409e669cf62126cd0416f00c1cea8ab933b9361b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:da26407911eac4c4fcff99ef11b9ae975540ff3ad9b5677c4d85a347c14b188d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266343873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bf110498531f91e80936e0181b8b63bac636481065a63df2e63e1aac2b1548`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:49 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e639cd467a9761616d6de8a409cb209d411f2f7ac84577b64566973d75ac5fa2`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e79c47b3010a916b04df087a57f16c399eec48d8080cb50a0f45d889323471`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 783.6 KB (783562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28152004afeb0fef135bc7f72c9c3f8605fa7f970ed9b908d8304af3ea29244`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 6.2 MB (6170281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c97bec1a3486df0287c44424237160304e8efa58d3d1ee5a191ccb45fa25303`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e885080b838ed1c6b7b5a9cb5427937014dee091f74f7371b01d9b538b636dbe`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6497d062da4fa91bf366b76e736a978762cb698b9ff1e12230118d43b124c820`  
		Last Modified: Sat, 18 Apr 2026 00:14:08 GMT  
		Size: 51.4 MB (51442459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d6178a9105eb0d5e61411f96f39c4d6500b46654be8fd130bd3bfbc6432eb`  
		Last Modified: Sat, 18 Apr 2026 00:14:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664c1f1ffcc8492f4c05894e234ba3577253cfa08919ad60b2a3323d52e7cac8`  
		Last Modified: Sat, 18 Apr 2026 00:14:10 GMT  
		Size: 160.6 MB (160628269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faff6d2a6d2f55b7cf1230e6b98303036b47e0817dfce3c5ca8ff65fd996cb5`  
		Last Modified: Sat, 18 Apr 2026 00:14:07 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:200c99f4fd2adb80e59f9b5ddde5cc8b3b7e2c90fa4b568da17a87f05c43841a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2f9dca420dd5d35f90a57ddc98c3bad21d241f0fc6c7f274c4debffda4d610`

```dockerfile
```

-	Layers:
	-	`sha256:6b65aba3f1f64e1d29ed5c0f839788403aeaec80bd07e669614ad67d695642d0`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b038cfc7980164d5219693a0827211109ac800244906ce3b65d883686d6612c`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d36eff8bce9626a30d9a53067fbc3f3929b3406fe4548c296ce2990585e58abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261447241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ca5ab30bf4ee9e428b79662b2e440e93912fc72f6408f1c5243dab5d554460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:18 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd414fac5cad07f393cbace2273171bff2f71ff6228b9118e8b6b72d195055f`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fde8c58f5021cf570a07a88e4dc7b3a2c01c772e5af1d20bbfd4cfcc8e3db9`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175ca4a36287d2506f12dd65b36c1e5269084cfd865815c70e4c09f94382745c`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 5.8 MB (5793264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f921be051e0c6462756bb035889736e272fd01828a8abdd1f13e16dcf3de3297`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1167dd93878509d66f2e3f08528ea12ceb9a823e45d5bca27e20199873a05`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb5786475529b351b067fec5c959deb8b048266b7885b434b176c782ac478d0`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 50.1 MB (50080397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d295fbc6d41d027458ae9f6b9479c90a58c714db1c208f57b5ef7f8a8ab282`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e994635adec80593755e571049efab4ba4bc1a7468498702e56bda9b84da85b`  
		Last Modified: Sat, 18 Apr 2026 00:13:51 GMT  
		Size: 158.9 MB (158926780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1274e1258c8e15a7c0aed082b7ac4f47dd327dabcc6774f39ae591e419f117b3`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9c82cc9b29ee178010cb60478cfea7696743e49f94710329120952b3e45f45f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f26768fe11299baa6669694b24d81a2b0d67daa498a46903111e1eedeefab6`

```dockerfile
```

-	Layers:
	-	`sha256:c06da225b9122f111fb64ccd9c8441b8c4aee1f59835b3be6673afa2b0296105`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a03073ece591c34e951f68d29baf88f8e7dcc3ca40235a0df3b02e2d9029ec1`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6-oraclelinux9`

```console
$ docker pull mysql@sha256:c5df04bee1a42b74a5841c6409e669cf62126cd0416f00c1cea8ab933b9361b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:da26407911eac4c4fcff99ef11b9ae975540ff3ad9b5677c4d85a347c14b188d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266343873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bf110498531f91e80936e0181b8b63bac636481065a63df2e63e1aac2b1548`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:49 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e639cd467a9761616d6de8a409cb209d411f2f7ac84577b64566973d75ac5fa2`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e79c47b3010a916b04df087a57f16c399eec48d8080cb50a0f45d889323471`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 783.6 KB (783562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28152004afeb0fef135bc7f72c9c3f8605fa7f970ed9b908d8304af3ea29244`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 6.2 MB (6170281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c97bec1a3486df0287c44424237160304e8efa58d3d1ee5a191ccb45fa25303`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e885080b838ed1c6b7b5a9cb5427937014dee091f74f7371b01d9b538b636dbe`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6497d062da4fa91bf366b76e736a978762cb698b9ff1e12230118d43b124c820`  
		Last Modified: Sat, 18 Apr 2026 00:14:08 GMT  
		Size: 51.4 MB (51442459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d6178a9105eb0d5e61411f96f39c4d6500b46654be8fd130bd3bfbc6432eb`  
		Last Modified: Sat, 18 Apr 2026 00:14:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664c1f1ffcc8492f4c05894e234ba3577253cfa08919ad60b2a3323d52e7cac8`  
		Last Modified: Sat, 18 Apr 2026 00:14:10 GMT  
		Size: 160.6 MB (160628269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faff6d2a6d2f55b7cf1230e6b98303036b47e0817dfce3c5ca8ff65fd996cb5`  
		Last Modified: Sat, 18 Apr 2026 00:14:07 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:200c99f4fd2adb80e59f9b5ddde5cc8b3b7e2c90fa4b568da17a87f05c43841a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2f9dca420dd5d35f90a57ddc98c3bad21d241f0fc6c7f274c4debffda4d610`

```dockerfile
```

-	Layers:
	-	`sha256:6b65aba3f1f64e1d29ed5c0f839788403aeaec80bd07e669614ad67d695642d0`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b038cfc7980164d5219693a0827211109ac800244906ce3b65d883686d6612c`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d36eff8bce9626a30d9a53067fbc3f3929b3406fe4548c296ce2990585e58abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261447241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ca5ab30bf4ee9e428b79662b2e440e93912fc72f6408f1c5243dab5d554460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:18 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd414fac5cad07f393cbace2273171bff2f71ff6228b9118e8b6b72d195055f`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fde8c58f5021cf570a07a88e4dc7b3a2c01c772e5af1d20bbfd4cfcc8e3db9`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175ca4a36287d2506f12dd65b36c1e5269084cfd865815c70e4c09f94382745c`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 5.8 MB (5793264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f921be051e0c6462756bb035889736e272fd01828a8abdd1f13e16dcf3de3297`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1167dd93878509d66f2e3f08528ea12ceb9a823e45d5bca27e20199873a05`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb5786475529b351b067fec5c959deb8b048266b7885b434b176c782ac478d0`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 50.1 MB (50080397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d295fbc6d41d027458ae9f6b9479c90a58c714db1c208f57b5ef7f8a8ab282`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e994635adec80593755e571049efab4ba4bc1a7468498702e56bda9b84da85b`  
		Last Modified: Sat, 18 Apr 2026 00:13:51 GMT  
		Size: 158.9 MB (158926780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1274e1258c8e15a7c0aed082b7ac4f47dd327dabcc6774f39ae591e419f117b3`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9c82cc9b29ee178010cb60478cfea7696743e49f94710329120952b3e45f45f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f26768fe11299baa6669694b24d81a2b0d67daa498a46903111e1eedeefab6`

```dockerfile
```

-	Layers:
	-	`sha256:c06da225b9122f111fb64ccd9c8441b8c4aee1f59835b3be6673afa2b0296105`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a03073ece591c34e951f68d29baf88f8e7dcc3ca40235a0df3b02e2d9029ec1`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0`

```console
$ docker pull mysql@sha256:c5df04bee1a42b74a5841c6409e669cf62126cd0416f00c1cea8ab933b9361b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0` - linux; amd64

```console
$ docker pull mysql@sha256:da26407911eac4c4fcff99ef11b9ae975540ff3ad9b5677c4d85a347c14b188d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266343873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bf110498531f91e80936e0181b8b63bac636481065a63df2e63e1aac2b1548`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:49 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e639cd467a9761616d6de8a409cb209d411f2f7ac84577b64566973d75ac5fa2`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e79c47b3010a916b04df087a57f16c399eec48d8080cb50a0f45d889323471`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 783.6 KB (783562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28152004afeb0fef135bc7f72c9c3f8605fa7f970ed9b908d8304af3ea29244`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 6.2 MB (6170281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c97bec1a3486df0287c44424237160304e8efa58d3d1ee5a191ccb45fa25303`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e885080b838ed1c6b7b5a9cb5427937014dee091f74f7371b01d9b538b636dbe`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6497d062da4fa91bf366b76e736a978762cb698b9ff1e12230118d43b124c820`  
		Last Modified: Sat, 18 Apr 2026 00:14:08 GMT  
		Size: 51.4 MB (51442459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d6178a9105eb0d5e61411f96f39c4d6500b46654be8fd130bd3bfbc6432eb`  
		Last Modified: Sat, 18 Apr 2026 00:14:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664c1f1ffcc8492f4c05894e234ba3577253cfa08919ad60b2a3323d52e7cac8`  
		Last Modified: Sat, 18 Apr 2026 00:14:10 GMT  
		Size: 160.6 MB (160628269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faff6d2a6d2f55b7cf1230e6b98303036b47e0817dfce3c5ca8ff65fd996cb5`  
		Last Modified: Sat, 18 Apr 2026 00:14:07 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0` - unknown; unknown

```console
$ docker pull mysql@sha256:200c99f4fd2adb80e59f9b5ddde5cc8b3b7e2c90fa4b568da17a87f05c43841a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2f9dca420dd5d35f90a57ddc98c3bad21d241f0fc6c7f274c4debffda4d610`

```dockerfile
```

-	Layers:
	-	`sha256:6b65aba3f1f64e1d29ed5c0f839788403aeaec80bd07e669614ad67d695642d0`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b038cfc7980164d5219693a0827211109ac800244906ce3b65d883686d6612c`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d36eff8bce9626a30d9a53067fbc3f3929b3406fe4548c296ce2990585e58abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261447241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ca5ab30bf4ee9e428b79662b2e440e93912fc72f6408f1c5243dab5d554460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:18 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd414fac5cad07f393cbace2273171bff2f71ff6228b9118e8b6b72d195055f`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fde8c58f5021cf570a07a88e4dc7b3a2c01c772e5af1d20bbfd4cfcc8e3db9`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175ca4a36287d2506f12dd65b36c1e5269084cfd865815c70e4c09f94382745c`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 5.8 MB (5793264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f921be051e0c6462756bb035889736e272fd01828a8abdd1f13e16dcf3de3297`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1167dd93878509d66f2e3f08528ea12ceb9a823e45d5bca27e20199873a05`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb5786475529b351b067fec5c959deb8b048266b7885b434b176c782ac478d0`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 50.1 MB (50080397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d295fbc6d41d027458ae9f6b9479c90a58c714db1c208f57b5ef7f8a8ab282`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e994635adec80593755e571049efab4ba4bc1a7468498702e56bda9b84da85b`  
		Last Modified: Sat, 18 Apr 2026 00:13:51 GMT  
		Size: 158.9 MB (158926780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1274e1258c8e15a7c0aed082b7ac4f47dd327dabcc6774f39ae591e419f117b3`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0` - unknown; unknown

```console
$ docker pull mysql@sha256:9c82cc9b29ee178010cb60478cfea7696743e49f94710329120952b3e45f45f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f26768fe11299baa6669694b24d81a2b0d67daa498a46903111e1eedeefab6`

```dockerfile
```

-	Layers:
	-	`sha256:c06da225b9122f111fb64ccd9c8441b8c4aee1f59835b3be6673afa2b0296105`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a03073ece591c34e951f68d29baf88f8e7dcc3ca40235a0df3b02e2d9029ec1`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0-oracle`

```console
$ docker pull mysql@sha256:c5df04bee1a42b74a5841c6409e669cf62126cd0416f00c1cea8ab933b9361b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:da26407911eac4c4fcff99ef11b9ae975540ff3ad9b5677c4d85a347c14b188d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266343873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bf110498531f91e80936e0181b8b63bac636481065a63df2e63e1aac2b1548`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:49 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e639cd467a9761616d6de8a409cb209d411f2f7ac84577b64566973d75ac5fa2`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e79c47b3010a916b04df087a57f16c399eec48d8080cb50a0f45d889323471`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 783.6 KB (783562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28152004afeb0fef135bc7f72c9c3f8605fa7f970ed9b908d8304af3ea29244`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 6.2 MB (6170281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c97bec1a3486df0287c44424237160304e8efa58d3d1ee5a191ccb45fa25303`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e885080b838ed1c6b7b5a9cb5427937014dee091f74f7371b01d9b538b636dbe`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6497d062da4fa91bf366b76e736a978762cb698b9ff1e12230118d43b124c820`  
		Last Modified: Sat, 18 Apr 2026 00:14:08 GMT  
		Size: 51.4 MB (51442459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d6178a9105eb0d5e61411f96f39c4d6500b46654be8fd130bd3bfbc6432eb`  
		Last Modified: Sat, 18 Apr 2026 00:14:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664c1f1ffcc8492f4c05894e234ba3577253cfa08919ad60b2a3323d52e7cac8`  
		Last Modified: Sat, 18 Apr 2026 00:14:10 GMT  
		Size: 160.6 MB (160628269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faff6d2a6d2f55b7cf1230e6b98303036b47e0817dfce3c5ca8ff65fd996cb5`  
		Last Modified: Sat, 18 Apr 2026 00:14:07 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:200c99f4fd2adb80e59f9b5ddde5cc8b3b7e2c90fa4b568da17a87f05c43841a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2f9dca420dd5d35f90a57ddc98c3bad21d241f0fc6c7f274c4debffda4d610`

```dockerfile
```

-	Layers:
	-	`sha256:6b65aba3f1f64e1d29ed5c0f839788403aeaec80bd07e669614ad67d695642d0`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b038cfc7980164d5219693a0827211109ac800244906ce3b65d883686d6612c`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d36eff8bce9626a30d9a53067fbc3f3929b3406fe4548c296ce2990585e58abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261447241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ca5ab30bf4ee9e428b79662b2e440e93912fc72f6408f1c5243dab5d554460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:18 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd414fac5cad07f393cbace2273171bff2f71ff6228b9118e8b6b72d195055f`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fde8c58f5021cf570a07a88e4dc7b3a2c01c772e5af1d20bbfd4cfcc8e3db9`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175ca4a36287d2506f12dd65b36c1e5269084cfd865815c70e4c09f94382745c`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 5.8 MB (5793264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f921be051e0c6462756bb035889736e272fd01828a8abdd1f13e16dcf3de3297`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1167dd93878509d66f2e3f08528ea12ceb9a823e45d5bca27e20199873a05`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb5786475529b351b067fec5c959deb8b048266b7885b434b176c782ac478d0`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 50.1 MB (50080397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d295fbc6d41d027458ae9f6b9479c90a58c714db1c208f57b5ef7f8a8ab282`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e994635adec80593755e571049efab4ba4bc1a7468498702e56bda9b84da85b`  
		Last Modified: Sat, 18 Apr 2026 00:13:51 GMT  
		Size: 158.9 MB (158926780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1274e1258c8e15a7c0aed082b7ac4f47dd327dabcc6774f39ae591e419f117b3`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9c82cc9b29ee178010cb60478cfea7696743e49f94710329120952b3e45f45f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f26768fe11299baa6669694b24d81a2b0d67daa498a46903111e1eedeefab6`

```dockerfile
```

-	Layers:
	-	`sha256:c06da225b9122f111fb64ccd9c8441b8c4aee1f59835b3be6673afa2b0296105`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a03073ece591c34e951f68d29baf88f8e7dcc3ca40235a0df3b02e2d9029ec1`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0-oraclelinux9`

```console
$ docker pull mysql@sha256:c5df04bee1a42b74a5841c6409e669cf62126cd0416f00c1cea8ab933b9361b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:da26407911eac4c4fcff99ef11b9ae975540ff3ad9b5677c4d85a347c14b188d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266343873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bf110498531f91e80936e0181b8b63bac636481065a63df2e63e1aac2b1548`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:49 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e639cd467a9761616d6de8a409cb209d411f2f7ac84577b64566973d75ac5fa2`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e79c47b3010a916b04df087a57f16c399eec48d8080cb50a0f45d889323471`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 783.6 KB (783562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28152004afeb0fef135bc7f72c9c3f8605fa7f970ed9b908d8304af3ea29244`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 6.2 MB (6170281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c97bec1a3486df0287c44424237160304e8efa58d3d1ee5a191ccb45fa25303`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e885080b838ed1c6b7b5a9cb5427937014dee091f74f7371b01d9b538b636dbe`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6497d062da4fa91bf366b76e736a978762cb698b9ff1e12230118d43b124c820`  
		Last Modified: Sat, 18 Apr 2026 00:14:08 GMT  
		Size: 51.4 MB (51442459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d6178a9105eb0d5e61411f96f39c4d6500b46654be8fd130bd3bfbc6432eb`  
		Last Modified: Sat, 18 Apr 2026 00:14:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664c1f1ffcc8492f4c05894e234ba3577253cfa08919ad60b2a3323d52e7cac8`  
		Last Modified: Sat, 18 Apr 2026 00:14:10 GMT  
		Size: 160.6 MB (160628269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faff6d2a6d2f55b7cf1230e6b98303036b47e0817dfce3c5ca8ff65fd996cb5`  
		Last Modified: Sat, 18 Apr 2026 00:14:07 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:200c99f4fd2adb80e59f9b5ddde5cc8b3b7e2c90fa4b568da17a87f05c43841a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2f9dca420dd5d35f90a57ddc98c3bad21d241f0fc6c7f274c4debffda4d610`

```dockerfile
```

-	Layers:
	-	`sha256:6b65aba3f1f64e1d29ed5c0f839788403aeaec80bd07e669614ad67d695642d0`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b038cfc7980164d5219693a0827211109ac800244906ce3b65d883686d6612c`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d36eff8bce9626a30d9a53067fbc3f3929b3406fe4548c296ce2990585e58abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261447241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ca5ab30bf4ee9e428b79662b2e440e93912fc72f6408f1c5243dab5d554460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:18 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd414fac5cad07f393cbace2273171bff2f71ff6228b9118e8b6b72d195055f`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fde8c58f5021cf570a07a88e4dc7b3a2c01c772e5af1d20bbfd4cfcc8e3db9`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175ca4a36287d2506f12dd65b36c1e5269084cfd865815c70e4c09f94382745c`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 5.8 MB (5793264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f921be051e0c6462756bb035889736e272fd01828a8abdd1f13e16dcf3de3297`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1167dd93878509d66f2e3f08528ea12ceb9a823e45d5bca27e20199873a05`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb5786475529b351b067fec5c959deb8b048266b7885b434b176c782ac478d0`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 50.1 MB (50080397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d295fbc6d41d027458ae9f6b9479c90a58c714db1c208f57b5ef7f8a8ab282`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e994635adec80593755e571049efab4ba4bc1a7468498702e56bda9b84da85b`  
		Last Modified: Sat, 18 Apr 2026 00:13:51 GMT  
		Size: 158.9 MB (158926780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1274e1258c8e15a7c0aed082b7ac4f47dd327dabcc6774f39ae591e419f117b3`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9c82cc9b29ee178010cb60478cfea7696743e49f94710329120952b3e45f45f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f26768fe11299baa6669694b24d81a2b0d67daa498a46903111e1eedeefab6`

```dockerfile
```

-	Layers:
	-	`sha256:c06da225b9122f111fb64ccd9c8441b8c4aee1f59835b3be6673afa2b0296105`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a03073ece591c34e951f68d29baf88f8e7dcc3ca40235a0df3b02e2d9029ec1`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:c5df04bee1a42b74a5841c6409e669cf62126cd0416f00c1cea8ab933b9361b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:da26407911eac4c4fcff99ef11b9ae975540ff3ad9b5677c4d85a347c14b188d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266343873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bf110498531f91e80936e0181b8b63bac636481065a63df2e63e1aac2b1548`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:49 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e639cd467a9761616d6de8a409cb209d411f2f7ac84577b64566973d75ac5fa2`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e79c47b3010a916b04df087a57f16c399eec48d8080cb50a0f45d889323471`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 783.6 KB (783562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28152004afeb0fef135bc7f72c9c3f8605fa7f970ed9b908d8304af3ea29244`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 6.2 MB (6170281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c97bec1a3486df0287c44424237160304e8efa58d3d1ee5a191ccb45fa25303`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e885080b838ed1c6b7b5a9cb5427937014dee091f74f7371b01d9b538b636dbe`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6497d062da4fa91bf366b76e736a978762cb698b9ff1e12230118d43b124c820`  
		Last Modified: Sat, 18 Apr 2026 00:14:08 GMT  
		Size: 51.4 MB (51442459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d6178a9105eb0d5e61411f96f39c4d6500b46654be8fd130bd3bfbc6432eb`  
		Last Modified: Sat, 18 Apr 2026 00:14:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664c1f1ffcc8492f4c05894e234ba3577253cfa08919ad60b2a3323d52e7cac8`  
		Last Modified: Sat, 18 Apr 2026 00:14:10 GMT  
		Size: 160.6 MB (160628269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faff6d2a6d2f55b7cf1230e6b98303036b47e0817dfce3c5ca8ff65fd996cb5`  
		Last Modified: Sat, 18 Apr 2026 00:14:07 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:200c99f4fd2adb80e59f9b5ddde5cc8b3b7e2c90fa4b568da17a87f05c43841a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2f9dca420dd5d35f90a57ddc98c3bad21d241f0fc6c7f274c4debffda4d610`

```dockerfile
```

-	Layers:
	-	`sha256:6b65aba3f1f64e1d29ed5c0f839788403aeaec80bd07e669614ad67d695642d0`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b038cfc7980164d5219693a0827211109ac800244906ce3b65d883686d6612c`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d36eff8bce9626a30d9a53067fbc3f3929b3406fe4548c296ce2990585e58abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261447241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ca5ab30bf4ee9e428b79662b2e440e93912fc72f6408f1c5243dab5d554460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:18 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd414fac5cad07f393cbace2273171bff2f71ff6228b9118e8b6b72d195055f`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fde8c58f5021cf570a07a88e4dc7b3a2c01c772e5af1d20bbfd4cfcc8e3db9`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175ca4a36287d2506f12dd65b36c1e5269084cfd865815c70e4c09f94382745c`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 5.8 MB (5793264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f921be051e0c6462756bb035889736e272fd01828a8abdd1f13e16dcf3de3297`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1167dd93878509d66f2e3f08528ea12ceb9a823e45d5bca27e20199873a05`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb5786475529b351b067fec5c959deb8b048266b7885b434b176c782ac478d0`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 50.1 MB (50080397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d295fbc6d41d027458ae9f6b9479c90a58c714db1c208f57b5ef7f8a8ab282`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e994635adec80593755e571049efab4ba4bc1a7468498702e56bda9b84da85b`  
		Last Modified: Sat, 18 Apr 2026 00:13:51 GMT  
		Size: 158.9 MB (158926780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1274e1258c8e15a7c0aed082b7ac4f47dd327dabcc6774f39ae591e419f117b3`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:9c82cc9b29ee178010cb60478cfea7696743e49f94710329120952b3e45f45f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f26768fe11299baa6669694b24d81a2b0d67daa498a46903111e1eedeefab6`

```dockerfile
```

-	Layers:
	-	`sha256:c06da225b9122f111fb64ccd9c8441b8c4aee1f59835b3be6673afa2b0296105`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a03073ece591c34e951f68d29baf88f8e7dcc3ca40235a0df3b02e2d9029ec1`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:c5df04bee1a42b74a5841c6409e669cf62126cd0416f00c1cea8ab933b9361b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:da26407911eac4c4fcff99ef11b9ae975540ff3ad9b5677c4d85a347c14b188d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266343873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bf110498531f91e80936e0181b8b63bac636481065a63df2e63e1aac2b1548`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:49 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e639cd467a9761616d6de8a409cb209d411f2f7ac84577b64566973d75ac5fa2`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e79c47b3010a916b04df087a57f16c399eec48d8080cb50a0f45d889323471`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 783.6 KB (783562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28152004afeb0fef135bc7f72c9c3f8605fa7f970ed9b908d8304af3ea29244`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 6.2 MB (6170281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c97bec1a3486df0287c44424237160304e8efa58d3d1ee5a191ccb45fa25303`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e885080b838ed1c6b7b5a9cb5427937014dee091f74f7371b01d9b538b636dbe`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6497d062da4fa91bf366b76e736a978762cb698b9ff1e12230118d43b124c820`  
		Last Modified: Sat, 18 Apr 2026 00:14:08 GMT  
		Size: 51.4 MB (51442459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d6178a9105eb0d5e61411f96f39c4d6500b46654be8fd130bd3bfbc6432eb`  
		Last Modified: Sat, 18 Apr 2026 00:14:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664c1f1ffcc8492f4c05894e234ba3577253cfa08919ad60b2a3323d52e7cac8`  
		Last Modified: Sat, 18 Apr 2026 00:14:10 GMT  
		Size: 160.6 MB (160628269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faff6d2a6d2f55b7cf1230e6b98303036b47e0817dfce3c5ca8ff65fd996cb5`  
		Last Modified: Sat, 18 Apr 2026 00:14:07 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:200c99f4fd2adb80e59f9b5ddde5cc8b3b7e2c90fa4b568da17a87f05c43841a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2f9dca420dd5d35f90a57ddc98c3bad21d241f0fc6c7f274c4debffda4d610`

```dockerfile
```

-	Layers:
	-	`sha256:6b65aba3f1f64e1d29ed5c0f839788403aeaec80bd07e669614ad67d695642d0`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b038cfc7980164d5219693a0827211109ac800244906ce3b65d883686d6612c`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d36eff8bce9626a30d9a53067fbc3f3929b3406fe4548c296ce2990585e58abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261447241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ca5ab30bf4ee9e428b79662b2e440e93912fc72f6408f1c5243dab5d554460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:18 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd414fac5cad07f393cbace2273171bff2f71ff6228b9118e8b6b72d195055f`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fde8c58f5021cf570a07a88e4dc7b3a2c01c772e5af1d20bbfd4cfcc8e3db9`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175ca4a36287d2506f12dd65b36c1e5269084cfd865815c70e4c09f94382745c`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 5.8 MB (5793264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f921be051e0c6462756bb035889736e272fd01828a8abdd1f13e16dcf3de3297`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1167dd93878509d66f2e3f08528ea12ceb9a823e45d5bca27e20199873a05`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb5786475529b351b067fec5c959deb8b048266b7885b434b176c782ac478d0`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 50.1 MB (50080397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d295fbc6d41d027458ae9f6b9479c90a58c714db1c208f57b5ef7f8a8ab282`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e994635adec80593755e571049efab4ba4bc1a7468498702e56bda9b84da85b`  
		Last Modified: Sat, 18 Apr 2026 00:13:51 GMT  
		Size: 158.9 MB (158926780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1274e1258c8e15a7c0aed082b7ac4f47dd327dabcc6774f39ae591e419f117b3`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9c82cc9b29ee178010cb60478cfea7696743e49f94710329120952b3e45f45f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f26768fe11299baa6669694b24d81a2b0d67daa498a46903111e1eedeefab6`

```dockerfile
```

-	Layers:
	-	`sha256:c06da225b9122f111fb64ccd9c8441b8c4aee1f59835b3be6673afa2b0296105`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a03073ece591c34e951f68d29baf88f8e7dcc3ca40235a0df3b02e2d9029ec1`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:c5df04bee1a42b74a5841c6409e669cf62126cd0416f00c1cea8ab933b9361b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:da26407911eac4c4fcff99ef11b9ae975540ff3ad9b5677c4d85a347c14b188d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266343873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bf110498531f91e80936e0181b8b63bac636481065a63df2e63e1aac2b1548`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:49 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e639cd467a9761616d6de8a409cb209d411f2f7ac84577b64566973d75ac5fa2`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e79c47b3010a916b04df087a57f16c399eec48d8080cb50a0f45d889323471`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 783.6 KB (783562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28152004afeb0fef135bc7f72c9c3f8605fa7f970ed9b908d8304af3ea29244`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 6.2 MB (6170281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c97bec1a3486df0287c44424237160304e8efa58d3d1ee5a191ccb45fa25303`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e885080b838ed1c6b7b5a9cb5427937014dee091f74f7371b01d9b538b636dbe`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6497d062da4fa91bf366b76e736a978762cb698b9ff1e12230118d43b124c820`  
		Last Modified: Sat, 18 Apr 2026 00:14:08 GMT  
		Size: 51.4 MB (51442459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d6178a9105eb0d5e61411f96f39c4d6500b46654be8fd130bd3bfbc6432eb`  
		Last Modified: Sat, 18 Apr 2026 00:14:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664c1f1ffcc8492f4c05894e234ba3577253cfa08919ad60b2a3323d52e7cac8`  
		Last Modified: Sat, 18 Apr 2026 00:14:10 GMT  
		Size: 160.6 MB (160628269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faff6d2a6d2f55b7cf1230e6b98303036b47e0817dfce3c5ca8ff65fd996cb5`  
		Last Modified: Sat, 18 Apr 2026 00:14:07 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:200c99f4fd2adb80e59f9b5ddde5cc8b3b7e2c90fa4b568da17a87f05c43841a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2f9dca420dd5d35f90a57ddc98c3bad21d241f0fc6c7f274c4debffda4d610`

```dockerfile
```

-	Layers:
	-	`sha256:6b65aba3f1f64e1d29ed5c0f839788403aeaec80bd07e669614ad67d695642d0`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b038cfc7980164d5219693a0827211109ac800244906ce3b65d883686d6612c`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d36eff8bce9626a30d9a53067fbc3f3929b3406fe4548c296ce2990585e58abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261447241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ca5ab30bf4ee9e428b79662b2e440e93912fc72f6408f1c5243dab5d554460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:18 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd414fac5cad07f393cbace2273171bff2f71ff6228b9118e8b6b72d195055f`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fde8c58f5021cf570a07a88e4dc7b3a2c01c772e5af1d20bbfd4cfcc8e3db9`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175ca4a36287d2506f12dd65b36c1e5269084cfd865815c70e4c09f94382745c`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 5.8 MB (5793264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f921be051e0c6462756bb035889736e272fd01828a8abdd1f13e16dcf3de3297`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1167dd93878509d66f2e3f08528ea12ceb9a823e45d5bca27e20199873a05`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb5786475529b351b067fec5c959deb8b048266b7885b434b176c782ac478d0`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 50.1 MB (50080397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d295fbc6d41d027458ae9f6b9479c90a58c714db1c208f57b5ef7f8a8ab282`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e994635adec80593755e571049efab4ba4bc1a7468498702e56bda9b84da85b`  
		Last Modified: Sat, 18 Apr 2026 00:13:51 GMT  
		Size: 158.9 MB (158926780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1274e1258c8e15a7c0aed082b7ac4f47dd327dabcc6774f39ae591e419f117b3`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9c82cc9b29ee178010cb60478cfea7696743e49f94710329120952b3e45f45f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f26768fe11299baa6669694b24d81a2b0d67daa498a46903111e1eedeefab6`

```dockerfile
```

-	Layers:
	-	`sha256:c06da225b9122f111fb64ccd9c8441b8c4aee1f59835b3be6673afa2b0296105`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a03073ece591c34e951f68d29baf88f8e7dcc3ca40235a0df3b02e2d9029ec1`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:c5df04bee1a42b74a5841c6409e669cf62126cd0416f00c1cea8ab933b9361b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:da26407911eac4c4fcff99ef11b9ae975540ff3ad9b5677c4d85a347c14b188d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266343873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bf110498531f91e80936e0181b8b63bac636481065a63df2e63e1aac2b1548`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:49 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e639cd467a9761616d6de8a409cb209d411f2f7ac84577b64566973d75ac5fa2`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e79c47b3010a916b04df087a57f16c399eec48d8080cb50a0f45d889323471`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 783.6 KB (783562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28152004afeb0fef135bc7f72c9c3f8605fa7f970ed9b908d8304af3ea29244`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 6.2 MB (6170281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c97bec1a3486df0287c44424237160304e8efa58d3d1ee5a191ccb45fa25303`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e885080b838ed1c6b7b5a9cb5427937014dee091f74f7371b01d9b538b636dbe`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6497d062da4fa91bf366b76e736a978762cb698b9ff1e12230118d43b124c820`  
		Last Modified: Sat, 18 Apr 2026 00:14:08 GMT  
		Size: 51.4 MB (51442459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d6178a9105eb0d5e61411f96f39c4d6500b46654be8fd130bd3bfbc6432eb`  
		Last Modified: Sat, 18 Apr 2026 00:14:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664c1f1ffcc8492f4c05894e234ba3577253cfa08919ad60b2a3323d52e7cac8`  
		Last Modified: Sat, 18 Apr 2026 00:14:10 GMT  
		Size: 160.6 MB (160628269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faff6d2a6d2f55b7cf1230e6b98303036b47e0817dfce3c5ca8ff65fd996cb5`  
		Last Modified: Sat, 18 Apr 2026 00:14:07 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:200c99f4fd2adb80e59f9b5ddde5cc8b3b7e2c90fa4b568da17a87f05c43841a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2f9dca420dd5d35f90a57ddc98c3bad21d241f0fc6c7f274c4debffda4d610`

```dockerfile
```

-	Layers:
	-	`sha256:6b65aba3f1f64e1d29ed5c0f839788403aeaec80bd07e669614ad67d695642d0`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b038cfc7980164d5219693a0827211109ac800244906ce3b65d883686d6612c`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d36eff8bce9626a30d9a53067fbc3f3929b3406fe4548c296ce2990585e58abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261447241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ca5ab30bf4ee9e428b79662b2e440e93912fc72f6408f1c5243dab5d554460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:18 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd414fac5cad07f393cbace2273171bff2f71ff6228b9118e8b6b72d195055f`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fde8c58f5021cf570a07a88e4dc7b3a2c01c772e5af1d20bbfd4cfcc8e3db9`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175ca4a36287d2506f12dd65b36c1e5269084cfd865815c70e4c09f94382745c`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 5.8 MB (5793264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f921be051e0c6462756bb035889736e272fd01828a8abdd1f13e16dcf3de3297`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1167dd93878509d66f2e3f08528ea12ceb9a823e45d5bca27e20199873a05`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb5786475529b351b067fec5c959deb8b048266b7885b434b176c782ac478d0`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 50.1 MB (50080397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d295fbc6d41d027458ae9f6b9479c90a58c714db1c208f57b5ef7f8a8ab282`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e994635adec80593755e571049efab4ba4bc1a7468498702e56bda9b84da85b`  
		Last Modified: Sat, 18 Apr 2026 00:13:51 GMT  
		Size: 158.9 MB (158926780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1274e1258c8e15a7c0aed082b7ac4f47dd327dabcc6774f39ae591e419f117b3`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:9c82cc9b29ee178010cb60478cfea7696743e49f94710329120952b3e45f45f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f26768fe11299baa6669694b24d81a2b0d67daa498a46903111e1eedeefab6`

```dockerfile
```

-	Layers:
	-	`sha256:c06da225b9122f111fb64ccd9c8441b8c4aee1f59835b3be6673afa2b0296105`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a03073ece591c34e951f68d29baf88f8e7dcc3ca40235a0df3b02e2d9029ec1`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:43bd9764df60666fb2ba2cf8217dd17b3d2414c150005d2fdd07a0cd73d3b7f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

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

### `mysql:lts` - unknown; unknown

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

### `mysql:lts` - linux; arm64 variant v8

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

### `mysql:lts` - unknown; unknown

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

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:43bd9764df60666fb2ba2cf8217dd17b3d2414c150005d2fdd07a0cd73d3b7f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

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

### `mysql:lts-oracle` - unknown; unknown

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

### `mysql:lts-oracle` - linux; arm64 variant v8

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

### `mysql:lts-oracle` - unknown; unknown

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

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:43bd9764df60666fb2ba2cf8217dd17b3d2414c150005d2fdd07a0cd73d3b7f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

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

### `mysql:lts-oraclelinux9` - unknown; unknown

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

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

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

### `mysql:lts-oraclelinux9` - unknown; unknown

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

## `mysql:oracle`

```console
$ docker pull mysql@sha256:c5df04bee1a42b74a5841c6409e669cf62126cd0416f00c1cea8ab933b9361b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:da26407911eac4c4fcff99ef11b9ae975540ff3ad9b5677c4d85a347c14b188d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266343873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bf110498531f91e80936e0181b8b63bac636481065a63df2e63e1aac2b1548`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:49 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e639cd467a9761616d6de8a409cb209d411f2f7ac84577b64566973d75ac5fa2`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e79c47b3010a916b04df087a57f16c399eec48d8080cb50a0f45d889323471`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 783.6 KB (783562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28152004afeb0fef135bc7f72c9c3f8605fa7f970ed9b908d8304af3ea29244`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 6.2 MB (6170281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c97bec1a3486df0287c44424237160304e8efa58d3d1ee5a191ccb45fa25303`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e885080b838ed1c6b7b5a9cb5427937014dee091f74f7371b01d9b538b636dbe`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6497d062da4fa91bf366b76e736a978762cb698b9ff1e12230118d43b124c820`  
		Last Modified: Sat, 18 Apr 2026 00:14:08 GMT  
		Size: 51.4 MB (51442459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d6178a9105eb0d5e61411f96f39c4d6500b46654be8fd130bd3bfbc6432eb`  
		Last Modified: Sat, 18 Apr 2026 00:14:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664c1f1ffcc8492f4c05894e234ba3577253cfa08919ad60b2a3323d52e7cac8`  
		Last Modified: Sat, 18 Apr 2026 00:14:10 GMT  
		Size: 160.6 MB (160628269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faff6d2a6d2f55b7cf1230e6b98303036b47e0817dfce3c5ca8ff65fd996cb5`  
		Last Modified: Sat, 18 Apr 2026 00:14:07 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:200c99f4fd2adb80e59f9b5ddde5cc8b3b7e2c90fa4b568da17a87f05c43841a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2f9dca420dd5d35f90a57ddc98c3bad21d241f0fc6c7f274c4debffda4d610`

```dockerfile
```

-	Layers:
	-	`sha256:6b65aba3f1f64e1d29ed5c0f839788403aeaec80bd07e669614ad67d695642d0`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b038cfc7980164d5219693a0827211109ac800244906ce3b65d883686d6612c`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d36eff8bce9626a30d9a53067fbc3f3929b3406fe4548c296ce2990585e58abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261447241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ca5ab30bf4ee9e428b79662b2e440e93912fc72f6408f1c5243dab5d554460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:18 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd414fac5cad07f393cbace2273171bff2f71ff6228b9118e8b6b72d195055f`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fde8c58f5021cf570a07a88e4dc7b3a2c01c772e5af1d20bbfd4cfcc8e3db9`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175ca4a36287d2506f12dd65b36c1e5269084cfd865815c70e4c09f94382745c`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 5.8 MB (5793264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f921be051e0c6462756bb035889736e272fd01828a8abdd1f13e16dcf3de3297`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1167dd93878509d66f2e3f08528ea12ceb9a823e45d5bca27e20199873a05`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb5786475529b351b067fec5c959deb8b048266b7885b434b176c782ac478d0`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 50.1 MB (50080397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d295fbc6d41d027458ae9f6b9479c90a58c714db1c208f57b5ef7f8a8ab282`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e994635adec80593755e571049efab4ba4bc1a7468498702e56bda9b84da85b`  
		Last Modified: Sat, 18 Apr 2026 00:13:51 GMT  
		Size: 158.9 MB (158926780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1274e1258c8e15a7c0aed082b7ac4f47dd327dabcc6774f39ae591e419f117b3`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9c82cc9b29ee178010cb60478cfea7696743e49f94710329120952b3e45f45f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f26768fe11299baa6669694b24d81a2b0d67daa498a46903111e1eedeefab6`

```dockerfile
```

-	Layers:
	-	`sha256:c06da225b9122f111fb64ccd9c8441b8c4aee1f59835b3be6673afa2b0296105`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a03073ece591c34e951f68d29baf88f8e7dcc3ca40235a0df3b02e2d9029ec1`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:c5df04bee1a42b74a5841c6409e669cf62126cd0416f00c1cea8ab933b9361b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:da26407911eac4c4fcff99ef11b9ae975540ff3ad9b5677c4d85a347c14b188d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266343873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bf110498531f91e80936e0181b8b63bac636481065a63df2e63e1aac2b1548`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:49 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:12:17 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:47 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e639cd467a9761616d6de8a409cb209d411f2f7ac84577b64566973d75ac5fa2`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e79c47b3010a916b04df087a57f16c399eec48d8080cb50a0f45d889323471`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 783.6 KB (783562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28152004afeb0fef135bc7f72c9c3f8605fa7f970ed9b908d8304af3ea29244`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 6.2 MB (6170281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c97bec1a3486df0287c44424237160304e8efa58d3d1ee5a191ccb45fa25303`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e885080b838ed1c6b7b5a9cb5427937014dee091f74f7371b01d9b538b636dbe`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6497d062da4fa91bf366b76e736a978762cb698b9ff1e12230118d43b124c820`  
		Last Modified: Sat, 18 Apr 2026 00:14:08 GMT  
		Size: 51.4 MB (51442459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d6178a9105eb0d5e61411f96f39c4d6500b46654be8fd130bd3bfbc6432eb`  
		Last Modified: Sat, 18 Apr 2026 00:14:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664c1f1ffcc8492f4c05894e234ba3577253cfa08919ad60b2a3323d52e7cac8`  
		Last Modified: Sat, 18 Apr 2026 00:14:10 GMT  
		Size: 160.6 MB (160628269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faff6d2a6d2f55b7cf1230e6b98303036b47e0817dfce3c5ca8ff65fd996cb5`  
		Last Modified: Sat, 18 Apr 2026 00:14:07 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:200c99f4fd2adb80e59f9b5ddde5cc8b3b7e2c90fa4b568da17a87f05c43841a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2f9dca420dd5d35f90a57ddc98c3bad21d241f0fc6c7f274c4debffda4d610`

```dockerfile
```

-	Layers:
	-	`sha256:6b65aba3f1f64e1d29ed5c0f839788403aeaec80bd07e669614ad67d695642d0`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b038cfc7980164d5219693a0827211109ac800244906ce3b65d883686d6612c`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d36eff8bce9626a30d9a53067fbc3f3929b3406fe4548c296ce2990585e58abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261447241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ca5ab30bf4ee9e428b79662b2e440e93912fc72f6408f1c5243dab5d554460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:18 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:18 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 18 Apr 2026 00:11:46 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:11:46 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:21 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Sat, 18 Apr 2026 00:13:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd414fac5cad07f393cbace2273171bff2f71ff6228b9118e8b6b72d195055f`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fde8c58f5021cf570a07a88e4dc7b3a2c01c772e5af1d20bbfd4cfcc8e3db9`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175ca4a36287d2506f12dd65b36c1e5269084cfd865815c70e4c09f94382745c`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 5.8 MB (5793264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f921be051e0c6462756bb035889736e272fd01828a8abdd1f13e16dcf3de3297`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1167dd93878509d66f2e3f08528ea12ceb9a823e45d5bca27e20199873a05`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb5786475529b351b067fec5c959deb8b048266b7885b434b176c782ac478d0`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 50.1 MB (50080397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d295fbc6d41d027458ae9f6b9479c90a58c714db1c208f57b5ef7f8a8ab282`  
		Last Modified: Sat, 18 Apr 2026 00:13:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e994635adec80593755e571049efab4ba4bc1a7468498702e56bda9b84da85b`  
		Last Modified: Sat, 18 Apr 2026 00:13:51 GMT  
		Size: 158.9 MB (158926780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1274e1258c8e15a7c0aed082b7ac4f47dd327dabcc6774f39ae591e419f117b3`  
		Last Modified: Sat, 18 Apr 2026 00:13:43 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9c82cc9b29ee178010cb60478cfea7696743e49f94710329120952b3e45f45f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f26768fe11299baa6669694b24d81a2b0d67daa498a46903111e1eedeefab6`

```dockerfile
```

-	Layers:
	-	`sha256:c06da225b9122f111fb64ccd9c8441b8c4aee1f59835b3be6673afa2b0296105`  
		Last Modified: Sat, 18 Apr 2026 00:13:41 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a03073ece591c34e951f68d29baf88f8e7dcc3ca40235a0df3b02e2d9029ec1`  
		Last Modified: Sat, 18 Apr 2026 00:13:40 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json
