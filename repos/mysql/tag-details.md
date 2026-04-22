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
