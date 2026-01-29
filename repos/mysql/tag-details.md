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
$ docker pull mysql@sha256:f1c7674d8dd3c94f439b0d607792187d55bd861f94e8c6d683b959b577152bdc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:8b3be4876b08746f2caa509afae13bac0aca1885ce967d1bb5ca0d177000f3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233227949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4511f663fb18c6cde7e5d9bdaafeed8c1c7019732b77279315145eb430e85dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:11:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:11:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:39 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:39 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad075f4936cf8a36f21e937e90b1d698baa6b0e625d13c69beef2586416bd2b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2ec557f75a04fa223e3c0bd71f6cc48ecc59f12a6c5e31a4ed48df3205387b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c1d58a53d79eac5a138b2337dda522a36661053c302535c365fc5f64af2ad`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 6.2 MB (6172774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c60e0e578e332d62e541d2460840ae181c04522af7b87a815b50532a0cd0b9`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0125f072a0a55ba4ae0188f2dcd165d077cf20a27ed19e114cb325eb5256a1cc`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c356f1b5fd3fb93d5570a71077cff86a0af06026ef7a77b257d5d83f73166d16`  
		Last Modified: Wed, 28 Jan 2026 22:13:12 GMT  
		Size: 47.8 MB (47810258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cb4bc116b0506e2ea4ab9fa6bc54cc451e350fa3274fa025479c731cbaad6d`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce6e8837913ee62730f9a78f444b9a4cdb9f29bd6e248340731f67a1c261849`  
		Last Modified: Wed, 28 Jan 2026 22:13:14 GMT  
		Size: 131.1 MB (131139180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885e95c29fdf0877c6ec82ac693521e9735cf0c19a64d0d6d950afeb84929b31`  
		Last Modified: Wed, 28 Jan 2026 22:13:11 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:798a0bad5920617757611d4a42a351558a280acbec05ebd5596f7aa5f9b00d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7698ea2fc5e9501ff603ff4bd1d0a97505093033193881b8e631982bb6483280`

```dockerfile
```

-	Layers:
	-	`sha256:c823f2fc76110ec949a1d955075948f84148e5766bc8d9751774c7fd1ddf24b5`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c856894eeb424a1604d601f5379bd90c5520e1e86430ff879bc9a4b675c5678`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e51f27439b7a2119f9322da62672bf29db9733dfe5efda7fe14a95b1978b77f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228695273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a187cad11f0bae46349c98546b174514318cd9934ece1aaf891d8bb165f437`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:45 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:47 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:23 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b8014f3539c98ae4d9db79063d0ac6da20c561da597e5080428d7fa2a81045`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581c2da28c304c8a55c89ffc142dfe9b49523660a41d23868aabdb3746f9b14e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311e3508c6b08056182bbc122c5da5bf25d876d8f0bd1eb0921f401aa6e4e794`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 5.8 MB (5792078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dac3a350ad94d3b3ff38d83b364f9dfeb47f767e8586aacb3733b7ba672656`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbefc80b7213ccab583b4d0250ca47d5a5ffbfcc700eb995807fb9e9c824552`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6900ac85f3c3185bf951b4c2ff044719ab72a728e44d91c4aeed766ee05b847d`  
		Last Modified: Wed, 28 Jan 2026 22:12:56 GMT  
		Size: 46.7 MB (46700971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc870ee9e6c819f59ecc85a2e7df376e613358eb45f4a14ebe822cf57fe76a26`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f95bece7002a8fd4dd526ef950d925ffb02f0937885175169806d3ec1ab8e1`  
		Last Modified: Wed, 28 Jan 2026 22:12:58 GMT  
		Size: 129.6 MB (129551997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923168c7bf209bd6189f93d4cb04d2c82f17faf0ae36433ab67dd1e72ec3ca29`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:ae951e3a0f700ccaab54d8aa559d60b9d07b96bd8f3121b6ed86971368f04b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282b71728f5dbf3f9d4b34689d6b80dc2aa9c48da7c3fe42eada863a8d347d0`

```dockerfile
```

-	Layers:
	-	`sha256:d66e901a34db0d11a63eea540fdacb6235f7c53a2a0b8b51cf5d898c1c80b2f7`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf852e8614823f7b667b3de07ca7069909c56a682daa323b1433a790564d9d2e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:f1c7674d8dd3c94f439b0d607792187d55bd861f94e8c6d683b959b577152bdc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8b3be4876b08746f2caa509afae13bac0aca1885ce967d1bb5ca0d177000f3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233227949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4511f663fb18c6cde7e5d9bdaafeed8c1c7019732b77279315145eb430e85dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:11:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:11:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:39 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:39 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad075f4936cf8a36f21e937e90b1d698baa6b0e625d13c69beef2586416bd2b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2ec557f75a04fa223e3c0bd71f6cc48ecc59f12a6c5e31a4ed48df3205387b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c1d58a53d79eac5a138b2337dda522a36661053c302535c365fc5f64af2ad`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 6.2 MB (6172774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c60e0e578e332d62e541d2460840ae181c04522af7b87a815b50532a0cd0b9`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0125f072a0a55ba4ae0188f2dcd165d077cf20a27ed19e114cb325eb5256a1cc`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c356f1b5fd3fb93d5570a71077cff86a0af06026ef7a77b257d5d83f73166d16`  
		Last Modified: Wed, 28 Jan 2026 22:13:12 GMT  
		Size: 47.8 MB (47810258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cb4bc116b0506e2ea4ab9fa6bc54cc451e350fa3274fa025479c731cbaad6d`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce6e8837913ee62730f9a78f444b9a4cdb9f29bd6e248340731f67a1c261849`  
		Last Modified: Wed, 28 Jan 2026 22:13:14 GMT  
		Size: 131.1 MB (131139180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885e95c29fdf0877c6ec82ac693521e9735cf0c19a64d0d6d950afeb84929b31`  
		Last Modified: Wed, 28 Jan 2026 22:13:11 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:798a0bad5920617757611d4a42a351558a280acbec05ebd5596f7aa5f9b00d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7698ea2fc5e9501ff603ff4bd1d0a97505093033193881b8e631982bb6483280`

```dockerfile
```

-	Layers:
	-	`sha256:c823f2fc76110ec949a1d955075948f84148e5766bc8d9751774c7fd1ddf24b5`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c856894eeb424a1604d601f5379bd90c5520e1e86430ff879bc9a4b675c5678`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e51f27439b7a2119f9322da62672bf29db9733dfe5efda7fe14a95b1978b77f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228695273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a187cad11f0bae46349c98546b174514318cd9934ece1aaf891d8bb165f437`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:45 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:47 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:23 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b8014f3539c98ae4d9db79063d0ac6da20c561da597e5080428d7fa2a81045`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581c2da28c304c8a55c89ffc142dfe9b49523660a41d23868aabdb3746f9b14e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311e3508c6b08056182bbc122c5da5bf25d876d8f0bd1eb0921f401aa6e4e794`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 5.8 MB (5792078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dac3a350ad94d3b3ff38d83b364f9dfeb47f767e8586aacb3733b7ba672656`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbefc80b7213ccab583b4d0250ca47d5a5ffbfcc700eb995807fb9e9c824552`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6900ac85f3c3185bf951b4c2ff044719ab72a728e44d91c4aeed766ee05b847d`  
		Last Modified: Wed, 28 Jan 2026 22:12:56 GMT  
		Size: 46.7 MB (46700971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc870ee9e6c819f59ecc85a2e7df376e613358eb45f4a14ebe822cf57fe76a26`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f95bece7002a8fd4dd526ef950d925ffb02f0937885175169806d3ec1ab8e1`  
		Last Modified: Wed, 28 Jan 2026 22:12:58 GMT  
		Size: 129.6 MB (129551997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923168c7bf209bd6189f93d4cb04d2c82f17faf0ae36433ab67dd1e72ec3ca29`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ae951e3a0f700ccaab54d8aa559d60b9d07b96bd8f3121b6ed86971368f04b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282b71728f5dbf3f9d4b34689d6b80dc2aa9c48da7c3fe42eada863a8d347d0`

```dockerfile
```

-	Layers:
	-	`sha256:d66e901a34db0d11a63eea540fdacb6235f7c53a2a0b8b51cf5d898c1c80b2f7`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf852e8614823f7b667b3de07ca7069909c56a682daa323b1433a790564d9d2e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:f1c7674d8dd3c94f439b0d607792187d55bd861f94e8c6d683b959b577152bdc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:8b3be4876b08746f2caa509afae13bac0aca1885ce967d1bb5ca0d177000f3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233227949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4511f663fb18c6cde7e5d9bdaafeed8c1c7019732b77279315145eb430e85dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:11:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:11:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:39 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:39 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad075f4936cf8a36f21e937e90b1d698baa6b0e625d13c69beef2586416bd2b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2ec557f75a04fa223e3c0bd71f6cc48ecc59f12a6c5e31a4ed48df3205387b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c1d58a53d79eac5a138b2337dda522a36661053c302535c365fc5f64af2ad`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 6.2 MB (6172774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c60e0e578e332d62e541d2460840ae181c04522af7b87a815b50532a0cd0b9`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0125f072a0a55ba4ae0188f2dcd165d077cf20a27ed19e114cb325eb5256a1cc`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c356f1b5fd3fb93d5570a71077cff86a0af06026ef7a77b257d5d83f73166d16`  
		Last Modified: Wed, 28 Jan 2026 22:13:12 GMT  
		Size: 47.8 MB (47810258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cb4bc116b0506e2ea4ab9fa6bc54cc451e350fa3274fa025479c731cbaad6d`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce6e8837913ee62730f9a78f444b9a4cdb9f29bd6e248340731f67a1c261849`  
		Last Modified: Wed, 28 Jan 2026 22:13:14 GMT  
		Size: 131.1 MB (131139180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885e95c29fdf0877c6ec82ac693521e9735cf0c19a64d0d6d950afeb84929b31`  
		Last Modified: Wed, 28 Jan 2026 22:13:11 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:798a0bad5920617757611d4a42a351558a280acbec05ebd5596f7aa5f9b00d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7698ea2fc5e9501ff603ff4bd1d0a97505093033193881b8e631982bb6483280`

```dockerfile
```

-	Layers:
	-	`sha256:c823f2fc76110ec949a1d955075948f84148e5766bc8d9751774c7fd1ddf24b5`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c856894eeb424a1604d601f5379bd90c5520e1e86430ff879bc9a4b675c5678`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e51f27439b7a2119f9322da62672bf29db9733dfe5efda7fe14a95b1978b77f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228695273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a187cad11f0bae46349c98546b174514318cd9934ece1aaf891d8bb165f437`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:45 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:47 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:23 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b8014f3539c98ae4d9db79063d0ac6da20c561da597e5080428d7fa2a81045`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581c2da28c304c8a55c89ffc142dfe9b49523660a41d23868aabdb3746f9b14e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311e3508c6b08056182bbc122c5da5bf25d876d8f0bd1eb0921f401aa6e4e794`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 5.8 MB (5792078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dac3a350ad94d3b3ff38d83b364f9dfeb47f767e8586aacb3733b7ba672656`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbefc80b7213ccab583b4d0250ca47d5a5ffbfcc700eb995807fb9e9c824552`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6900ac85f3c3185bf951b4c2ff044719ab72a728e44d91c4aeed766ee05b847d`  
		Last Modified: Wed, 28 Jan 2026 22:12:56 GMT  
		Size: 46.7 MB (46700971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc870ee9e6c819f59ecc85a2e7df376e613358eb45f4a14ebe822cf57fe76a26`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f95bece7002a8fd4dd526ef950d925ffb02f0937885175169806d3ec1ab8e1`  
		Last Modified: Wed, 28 Jan 2026 22:12:58 GMT  
		Size: 129.6 MB (129551997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923168c7bf209bd6189f93d4cb04d2c82f17faf0ae36433ab67dd1e72ec3ca29`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ae951e3a0f700ccaab54d8aa559d60b9d07b96bd8f3121b6ed86971368f04b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282b71728f5dbf3f9d4b34689d6b80dc2aa9c48da7c3fe42eada863a8d347d0`

```dockerfile
```

-	Layers:
	-	`sha256:d66e901a34db0d11a63eea540fdacb6235f7c53a2a0b8b51cf5d898c1c80b2f7`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf852e8614823f7b667b3de07ca7069909c56a682daa323b1433a790564d9d2e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:68bee0989e5623da84778fe2e20d38a0b2432e46645cf8e4667b9ea15e8ee373
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:3ad50ea218eeca078cbaaf012932984ebd0a65aa67c65884f2e3e0ce672b5285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232301209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73678e5bb5566a44426e48a76165e8655f31c5e7a21468360859fbc842bf3819`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:11:59 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:11:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:12:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:12:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:12:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 28 Jan 2026 22:12:25 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:12:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:12:54 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:12:54 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:12:54 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:13:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:13:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 22:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:13:30 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:13:30 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66262e8c98ce4c2bfbd6f85a9a924ff94cd6b78d5ed82423c3112f9640b28c0b`  
		Last Modified: Wed, 28 Jan 2026 22:14:00 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c852e6fd6ca689f343ecd9556696c9a055807db926532774b7ce980b99660208`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5417dc65ba4347a7a9f71250e80e8ab02850cf1891191788a8d3a6bd7fd102`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 6.2 MB (6172820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cda71723ca490ed94103a8ffaf9a018564afb567a1cd11bdb88ffe6739ba29`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f3eb4051e12d7643406a550c0b9ae9aec223ca08500761dad291be8a676e17`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f75bb8cb9075b2637ebc1e4fece5007fdd969d063877f4379b2fa2122a933c`  
		Last Modified: Wed, 28 Jan 2026 22:14:04 GMT  
		Size: 49.9 MB (49921194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85492c82cc5e83a101deac2585097ae10941432849cacd0e85612f89f005a746`  
		Last Modified: Wed, 28 Jan 2026 22:14:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c48ae948a50c8a66f2e0d1671683d43038e454ad971b80d6c897120b5fc53e`  
		Last Modified: Wed, 28 Jan 2026 22:14:06 GMT  
		Size: 128.1 MB (128101341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a46d9073fa47ff8bfe8d4dba9438d9bdcc204905a9476c61b53a836cf4b538c`  
		Last Modified: Wed, 28 Jan 2026 22:14:03 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496c3bd4b1509fc6c4c59fe31ed2a8ae93ebf144188eb997989dedb85772a8c4`  
		Last Modified: Wed, 28 Jan 2026 22:14:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:6d8facabe1744878461496ccfedc82f577c37d2d2d40cfaaf37091897c16ffc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcced7a5130d8700fe05151d79f8786f72a78298e6703646d8090c8078617af`

```dockerfile
```

-	Layers:
	-	`sha256:11db86e8e763cff65b4b51a32856f1cf15b44bf9806cced161ca911fd8e638e6`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 15.0 MB (14957489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd069fba1e52cef3eb858bf86615571052ce5254c2ea0ffd8bbbb239d53ae64b`  
		Last Modified: Wed, 28 Jan 2026 22:14:00 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bd5aa59105ea8c2f2a1d29be9f495e7804d7f4f6ef0514c6a0a5986bef524591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227901504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b5f19aa0c60edc52a62857a800bb649a049910324e552c9d68a34c42e27dc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:53 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:12:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 22:12:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450daa4e0f5ea96d16aa389a8e87426a9214ab0f71182b7803908dcca98a5209`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1724ce9d93488b72bca491622c74d25eb8ac6509f2b162df09de51ea638d66`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 737.5 KB (737521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d00b1e5474cb62a592b7175ac90c0112ff6b00baecfe975562a86f6700b478`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 5.8 MB (5792045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2166d6728093b8d49f9e466e247b361c27598c8ff03217028c748cb55628b30f`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585b27da4caa49eae873de2c47465c7417c0a211d48a37035499aa4dcb96f8f0`  
		Last Modified: Wed, 28 Jan 2026 22:13:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0197c3019186bd4e5cf971458359bbf6714eb0569d9218b47da645ef7ca325cf`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 48.8 MB (48775828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2cc4c99fca6f8f458876393d8464b0399bd60c88a67bddc6b2ca1a5329aa01`  
		Last Modified: Wed, 28 Jan 2026 22:13:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9825076cf2cb6def3e2047e534f69c9c67c6df732b4d944df1046de2068e5d`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 126.7 MB (126683295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e4a9a975ca1f3e336e6943ef6c033b230f4ae9e08b954d835007e0055a1651`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb92b3cef2d2aa649d1b6de58251b791173d3d04630e53f37ba4773c032db7c`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:67afce0904ef71f1cb18d81caf27f0688fc409eb40c79a00e5cb853efc1b9c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d5ba34f9151a6ec11a847750e441e5725a7f9e716660fbfb805f08bd359127`

```dockerfile
```

-	Layers:
	-	`sha256:609ef88e20510e9c30596b1934e89afe72d822012891409310fe59fef8ca767f`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 15.0 MB (14955837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d3ad32f16baf32289de86d7d6826f4b35670e14220600d45947afe7b8e469ef`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 35.2 KB (35158 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:5284868db9fd4c480d37e8394fb37316ba29b1bdbec31185676faaf42cd82612
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:dee7500826371f0383c6673ab1fc4cece140d7f8fb365550597548549b253dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183455449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb471428bdc168577f9e02a48169eda26499d392561b1978b431aa483d45e642`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 21 Jan 2026 22:49:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 21 Jan 2026 22:49:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:49:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Jan 2026 22:49:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Wed, 21 Jan 2026 22:49:25 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:36 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa36b2e2c985c829bdf403d8168eeae8890c3217a30563a2b5b3aa68e1efdba`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d1348177f9534b0b93188d0bd2781bf8088988b503664ef3329e9462ec5e6d`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 4.4 MB (4423336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106cdb304c5842e0232ae8ce1fcf6877cff36e384ba2d8ecc68dd0b670d04f34`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 1.2 MB (1248714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f855ce4e64c494fdd0390394941885efc48adffab2266c04a67f71c80b55fce`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb9b517325f53660036f1de6ca0e9494dbc84aafe02d886a34f2bd505a0d80c`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 15.3 MB (15295819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94beb5f31bf6179d42df34e5693e2f2e1e7b3efe8ab3be7410347bd25082c2c`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab60d99d7fa5f30783088438eb8f263f39c3c315a7da872044328dd07ca2a26`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c09fbe4bbb7dde90633da807e1f347b7caf14883cab671790a4369c31ded78f`  
		Last Modified: Wed, 21 Jan 2026 22:50:01 GMT  
		Size: 134.2 MB (134248192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ed9baa1e80f6b50800638f3cdc195044965a20d046ae3565fdfb32a2f8eb6b`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c36bcd4939de82e2db98188dc2dd518dbda890712040edb19e8befbbe028557`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29984f882141106a3f505fd1ee0d8afaf76a58bf3e0e8f6d953f5bee612777fa`  
		Last Modified: Wed, 21 Jan 2026 22:50:00 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:a7eddc6833b1dad7a3743fa776da9e6c8604dd9b860673e99b88d15d65e4693a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c526e7816588d61af24be57343f0050e43cdbbad362b3b6ba103554894ebe19b`

```dockerfile
```

-	Layers:
	-	`sha256:cade0013c36201ab6c42ec4b5f213e754609b2f3fe9fc19478d78770c9747810`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b99cd63676959f0fe9ca9cd457e9c74b4e5e604d39c4d8bca1ba174822cf3c7`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:5284868db9fd4c480d37e8394fb37316ba29b1bdbec31185676faaf42cd82612
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:dee7500826371f0383c6673ab1fc4cece140d7f8fb365550597548549b253dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183455449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb471428bdc168577f9e02a48169eda26499d392561b1978b431aa483d45e642`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 21 Jan 2026 22:49:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 21 Jan 2026 22:49:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:49:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Jan 2026 22:49:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Wed, 21 Jan 2026 22:49:25 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:36 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa36b2e2c985c829bdf403d8168eeae8890c3217a30563a2b5b3aa68e1efdba`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d1348177f9534b0b93188d0bd2781bf8088988b503664ef3329e9462ec5e6d`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 4.4 MB (4423336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106cdb304c5842e0232ae8ce1fcf6877cff36e384ba2d8ecc68dd0b670d04f34`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 1.2 MB (1248714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f855ce4e64c494fdd0390394941885efc48adffab2266c04a67f71c80b55fce`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb9b517325f53660036f1de6ca0e9494dbc84aafe02d886a34f2bd505a0d80c`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 15.3 MB (15295819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94beb5f31bf6179d42df34e5693e2f2e1e7b3efe8ab3be7410347bd25082c2c`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab60d99d7fa5f30783088438eb8f263f39c3c315a7da872044328dd07ca2a26`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c09fbe4bbb7dde90633da807e1f347b7caf14883cab671790a4369c31ded78f`  
		Last Modified: Wed, 21 Jan 2026 22:50:01 GMT  
		Size: 134.2 MB (134248192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ed9baa1e80f6b50800638f3cdc195044965a20d046ae3565fdfb32a2f8eb6b`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c36bcd4939de82e2db98188dc2dd518dbda890712040edb19e8befbbe028557`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29984f882141106a3f505fd1ee0d8afaf76a58bf3e0e8f6d953f5bee612777fa`  
		Last Modified: Wed, 21 Jan 2026 22:50:00 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:a7eddc6833b1dad7a3743fa776da9e6c8604dd9b860673e99b88d15d65e4693a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c526e7816588d61af24be57343f0050e43cdbbad362b3b6ba103554894ebe19b`

```dockerfile
```

-	Layers:
	-	`sha256:cade0013c36201ab6c42ec4b5f213e754609b2f3fe9fc19478d78770c9747810`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b99cd63676959f0fe9ca9cd457e9c74b4e5e604d39c4d8bca1ba174822cf3c7`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:68bee0989e5623da84778fe2e20d38a0b2432e46645cf8e4667b9ea15e8ee373
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:3ad50ea218eeca078cbaaf012932984ebd0a65aa67c65884f2e3e0ce672b5285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232301209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73678e5bb5566a44426e48a76165e8655f31c5e7a21468360859fbc842bf3819`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:11:59 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:11:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:12:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:12:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:12:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 28 Jan 2026 22:12:25 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:12:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:12:54 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:12:54 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:12:54 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:13:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:13:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 22:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:13:30 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:13:30 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66262e8c98ce4c2bfbd6f85a9a924ff94cd6b78d5ed82423c3112f9640b28c0b`  
		Last Modified: Wed, 28 Jan 2026 22:14:00 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c852e6fd6ca689f343ecd9556696c9a055807db926532774b7ce980b99660208`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5417dc65ba4347a7a9f71250e80e8ab02850cf1891191788a8d3a6bd7fd102`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 6.2 MB (6172820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cda71723ca490ed94103a8ffaf9a018564afb567a1cd11bdb88ffe6739ba29`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f3eb4051e12d7643406a550c0b9ae9aec223ca08500761dad291be8a676e17`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f75bb8cb9075b2637ebc1e4fece5007fdd969d063877f4379b2fa2122a933c`  
		Last Modified: Wed, 28 Jan 2026 22:14:04 GMT  
		Size: 49.9 MB (49921194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85492c82cc5e83a101deac2585097ae10941432849cacd0e85612f89f005a746`  
		Last Modified: Wed, 28 Jan 2026 22:14:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c48ae948a50c8a66f2e0d1671683d43038e454ad971b80d6c897120b5fc53e`  
		Last Modified: Wed, 28 Jan 2026 22:14:06 GMT  
		Size: 128.1 MB (128101341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a46d9073fa47ff8bfe8d4dba9438d9bdcc204905a9476c61b53a836cf4b538c`  
		Last Modified: Wed, 28 Jan 2026 22:14:03 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496c3bd4b1509fc6c4c59fe31ed2a8ae93ebf144188eb997989dedb85772a8c4`  
		Last Modified: Wed, 28 Jan 2026 22:14:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6d8facabe1744878461496ccfedc82f577c37d2d2d40cfaaf37091897c16ffc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcced7a5130d8700fe05151d79f8786f72a78298e6703646d8090c8078617af`

```dockerfile
```

-	Layers:
	-	`sha256:11db86e8e763cff65b4b51a32856f1cf15b44bf9806cced161ca911fd8e638e6`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 15.0 MB (14957489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd069fba1e52cef3eb858bf86615571052ce5254c2ea0ffd8bbbb239d53ae64b`  
		Last Modified: Wed, 28 Jan 2026 22:14:00 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bd5aa59105ea8c2f2a1d29be9f495e7804d7f4f6ef0514c6a0a5986bef524591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227901504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b5f19aa0c60edc52a62857a800bb649a049910324e552c9d68a34c42e27dc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:53 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:12:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 22:12:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450daa4e0f5ea96d16aa389a8e87426a9214ab0f71182b7803908dcca98a5209`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1724ce9d93488b72bca491622c74d25eb8ac6509f2b162df09de51ea638d66`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 737.5 KB (737521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d00b1e5474cb62a592b7175ac90c0112ff6b00baecfe975562a86f6700b478`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 5.8 MB (5792045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2166d6728093b8d49f9e466e247b361c27598c8ff03217028c748cb55628b30f`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585b27da4caa49eae873de2c47465c7417c0a211d48a37035499aa4dcb96f8f0`  
		Last Modified: Wed, 28 Jan 2026 22:13:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0197c3019186bd4e5cf971458359bbf6714eb0569d9218b47da645ef7ca325cf`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 48.8 MB (48775828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2cc4c99fca6f8f458876393d8464b0399bd60c88a67bddc6b2ca1a5329aa01`  
		Last Modified: Wed, 28 Jan 2026 22:13:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9825076cf2cb6def3e2047e534f69c9c67c6df732b4d944df1046de2068e5d`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 126.7 MB (126683295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e4a9a975ca1f3e336e6943ef6c033b230f4ae9e08b954d835007e0055a1651`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb92b3cef2d2aa649d1b6de58251b791173d3d04630e53f37ba4773c032db7c`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:67afce0904ef71f1cb18d81caf27f0688fc409eb40c79a00e5cb853efc1b9c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d5ba34f9151a6ec11a847750e441e5725a7f9e716660fbfb805f08bd359127`

```dockerfile
```

-	Layers:
	-	`sha256:609ef88e20510e9c30596b1934e89afe72d822012891409310fe59fef8ca767f`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 15.0 MB (14955837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d3ad32f16baf32289de86d7d6826f4b35670e14220600d45947afe7b8e469ef`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 35.2 KB (35158 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:68bee0989e5623da84778fe2e20d38a0b2432e46645cf8e4667b9ea15e8ee373
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:3ad50ea218eeca078cbaaf012932984ebd0a65aa67c65884f2e3e0ce672b5285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232301209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73678e5bb5566a44426e48a76165e8655f31c5e7a21468360859fbc842bf3819`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:11:59 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:11:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:12:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:12:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:12:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 28 Jan 2026 22:12:25 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:12:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:12:54 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:12:54 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:12:54 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:13:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:13:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 22:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:13:30 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:13:30 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66262e8c98ce4c2bfbd6f85a9a924ff94cd6b78d5ed82423c3112f9640b28c0b`  
		Last Modified: Wed, 28 Jan 2026 22:14:00 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c852e6fd6ca689f343ecd9556696c9a055807db926532774b7ce980b99660208`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5417dc65ba4347a7a9f71250e80e8ab02850cf1891191788a8d3a6bd7fd102`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 6.2 MB (6172820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cda71723ca490ed94103a8ffaf9a018564afb567a1cd11bdb88ffe6739ba29`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f3eb4051e12d7643406a550c0b9ae9aec223ca08500761dad291be8a676e17`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f75bb8cb9075b2637ebc1e4fece5007fdd969d063877f4379b2fa2122a933c`  
		Last Modified: Wed, 28 Jan 2026 22:14:04 GMT  
		Size: 49.9 MB (49921194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85492c82cc5e83a101deac2585097ae10941432849cacd0e85612f89f005a746`  
		Last Modified: Wed, 28 Jan 2026 22:14:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c48ae948a50c8a66f2e0d1671683d43038e454ad971b80d6c897120b5fc53e`  
		Last Modified: Wed, 28 Jan 2026 22:14:06 GMT  
		Size: 128.1 MB (128101341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a46d9073fa47ff8bfe8d4dba9438d9bdcc204905a9476c61b53a836cf4b538c`  
		Last Modified: Wed, 28 Jan 2026 22:14:03 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496c3bd4b1509fc6c4c59fe31ed2a8ae93ebf144188eb997989dedb85772a8c4`  
		Last Modified: Wed, 28 Jan 2026 22:14:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6d8facabe1744878461496ccfedc82f577c37d2d2d40cfaaf37091897c16ffc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcced7a5130d8700fe05151d79f8786f72a78298e6703646d8090c8078617af`

```dockerfile
```

-	Layers:
	-	`sha256:11db86e8e763cff65b4b51a32856f1cf15b44bf9806cced161ca911fd8e638e6`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 15.0 MB (14957489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd069fba1e52cef3eb858bf86615571052ce5254c2ea0ffd8bbbb239d53ae64b`  
		Last Modified: Wed, 28 Jan 2026 22:14:00 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bd5aa59105ea8c2f2a1d29be9f495e7804d7f4f6ef0514c6a0a5986bef524591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227901504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b5f19aa0c60edc52a62857a800bb649a049910324e552c9d68a34c42e27dc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:53 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:12:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 22:12:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450daa4e0f5ea96d16aa389a8e87426a9214ab0f71182b7803908dcca98a5209`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1724ce9d93488b72bca491622c74d25eb8ac6509f2b162df09de51ea638d66`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 737.5 KB (737521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d00b1e5474cb62a592b7175ac90c0112ff6b00baecfe975562a86f6700b478`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 5.8 MB (5792045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2166d6728093b8d49f9e466e247b361c27598c8ff03217028c748cb55628b30f`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585b27da4caa49eae873de2c47465c7417c0a211d48a37035499aa4dcb96f8f0`  
		Last Modified: Wed, 28 Jan 2026 22:13:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0197c3019186bd4e5cf971458359bbf6714eb0569d9218b47da645ef7ca325cf`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 48.8 MB (48775828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2cc4c99fca6f8f458876393d8464b0399bd60c88a67bddc6b2ca1a5329aa01`  
		Last Modified: Wed, 28 Jan 2026 22:13:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9825076cf2cb6def3e2047e534f69c9c67c6df732b4d944df1046de2068e5d`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 126.7 MB (126683295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e4a9a975ca1f3e336e6943ef6c033b230f4ae9e08b954d835007e0055a1651`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb92b3cef2d2aa649d1b6de58251b791173d3d04630e53f37ba4773c032db7c`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:67afce0904ef71f1cb18d81caf27f0688fc409eb40c79a00e5cb853efc1b9c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d5ba34f9151a6ec11a847750e441e5725a7f9e716660fbfb805f08bd359127`

```dockerfile
```

-	Layers:
	-	`sha256:609ef88e20510e9c30596b1934e89afe72d822012891409310fe59fef8ca767f`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 15.0 MB (14955837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d3ad32f16baf32289de86d7d6826f4b35670e14220600d45947afe7b8e469ef`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 35.2 KB (35158 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45`

```console
$ docker pull mysql@sha256:68bee0989e5623da84778fe2e20d38a0b2432e46645cf8e4667b9ea15e8ee373
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45` - linux; amd64

```console
$ docker pull mysql@sha256:3ad50ea218eeca078cbaaf012932984ebd0a65aa67c65884f2e3e0ce672b5285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232301209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73678e5bb5566a44426e48a76165e8655f31c5e7a21468360859fbc842bf3819`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:11:59 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:11:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:12:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:12:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:12:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 28 Jan 2026 22:12:25 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:12:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:12:54 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:12:54 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:12:54 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:13:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:13:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 22:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:13:30 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:13:30 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66262e8c98ce4c2bfbd6f85a9a924ff94cd6b78d5ed82423c3112f9640b28c0b`  
		Last Modified: Wed, 28 Jan 2026 22:14:00 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c852e6fd6ca689f343ecd9556696c9a055807db926532774b7ce980b99660208`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5417dc65ba4347a7a9f71250e80e8ab02850cf1891191788a8d3a6bd7fd102`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 6.2 MB (6172820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cda71723ca490ed94103a8ffaf9a018564afb567a1cd11bdb88ffe6739ba29`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f3eb4051e12d7643406a550c0b9ae9aec223ca08500761dad291be8a676e17`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f75bb8cb9075b2637ebc1e4fece5007fdd969d063877f4379b2fa2122a933c`  
		Last Modified: Wed, 28 Jan 2026 22:14:04 GMT  
		Size: 49.9 MB (49921194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85492c82cc5e83a101deac2585097ae10941432849cacd0e85612f89f005a746`  
		Last Modified: Wed, 28 Jan 2026 22:14:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c48ae948a50c8a66f2e0d1671683d43038e454ad971b80d6c897120b5fc53e`  
		Last Modified: Wed, 28 Jan 2026 22:14:06 GMT  
		Size: 128.1 MB (128101341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a46d9073fa47ff8bfe8d4dba9438d9bdcc204905a9476c61b53a836cf4b538c`  
		Last Modified: Wed, 28 Jan 2026 22:14:03 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496c3bd4b1509fc6c4c59fe31ed2a8ae93ebf144188eb997989dedb85772a8c4`  
		Last Modified: Wed, 28 Jan 2026 22:14:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45` - unknown; unknown

```console
$ docker pull mysql@sha256:6d8facabe1744878461496ccfedc82f577c37d2d2d40cfaaf37091897c16ffc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcced7a5130d8700fe05151d79f8786f72a78298e6703646d8090c8078617af`

```dockerfile
```

-	Layers:
	-	`sha256:11db86e8e763cff65b4b51a32856f1cf15b44bf9806cced161ca911fd8e638e6`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 15.0 MB (14957489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd069fba1e52cef3eb858bf86615571052ce5254c2ea0ffd8bbbb239d53ae64b`  
		Last Modified: Wed, 28 Jan 2026 22:14:00 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bd5aa59105ea8c2f2a1d29be9f495e7804d7f4f6ef0514c6a0a5986bef524591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227901504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b5f19aa0c60edc52a62857a800bb649a049910324e552c9d68a34c42e27dc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:53 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:12:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 22:12:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450daa4e0f5ea96d16aa389a8e87426a9214ab0f71182b7803908dcca98a5209`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1724ce9d93488b72bca491622c74d25eb8ac6509f2b162df09de51ea638d66`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 737.5 KB (737521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d00b1e5474cb62a592b7175ac90c0112ff6b00baecfe975562a86f6700b478`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 5.8 MB (5792045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2166d6728093b8d49f9e466e247b361c27598c8ff03217028c748cb55628b30f`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585b27da4caa49eae873de2c47465c7417c0a211d48a37035499aa4dcb96f8f0`  
		Last Modified: Wed, 28 Jan 2026 22:13:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0197c3019186bd4e5cf971458359bbf6714eb0569d9218b47da645ef7ca325cf`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 48.8 MB (48775828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2cc4c99fca6f8f458876393d8464b0399bd60c88a67bddc6b2ca1a5329aa01`  
		Last Modified: Wed, 28 Jan 2026 22:13:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9825076cf2cb6def3e2047e534f69c9c67c6df732b4d944df1046de2068e5d`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 126.7 MB (126683295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e4a9a975ca1f3e336e6943ef6c033b230f4ae9e08b954d835007e0055a1651`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb92b3cef2d2aa649d1b6de58251b791173d3d04630e53f37ba4773c032db7c`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45` - unknown; unknown

```console
$ docker pull mysql@sha256:67afce0904ef71f1cb18d81caf27f0688fc409eb40c79a00e5cb853efc1b9c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d5ba34f9151a6ec11a847750e441e5725a7f9e716660fbfb805f08bd359127`

```dockerfile
```

-	Layers:
	-	`sha256:609ef88e20510e9c30596b1934e89afe72d822012891409310fe59fef8ca767f`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 15.0 MB (14955837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d3ad32f16baf32289de86d7d6826f4b35670e14220600d45947afe7b8e469ef`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 35.2 KB (35158 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-bookworm`

```console
$ docker pull mysql@sha256:5284868db9fd4c480d37e8394fb37316ba29b1bdbec31185676faaf42cd82612
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.45-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:dee7500826371f0383c6673ab1fc4cece140d7f8fb365550597548549b253dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183455449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb471428bdc168577f9e02a48169eda26499d392561b1978b431aa483d45e642`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 21 Jan 2026 22:49:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 21 Jan 2026 22:49:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:49:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Jan 2026 22:49:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Wed, 21 Jan 2026 22:49:25 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:36 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa36b2e2c985c829bdf403d8168eeae8890c3217a30563a2b5b3aa68e1efdba`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d1348177f9534b0b93188d0bd2781bf8088988b503664ef3329e9462ec5e6d`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 4.4 MB (4423336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106cdb304c5842e0232ae8ce1fcf6877cff36e384ba2d8ecc68dd0b670d04f34`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 1.2 MB (1248714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f855ce4e64c494fdd0390394941885efc48adffab2266c04a67f71c80b55fce`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb9b517325f53660036f1de6ca0e9494dbc84aafe02d886a34f2bd505a0d80c`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 15.3 MB (15295819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94beb5f31bf6179d42df34e5693e2f2e1e7b3efe8ab3be7410347bd25082c2c`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab60d99d7fa5f30783088438eb8f263f39c3c315a7da872044328dd07ca2a26`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c09fbe4bbb7dde90633da807e1f347b7caf14883cab671790a4369c31ded78f`  
		Last Modified: Wed, 21 Jan 2026 22:50:01 GMT  
		Size: 134.2 MB (134248192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ed9baa1e80f6b50800638f3cdc195044965a20d046ae3565fdfb32a2f8eb6b`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c36bcd4939de82e2db98188dc2dd518dbda890712040edb19e8befbbe028557`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29984f882141106a3f505fd1ee0d8afaf76a58bf3e0e8f6d953f5bee612777fa`  
		Last Modified: Wed, 21 Jan 2026 22:50:00 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:a7eddc6833b1dad7a3743fa776da9e6c8604dd9b860673e99b88d15d65e4693a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c526e7816588d61af24be57343f0050e43cdbbad362b3b6ba103554894ebe19b`

```dockerfile
```

-	Layers:
	-	`sha256:cade0013c36201ab6c42ec4b5f213e754609b2f3fe9fc19478d78770c9747810`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b99cd63676959f0fe9ca9cd457e9c74b4e5e604d39c4d8bca1ba174822cf3c7`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-debian`

```console
$ docker pull mysql@sha256:5284868db9fd4c480d37e8394fb37316ba29b1bdbec31185676faaf42cd82612
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.45-debian` - linux; amd64

```console
$ docker pull mysql@sha256:dee7500826371f0383c6673ab1fc4cece140d7f8fb365550597548549b253dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183455449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb471428bdc168577f9e02a48169eda26499d392561b1978b431aa483d45e642`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 21 Jan 2026 22:49:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 21 Jan 2026 22:49:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:49:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Jan 2026 22:49:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Wed, 21 Jan 2026 22:49:25 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:36 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa36b2e2c985c829bdf403d8168eeae8890c3217a30563a2b5b3aa68e1efdba`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d1348177f9534b0b93188d0bd2781bf8088988b503664ef3329e9462ec5e6d`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 4.4 MB (4423336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106cdb304c5842e0232ae8ce1fcf6877cff36e384ba2d8ecc68dd0b670d04f34`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 1.2 MB (1248714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f855ce4e64c494fdd0390394941885efc48adffab2266c04a67f71c80b55fce`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb9b517325f53660036f1de6ca0e9494dbc84aafe02d886a34f2bd505a0d80c`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 15.3 MB (15295819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94beb5f31bf6179d42df34e5693e2f2e1e7b3efe8ab3be7410347bd25082c2c`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab60d99d7fa5f30783088438eb8f263f39c3c315a7da872044328dd07ca2a26`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c09fbe4bbb7dde90633da807e1f347b7caf14883cab671790a4369c31ded78f`  
		Last Modified: Wed, 21 Jan 2026 22:50:01 GMT  
		Size: 134.2 MB (134248192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ed9baa1e80f6b50800638f3cdc195044965a20d046ae3565fdfb32a2f8eb6b`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c36bcd4939de82e2db98188dc2dd518dbda890712040edb19e8befbbe028557`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29984f882141106a3f505fd1ee0d8afaf76a58bf3e0e8f6d953f5bee612777fa`  
		Last Modified: Wed, 21 Jan 2026 22:50:00 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:a7eddc6833b1dad7a3743fa776da9e6c8604dd9b860673e99b88d15d65e4693a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c526e7816588d61af24be57343f0050e43cdbbad362b3b6ba103554894ebe19b`

```dockerfile
```

-	Layers:
	-	`sha256:cade0013c36201ab6c42ec4b5f213e754609b2f3fe9fc19478d78770c9747810`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b99cd63676959f0fe9ca9cd457e9c74b4e5e604d39c4d8bca1ba174822cf3c7`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-oracle`

```console
$ docker pull mysql@sha256:68bee0989e5623da84778fe2e20d38a0b2432e46645cf8e4667b9ea15e8ee373
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:3ad50ea218eeca078cbaaf012932984ebd0a65aa67c65884f2e3e0ce672b5285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232301209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73678e5bb5566a44426e48a76165e8655f31c5e7a21468360859fbc842bf3819`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:11:59 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:11:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:12:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:12:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:12:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 28 Jan 2026 22:12:25 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:12:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:12:54 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:12:54 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:12:54 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:13:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:13:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 22:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:13:30 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:13:30 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66262e8c98ce4c2bfbd6f85a9a924ff94cd6b78d5ed82423c3112f9640b28c0b`  
		Last Modified: Wed, 28 Jan 2026 22:14:00 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c852e6fd6ca689f343ecd9556696c9a055807db926532774b7ce980b99660208`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5417dc65ba4347a7a9f71250e80e8ab02850cf1891191788a8d3a6bd7fd102`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 6.2 MB (6172820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cda71723ca490ed94103a8ffaf9a018564afb567a1cd11bdb88ffe6739ba29`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f3eb4051e12d7643406a550c0b9ae9aec223ca08500761dad291be8a676e17`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f75bb8cb9075b2637ebc1e4fece5007fdd969d063877f4379b2fa2122a933c`  
		Last Modified: Wed, 28 Jan 2026 22:14:04 GMT  
		Size: 49.9 MB (49921194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85492c82cc5e83a101deac2585097ae10941432849cacd0e85612f89f005a746`  
		Last Modified: Wed, 28 Jan 2026 22:14:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c48ae948a50c8a66f2e0d1671683d43038e454ad971b80d6c897120b5fc53e`  
		Last Modified: Wed, 28 Jan 2026 22:14:06 GMT  
		Size: 128.1 MB (128101341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a46d9073fa47ff8bfe8d4dba9438d9bdcc204905a9476c61b53a836cf4b538c`  
		Last Modified: Wed, 28 Jan 2026 22:14:03 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496c3bd4b1509fc6c4c59fe31ed2a8ae93ebf144188eb997989dedb85772a8c4`  
		Last Modified: Wed, 28 Jan 2026 22:14:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6d8facabe1744878461496ccfedc82f577c37d2d2d40cfaaf37091897c16ffc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcced7a5130d8700fe05151d79f8786f72a78298e6703646d8090c8078617af`

```dockerfile
```

-	Layers:
	-	`sha256:11db86e8e763cff65b4b51a32856f1cf15b44bf9806cced161ca911fd8e638e6`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 15.0 MB (14957489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd069fba1e52cef3eb858bf86615571052ce5254c2ea0ffd8bbbb239d53ae64b`  
		Last Modified: Wed, 28 Jan 2026 22:14:00 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bd5aa59105ea8c2f2a1d29be9f495e7804d7f4f6ef0514c6a0a5986bef524591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227901504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b5f19aa0c60edc52a62857a800bb649a049910324e552c9d68a34c42e27dc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:53 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:12:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 22:12:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450daa4e0f5ea96d16aa389a8e87426a9214ab0f71182b7803908dcca98a5209`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1724ce9d93488b72bca491622c74d25eb8ac6509f2b162df09de51ea638d66`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 737.5 KB (737521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d00b1e5474cb62a592b7175ac90c0112ff6b00baecfe975562a86f6700b478`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 5.8 MB (5792045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2166d6728093b8d49f9e466e247b361c27598c8ff03217028c748cb55628b30f`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585b27da4caa49eae873de2c47465c7417c0a211d48a37035499aa4dcb96f8f0`  
		Last Modified: Wed, 28 Jan 2026 22:13:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0197c3019186bd4e5cf971458359bbf6714eb0569d9218b47da645ef7ca325cf`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 48.8 MB (48775828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2cc4c99fca6f8f458876393d8464b0399bd60c88a67bddc6b2ca1a5329aa01`  
		Last Modified: Wed, 28 Jan 2026 22:13:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9825076cf2cb6def3e2047e534f69c9c67c6df732b4d944df1046de2068e5d`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 126.7 MB (126683295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e4a9a975ca1f3e336e6943ef6c033b230f4ae9e08b954d835007e0055a1651`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb92b3cef2d2aa649d1b6de58251b791173d3d04630e53f37ba4773c032db7c`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:67afce0904ef71f1cb18d81caf27f0688fc409eb40c79a00e5cb853efc1b9c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d5ba34f9151a6ec11a847750e441e5725a7f9e716660fbfb805f08bd359127`

```dockerfile
```

-	Layers:
	-	`sha256:609ef88e20510e9c30596b1934e89afe72d822012891409310fe59fef8ca767f`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 15.0 MB (14955837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d3ad32f16baf32289de86d7d6826f4b35670e14220600d45947afe7b8e469ef`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 35.2 KB (35158 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-oraclelinux9`

```console
$ docker pull mysql@sha256:68bee0989e5623da84778fe2e20d38a0b2432e46645cf8e4667b9ea15e8ee373
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:3ad50ea218eeca078cbaaf012932984ebd0a65aa67c65884f2e3e0ce672b5285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232301209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73678e5bb5566a44426e48a76165e8655f31c5e7a21468360859fbc842bf3819`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:11:59 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:11:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:12:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:12:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:12:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 28 Jan 2026 22:12:25 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:12:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:12:54 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:12:54 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:12:54 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:13:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:13:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 22:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:13:30 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:13:30 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66262e8c98ce4c2bfbd6f85a9a924ff94cd6b78d5ed82423c3112f9640b28c0b`  
		Last Modified: Wed, 28 Jan 2026 22:14:00 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c852e6fd6ca689f343ecd9556696c9a055807db926532774b7ce980b99660208`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5417dc65ba4347a7a9f71250e80e8ab02850cf1891191788a8d3a6bd7fd102`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 6.2 MB (6172820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cda71723ca490ed94103a8ffaf9a018564afb567a1cd11bdb88ffe6739ba29`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f3eb4051e12d7643406a550c0b9ae9aec223ca08500761dad291be8a676e17`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f75bb8cb9075b2637ebc1e4fece5007fdd969d063877f4379b2fa2122a933c`  
		Last Modified: Wed, 28 Jan 2026 22:14:04 GMT  
		Size: 49.9 MB (49921194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85492c82cc5e83a101deac2585097ae10941432849cacd0e85612f89f005a746`  
		Last Modified: Wed, 28 Jan 2026 22:14:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c48ae948a50c8a66f2e0d1671683d43038e454ad971b80d6c897120b5fc53e`  
		Last Modified: Wed, 28 Jan 2026 22:14:06 GMT  
		Size: 128.1 MB (128101341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a46d9073fa47ff8bfe8d4dba9438d9bdcc204905a9476c61b53a836cf4b538c`  
		Last Modified: Wed, 28 Jan 2026 22:14:03 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496c3bd4b1509fc6c4c59fe31ed2a8ae93ebf144188eb997989dedb85772a8c4`  
		Last Modified: Wed, 28 Jan 2026 22:14:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6d8facabe1744878461496ccfedc82f577c37d2d2d40cfaaf37091897c16ffc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcced7a5130d8700fe05151d79f8786f72a78298e6703646d8090c8078617af`

```dockerfile
```

-	Layers:
	-	`sha256:11db86e8e763cff65b4b51a32856f1cf15b44bf9806cced161ca911fd8e638e6`  
		Last Modified: Wed, 28 Jan 2026 22:14:01 GMT  
		Size: 15.0 MB (14957489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd069fba1e52cef3eb858bf86615571052ce5254c2ea0ffd8bbbb239d53ae64b`  
		Last Modified: Wed, 28 Jan 2026 22:14:00 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bd5aa59105ea8c2f2a1d29be9f495e7804d7f4f6ef0514c6a0a5986bef524591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227901504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b5f19aa0c60edc52a62857a800bb649a049910324e552c9d68a34c42e27dc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:53 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Wed, 28 Jan 2026 22:12:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 22:12:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450daa4e0f5ea96d16aa389a8e87426a9214ab0f71182b7803908dcca98a5209`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1724ce9d93488b72bca491622c74d25eb8ac6509f2b162df09de51ea638d66`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 737.5 KB (737521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d00b1e5474cb62a592b7175ac90c0112ff6b00baecfe975562a86f6700b478`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 5.8 MB (5792045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2166d6728093b8d49f9e466e247b361c27598c8ff03217028c748cb55628b30f`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585b27da4caa49eae873de2c47465c7417c0a211d48a37035499aa4dcb96f8f0`  
		Last Modified: Wed, 28 Jan 2026 22:13:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0197c3019186bd4e5cf971458359bbf6714eb0569d9218b47da645ef7ca325cf`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 48.8 MB (48775828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2cc4c99fca6f8f458876393d8464b0399bd60c88a67bddc6b2ca1a5329aa01`  
		Last Modified: Wed, 28 Jan 2026 22:13:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9825076cf2cb6def3e2047e534f69c9c67c6df732b4d944df1046de2068e5d`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 126.7 MB (126683295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e4a9a975ca1f3e336e6943ef6c033b230f4ae9e08b954d835007e0055a1651`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb92b3cef2d2aa649d1b6de58251b791173d3d04630e53f37ba4773c032db7c`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:67afce0904ef71f1cb18d81caf27f0688fc409eb40c79a00e5cb853efc1b9c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d5ba34f9151a6ec11a847750e441e5725a7f9e716660fbfb805f08bd359127`

```dockerfile
```

-	Layers:
	-	`sha256:609ef88e20510e9c30596b1934e89afe72d822012891409310fe59fef8ca767f`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 15.0 MB (14955837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d3ad32f16baf32289de86d7d6826f4b35670e14220600d45947afe7b8e469ef`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 35.2 KB (35158 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:f1c7674d8dd3c94f439b0d607792187d55bd861f94e8c6d683b959b577152bdc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:8b3be4876b08746f2caa509afae13bac0aca1885ce967d1bb5ca0d177000f3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233227949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4511f663fb18c6cde7e5d9bdaafeed8c1c7019732b77279315145eb430e85dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:11:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:11:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:39 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:39 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad075f4936cf8a36f21e937e90b1d698baa6b0e625d13c69beef2586416bd2b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2ec557f75a04fa223e3c0bd71f6cc48ecc59f12a6c5e31a4ed48df3205387b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c1d58a53d79eac5a138b2337dda522a36661053c302535c365fc5f64af2ad`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 6.2 MB (6172774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c60e0e578e332d62e541d2460840ae181c04522af7b87a815b50532a0cd0b9`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0125f072a0a55ba4ae0188f2dcd165d077cf20a27ed19e114cb325eb5256a1cc`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c356f1b5fd3fb93d5570a71077cff86a0af06026ef7a77b257d5d83f73166d16`  
		Last Modified: Wed, 28 Jan 2026 22:13:12 GMT  
		Size: 47.8 MB (47810258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cb4bc116b0506e2ea4ab9fa6bc54cc451e350fa3274fa025479c731cbaad6d`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce6e8837913ee62730f9a78f444b9a4cdb9f29bd6e248340731f67a1c261849`  
		Last Modified: Wed, 28 Jan 2026 22:13:14 GMT  
		Size: 131.1 MB (131139180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885e95c29fdf0877c6ec82ac693521e9735cf0c19a64d0d6d950afeb84929b31`  
		Last Modified: Wed, 28 Jan 2026 22:13:11 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:798a0bad5920617757611d4a42a351558a280acbec05ebd5596f7aa5f9b00d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7698ea2fc5e9501ff603ff4bd1d0a97505093033193881b8e631982bb6483280`

```dockerfile
```

-	Layers:
	-	`sha256:c823f2fc76110ec949a1d955075948f84148e5766bc8d9751774c7fd1ddf24b5`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c856894eeb424a1604d601f5379bd90c5520e1e86430ff879bc9a4b675c5678`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e51f27439b7a2119f9322da62672bf29db9733dfe5efda7fe14a95b1978b77f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228695273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a187cad11f0bae46349c98546b174514318cd9934ece1aaf891d8bb165f437`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:45 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:47 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:23 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b8014f3539c98ae4d9db79063d0ac6da20c561da597e5080428d7fa2a81045`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581c2da28c304c8a55c89ffc142dfe9b49523660a41d23868aabdb3746f9b14e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311e3508c6b08056182bbc122c5da5bf25d876d8f0bd1eb0921f401aa6e4e794`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 5.8 MB (5792078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dac3a350ad94d3b3ff38d83b364f9dfeb47f767e8586aacb3733b7ba672656`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbefc80b7213ccab583b4d0250ca47d5a5ffbfcc700eb995807fb9e9c824552`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6900ac85f3c3185bf951b4c2ff044719ab72a728e44d91c4aeed766ee05b847d`  
		Last Modified: Wed, 28 Jan 2026 22:12:56 GMT  
		Size: 46.7 MB (46700971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc870ee9e6c819f59ecc85a2e7df376e613358eb45f4a14ebe822cf57fe76a26`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f95bece7002a8fd4dd526ef950d925ffb02f0937885175169806d3ec1ab8e1`  
		Last Modified: Wed, 28 Jan 2026 22:12:58 GMT  
		Size: 129.6 MB (129551997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923168c7bf209bd6189f93d4cb04d2c82f17faf0ae36433ab67dd1e72ec3ca29`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:ae951e3a0f700ccaab54d8aa559d60b9d07b96bd8f3121b6ed86971368f04b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282b71728f5dbf3f9d4b34689d6b80dc2aa9c48da7c3fe42eada863a8d347d0`

```dockerfile
```

-	Layers:
	-	`sha256:d66e901a34db0d11a63eea540fdacb6235f7c53a2a0b8b51cf5d898c1c80b2f7`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf852e8614823f7b667b3de07ca7069909c56a682daa323b1433a790564d9d2e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:f1c7674d8dd3c94f439b0d607792187d55bd861f94e8c6d683b959b577152bdc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8b3be4876b08746f2caa509afae13bac0aca1885ce967d1bb5ca0d177000f3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233227949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4511f663fb18c6cde7e5d9bdaafeed8c1c7019732b77279315145eb430e85dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:11:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:11:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:39 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:39 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad075f4936cf8a36f21e937e90b1d698baa6b0e625d13c69beef2586416bd2b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2ec557f75a04fa223e3c0bd71f6cc48ecc59f12a6c5e31a4ed48df3205387b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c1d58a53d79eac5a138b2337dda522a36661053c302535c365fc5f64af2ad`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 6.2 MB (6172774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c60e0e578e332d62e541d2460840ae181c04522af7b87a815b50532a0cd0b9`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0125f072a0a55ba4ae0188f2dcd165d077cf20a27ed19e114cb325eb5256a1cc`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c356f1b5fd3fb93d5570a71077cff86a0af06026ef7a77b257d5d83f73166d16`  
		Last Modified: Wed, 28 Jan 2026 22:13:12 GMT  
		Size: 47.8 MB (47810258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cb4bc116b0506e2ea4ab9fa6bc54cc451e350fa3274fa025479c731cbaad6d`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce6e8837913ee62730f9a78f444b9a4cdb9f29bd6e248340731f67a1c261849`  
		Last Modified: Wed, 28 Jan 2026 22:13:14 GMT  
		Size: 131.1 MB (131139180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885e95c29fdf0877c6ec82ac693521e9735cf0c19a64d0d6d950afeb84929b31`  
		Last Modified: Wed, 28 Jan 2026 22:13:11 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:798a0bad5920617757611d4a42a351558a280acbec05ebd5596f7aa5f9b00d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7698ea2fc5e9501ff603ff4bd1d0a97505093033193881b8e631982bb6483280`

```dockerfile
```

-	Layers:
	-	`sha256:c823f2fc76110ec949a1d955075948f84148e5766bc8d9751774c7fd1ddf24b5`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c856894eeb424a1604d601f5379bd90c5520e1e86430ff879bc9a4b675c5678`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e51f27439b7a2119f9322da62672bf29db9733dfe5efda7fe14a95b1978b77f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228695273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a187cad11f0bae46349c98546b174514318cd9934ece1aaf891d8bb165f437`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:45 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:47 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:23 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b8014f3539c98ae4d9db79063d0ac6da20c561da597e5080428d7fa2a81045`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581c2da28c304c8a55c89ffc142dfe9b49523660a41d23868aabdb3746f9b14e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311e3508c6b08056182bbc122c5da5bf25d876d8f0bd1eb0921f401aa6e4e794`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 5.8 MB (5792078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dac3a350ad94d3b3ff38d83b364f9dfeb47f767e8586aacb3733b7ba672656`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbefc80b7213ccab583b4d0250ca47d5a5ffbfcc700eb995807fb9e9c824552`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6900ac85f3c3185bf951b4c2ff044719ab72a728e44d91c4aeed766ee05b847d`  
		Last Modified: Wed, 28 Jan 2026 22:12:56 GMT  
		Size: 46.7 MB (46700971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc870ee9e6c819f59ecc85a2e7df376e613358eb45f4a14ebe822cf57fe76a26`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f95bece7002a8fd4dd526ef950d925ffb02f0937885175169806d3ec1ab8e1`  
		Last Modified: Wed, 28 Jan 2026 22:12:58 GMT  
		Size: 129.6 MB (129551997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923168c7bf209bd6189f93d4cb04d2c82f17faf0ae36433ab67dd1e72ec3ca29`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ae951e3a0f700ccaab54d8aa559d60b9d07b96bd8f3121b6ed86971368f04b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282b71728f5dbf3f9d4b34689d6b80dc2aa9c48da7c3fe42eada863a8d347d0`

```dockerfile
```

-	Layers:
	-	`sha256:d66e901a34db0d11a63eea540fdacb6235f7c53a2a0b8b51cf5d898c1c80b2f7`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf852e8614823f7b667b3de07ca7069909c56a682daa323b1433a790564d9d2e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:f1c7674d8dd3c94f439b0d607792187d55bd861f94e8c6d683b959b577152bdc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:8b3be4876b08746f2caa509afae13bac0aca1885ce967d1bb5ca0d177000f3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233227949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4511f663fb18c6cde7e5d9bdaafeed8c1c7019732b77279315145eb430e85dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:11:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:11:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:39 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:39 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad075f4936cf8a36f21e937e90b1d698baa6b0e625d13c69beef2586416bd2b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2ec557f75a04fa223e3c0bd71f6cc48ecc59f12a6c5e31a4ed48df3205387b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c1d58a53d79eac5a138b2337dda522a36661053c302535c365fc5f64af2ad`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 6.2 MB (6172774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c60e0e578e332d62e541d2460840ae181c04522af7b87a815b50532a0cd0b9`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0125f072a0a55ba4ae0188f2dcd165d077cf20a27ed19e114cb325eb5256a1cc`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c356f1b5fd3fb93d5570a71077cff86a0af06026ef7a77b257d5d83f73166d16`  
		Last Modified: Wed, 28 Jan 2026 22:13:12 GMT  
		Size: 47.8 MB (47810258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cb4bc116b0506e2ea4ab9fa6bc54cc451e350fa3274fa025479c731cbaad6d`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce6e8837913ee62730f9a78f444b9a4cdb9f29bd6e248340731f67a1c261849`  
		Last Modified: Wed, 28 Jan 2026 22:13:14 GMT  
		Size: 131.1 MB (131139180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885e95c29fdf0877c6ec82ac693521e9735cf0c19a64d0d6d950afeb84929b31`  
		Last Modified: Wed, 28 Jan 2026 22:13:11 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:798a0bad5920617757611d4a42a351558a280acbec05ebd5596f7aa5f9b00d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7698ea2fc5e9501ff603ff4bd1d0a97505093033193881b8e631982bb6483280`

```dockerfile
```

-	Layers:
	-	`sha256:c823f2fc76110ec949a1d955075948f84148e5766bc8d9751774c7fd1ddf24b5`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c856894eeb424a1604d601f5379bd90c5520e1e86430ff879bc9a4b675c5678`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e51f27439b7a2119f9322da62672bf29db9733dfe5efda7fe14a95b1978b77f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228695273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a187cad11f0bae46349c98546b174514318cd9934ece1aaf891d8bb165f437`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:45 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:47 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:23 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b8014f3539c98ae4d9db79063d0ac6da20c561da597e5080428d7fa2a81045`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581c2da28c304c8a55c89ffc142dfe9b49523660a41d23868aabdb3746f9b14e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311e3508c6b08056182bbc122c5da5bf25d876d8f0bd1eb0921f401aa6e4e794`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 5.8 MB (5792078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dac3a350ad94d3b3ff38d83b364f9dfeb47f767e8586aacb3733b7ba672656`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbefc80b7213ccab583b4d0250ca47d5a5ffbfcc700eb995807fb9e9c824552`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6900ac85f3c3185bf951b4c2ff044719ab72a728e44d91c4aeed766ee05b847d`  
		Last Modified: Wed, 28 Jan 2026 22:12:56 GMT  
		Size: 46.7 MB (46700971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc870ee9e6c819f59ecc85a2e7df376e613358eb45f4a14ebe822cf57fe76a26`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f95bece7002a8fd4dd526ef950d925ffb02f0937885175169806d3ec1ab8e1`  
		Last Modified: Wed, 28 Jan 2026 22:12:58 GMT  
		Size: 129.6 MB (129551997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923168c7bf209bd6189f93d4cb04d2c82f17faf0ae36433ab67dd1e72ec3ca29`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ae951e3a0f700ccaab54d8aa559d60b9d07b96bd8f3121b6ed86971368f04b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282b71728f5dbf3f9d4b34689d6b80dc2aa9c48da7c3fe42eada863a8d347d0`

```dockerfile
```

-	Layers:
	-	`sha256:d66e901a34db0d11a63eea540fdacb6235f7c53a2a0b8b51cf5d898c1c80b2f7`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf852e8614823f7b667b3de07ca7069909c56a682daa323b1433a790564d9d2e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8`

```console
$ docker pull mysql@sha256:f1c7674d8dd3c94f439b0d607792187d55bd861f94e8c6d683b959b577152bdc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8` - linux; amd64

```console
$ docker pull mysql@sha256:8b3be4876b08746f2caa509afae13bac0aca1885ce967d1bb5ca0d177000f3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233227949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4511f663fb18c6cde7e5d9bdaafeed8c1c7019732b77279315145eb430e85dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:11:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:11:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:39 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:39 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad075f4936cf8a36f21e937e90b1d698baa6b0e625d13c69beef2586416bd2b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2ec557f75a04fa223e3c0bd71f6cc48ecc59f12a6c5e31a4ed48df3205387b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c1d58a53d79eac5a138b2337dda522a36661053c302535c365fc5f64af2ad`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 6.2 MB (6172774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c60e0e578e332d62e541d2460840ae181c04522af7b87a815b50532a0cd0b9`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0125f072a0a55ba4ae0188f2dcd165d077cf20a27ed19e114cb325eb5256a1cc`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c356f1b5fd3fb93d5570a71077cff86a0af06026ef7a77b257d5d83f73166d16`  
		Last Modified: Wed, 28 Jan 2026 22:13:12 GMT  
		Size: 47.8 MB (47810258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cb4bc116b0506e2ea4ab9fa6bc54cc451e350fa3274fa025479c731cbaad6d`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce6e8837913ee62730f9a78f444b9a4cdb9f29bd6e248340731f67a1c261849`  
		Last Modified: Wed, 28 Jan 2026 22:13:14 GMT  
		Size: 131.1 MB (131139180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885e95c29fdf0877c6ec82ac693521e9735cf0c19a64d0d6d950afeb84929b31`  
		Last Modified: Wed, 28 Jan 2026 22:13:11 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8` - unknown; unknown

```console
$ docker pull mysql@sha256:798a0bad5920617757611d4a42a351558a280acbec05ebd5596f7aa5f9b00d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7698ea2fc5e9501ff603ff4bd1d0a97505093033193881b8e631982bb6483280`

```dockerfile
```

-	Layers:
	-	`sha256:c823f2fc76110ec949a1d955075948f84148e5766bc8d9751774c7fd1ddf24b5`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c856894eeb424a1604d601f5379bd90c5520e1e86430ff879bc9a4b675c5678`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e51f27439b7a2119f9322da62672bf29db9733dfe5efda7fe14a95b1978b77f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228695273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a187cad11f0bae46349c98546b174514318cd9934ece1aaf891d8bb165f437`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:45 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:47 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:23 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b8014f3539c98ae4d9db79063d0ac6da20c561da597e5080428d7fa2a81045`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581c2da28c304c8a55c89ffc142dfe9b49523660a41d23868aabdb3746f9b14e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311e3508c6b08056182bbc122c5da5bf25d876d8f0bd1eb0921f401aa6e4e794`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 5.8 MB (5792078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dac3a350ad94d3b3ff38d83b364f9dfeb47f767e8586aacb3733b7ba672656`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbefc80b7213ccab583b4d0250ca47d5a5ffbfcc700eb995807fb9e9c824552`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6900ac85f3c3185bf951b4c2ff044719ab72a728e44d91c4aeed766ee05b847d`  
		Last Modified: Wed, 28 Jan 2026 22:12:56 GMT  
		Size: 46.7 MB (46700971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc870ee9e6c819f59ecc85a2e7df376e613358eb45f4a14ebe822cf57fe76a26`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f95bece7002a8fd4dd526ef950d925ffb02f0937885175169806d3ec1ab8e1`  
		Last Modified: Wed, 28 Jan 2026 22:12:58 GMT  
		Size: 129.6 MB (129551997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923168c7bf209bd6189f93d4cb04d2c82f17faf0ae36433ab67dd1e72ec3ca29`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8` - unknown; unknown

```console
$ docker pull mysql@sha256:ae951e3a0f700ccaab54d8aa559d60b9d07b96bd8f3121b6ed86971368f04b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282b71728f5dbf3f9d4b34689d6b80dc2aa9c48da7c3fe42eada863a8d347d0`

```dockerfile
```

-	Layers:
	-	`sha256:d66e901a34db0d11a63eea540fdacb6235f7c53a2a0b8b51cf5d898c1c80b2f7`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf852e8614823f7b667b3de07ca7069909c56a682daa323b1433a790564d9d2e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8-oracle`

```console
$ docker pull mysql@sha256:f1c7674d8dd3c94f439b0d607792187d55bd861f94e8c6d683b959b577152bdc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8b3be4876b08746f2caa509afae13bac0aca1885ce967d1bb5ca0d177000f3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233227949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4511f663fb18c6cde7e5d9bdaafeed8c1c7019732b77279315145eb430e85dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:11:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:11:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:39 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:39 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad075f4936cf8a36f21e937e90b1d698baa6b0e625d13c69beef2586416bd2b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2ec557f75a04fa223e3c0bd71f6cc48ecc59f12a6c5e31a4ed48df3205387b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c1d58a53d79eac5a138b2337dda522a36661053c302535c365fc5f64af2ad`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 6.2 MB (6172774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c60e0e578e332d62e541d2460840ae181c04522af7b87a815b50532a0cd0b9`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0125f072a0a55ba4ae0188f2dcd165d077cf20a27ed19e114cb325eb5256a1cc`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c356f1b5fd3fb93d5570a71077cff86a0af06026ef7a77b257d5d83f73166d16`  
		Last Modified: Wed, 28 Jan 2026 22:13:12 GMT  
		Size: 47.8 MB (47810258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cb4bc116b0506e2ea4ab9fa6bc54cc451e350fa3274fa025479c731cbaad6d`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce6e8837913ee62730f9a78f444b9a4cdb9f29bd6e248340731f67a1c261849`  
		Last Modified: Wed, 28 Jan 2026 22:13:14 GMT  
		Size: 131.1 MB (131139180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885e95c29fdf0877c6ec82ac693521e9735cf0c19a64d0d6d950afeb84929b31`  
		Last Modified: Wed, 28 Jan 2026 22:13:11 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:798a0bad5920617757611d4a42a351558a280acbec05ebd5596f7aa5f9b00d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7698ea2fc5e9501ff603ff4bd1d0a97505093033193881b8e631982bb6483280`

```dockerfile
```

-	Layers:
	-	`sha256:c823f2fc76110ec949a1d955075948f84148e5766bc8d9751774c7fd1ddf24b5`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c856894eeb424a1604d601f5379bd90c5520e1e86430ff879bc9a4b675c5678`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e51f27439b7a2119f9322da62672bf29db9733dfe5efda7fe14a95b1978b77f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228695273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a187cad11f0bae46349c98546b174514318cd9934ece1aaf891d8bb165f437`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:45 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:47 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:23 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b8014f3539c98ae4d9db79063d0ac6da20c561da597e5080428d7fa2a81045`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581c2da28c304c8a55c89ffc142dfe9b49523660a41d23868aabdb3746f9b14e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311e3508c6b08056182bbc122c5da5bf25d876d8f0bd1eb0921f401aa6e4e794`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 5.8 MB (5792078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dac3a350ad94d3b3ff38d83b364f9dfeb47f767e8586aacb3733b7ba672656`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbefc80b7213ccab583b4d0250ca47d5a5ffbfcc700eb995807fb9e9c824552`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6900ac85f3c3185bf951b4c2ff044719ab72a728e44d91c4aeed766ee05b847d`  
		Last Modified: Wed, 28 Jan 2026 22:12:56 GMT  
		Size: 46.7 MB (46700971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc870ee9e6c819f59ecc85a2e7df376e613358eb45f4a14ebe822cf57fe76a26`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f95bece7002a8fd4dd526ef950d925ffb02f0937885175169806d3ec1ab8e1`  
		Last Modified: Wed, 28 Jan 2026 22:12:58 GMT  
		Size: 129.6 MB (129551997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923168c7bf209bd6189f93d4cb04d2c82f17faf0ae36433ab67dd1e72ec3ca29`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ae951e3a0f700ccaab54d8aa559d60b9d07b96bd8f3121b6ed86971368f04b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282b71728f5dbf3f9d4b34689d6b80dc2aa9c48da7c3fe42eada863a8d347d0`

```dockerfile
```

-	Layers:
	-	`sha256:d66e901a34db0d11a63eea540fdacb6235f7c53a2a0b8b51cf5d898c1c80b2f7`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf852e8614823f7b667b3de07ca7069909c56a682daa323b1433a790564d9d2e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8-oraclelinux9`

```console
$ docker pull mysql@sha256:f1c7674d8dd3c94f439b0d607792187d55bd861f94e8c6d683b959b577152bdc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:8b3be4876b08746f2caa509afae13bac0aca1885ce967d1bb5ca0d177000f3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233227949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4511f663fb18c6cde7e5d9bdaafeed8c1c7019732b77279315145eb430e85dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:11:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:11:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:39 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:39 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad075f4936cf8a36f21e937e90b1d698baa6b0e625d13c69beef2586416bd2b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2ec557f75a04fa223e3c0bd71f6cc48ecc59f12a6c5e31a4ed48df3205387b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c1d58a53d79eac5a138b2337dda522a36661053c302535c365fc5f64af2ad`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 6.2 MB (6172774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c60e0e578e332d62e541d2460840ae181c04522af7b87a815b50532a0cd0b9`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0125f072a0a55ba4ae0188f2dcd165d077cf20a27ed19e114cb325eb5256a1cc`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c356f1b5fd3fb93d5570a71077cff86a0af06026ef7a77b257d5d83f73166d16`  
		Last Modified: Wed, 28 Jan 2026 22:13:12 GMT  
		Size: 47.8 MB (47810258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cb4bc116b0506e2ea4ab9fa6bc54cc451e350fa3274fa025479c731cbaad6d`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce6e8837913ee62730f9a78f444b9a4cdb9f29bd6e248340731f67a1c261849`  
		Last Modified: Wed, 28 Jan 2026 22:13:14 GMT  
		Size: 131.1 MB (131139180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885e95c29fdf0877c6ec82ac693521e9735cf0c19a64d0d6d950afeb84929b31`  
		Last Modified: Wed, 28 Jan 2026 22:13:11 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:798a0bad5920617757611d4a42a351558a280acbec05ebd5596f7aa5f9b00d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7698ea2fc5e9501ff603ff4bd1d0a97505093033193881b8e631982bb6483280`

```dockerfile
```

-	Layers:
	-	`sha256:c823f2fc76110ec949a1d955075948f84148e5766bc8d9751774c7fd1ddf24b5`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c856894eeb424a1604d601f5379bd90c5520e1e86430ff879bc9a4b675c5678`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e51f27439b7a2119f9322da62672bf29db9733dfe5efda7fe14a95b1978b77f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228695273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a187cad11f0bae46349c98546b174514318cd9934ece1aaf891d8bb165f437`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:45 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:47 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:23 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b8014f3539c98ae4d9db79063d0ac6da20c561da597e5080428d7fa2a81045`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581c2da28c304c8a55c89ffc142dfe9b49523660a41d23868aabdb3746f9b14e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311e3508c6b08056182bbc122c5da5bf25d876d8f0bd1eb0921f401aa6e4e794`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 5.8 MB (5792078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dac3a350ad94d3b3ff38d83b364f9dfeb47f767e8586aacb3733b7ba672656`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbefc80b7213ccab583b4d0250ca47d5a5ffbfcc700eb995807fb9e9c824552`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6900ac85f3c3185bf951b4c2ff044719ab72a728e44d91c4aeed766ee05b847d`  
		Last Modified: Wed, 28 Jan 2026 22:12:56 GMT  
		Size: 46.7 MB (46700971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc870ee9e6c819f59ecc85a2e7df376e613358eb45f4a14ebe822cf57fe76a26`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f95bece7002a8fd4dd526ef950d925ffb02f0937885175169806d3ec1ab8e1`  
		Last Modified: Wed, 28 Jan 2026 22:12:58 GMT  
		Size: 129.6 MB (129551997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923168c7bf209bd6189f93d4cb04d2c82f17faf0ae36433ab67dd1e72ec3ca29`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ae951e3a0f700ccaab54d8aa559d60b9d07b96bd8f3121b6ed86971368f04b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282b71728f5dbf3f9d4b34689d6b80dc2aa9c48da7c3fe42eada863a8d347d0`

```dockerfile
```

-	Layers:
	-	`sha256:d66e901a34db0d11a63eea540fdacb6235f7c53a2a0b8b51cf5d898c1c80b2f7`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf852e8614823f7b667b3de07ca7069909c56a682daa323b1433a790564d9d2e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:6c4bb839cbeb064c8bdd671a0930ab77198552d08ca228954d5f1ffcf5e2a245
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:be839f50567bd9e9b4680daaf94f7a2bf8bdeaeeb686c894928c28eb4d0cd404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266367777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d908a4b37e716ceba34c676d8fad3b3278eeec84262b03f1f3a3eb2addb608c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:57 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:12:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea46c317a61d3bce4e582fd911ca41e9b7e93c969318d44d1837b2e4f98fe55f`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e2d76b3c84e490335ca4d201d49ff35f28c63a3731b1380aa24f18e8d6c59`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99807da0aa3ebed973d9ab7775a13c12a398ba7ee2e8566c30b2831b088dc2a0`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 6.2 MB (6172772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4e3fe5c775467a044c8fef23b1c394e95e45711a86138052f4ca36090b92a`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f5ea10890a73457a7b47d0efe15550d1c7f55e8a03f6cf77ed61779304c31`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0515329831db25b3f47e2f85af6830c4648722f7f13873520311958acdb9431`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 51.5 MB (51454735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d412db7529763ac2d5b68e4c0045f7da0952b943f210d530eef8500728dbb1`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab87ea2260ebbc8b586e1b34e18c8a687d63bb96f8ad95d780b963d0d1ae3c1`  
		Last Modified: Wed, 28 Jan 2026 22:13:08 GMT  
		Size: 160.6 MB (160634515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597522658cfdad424b8f9a3f789f9e4fabc63d5f7c73794ab1c523c402983a44`  
		Last Modified: Wed, 28 Jan 2026 22:13:05 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:9dd0742ab3b29db9abf08d0987d40244876e9fe66037de738190b478555f7545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0552835d0ea3ec77e0128b2aa7bb40321f750bbe3604352b55b9a1e62a14ec20`

```dockerfile
```

-	Layers:
	-	`sha256:b76b581664da5f8977e815531d66d1fb753391c7b9c3bb2183cf610333ef0c33`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5812b86ec91834039854ddef53715693a87c1b6427a04a1eb60088c579dad047`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1933b6d38f5465a58393720841a79d8d9cac80e30f82afe04032cd56cf621a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df396d67d146f1f5fd22760aa8b9399fdb2daca7a61c83898ed35e6b9b311c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:09:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:09:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:09:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:11:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:11:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:11:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b9f6336edabe964959935b71ddd935ea108970a12de0dc95c486d68d6e41f0`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843a2959b2f7957e24ea77a7ddfde626093d8e533235803dad6daa2eda4b584`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77567d6b6a592cea7cfe8f30b5c69c63e972246a8fc78a610f8368bbebe655e`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 5.8 MB (5792107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f62f1d59922bddd8768b231d3899c202b2c6854109ee0695d6b4fdd145d20`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e56a90a8355d4657e7b374815568765dadd28e638118a0429760b4c5a5ee05`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faa10d9d71c3239da13566530e25099bb4a6e43671301f361de72741efe87ec`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 50.1 MB (50087338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da467ea611ce156e737b4d6e0ee876a2da337ec10e59c5df1d9acb20871d232f`  
		Last Modified: Wed, 28 Jan 2026 22:12:23 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb7744a65c8750c12ebd400b0200bf8d0fbd1add8040c5fbac90231c471d515`  
		Last Modified: Wed, 28 Jan 2026 22:12:28 GMT  
		Size: 158.9 MB (158939149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b304c02e4c3be8f0263635faf47084af6def9f9b5cef9dec3028df8a12f778`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:403c008b951a77a1c2c5ed7d6dfb83fb961cbae9cdb0eb372dbaf77546c78d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf8e3e5903b1d3e027e1361419af03cd830843fe62a0870b20f4ce14d9701e2`

```dockerfile
```

-	Layers:
	-	`sha256:ce8d5de6470f8fc4b0fb87f2b01dd4e1402bf663652176f93730b05fc4dc8e9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0d0e1472550400a760f60aa7d745184c90567135b800881c802e3060146c9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:6c4bb839cbeb064c8bdd671a0930ab77198552d08ca228954d5f1ffcf5e2a245
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:be839f50567bd9e9b4680daaf94f7a2bf8bdeaeeb686c894928c28eb4d0cd404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266367777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d908a4b37e716ceba34c676d8fad3b3278eeec84262b03f1f3a3eb2addb608c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:57 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:12:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea46c317a61d3bce4e582fd911ca41e9b7e93c969318d44d1837b2e4f98fe55f`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e2d76b3c84e490335ca4d201d49ff35f28c63a3731b1380aa24f18e8d6c59`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99807da0aa3ebed973d9ab7775a13c12a398ba7ee2e8566c30b2831b088dc2a0`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 6.2 MB (6172772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4e3fe5c775467a044c8fef23b1c394e95e45711a86138052f4ca36090b92a`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f5ea10890a73457a7b47d0efe15550d1c7f55e8a03f6cf77ed61779304c31`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0515329831db25b3f47e2f85af6830c4648722f7f13873520311958acdb9431`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 51.5 MB (51454735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d412db7529763ac2d5b68e4c0045f7da0952b943f210d530eef8500728dbb1`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab87ea2260ebbc8b586e1b34e18c8a687d63bb96f8ad95d780b963d0d1ae3c1`  
		Last Modified: Wed, 28 Jan 2026 22:13:08 GMT  
		Size: 160.6 MB (160634515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597522658cfdad424b8f9a3f789f9e4fabc63d5f7c73794ab1c523c402983a44`  
		Last Modified: Wed, 28 Jan 2026 22:13:05 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9dd0742ab3b29db9abf08d0987d40244876e9fe66037de738190b478555f7545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0552835d0ea3ec77e0128b2aa7bb40321f750bbe3604352b55b9a1e62a14ec20`

```dockerfile
```

-	Layers:
	-	`sha256:b76b581664da5f8977e815531d66d1fb753391c7b9c3bb2183cf610333ef0c33`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5812b86ec91834039854ddef53715693a87c1b6427a04a1eb60088c579dad047`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1933b6d38f5465a58393720841a79d8d9cac80e30f82afe04032cd56cf621a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df396d67d146f1f5fd22760aa8b9399fdb2daca7a61c83898ed35e6b9b311c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:09:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:09:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:09:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:11:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:11:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:11:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b9f6336edabe964959935b71ddd935ea108970a12de0dc95c486d68d6e41f0`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843a2959b2f7957e24ea77a7ddfde626093d8e533235803dad6daa2eda4b584`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77567d6b6a592cea7cfe8f30b5c69c63e972246a8fc78a610f8368bbebe655e`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 5.8 MB (5792107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f62f1d59922bddd8768b231d3899c202b2c6854109ee0695d6b4fdd145d20`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e56a90a8355d4657e7b374815568765dadd28e638118a0429760b4c5a5ee05`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faa10d9d71c3239da13566530e25099bb4a6e43671301f361de72741efe87ec`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 50.1 MB (50087338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da467ea611ce156e737b4d6e0ee876a2da337ec10e59c5df1d9acb20871d232f`  
		Last Modified: Wed, 28 Jan 2026 22:12:23 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb7744a65c8750c12ebd400b0200bf8d0fbd1add8040c5fbac90231c471d515`  
		Last Modified: Wed, 28 Jan 2026 22:12:28 GMT  
		Size: 158.9 MB (158939149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b304c02e4c3be8f0263635faf47084af6def9f9b5cef9dec3028df8a12f778`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:403c008b951a77a1c2c5ed7d6dfb83fb961cbae9cdb0eb372dbaf77546c78d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf8e3e5903b1d3e027e1361419af03cd830843fe62a0870b20f4ce14d9701e2`

```dockerfile
```

-	Layers:
	-	`sha256:ce8d5de6470f8fc4b0fb87f2b01dd4e1402bf663652176f93730b05fc4dc8e9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0d0e1472550400a760f60aa7d745184c90567135b800881c802e3060146c9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:6c4bb839cbeb064c8bdd671a0930ab77198552d08ca228954d5f1ffcf5e2a245
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:be839f50567bd9e9b4680daaf94f7a2bf8bdeaeeb686c894928c28eb4d0cd404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266367777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d908a4b37e716ceba34c676d8fad3b3278eeec84262b03f1f3a3eb2addb608c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:57 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:12:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea46c317a61d3bce4e582fd911ca41e9b7e93c969318d44d1837b2e4f98fe55f`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e2d76b3c84e490335ca4d201d49ff35f28c63a3731b1380aa24f18e8d6c59`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99807da0aa3ebed973d9ab7775a13c12a398ba7ee2e8566c30b2831b088dc2a0`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 6.2 MB (6172772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4e3fe5c775467a044c8fef23b1c394e95e45711a86138052f4ca36090b92a`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f5ea10890a73457a7b47d0efe15550d1c7f55e8a03f6cf77ed61779304c31`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0515329831db25b3f47e2f85af6830c4648722f7f13873520311958acdb9431`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 51.5 MB (51454735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d412db7529763ac2d5b68e4c0045f7da0952b943f210d530eef8500728dbb1`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab87ea2260ebbc8b586e1b34e18c8a687d63bb96f8ad95d780b963d0d1ae3c1`  
		Last Modified: Wed, 28 Jan 2026 22:13:08 GMT  
		Size: 160.6 MB (160634515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597522658cfdad424b8f9a3f789f9e4fabc63d5f7c73794ab1c523c402983a44`  
		Last Modified: Wed, 28 Jan 2026 22:13:05 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9dd0742ab3b29db9abf08d0987d40244876e9fe66037de738190b478555f7545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0552835d0ea3ec77e0128b2aa7bb40321f750bbe3604352b55b9a1e62a14ec20`

```dockerfile
```

-	Layers:
	-	`sha256:b76b581664da5f8977e815531d66d1fb753391c7b9c3bb2183cf610333ef0c33`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5812b86ec91834039854ddef53715693a87c1b6427a04a1eb60088c579dad047`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1933b6d38f5465a58393720841a79d8d9cac80e30f82afe04032cd56cf621a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df396d67d146f1f5fd22760aa8b9399fdb2daca7a61c83898ed35e6b9b311c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:09:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:09:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:09:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:11:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:11:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:11:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b9f6336edabe964959935b71ddd935ea108970a12de0dc95c486d68d6e41f0`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843a2959b2f7957e24ea77a7ddfde626093d8e533235803dad6daa2eda4b584`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77567d6b6a592cea7cfe8f30b5c69c63e972246a8fc78a610f8368bbebe655e`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 5.8 MB (5792107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f62f1d59922bddd8768b231d3899c202b2c6854109ee0695d6b4fdd145d20`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e56a90a8355d4657e7b374815568765dadd28e638118a0429760b4c5a5ee05`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faa10d9d71c3239da13566530e25099bb4a6e43671301f361de72741efe87ec`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 50.1 MB (50087338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da467ea611ce156e737b4d6e0ee876a2da337ec10e59c5df1d9acb20871d232f`  
		Last Modified: Wed, 28 Jan 2026 22:12:23 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb7744a65c8750c12ebd400b0200bf8d0fbd1add8040c5fbac90231c471d515`  
		Last Modified: Wed, 28 Jan 2026 22:12:28 GMT  
		Size: 158.9 MB (158939149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b304c02e4c3be8f0263635faf47084af6def9f9b5cef9dec3028df8a12f778`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:403c008b951a77a1c2c5ed7d6dfb83fb961cbae9cdb0eb372dbaf77546c78d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf8e3e5903b1d3e027e1361419af03cd830843fe62a0870b20f4ce14d9701e2`

```dockerfile
```

-	Layers:
	-	`sha256:ce8d5de6470f8fc4b0fb87f2b01dd4e1402bf663652176f93730b05fc4dc8e9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0d0e1472550400a760f60aa7d745184c90567135b800881c802e3060146c9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6`

```console
$ docker pull mysql@sha256:6c4bb839cbeb064c8bdd671a0930ab77198552d08ca228954d5f1ffcf5e2a245
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6` - linux; amd64

```console
$ docker pull mysql@sha256:be839f50567bd9e9b4680daaf94f7a2bf8bdeaeeb686c894928c28eb4d0cd404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266367777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d908a4b37e716ceba34c676d8fad3b3278eeec84262b03f1f3a3eb2addb608c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:57 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:12:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea46c317a61d3bce4e582fd911ca41e9b7e93c969318d44d1837b2e4f98fe55f`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e2d76b3c84e490335ca4d201d49ff35f28c63a3731b1380aa24f18e8d6c59`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99807da0aa3ebed973d9ab7775a13c12a398ba7ee2e8566c30b2831b088dc2a0`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 6.2 MB (6172772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4e3fe5c775467a044c8fef23b1c394e95e45711a86138052f4ca36090b92a`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f5ea10890a73457a7b47d0efe15550d1c7f55e8a03f6cf77ed61779304c31`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0515329831db25b3f47e2f85af6830c4648722f7f13873520311958acdb9431`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 51.5 MB (51454735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d412db7529763ac2d5b68e4c0045f7da0952b943f210d530eef8500728dbb1`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab87ea2260ebbc8b586e1b34e18c8a687d63bb96f8ad95d780b963d0d1ae3c1`  
		Last Modified: Wed, 28 Jan 2026 22:13:08 GMT  
		Size: 160.6 MB (160634515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597522658cfdad424b8f9a3f789f9e4fabc63d5f7c73794ab1c523c402983a44`  
		Last Modified: Wed, 28 Jan 2026 22:13:05 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6` - unknown; unknown

```console
$ docker pull mysql@sha256:9dd0742ab3b29db9abf08d0987d40244876e9fe66037de738190b478555f7545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0552835d0ea3ec77e0128b2aa7bb40321f750bbe3604352b55b9a1e62a14ec20`

```dockerfile
```

-	Layers:
	-	`sha256:b76b581664da5f8977e815531d66d1fb753391c7b9c3bb2183cf610333ef0c33`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5812b86ec91834039854ddef53715693a87c1b6427a04a1eb60088c579dad047`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1933b6d38f5465a58393720841a79d8d9cac80e30f82afe04032cd56cf621a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df396d67d146f1f5fd22760aa8b9399fdb2daca7a61c83898ed35e6b9b311c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:09:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:09:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:09:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:11:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:11:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:11:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b9f6336edabe964959935b71ddd935ea108970a12de0dc95c486d68d6e41f0`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843a2959b2f7957e24ea77a7ddfde626093d8e533235803dad6daa2eda4b584`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77567d6b6a592cea7cfe8f30b5c69c63e972246a8fc78a610f8368bbebe655e`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 5.8 MB (5792107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f62f1d59922bddd8768b231d3899c202b2c6854109ee0695d6b4fdd145d20`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e56a90a8355d4657e7b374815568765dadd28e638118a0429760b4c5a5ee05`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faa10d9d71c3239da13566530e25099bb4a6e43671301f361de72741efe87ec`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 50.1 MB (50087338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da467ea611ce156e737b4d6e0ee876a2da337ec10e59c5df1d9acb20871d232f`  
		Last Modified: Wed, 28 Jan 2026 22:12:23 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb7744a65c8750c12ebd400b0200bf8d0fbd1add8040c5fbac90231c471d515`  
		Last Modified: Wed, 28 Jan 2026 22:12:28 GMT  
		Size: 158.9 MB (158939149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b304c02e4c3be8f0263635faf47084af6def9f9b5cef9dec3028df8a12f778`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6` - unknown; unknown

```console
$ docker pull mysql@sha256:403c008b951a77a1c2c5ed7d6dfb83fb961cbae9cdb0eb372dbaf77546c78d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf8e3e5903b1d3e027e1361419af03cd830843fe62a0870b20f4ce14d9701e2`

```dockerfile
```

-	Layers:
	-	`sha256:ce8d5de6470f8fc4b0fb87f2b01dd4e1402bf663652176f93730b05fc4dc8e9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0d0e1472550400a760f60aa7d745184c90567135b800881c802e3060146c9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6-oracle`

```console
$ docker pull mysql@sha256:6c4bb839cbeb064c8bdd671a0930ab77198552d08ca228954d5f1ffcf5e2a245
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:be839f50567bd9e9b4680daaf94f7a2bf8bdeaeeb686c894928c28eb4d0cd404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266367777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d908a4b37e716ceba34c676d8fad3b3278eeec84262b03f1f3a3eb2addb608c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:57 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:12:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea46c317a61d3bce4e582fd911ca41e9b7e93c969318d44d1837b2e4f98fe55f`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e2d76b3c84e490335ca4d201d49ff35f28c63a3731b1380aa24f18e8d6c59`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99807da0aa3ebed973d9ab7775a13c12a398ba7ee2e8566c30b2831b088dc2a0`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 6.2 MB (6172772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4e3fe5c775467a044c8fef23b1c394e95e45711a86138052f4ca36090b92a`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f5ea10890a73457a7b47d0efe15550d1c7f55e8a03f6cf77ed61779304c31`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0515329831db25b3f47e2f85af6830c4648722f7f13873520311958acdb9431`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 51.5 MB (51454735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d412db7529763ac2d5b68e4c0045f7da0952b943f210d530eef8500728dbb1`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab87ea2260ebbc8b586e1b34e18c8a687d63bb96f8ad95d780b963d0d1ae3c1`  
		Last Modified: Wed, 28 Jan 2026 22:13:08 GMT  
		Size: 160.6 MB (160634515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597522658cfdad424b8f9a3f789f9e4fabc63d5f7c73794ab1c523c402983a44`  
		Last Modified: Wed, 28 Jan 2026 22:13:05 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9dd0742ab3b29db9abf08d0987d40244876e9fe66037de738190b478555f7545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0552835d0ea3ec77e0128b2aa7bb40321f750bbe3604352b55b9a1e62a14ec20`

```dockerfile
```

-	Layers:
	-	`sha256:b76b581664da5f8977e815531d66d1fb753391c7b9c3bb2183cf610333ef0c33`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5812b86ec91834039854ddef53715693a87c1b6427a04a1eb60088c579dad047`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1933b6d38f5465a58393720841a79d8d9cac80e30f82afe04032cd56cf621a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df396d67d146f1f5fd22760aa8b9399fdb2daca7a61c83898ed35e6b9b311c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:09:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:09:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:09:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:11:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:11:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:11:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b9f6336edabe964959935b71ddd935ea108970a12de0dc95c486d68d6e41f0`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843a2959b2f7957e24ea77a7ddfde626093d8e533235803dad6daa2eda4b584`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77567d6b6a592cea7cfe8f30b5c69c63e972246a8fc78a610f8368bbebe655e`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 5.8 MB (5792107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f62f1d59922bddd8768b231d3899c202b2c6854109ee0695d6b4fdd145d20`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e56a90a8355d4657e7b374815568765dadd28e638118a0429760b4c5a5ee05`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faa10d9d71c3239da13566530e25099bb4a6e43671301f361de72741efe87ec`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 50.1 MB (50087338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da467ea611ce156e737b4d6e0ee876a2da337ec10e59c5df1d9acb20871d232f`  
		Last Modified: Wed, 28 Jan 2026 22:12:23 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb7744a65c8750c12ebd400b0200bf8d0fbd1add8040c5fbac90231c471d515`  
		Last Modified: Wed, 28 Jan 2026 22:12:28 GMT  
		Size: 158.9 MB (158939149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b304c02e4c3be8f0263635faf47084af6def9f9b5cef9dec3028df8a12f778`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:403c008b951a77a1c2c5ed7d6dfb83fb961cbae9cdb0eb372dbaf77546c78d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf8e3e5903b1d3e027e1361419af03cd830843fe62a0870b20f4ce14d9701e2`

```dockerfile
```

-	Layers:
	-	`sha256:ce8d5de6470f8fc4b0fb87f2b01dd4e1402bf663652176f93730b05fc4dc8e9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0d0e1472550400a760f60aa7d745184c90567135b800881c802e3060146c9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6-oraclelinux9`

```console
$ docker pull mysql@sha256:6c4bb839cbeb064c8bdd671a0930ab77198552d08ca228954d5f1ffcf5e2a245
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:be839f50567bd9e9b4680daaf94f7a2bf8bdeaeeb686c894928c28eb4d0cd404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266367777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d908a4b37e716ceba34c676d8fad3b3278eeec84262b03f1f3a3eb2addb608c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:57 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:12:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea46c317a61d3bce4e582fd911ca41e9b7e93c969318d44d1837b2e4f98fe55f`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e2d76b3c84e490335ca4d201d49ff35f28c63a3731b1380aa24f18e8d6c59`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99807da0aa3ebed973d9ab7775a13c12a398ba7ee2e8566c30b2831b088dc2a0`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 6.2 MB (6172772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4e3fe5c775467a044c8fef23b1c394e95e45711a86138052f4ca36090b92a`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f5ea10890a73457a7b47d0efe15550d1c7f55e8a03f6cf77ed61779304c31`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0515329831db25b3f47e2f85af6830c4648722f7f13873520311958acdb9431`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 51.5 MB (51454735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d412db7529763ac2d5b68e4c0045f7da0952b943f210d530eef8500728dbb1`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab87ea2260ebbc8b586e1b34e18c8a687d63bb96f8ad95d780b963d0d1ae3c1`  
		Last Modified: Wed, 28 Jan 2026 22:13:08 GMT  
		Size: 160.6 MB (160634515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597522658cfdad424b8f9a3f789f9e4fabc63d5f7c73794ab1c523c402983a44`  
		Last Modified: Wed, 28 Jan 2026 22:13:05 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9dd0742ab3b29db9abf08d0987d40244876e9fe66037de738190b478555f7545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0552835d0ea3ec77e0128b2aa7bb40321f750bbe3604352b55b9a1e62a14ec20`

```dockerfile
```

-	Layers:
	-	`sha256:b76b581664da5f8977e815531d66d1fb753391c7b9c3bb2183cf610333ef0c33`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5812b86ec91834039854ddef53715693a87c1b6427a04a1eb60088c579dad047`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1933b6d38f5465a58393720841a79d8d9cac80e30f82afe04032cd56cf621a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df396d67d146f1f5fd22760aa8b9399fdb2daca7a61c83898ed35e6b9b311c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:09:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:09:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:09:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:11:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:11:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:11:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b9f6336edabe964959935b71ddd935ea108970a12de0dc95c486d68d6e41f0`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843a2959b2f7957e24ea77a7ddfde626093d8e533235803dad6daa2eda4b584`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77567d6b6a592cea7cfe8f30b5c69c63e972246a8fc78a610f8368bbebe655e`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 5.8 MB (5792107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f62f1d59922bddd8768b231d3899c202b2c6854109ee0695d6b4fdd145d20`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e56a90a8355d4657e7b374815568765dadd28e638118a0429760b4c5a5ee05`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faa10d9d71c3239da13566530e25099bb4a6e43671301f361de72741efe87ec`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 50.1 MB (50087338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da467ea611ce156e737b4d6e0ee876a2da337ec10e59c5df1d9acb20871d232f`  
		Last Modified: Wed, 28 Jan 2026 22:12:23 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb7744a65c8750c12ebd400b0200bf8d0fbd1add8040c5fbac90231c471d515`  
		Last Modified: Wed, 28 Jan 2026 22:12:28 GMT  
		Size: 158.9 MB (158939149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b304c02e4c3be8f0263635faf47084af6def9f9b5cef9dec3028df8a12f778`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:403c008b951a77a1c2c5ed7d6dfb83fb961cbae9cdb0eb372dbaf77546c78d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf8e3e5903b1d3e027e1361419af03cd830843fe62a0870b20f4ce14d9701e2`

```dockerfile
```

-	Layers:
	-	`sha256:ce8d5de6470f8fc4b0fb87f2b01dd4e1402bf663652176f93730b05fc4dc8e9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0d0e1472550400a760f60aa7d745184c90567135b800881c802e3060146c9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0`

```console
$ docker pull mysql@sha256:6c4bb839cbeb064c8bdd671a0930ab77198552d08ca228954d5f1ffcf5e2a245
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0` - linux; amd64

```console
$ docker pull mysql@sha256:be839f50567bd9e9b4680daaf94f7a2bf8bdeaeeb686c894928c28eb4d0cd404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266367777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d908a4b37e716ceba34c676d8fad3b3278eeec84262b03f1f3a3eb2addb608c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:57 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:12:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea46c317a61d3bce4e582fd911ca41e9b7e93c969318d44d1837b2e4f98fe55f`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e2d76b3c84e490335ca4d201d49ff35f28c63a3731b1380aa24f18e8d6c59`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99807da0aa3ebed973d9ab7775a13c12a398ba7ee2e8566c30b2831b088dc2a0`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 6.2 MB (6172772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4e3fe5c775467a044c8fef23b1c394e95e45711a86138052f4ca36090b92a`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f5ea10890a73457a7b47d0efe15550d1c7f55e8a03f6cf77ed61779304c31`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0515329831db25b3f47e2f85af6830c4648722f7f13873520311958acdb9431`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 51.5 MB (51454735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d412db7529763ac2d5b68e4c0045f7da0952b943f210d530eef8500728dbb1`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab87ea2260ebbc8b586e1b34e18c8a687d63bb96f8ad95d780b963d0d1ae3c1`  
		Last Modified: Wed, 28 Jan 2026 22:13:08 GMT  
		Size: 160.6 MB (160634515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597522658cfdad424b8f9a3f789f9e4fabc63d5f7c73794ab1c523c402983a44`  
		Last Modified: Wed, 28 Jan 2026 22:13:05 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0` - unknown; unknown

```console
$ docker pull mysql@sha256:9dd0742ab3b29db9abf08d0987d40244876e9fe66037de738190b478555f7545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0552835d0ea3ec77e0128b2aa7bb40321f750bbe3604352b55b9a1e62a14ec20`

```dockerfile
```

-	Layers:
	-	`sha256:b76b581664da5f8977e815531d66d1fb753391c7b9c3bb2183cf610333ef0c33`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5812b86ec91834039854ddef53715693a87c1b6427a04a1eb60088c579dad047`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1933b6d38f5465a58393720841a79d8d9cac80e30f82afe04032cd56cf621a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df396d67d146f1f5fd22760aa8b9399fdb2daca7a61c83898ed35e6b9b311c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:09:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:09:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:09:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:11:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:11:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:11:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b9f6336edabe964959935b71ddd935ea108970a12de0dc95c486d68d6e41f0`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843a2959b2f7957e24ea77a7ddfde626093d8e533235803dad6daa2eda4b584`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77567d6b6a592cea7cfe8f30b5c69c63e972246a8fc78a610f8368bbebe655e`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 5.8 MB (5792107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f62f1d59922bddd8768b231d3899c202b2c6854109ee0695d6b4fdd145d20`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e56a90a8355d4657e7b374815568765dadd28e638118a0429760b4c5a5ee05`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faa10d9d71c3239da13566530e25099bb4a6e43671301f361de72741efe87ec`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 50.1 MB (50087338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da467ea611ce156e737b4d6e0ee876a2da337ec10e59c5df1d9acb20871d232f`  
		Last Modified: Wed, 28 Jan 2026 22:12:23 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb7744a65c8750c12ebd400b0200bf8d0fbd1add8040c5fbac90231c471d515`  
		Last Modified: Wed, 28 Jan 2026 22:12:28 GMT  
		Size: 158.9 MB (158939149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b304c02e4c3be8f0263635faf47084af6def9f9b5cef9dec3028df8a12f778`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0` - unknown; unknown

```console
$ docker pull mysql@sha256:403c008b951a77a1c2c5ed7d6dfb83fb961cbae9cdb0eb372dbaf77546c78d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf8e3e5903b1d3e027e1361419af03cd830843fe62a0870b20f4ce14d9701e2`

```dockerfile
```

-	Layers:
	-	`sha256:ce8d5de6470f8fc4b0fb87f2b01dd4e1402bf663652176f93730b05fc4dc8e9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0d0e1472550400a760f60aa7d745184c90567135b800881c802e3060146c9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0-oracle`

```console
$ docker pull mysql@sha256:6c4bb839cbeb064c8bdd671a0930ab77198552d08ca228954d5f1ffcf5e2a245
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:be839f50567bd9e9b4680daaf94f7a2bf8bdeaeeb686c894928c28eb4d0cd404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266367777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d908a4b37e716ceba34c676d8fad3b3278eeec84262b03f1f3a3eb2addb608c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:57 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:12:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea46c317a61d3bce4e582fd911ca41e9b7e93c969318d44d1837b2e4f98fe55f`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e2d76b3c84e490335ca4d201d49ff35f28c63a3731b1380aa24f18e8d6c59`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99807da0aa3ebed973d9ab7775a13c12a398ba7ee2e8566c30b2831b088dc2a0`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 6.2 MB (6172772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4e3fe5c775467a044c8fef23b1c394e95e45711a86138052f4ca36090b92a`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f5ea10890a73457a7b47d0efe15550d1c7f55e8a03f6cf77ed61779304c31`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0515329831db25b3f47e2f85af6830c4648722f7f13873520311958acdb9431`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 51.5 MB (51454735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d412db7529763ac2d5b68e4c0045f7da0952b943f210d530eef8500728dbb1`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab87ea2260ebbc8b586e1b34e18c8a687d63bb96f8ad95d780b963d0d1ae3c1`  
		Last Modified: Wed, 28 Jan 2026 22:13:08 GMT  
		Size: 160.6 MB (160634515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597522658cfdad424b8f9a3f789f9e4fabc63d5f7c73794ab1c523c402983a44`  
		Last Modified: Wed, 28 Jan 2026 22:13:05 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9dd0742ab3b29db9abf08d0987d40244876e9fe66037de738190b478555f7545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0552835d0ea3ec77e0128b2aa7bb40321f750bbe3604352b55b9a1e62a14ec20`

```dockerfile
```

-	Layers:
	-	`sha256:b76b581664da5f8977e815531d66d1fb753391c7b9c3bb2183cf610333ef0c33`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5812b86ec91834039854ddef53715693a87c1b6427a04a1eb60088c579dad047`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1933b6d38f5465a58393720841a79d8d9cac80e30f82afe04032cd56cf621a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df396d67d146f1f5fd22760aa8b9399fdb2daca7a61c83898ed35e6b9b311c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:09:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:09:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:09:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:11:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:11:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:11:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b9f6336edabe964959935b71ddd935ea108970a12de0dc95c486d68d6e41f0`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843a2959b2f7957e24ea77a7ddfde626093d8e533235803dad6daa2eda4b584`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77567d6b6a592cea7cfe8f30b5c69c63e972246a8fc78a610f8368bbebe655e`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 5.8 MB (5792107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f62f1d59922bddd8768b231d3899c202b2c6854109ee0695d6b4fdd145d20`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e56a90a8355d4657e7b374815568765dadd28e638118a0429760b4c5a5ee05`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faa10d9d71c3239da13566530e25099bb4a6e43671301f361de72741efe87ec`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 50.1 MB (50087338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da467ea611ce156e737b4d6e0ee876a2da337ec10e59c5df1d9acb20871d232f`  
		Last Modified: Wed, 28 Jan 2026 22:12:23 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb7744a65c8750c12ebd400b0200bf8d0fbd1add8040c5fbac90231c471d515`  
		Last Modified: Wed, 28 Jan 2026 22:12:28 GMT  
		Size: 158.9 MB (158939149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b304c02e4c3be8f0263635faf47084af6def9f9b5cef9dec3028df8a12f778`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:403c008b951a77a1c2c5ed7d6dfb83fb961cbae9cdb0eb372dbaf77546c78d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf8e3e5903b1d3e027e1361419af03cd830843fe62a0870b20f4ce14d9701e2`

```dockerfile
```

-	Layers:
	-	`sha256:ce8d5de6470f8fc4b0fb87f2b01dd4e1402bf663652176f93730b05fc4dc8e9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0d0e1472550400a760f60aa7d745184c90567135b800881c802e3060146c9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0-oraclelinux9`

```console
$ docker pull mysql@sha256:6c4bb839cbeb064c8bdd671a0930ab77198552d08ca228954d5f1ffcf5e2a245
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:be839f50567bd9e9b4680daaf94f7a2bf8bdeaeeb686c894928c28eb4d0cd404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266367777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d908a4b37e716ceba34c676d8fad3b3278eeec84262b03f1f3a3eb2addb608c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:57 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:12:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea46c317a61d3bce4e582fd911ca41e9b7e93c969318d44d1837b2e4f98fe55f`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e2d76b3c84e490335ca4d201d49ff35f28c63a3731b1380aa24f18e8d6c59`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99807da0aa3ebed973d9ab7775a13c12a398ba7ee2e8566c30b2831b088dc2a0`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 6.2 MB (6172772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4e3fe5c775467a044c8fef23b1c394e95e45711a86138052f4ca36090b92a`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f5ea10890a73457a7b47d0efe15550d1c7f55e8a03f6cf77ed61779304c31`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0515329831db25b3f47e2f85af6830c4648722f7f13873520311958acdb9431`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 51.5 MB (51454735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d412db7529763ac2d5b68e4c0045f7da0952b943f210d530eef8500728dbb1`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab87ea2260ebbc8b586e1b34e18c8a687d63bb96f8ad95d780b963d0d1ae3c1`  
		Last Modified: Wed, 28 Jan 2026 22:13:08 GMT  
		Size: 160.6 MB (160634515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597522658cfdad424b8f9a3f789f9e4fabc63d5f7c73794ab1c523c402983a44`  
		Last Modified: Wed, 28 Jan 2026 22:13:05 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9dd0742ab3b29db9abf08d0987d40244876e9fe66037de738190b478555f7545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0552835d0ea3ec77e0128b2aa7bb40321f750bbe3604352b55b9a1e62a14ec20`

```dockerfile
```

-	Layers:
	-	`sha256:b76b581664da5f8977e815531d66d1fb753391c7b9c3bb2183cf610333ef0c33`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5812b86ec91834039854ddef53715693a87c1b6427a04a1eb60088c579dad047`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1933b6d38f5465a58393720841a79d8d9cac80e30f82afe04032cd56cf621a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df396d67d146f1f5fd22760aa8b9399fdb2daca7a61c83898ed35e6b9b311c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:09:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:09:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:09:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:11:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:11:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:11:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b9f6336edabe964959935b71ddd935ea108970a12de0dc95c486d68d6e41f0`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843a2959b2f7957e24ea77a7ddfde626093d8e533235803dad6daa2eda4b584`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77567d6b6a592cea7cfe8f30b5c69c63e972246a8fc78a610f8368bbebe655e`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 5.8 MB (5792107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f62f1d59922bddd8768b231d3899c202b2c6854109ee0695d6b4fdd145d20`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e56a90a8355d4657e7b374815568765dadd28e638118a0429760b4c5a5ee05`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faa10d9d71c3239da13566530e25099bb4a6e43671301f361de72741efe87ec`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 50.1 MB (50087338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da467ea611ce156e737b4d6e0ee876a2da337ec10e59c5df1d9acb20871d232f`  
		Last Modified: Wed, 28 Jan 2026 22:12:23 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb7744a65c8750c12ebd400b0200bf8d0fbd1add8040c5fbac90231c471d515`  
		Last Modified: Wed, 28 Jan 2026 22:12:28 GMT  
		Size: 158.9 MB (158939149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b304c02e4c3be8f0263635faf47084af6def9f9b5cef9dec3028df8a12f778`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:403c008b951a77a1c2c5ed7d6dfb83fb961cbae9cdb0eb372dbaf77546c78d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf8e3e5903b1d3e027e1361419af03cd830843fe62a0870b20f4ce14d9701e2`

```dockerfile
```

-	Layers:
	-	`sha256:ce8d5de6470f8fc4b0fb87f2b01dd4e1402bf663652176f93730b05fc4dc8e9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0d0e1472550400a760f60aa7d745184c90567135b800881c802e3060146c9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:6c4bb839cbeb064c8bdd671a0930ab77198552d08ca228954d5f1ffcf5e2a245
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:be839f50567bd9e9b4680daaf94f7a2bf8bdeaeeb686c894928c28eb4d0cd404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266367777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d908a4b37e716ceba34c676d8fad3b3278eeec84262b03f1f3a3eb2addb608c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:57 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:12:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea46c317a61d3bce4e582fd911ca41e9b7e93c969318d44d1837b2e4f98fe55f`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e2d76b3c84e490335ca4d201d49ff35f28c63a3731b1380aa24f18e8d6c59`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99807da0aa3ebed973d9ab7775a13c12a398ba7ee2e8566c30b2831b088dc2a0`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 6.2 MB (6172772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4e3fe5c775467a044c8fef23b1c394e95e45711a86138052f4ca36090b92a`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f5ea10890a73457a7b47d0efe15550d1c7f55e8a03f6cf77ed61779304c31`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0515329831db25b3f47e2f85af6830c4648722f7f13873520311958acdb9431`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 51.5 MB (51454735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d412db7529763ac2d5b68e4c0045f7da0952b943f210d530eef8500728dbb1`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab87ea2260ebbc8b586e1b34e18c8a687d63bb96f8ad95d780b963d0d1ae3c1`  
		Last Modified: Wed, 28 Jan 2026 22:13:08 GMT  
		Size: 160.6 MB (160634515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597522658cfdad424b8f9a3f789f9e4fabc63d5f7c73794ab1c523c402983a44`  
		Last Modified: Wed, 28 Jan 2026 22:13:05 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:9dd0742ab3b29db9abf08d0987d40244876e9fe66037de738190b478555f7545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0552835d0ea3ec77e0128b2aa7bb40321f750bbe3604352b55b9a1e62a14ec20`

```dockerfile
```

-	Layers:
	-	`sha256:b76b581664da5f8977e815531d66d1fb753391c7b9c3bb2183cf610333ef0c33`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5812b86ec91834039854ddef53715693a87c1b6427a04a1eb60088c579dad047`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1933b6d38f5465a58393720841a79d8d9cac80e30f82afe04032cd56cf621a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df396d67d146f1f5fd22760aa8b9399fdb2daca7a61c83898ed35e6b9b311c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:09:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:09:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:09:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:11:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:11:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:11:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b9f6336edabe964959935b71ddd935ea108970a12de0dc95c486d68d6e41f0`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843a2959b2f7957e24ea77a7ddfde626093d8e533235803dad6daa2eda4b584`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77567d6b6a592cea7cfe8f30b5c69c63e972246a8fc78a610f8368bbebe655e`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 5.8 MB (5792107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f62f1d59922bddd8768b231d3899c202b2c6854109ee0695d6b4fdd145d20`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e56a90a8355d4657e7b374815568765dadd28e638118a0429760b4c5a5ee05`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faa10d9d71c3239da13566530e25099bb4a6e43671301f361de72741efe87ec`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 50.1 MB (50087338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da467ea611ce156e737b4d6e0ee876a2da337ec10e59c5df1d9acb20871d232f`  
		Last Modified: Wed, 28 Jan 2026 22:12:23 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb7744a65c8750c12ebd400b0200bf8d0fbd1add8040c5fbac90231c471d515`  
		Last Modified: Wed, 28 Jan 2026 22:12:28 GMT  
		Size: 158.9 MB (158939149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b304c02e4c3be8f0263635faf47084af6def9f9b5cef9dec3028df8a12f778`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:403c008b951a77a1c2c5ed7d6dfb83fb961cbae9cdb0eb372dbaf77546c78d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf8e3e5903b1d3e027e1361419af03cd830843fe62a0870b20f4ce14d9701e2`

```dockerfile
```

-	Layers:
	-	`sha256:ce8d5de6470f8fc4b0fb87f2b01dd4e1402bf663652176f93730b05fc4dc8e9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0d0e1472550400a760f60aa7d745184c90567135b800881c802e3060146c9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:6c4bb839cbeb064c8bdd671a0930ab77198552d08ca228954d5f1ffcf5e2a245
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:be839f50567bd9e9b4680daaf94f7a2bf8bdeaeeb686c894928c28eb4d0cd404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266367777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d908a4b37e716ceba34c676d8fad3b3278eeec84262b03f1f3a3eb2addb608c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:57 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:12:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea46c317a61d3bce4e582fd911ca41e9b7e93c969318d44d1837b2e4f98fe55f`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e2d76b3c84e490335ca4d201d49ff35f28c63a3731b1380aa24f18e8d6c59`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99807da0aa3ebed973d9ab7775a13c12a398ba7ee2e8566c30b2831b088dc2a0`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 6.2 MB (6172772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4e3fe5c775467a044c8fef23b1c394e95e45711a86138052f4ca36090b92a`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f5ea10890a73457a7b47d0efe15550d1c7f55e8a03f6cf77ed61779304c31`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0515329831db25b3f47e2f85af6830c4648722f7f13873520311958acdb9431`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 51.5 MB (51454735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d412db7529763ac2d5b68e4c0045f7da0952b943f210d530eef8500728dbb1`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab87ea2260ebbc8b586e1b34e18c8a687d63bb96f8ad95d780b963d0d1ae3c1`  
		Last Modified: Wed, 28 Jan 2026 22:13:08 GMT  
		Size: 160.6 MB (160634515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597522658cfdad424b8f9a3f789f9e4fabc63d5f7c73794ab1c523c402983a44`  
		Last Modified: Wed, 28 Jan 2026 22:13:05 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9dd0742ab3b29db9abf08d0987d40244876e9fe66037de738190b478555f7545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0552835d0ea3ec77e0128b2aa7bb40321f750bbe3604352b55b9a1e62a14ec20`

```dockerfile
```

-	Layers:
	-	`sha256:b76b581664da5f8977e815531d66d1fb753391c7b9c3bb2183cf610333ef0c33`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5812b86ec91834039854ddef53715693a87c1b6427a04a1eb60088c579dad047`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1933b6d38f5465a58393720841a79d8d9cac80e30f82afe04032cd56cf621a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df396d67d146f1f5fd22760aa8b9399fdb2daca7a61c83898ed35e6b9b311c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:09:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:09:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:09:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:11:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:11:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:11:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b9f6336edabe964959935b71ddd935ea108970a12de0dc95c486d68d6e41f0`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843a2959b2f7957e24ea77a7ddfde626093d8e533235803dad6daa2eda4b584`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77567d6b6a592cea7cfe8f30b5c69c63e972246a8fc78a610f8368bbebe655e`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 5.8 MB (5792107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f62f1d59922bddd8768b231d3899c202b2c6854109ee0695d6b4fdd145d20`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e56a90a8355d4657e7b374815568765dadd28e638118a0429760b4c5a5ee05`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faa10d9d71c3239da13566530e25099bb4a6e43671301f361de72741efe87ec`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 50.1 MB (50087338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da467ea611ce156e737b4d6e0ee876a2da337ec10e59c5df1d9acb20871d232f`  
		Last Modified: Wed, 28 Jan 2026 22:12:23 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb7744a65c8750c12ebd400b0200bf8d0fbd1add8040c5fbac90231c471d515`  
		Last Modified: Wed, 28 Jan 2026 22:12:28 GMT  
		Size: 158.9 MB (158939149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b304c02e4c3be8f0263635faf47084af6def9f9b5cef9dec3028df8a12f778`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:403c008b951a77a1c2c5ed7d6dfb83fb961cbae9cdb0eb372dbaf77546c78d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf8e3e5903b1d3e027e1361419af03cd830843fe62a0870b20f4ce14d9701e2`

```dockerfile
```

-	Layers:
	-	`sha256:ce8d5de6470f8fc4b0fb87f2b01dd4e1402bf663652176f93730b05fc4dc8e9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0d0e1472550400a760f60aa7d745184c90567135b800881c802e3060146c9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:6c4bb839cbeb064c8bdd671a0930ab77198552d08ca228954d5f1ffcf5e2a245
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:be839f50567bd9e9b4680daaf94f7a2bf8bdeaeeb686c894928c28eb4d0cd404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266367777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d908a4b37e716ceba34c676d8fad3b3278eeec84262b03f1f3a3eb2addb608c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:57 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:12:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea46c317a61d3bce4e582fd911ca41e9b7e93c969318d44d1837b2e4f98fe55f`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e2d76b3c84e490335ca4d201d49ff35f28c63a3731b1380aa24f18e8d6c59`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99807da0aa3ebed973d9ab7775a13c12a398ba7ee2e8566c30b2831b088dc2a0`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 6.2 MB (6172772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4e3fe5c775467a044c8fef23b1c394e95e45711a86138052f4ca36090b92a`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f5ea10890a73457a7b47d0efe15550d1c7f55e8a03f6cf77ed61779304c31`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0515329831db25b3f47e2f85af6830c4648722f7f13873520311958acdb9431`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 51.5 MB (51454735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d412db7529763ac2d5b68e4c0045f7da0952b943f210d530eef8500728dbb1`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab87ea2260ebbc8b586e1b34e18c8a687d63bb96f8ad95d780b963d0d1ae3c1`  
		Last Modified: Wed, 28 Jan 2026 22:13:08 GMT  
		Size: 160.6 MB (160634515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597522658cfdad424b8f9a3f789f9e4fabc63d5f7c73794ab1c523c402983a44`  
		Last Modified: Wed, 28 Jan 2026 22:13:05 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9dd0742ab3b29db9abf08d0987d40244876e9fe66037de738190b478555f7545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0552835d0ea3ec77e0128b2aa7bb40321f750bbe3604352b55b9a1e62a14ec20`

```dockerfile
```

-	Layers:
	-	`sha256:b76b581664da5f8977e815531d66d1fb753391c7b9c3bb2183cf610333ef0c33`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5812b86ec91834039854ddef53715693a87c1b6427a04a1eb60088c579dad047`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1933b6d38f5465a58393720841a79d8d9cac80e30f82afe04032cd56cf621a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df396d67d146f1f5fd22760aa8b9399fdb2daca7a61c83898ed35e6b9b311c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:09:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:09:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:09:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:11:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:11:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:11:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b9f6336edabe964959935b71ddd935ea108970a12de0dc95c486d68d6e41f0`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843a2959b2f7957e24ea77a7ddfde626093d8e533235803dad6daa2eda4b584`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77567d6b6a592cea7cfe8f30b5c69c63e972246a8fc78a610f8368bbebe655e`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 5.8 MB (5792107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f62f1d59922bddd8768b231d3899c202b2c6854109ee0695d6b4fdd145d20`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e56a90a8355d4657e7b374815568765dadd28e638118a0429760b4c5a5ee05`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faa10d9d71c3239da13566530e25099bb4a6e43671301f361de72741efe87ec`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 50.1 MB (50087338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da467ea611ce156e737b4d6e0ee876a2da337ec10e59c5df1d9acb20871d232f`  
		Last Modified: Wed, 28 Jan 2026 22:12:23 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb7744a65c8750c12ebd400b0200bf8d0fbd1add8040c5fbac90231c471d515`  
		Last Modified: Wed, 28 Jan 2026 22:12:28 GMT  
		Size: 158.9 MB (158939149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b304c02e4c3be8f0263635faf47084af6def9f9b5cef9dec3028df8a12f778`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:403c008b951a77a1c2c5ed7d6dfb83fb961cbae9cdb0eb372dbaf77546c78d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf8e3e5903b1d3e027e1361419af03cd830843fe62a0870b20f4ce14d9701e2`

```dockerfile
```

-	Layers:
	-	`sha256:ce8d5de6470f8fc4b0fb87f2b01dd4e1402bf663652176f93730b05fc4dc8e9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0d0e1472550400a760f60aa7d745184c90567135b800881c802e3060146c9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:6c4bb839cbeb064c8bdd671a0930ab77198552d08ca228954d5f1ffcf5e2a245
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:be839f50567bd9e9b4680daaf94f7a2bf8bdeaeeb686c894928c28eb4d0cd404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266367777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d908a4b37e716ceba34c676d8fad3b3278eeec84262b03f1f3a3eb2addb608c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:57 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:12:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea46c317a61d3bce4e582fd911ca41e9b7e93c969318d44d1837b2e4f98fe55f`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e2d76b3c84e490335ca4d201d49ff35f28c63a3731b1380aa24f18e8d6c59`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99807da0aa3ebed973d9ab7775a13c12a398ba7ee2e8566c30b2831b088dc2a0`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 6.2 MB (6172772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4e3fe5c775467a044c8fef23b1c394e95e45711a86138052f4ca36090b92a`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f5ea10890a73457a7b47d0efe15550d1c7f55e8a03f6cf77ed61779304c31`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0515329831db25b3f47e2f85af6830c4648722f7f13873520311958acdb9431`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 51.5 MB (51454735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d412db7529763ac2d5b68e4c0045f7da0952b943f210d530eef8500728dbb1`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab87ea2260ebbc8b586e1b34e18c8a687d63bb96f8ad95d780b963d0d1ae3c1`  
		Last Modified: Wed, 28 Jan 2026 22:13:08 GMT  
		Size: 160.6 MB (160634515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597522658cfdad424b8f9a3f789f9e4fabc63d5f7c73794ab1c523c402983a44`  
		Last Modified: Wed, 28 Jan 2026 22:13:05 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:9dd0742ab3b29db9abf08d0987d40244876e9fe66037de738190b478555f7545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0552835d0ea3ec77e0128b2aa7bb40321f750bbe3604352b55b9a1e62a14ec20`

```dockerfile
```

-	Layers:
	-	`sha256:b76b581664da5f8977e815531d66d1fb753391c7b9c3bb2183cf610333ef0c33`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5812b86ec91834039854ddef53715693a87c1b6427a04a1eb60088c579dad047`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1933b6d38f5465a58393720841a79d8d9cac80e30f82afe04032cd56cf621a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df396d67d146f1f5fd22760aa8b9399fdb2daca7a61c83898ed35e6b9b311c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:09:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:09:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:09:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:11:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:11:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:11:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b9f6336edabe964959935b71ddd935ea108970a12de0dc95c486d68d6e41f0`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843a2959b2f7957e24ea77a7ddfde626093d8e533235803dad6daa2eda4b584`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77567d6b6a592cea7cfe8f30b5c69c63e972246a8fc78a610f8368bbebe655e`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 5.8 MB (5792107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f62f1d59922bddd8768b231d3899c202b2c6854109ee0695d6b4fdd145d20`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e56a90a8355d4657e7b374815568765dadd28e638118a0429760b4c5a5ee05`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faa10d9d71c3239da13566530e25099bb4a6e43671301f361de72741efe87ec`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 50.1 MB (50087338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da467ea611ce156e737b4d6e0ee876a2da337ec10e59c5df1d9acb20871d232f`  
		Last Modified: Wed, 28 Jan 2026 22:12:23 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb7744a65c8750c12ebd400b0200bf8d0fbd1add8040c5fbac90231c471d515`  
		Last Modified: Wed, 28 Jan 2026 22:12:28 GMT  
		Size: 158.9 MB (158939149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b304c02e4c3be8f0263635faf47084af6def9f9b5cef9dec3028df8a12f778`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:403c008b951a77a1c2c5ed7d6dfb83fb961cbae9cdb0eb372dbaf77546c78d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf8e3e5903b1d3e027e1361419af03cd830843fe62a0870b20f4ce14d9701e2`

```dockerfile
```

-	Layers:
	-	`sha256:ce8d5de6470f8fc4b0fb87f2b01dd4e1402bf663652176f93730b05fc4dc8e9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0d0e1472550400a760f60aa7d745184c90567135b800881c802e3060146c9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:f1c7674d8dd3c94f439b0d607792187d55bd861f94e8c6d683b959b577152bdc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:8b3be4876b08746f2caa509afae13bac0aca1885ce967d1bb5ca0d177000f3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233227949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4511f663fb18c6cde7e5d9bdaafeed8c1c7019732b77279315145eb430e85dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:11:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:11:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:39 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:39 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad075f4936cf8a36f21e937e90b1d698baa6b0e625d13c69beef2586416bd2b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2ec557f75a04fa223e3c0bd71f6cc48ecc59f12a6c5e31a4ed48df3205387b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c1d58a53d79eac5a138b2337dda522a36661053c302535c365fc5f64af2ad`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 6.2 MB (6172774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c60e0e578e332d62e541d2460840ae181c04522af7b87a815b50532a0cd0b9`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0125f072a0a55ba4ae0188f2dcd165d077cf20a27ed19e114cb325eb5256a1cc`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c356f1b5fd3fb93d5570a71077cff86a0af06026ef7a77b257d5d83f73166d16`  
		Last Modified: Wed, 28 Jan 2026 22:13:12 GMT  
		Size: 47.8 MB (47810258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cb4bc116b0506e2ea4ab9fa6bc54cc451e350fa3274fa025479c731cbaad6d`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce6e8837913ee62730f9a78f444b9a4cdb9f29bd6e248340731f67a1c261849`  
		Last Modified: Wed, 28 Jan 2026 22:13:14 GMT  
		Size: 131.1 MB (131139180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885e95c29fdf0877c6ec82ac693521e9735cf0c19a64d0d6d950afeb84929b31`  
		Last Modified: Wed, 28 Jan 2026 22:13:11 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:798a0bad5920617757611d4a42a351558a280acbec05ebd5596f7aa5f9b00d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7698ea2fc5e9501ff603ff4bd1d0a97505093033193881b8e631982bb6483280`

```dockerfile
```

-	Layers:
	-	`sha256:c823f2fc76110ec949a1d955075948f84148e5766bc8d9751774c7fd1ddf24b5`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c856894eeb424a1604d601f5379bd90c5520e1e86430ff879bc9a4b675c5678`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e51f27439b7a2119f9322da62672bf29db9733dfe5efda7fe14a95b1978b77f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228695273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a187cad11f0bae46349c98546b174514318cd9934ece1aaf891d8bb165f437`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:45 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:47 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:23 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b8014f3539c98ae4d9db79063d0ac6da20c561da597e5080428d7fa2a81045`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581c2da28c304c8a55c89ffc142dfe9b49523660a41d23868aabdb3746f9b14e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311e3508c6b08056182bbc122c5da5bf25d876d8f0bd1eb0921f401aa6e4e794`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 5.8 MB (5792078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dac3a350ad94d3b3ff38d83b364f9dfeb47f767e8586aacb3733b7ba672656`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbefc80b7213ccab583b4d0250ca47d5a5ffbfcc700eb995807fb9e9c824552`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6900ac85f3c3185bf951b4c2ff044719ab72a728e44d91c4aeed766ee05b847d`  
		Last Modified: Wed, 28 Jan 2026 22:12:56 GMT  
		Size: 46.7 MB (46700971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc870ee9e6c819f59ecc85a2e7df376e613358eb45f4a14ebe822cf57fe76a26`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f95bece7002a8fd4dd526ef950d925ffb02f0937885175169806d3ec1ab8e1`  
		Last Modified: Wed, 28 Jan 2026 22:12:58 GMT  
		Size: 129.6 MB (129551997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923168c7bf209bd6189f93d4cb04d2c82f17faf0ae36433ab67dd1e72ec3ca29`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:ae951e3a0f700ccaab54d8aa559d60b9d07b96bd8f3121b6ed86971368f04b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282b71728f5dbf3f9d4b34689d6b80dc2aa9c48da7c3fe42eada863a8d347d0`

```dockerfile
```

-	Layers:
	-	`sha256:d66e901a34db0d11a63eea540fdacb6235f7c53a2a0b8b51cf5d898c1c80b2f7`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf852e8614823f7b667b3de07ca7069909c56a682daa323b1433a790564d9d2e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:f1c7674d8dd3c94f439b0d607792187d55bd861f94e8c6d683b959b577152bdc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8b3be4876b08746f2caa509afae13bac0aca1885ce967d1bb5ca0d177000f3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233227949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4511f663fb18c6cde7e5d9bdaafeed8c1c7019732b77279315145eb430e85dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:11:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:11:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:39 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:39 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad075f4936cf8a36f21e937e90b1d698baa6b0e625d13c69beef2586416bd2b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2ec557f75a04fa223e3c0bd71f6cc48ecc59f12a6c5e31a4ed48df3205387b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c1d58a53d79eac5a138b2337dda522a36661053c302535c365fc5f64af2ad`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 6.2 MB (6172774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c60e0e578e332d62e541d2460840ae181c04522af7b87a815b50532a0cd0b9`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0125f072a0a55ba4ae0188f2dcd165d077cf20a27ed19e114cb325eb5256a1cc`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c356f1b5fd3fb93d5570a71077cff86a0af06026ef7a77b257d5d83f73166d16`  
		Last Modified: Wed, 28 Jan 2026 22:13:12 GMT  
		Size: 47.8 MB (47810258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cb4bc116b0506e2ea4ab9fa6bc54cc451e350fa3274fa025479c731cbaad6d`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce6e8837913ee62730f9a78f444b9a4cdb9f29bd6e248340731f67a1c261849`  
		Last Modified: Wed, 28 Jan 2026 22:13:14 GMT  
		Size: 131.1 MB (131139180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885e95c29fdf0877c6ec82ac693521e9735cf0c19a64d0d6d950afeb84929b31`  
		Last Modified: Wed, 28 Jan 2026 22:13:11 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:798a0bad5920617757611d4a42a351558a280acbec05ebd5596f7aa5f9b00d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7698ea2fc5e9501ff603ff4bd1d0a97505093033193881b8e631982bb6483280`

```dockerfile
```

-	Layers:
	-	`sha256:c823f2fc76110ec949a1d955075948f84148e5766bc8d9751774c7fd1ddf24b5`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c856894eeb424a1604d601f5379bd90c5520e1e86430ff879bc9a4b675c5678`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e51f27439b7a2119f9322da62672bf29db9733dfe5efda7fe14a95b1978b77f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228695273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a187cad11f0bae46349c98546b174514318cd9934ece1aaf891d8bb165f437`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:45 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:47 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:23 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b8014f3539c98ae4d9db79063d0ac6da20c561da597e5080428d7fa2a81045`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581c2da28c304c8a55c89ffc142dfe9b49523660a41d23868aabdb3746f9b14e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311e3508c6b08056182bbc122c5da5bf25d876d8f0bd1eb0921f401aa6e4e794`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 5.8 MB (5792078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dac3a350ad94d3b3ff38d83b364f9dfeb47f767e8586aacb3733b7ba672656`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbefc80b7213ccab583b4d0250ca47d5a5ffbfcc700eb995807fb9e9c824552`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6900ac85f3c3185bf951b4c2ff044719ab72a728e44d91c4aeed766ee05b847d`  
		Last Modified: Wed, 28 Jan 2026 22:12:56 GMT  
		Size: 46.7 MB (46700971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc870ee9e6c819f59ecc85a2e7df376e613358eb45f4a14ebe822cf57fe76a26`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f95bece7002a8fd4dd526ef950d925ffb02f0937885175169806d3ec1ab8e1`  
		Last Modified: Wed, 28 Jan 2026 22:12:58 GMT  
		Size: 129.6 MB (129551997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923168c7bf209bd6189f93d4cb04d2c82f17faf0ae36433ab67dd1e72ec3ca29`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ae951e3a0f700ccaab54d8aa559d60b9d07b96bd8f3121b6ed86971368f04b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282b71728f5dbf3f9d4b34689d6b80dc2aa9c48da7c3fe42eada863a8d347d0`

```dockerfile
```

-	Layers:
	-	`sha256:d66e901a34db0d11a63eea540fdacb6235f7c53a2a0b8b51cf5d898c1c80b2f7`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf852e8614823f7b667b3de07ca7069909c56a682daa323b1433a790564d9d2e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:f1c7674d8dd3c94f439b0d607792187d55bd861f94e8c6d683b959b577152bdc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:8b3be4876b08746f2caa509afae13bac0aca1885ce967d1bb5ca0d177000f3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233227949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4511f663fb18c6cde7e5d9bdaafeed8c1c7019732b77279315145eb430e85dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:11:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:11:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:39 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:39 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad075f4936cf8a36f21e937e90b1d698baa6b0e625d13c69beef2586416bd2b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2ec557f75a04fa223e3c0bd71f6cc48ecc59f12a6c5e31a4ed48df3205387b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c1d58a53d79eac5a138b2337dda522a36661053c302535c365fc5f64af2ad`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 6.2 MB (6172774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c60e0e578e332d62e541d2460840ae181c04522af7b87a815b50532a0cd0b9`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0125f072a0a55ba4ae0188f2dcd165d077cf20a27ed19e114cb325eb5256a1cc`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c356f1b5fd3fb93d5570a71077cff86a0af06026ef7a77b257d5d83f73166d16`  
		Last Modified: Wed, 28 Jan 2026 22:13:12 GMT  
		Size: 47.8 MB (47810258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cb4bc116b0506e2ea4ab9fa6bc54cc451e350fa3274fa025479c731cbaad6d`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce6e8837913ee62730f9a78f444b9a4cdb9f29bd6e248340731f67a1c261849`  
		Last Modified: Wed, 28 Jan 2026 22:13:14 GMT  
		Size: 131.1 MB (131139180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885e95c29fdf0877c6ec82ac693521e9735cf0c19a64d0d6d950afeb84929b31`  
		Last Modified: Wed, 28 Jan 2026 22:13:11 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:798a0bad5920617757611d4a42a351558a280acbec05ebd5596f7aa5f9b00d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7698ea2fc5e9501ff603ff4bd1d0a97505093033193881b8e631982bb6483280`

```dockerfile
```

-	Layers:
	-	`sha256:c823f2fc76110ec949a1d955075948f84148e5766bc8d9751774c7fd1ddf24b5`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c856894eeb424a1604d601f5379bd90c5520e1e86430ff879bc9a4b675c5678`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e51f27439b7a2119f9322da62672bf29db9733dfe5efda7fe14a95b1978b77f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228695273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a187cad11f0bae46349c98546b174514318cd9934ece1aaf891d8bb165f437`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:45 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:47 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:23 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b8014f3539c98ae4d9db79063d0ac6da20c561da597e5080428d7fa2a81045`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581c2da28c304c8a55c89ffc142dfe9b49523660a41d23868aabdb3746f9b14e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311e3508c6b08056182bbc122c5da5bf25d876d8f0bd1eb0921f401aa6e4e794`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 5.8 MB (5792078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dac3a350ad94d3b3ff38d83b364f9dfeb47f767e8586aacb3733b7ba672656`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbefc80b7213ccab583b4d0250ca47d5a5ffbfcc700eb995807fb9e9c824552`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6900ac85f3c3185bf951b4c2ff044719ab72a728e44d91c4aeed766ee05b847d`  
		Last Modified: Wed, 28 Jan 2026 22:12:56 GMT  
		Size: 46.7 MB (46700971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc870ee9e6c819f59ecc85a2e7df376e613358eb45f4a14ebe822cf57fe76a26`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f95bece7002a8fd4dd526ef950d925ffb02f0937885175169806d3ec1ab8e1`  
		Last Modified: Wed, 28 Jan 2026 22:12:58 GMT  
		Size: 129.6 MB (129551997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923168c7bf209bd6189f93d4cb04d2c82f17faf0ae36433ab67dd1e72ec3ca29`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ae951e3a0f700ccaab54d8aa559d60b9d07b96bd8f3121b6ed86971368f04b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282b71728f5dbf3f9d4b34689d6b80dc2aa9c48da7c3fe42eada863a8d347d0`

```dockerfile
```

-	Layers:
	-	`sha256:d66e901a34db0d11a63eea540fdacb6235f7c53a2a0b8b51cf5d898c1c80b2f7`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf852e8614823f7b667b3de07ca7069909c56a682daa323b1433a790564d9d2e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:6c4bb839cbeb064c8bdd671a0930ab77198552d08ca228954d5f1ffcf5e2a245
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:be839f50567bd9e9b4680daaf94f7a2bf8bdeaeeb686c894928c28eb4d0cd404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266367777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d908a4b37e716ceba34c676d8fad3b3278eeec84262b03f1f3a3eb2addb608c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:57 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:12:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea46c317a61d3bce4e582fd911ca41e9b7e93c969318d44d1837b2e4f98fe55f`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e2d76b3c84e490335ca4d201d49ff35f28c63a3731b1380aa24f18e8d6c59`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99807da0aa3ebed973d9ab7775a13c12a398ba7ee2e8566c30b2831b088dc2a0`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 6.2 MB (6172772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4e3fe5c775467a044c8fef23b1c394e95e45711a86138052f4ca36090b92a`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f5ea10890a73457a7b47d0efe15550d1c7f55e8a03f6cf77ed61779304c31`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0515329831db25b3f47e2f85af6830c4648722f7f13873520311958acdb9431`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 51.5 MB (51454735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d412db7529763ac2d5b68e4c0045f7da0952b943f210d530eef8500728dbb1`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab87ea2260ebbc8b586e1b34e18c8a687d63bb96f8ad95d780b963d0d1ae3c1`  
		Last Modified: Wed, 28 Jan 2026 22:13:08 GMT  
		Size: 160.6 MB (160634515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597522658cfdad424b8f9a3f789f9e4fabc63d5f7c73794ab1c523c402983a44`  
		Last Modified: Wed, 28 Jan 2026 22:13:05 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9dd0742ab3b29db9abf08d0987d40244876e9fe66037de738190b478555f7545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0552835d0ea3ec77e0128b2aa7bb40321f750bbe3604352b55b9a1e62a14ec20`

```dockerfile
```

-	Layers:
	-	`sha256:b76b581664da5f8977e815531d66d1fb753391c7b9c3bb2183cf610333ef0c33`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5812b86ec91834039854ddef53715693a87c1b6427a04a1eb60088c579dad047`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1933b6d38f5465a58393720841a79d8d9cac80e30f82afe04032cd56cf621a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df396d67d146f1f5fd22760aa8b9399fdb2daca7a61c83898ed35e6b9b311c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:09:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:09:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:09:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:11:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:11:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:11:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b9f6336edabe964959935b71ddd935ea108970a12de0dc95c486d68d6e41f0`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843a2959b2f7957e24ea77a7ddfde626093d8e533235803dad6daa2eda4b584`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77567d6b6a592cea7cfe8f30b5c69c63e972246a8fc78a610f8368bbebe655e`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 5.8 MB (5792107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f62f1d59922bddd8768b231d3899c202b2c6854109ee0695d6b4fdd145d20`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e56a90a8355d4657e7b374815568765dadd28e638118a0429760b4c5a5ee05`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faa10d9d71c3239da13566530e25099bb4a6e43671301f361de72741efe87ec`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 50.1 MB (50087338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da467ea611ce156e737b4d6e0ee876a2da337ec10e59c5df1d9acb20871d232f`  
		Last Modified: Wed, 28 Jan 2026 22:12:23 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb7744a65c8750c12ebd400b0200bf8d0fbd1add8040c5fbac90231c471d515`  
		Last Modified: Wed, 28 Jan 2026 22:12:28 GMT  
		Size: 158.9 MB (158939149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b304c02e4c3be8f0263635faf47084af6def9f9b5cef9dec3028df8a12f778`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:403c008b951a77a1c2c5ed7d6dfb83fb961cbae9cdb0eb372dbaf77546c78d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf8e3e5903b1d3e027e1361419af03cd830843fe62a0870b20f4ce14d9701e2`

```dockerfile
```

-	Layers:
	-	`sha256:ce8d5de6470f8fc4b0fb87f2b01dd4e1402bf663652176f93730b05fc4dc8e9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0d0e1472550400a760f60aa7d745184c90567135b800881c802e3060146c9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:6c4bb839cbeb064c8bdd671a0930ab77198552d08ca228954d5f1ffcf5e2a245
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:be839f50567bd9e9b4680daaf94f7a2bf8bdeaeeb686c894928c28eb4d0cd404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266367777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d908a4b37e716ceba34c676d8fad3b3278eeec84262b03f1f3a3eb2addb608c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:57 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:11:22 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:50 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:12:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea46c317a61d3bce4e582fd911ca41e9b7e93c969318d44d1837b2e4f98fe55f`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e2d76b3c84e490335ca4d201d49ff35f28c63a3731b1380aa24f18e8d6c59`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99807da0aa3ebed973d9ab7775a13c12a398ba7ee2e8566c30b2831b088dc2a0`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 6.2 MB (6172772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4e3fe5c775467a044c8fef23b1c394e95e45711a86138052f4ca36090b92a`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f5ea10890a73457a7b47d0efe15550d1c7f55e8a03f6cf77ed61779304c31`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0515329831db25b3f47e2f85af6830c4648722f7f13873520311958acdb9431`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 51.5 MB (51454735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d412db7529763ac2d5b68e4c0045f7da0952b943f210d530eef8500728dbb1`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab87ea2260ebbc8b586e1b34e18c8a687d63bb96f8ad95d780b963d0d1ae3c1`  
		Last Modified: Wed, 28 Jan 2026 22:13:08 GMT  
		Size: 160.6 MB (160634515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597522658cfdad424b8f9a3f789f9e4fabc63d5f7c73794ab1c523c402983a44`  
		Last Modified: Wed, 28 Jan 2026 22:13:05 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9dd0742ab3b29db9abf08d0987d40244876e9fe66037de738190b478555f7545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0552835d0ea3ec77e0128b2aa7bb40321f750bbe3604352b55b9a1e62a14ec20`

```dockerfile
```

-	Layers:
	-	`sha256:b76b581664da5f8977e815531d66d1fb753391c7b9c3bb2183cf610333ef0c33`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 16.3 MB (16297400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5812b86ec91834039854ddef53715693a87c1b6427a04a1eb60088c579dad047`  
		Last Modified: Wed, 28 Jan 2026 22:13:03 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1933b6d38f5465a58393720841a79d8d9cac80e30f82afe04032cd56cf621a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df396d67d146f1f5fd22760aa8b9399fdb2daca7a61c83898ed35e6b9b311c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:09:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:09:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:09:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:10:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 28 Jan 2026 22:10:25 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:10:25 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:10:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 28 Jan 2026 22:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:11:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:11:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:11:46 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:11:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b9f6336edabe964959935b71ddd935ea108970a12de0dc95c486d68d6e41f0`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843a2959b2f7957e24ea77a7ddfde626093d8e533235803dad6daa2eda4b584`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77567d6b6a592cea7cfe8f30b5c69c63e972246a8fc78a610f8368bbebe655e`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 5.8 MB (5792107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f62f1d59922bddd8768b231d3899c202b2c6854109ee0695d6b4fdd145d20`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e56a90a8355d4657e7b374815568765dadd28e638118a0429760b4c5a5ee05`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faa10d9d71c3239da13566530e25099bb4a6e43671301f361de72741efe87ec`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 50.1 MB (50087338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da467ea611ce156e737b4d6e0ee876a2da337ec10e59c5df1d9acb20871d232f`  
		Last Modified: Wed, 28 Jan 2026 22:12:23 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb7744a65c8750c12ebd400b0200bf8d0fbd1add8040c5fbac90231c471d515`  
		Last Modified: Wed, 28 Jan 2026 22:12:28 GMT  
		Size: 158.9 MB (158939149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b304c02e4c3be8f0263635faf47084af6def9f9b5cef9dec3028df8a12f778`  
		Last Modified: Wed, 28 Jan 2026 22:12:24 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:403c008b951a77a1c2c5ed7d6dfb83fb961cbae9cdb0eb372dbaf77546c78d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf8e3e5903b1d3e027e1361419af03cd830843fe62a0870b20f4ce14d9701e2`

```dockerfile
```

-	Layers:
	-	`sha256:ce8d5de6470f8fc4b0fb87f2b01dd4e1402bf663652176f93730b05fc4dc8e9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:22 GMT  
		Size: 16.3 MB (16295856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0d0e1472550400a760f60aa7d745184c90567135b800881c802e3060146c9d`  
		Last Modified: Wed, 28 Jan 2026 22:12:21 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json
