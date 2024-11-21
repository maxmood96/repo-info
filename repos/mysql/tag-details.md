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
$ docker pull mysql@sha256:2bed89deaa6122df7e3bfdb3006d2f09251e2fa925bdd4f6a5ccff7badf070ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:8d111b535dbe6d9fbdaafcb0e3157aff64664ef5052ceae3c57f974166a6cff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171514588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bb57dc6b1d1f9bbd9ab9843af36264c74b6944360d37703fc8cdb932c1587f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5e9755d4041de874322937a7e4aba7eae546b110eaf21c99fd9ee849a31f0b`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6f939b5bdeb93950dd408d5e339b273a43e8129bb908aa25a492fd41925b5e`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4825be18a9da34ab830e99c285416149b22324acc5d70e0fe35719306a672a39`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 6.9 MB (6902532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d101851db8708b91cdb31331ed5fd7584d9109fd10ae799295f8e4b1c372ee`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e6fd8a5fc375e4c5061959d05b0c1727be47165db7fcf903582c94045798ff`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b46238a9af0862e613cea2905d7fa437227a27976fbfcac6e82db8164ba40d`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 47.6 MB (47559393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13a1e3aee9ee85855737c1af5191eef5fbf6d612b81b87f12fcd6dd59d7594a`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444e8e4164f357b6d69d3d1932320dbd2f6e3f0970bf6ee1cacb47a88e87780f`  
		Last Modified: Thu, 21 Nov 2024 00:24:51 GMT  
		Size: 67.0 MB (66961014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef40cced209d5affe747d3e62bcaef3f4800e24279555efd1d9a0a68d5902c1`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:d24e1e14db4144ad85299ee67329e83eab737d53eabb1c765795ef88d63f8d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97e864c12a8d34ccf20924c9821a42b95f8a22305076fb1ef870ab42aa83988`

```dockerfile
```

-	Layers:
	-	`sha256:978b2ae2ea66ace5f526e29cbe706f1d9b0139220749975cfb696fbcbc463daf`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 14.9 MB (14871754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade4558bfff869010112ad9fbb8710524f7b764f662ceaedb75071b90e9a9d7c`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 34.2 KB (34248 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2516a10a1ea246e0b9391b259194e9f0c6a0669dfd1fccc337e62450f657acc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168737549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6672c03fe2b69c64f378bc123bffddae0ceb6db9d80968d238151dffa2706c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd77c1317d3aa167ce525e562b4150ca934ca0a6931888f4facee3c2832b430`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6319ad690265786884f89a8528c43a7641f5ec4ee13646914915d4fbbeef78b`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 46.5 MB (46450201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e66d86f17d19ad1ee543340630050da5690d888f02bc186b07736702382eb09`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d04267626c09db36ba57db446ffa128a79b92b28e520e9bbb60d84c92b94c0`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 67.2 MB (67201722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58f7aad98ac58f55673caa5b917718391795ff9a3b1f479fc7b787d78f3a354`  
		Last Modified: Thu, 21 Nov 2024 00:26:32 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:3d5efe1ed7cf29dad01a2c69594ceb6b0ca523977f24d2767d3ef13de6f6b9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131563af08c9fd291fd2f7c813846125fe715f006a3d396bde57881e1cc0a186`

```dockerfile
```

-	Layers:
	-	`sha256:0c0d39bebfbb0c7af2b65758f081a44f9b9d036cb843b36bf3d346a568b44c6b`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 14.9 MB (14866904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e11d0d508b78947bc35881c46c4902ec23e4a3e0154d972b7b3bbd47d11d51c`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 34.6 KB (34553 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:2bed89deaa6122df7e3bfdb3006d2f09251e2fa925bdd4f6a5ccff7badf070ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8d111b535dbe6d9fbdaafcb0e3157aff64664ef5052ceae3c57f974166a6cff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171514588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bb57dc6b1d1f9bbd9ab9843af36264c74b6944360d37703fc8cdb932c1587f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5e9755d4041de874322937a7e4aba7eae546b110eaf21c99fd9ee849a31f0b`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6f939b5bdeb93950dd408d5e339b273a43e8129bb908aa25a492fd41925b5e`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4825be18a9da34ab830e99c285416149b22324acc5d70e0fe35719306a672a39`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 6.9 MB (6902532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d101851db8708b91cdb31331ed5fd7584d9109fd10ae799295f8e4b1c372ee`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e6fd8a5fc375e4c5061959d05b0c1727be47165db7fcf903582c94045798ff`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b46238a9af0862e613cea2905d7fa437227a27976fbfcac6e82db8164ba40d`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 47.6 MB (47559393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13a1e3aee9ee85855737c1af5191eef5fbf6d612b81b87f12fcd6dd59d7594a`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444e8e4164f357b6d69d3d1932320dbd2f6e3f0970bf6ee1cacb47a88e87780f`  
		Last Modified: Thu, 21 Nov 2024 00:24:51 GMT  
		Size: 67.0 MB (66961014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef40cced209d5affe747d3e62bcaef3f4800e24279555efd1d9a0a68d5902c1`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d24e1e14db4144ad85299ee67329e83eab737d53eabb1c765795ef88d63f8d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97e864c12a8d34ccf20924c9821a42b95f8a22305076fb1ef870ab42aa83988`

```dockerfile
```

-	Layers:
	-	`sha256:978b2ae2ea66ace5f526e29cbe706f1d9b0139220749975cfb696fbcbc463daf`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 14.9 MB (14871754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade4558bfff869010112ad9fbb8710524f7b764f662ceaedb75071b90e9a9d7c`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 34.2 KB (34248 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2516a10a1ea246e0b9391b259194e9f0c6a0669dfd1fccc337e62450f657acc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168737549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6672c03fe2b69c64f378bc123bffddae0ceb6db9d80968d238151dffa2706c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd77c1317d3aa167ce525e562b4150ca934ca0a6931888f4facee3c2832b430`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6319ad690265786884f89a8528c43a7641f5ec4ee13646914915d4fbbeef78b`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 46.5 MB (46450201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e66d86f17d19ad1ee543340630050da5690d888f02bc186b07736702382eb09`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d04267626c09db36ba57db446ffa128a79b92b28e520e9bbb60d84c92b94c0`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 67.2 MB (67201722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58f7aad98ac58f55673caa5b917718391795ff9a3b1f479fc7b787d78f3a354`  
		Last Modified: Thu, 21 Nov 2024 00:26:32 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3d5efe1ed7cf29dad01a2c69594ceb6b0ca523977f24d2767d3ef13de6f6b9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131563af08c9fd291fd2f7c813846125fe715f006a3d396bde57881e1cc0a186`

```dockerfile
```

-	Layers:
	-	`sha256:0c0d39bebfbb0c7af2b65758f081a44f9b9d036cb843b36bf3d346a568b44c6b`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 14.9 MB (14866904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e11d0d508b78947bc35881c46c4902ec23e4a3e0154d972b7b3bbd47d11d51c`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 34.6 KB (34553 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:2bed89deaa6122df7e3bfdb3006d2f09251e2fa925bdd4f6a5ccff7badf070ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:8d111b535dbe6d9fbdaafcb0e3157aff64664ef5052ceae3c57f974166a6cff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171514588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bb57dc6b1d1f9bbd9ab9843af36264c74b6944360d37703fc8cdb932c1587f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5e9755d4041de874322937a7e4aba7eae546b110eaf21c99fd9ee849a31f0b`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6f939b5bdeb93950dd408d5e339b273a43e8129bb908aa25a492fd41925b5e`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4825be18a9da34ab830e99c285416149b22324acc5d70e0fe35719306a672a39`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 6.9 MB (6902532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d101851db8708b91cdb31331ed5fd7584d9109fd10ae799295f8e4b1c372ee`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e6fd8a5fc375e4c5061959d05b0c1727be47165db7fcf903582c94045798ff`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b46238a9af0862e613cea2905d7fa437227a27976fbfcac6e82db8164ba40d`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 47.6 MB (47559393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13a1e3aee9ee85855737c1af5191eef5fbf6d612b81b87f12fcd6dd59d7594a`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444e8e4164f357b6d69d3d1932320dbd2f6e3f0970bf6ee1cacb47a88e87780f`  
		Last Modified: Thu, 21 Nov 2024 00:24:51 GMT  
		Size: 67.0 MB (66961014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef40cced209d5affe747d3e62bcaef3f4800e24279555efd1d9a0a68d5902c1`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d24e1e14db4144ad85299ee67329e83eab737d53eabb1c765795ef88d63f8d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97e864c12a8d34ccf20924c9821a42b95f8a22305076fb1ef870ab42aa83988`

```dockerfile
```

-	Layers:
	-	`sha256:978b2ae2ea66ace5f526e29cbe706f1d9b0139220749975cfb696fbcbc463daf`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 14.9 MB (14871754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade4558bfff869010112ad9fbb8710524f7b764f662ceaedb75071b90e9a9d7c`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 34.2 KB (34248 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2516a10a1ea246e0b9391b259194e9f0c6a0669dfd1fccc337e62450f657acc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168737549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6672c03fe2b69c64f378bc123bffddae0ceb6db9d80968d238151dffa2706c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd77c1317d3aa167ce525e562b4150ca934ca0a6931888f4facee3c2832b430`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6319ad690265786884f89a8528c43a7641f5ec4ee13646914915d4fbbeef78b`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 46.5 MB (46450201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e66d86f17d19ad1ee543340630050da5690d888f02bc186b07736702382eb09`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d04267626c09db36ba57db446ffa128a79b92b28e520e9bbb60d84c92b94c0`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 67.2 MB (67201722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58f7aad98ac58f55673caa5b917718391795ff9a3b1f479fc7b787d78f3a354`  
		Last Modified: Thu, 21 Nov 2024 00:26:32 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3d5efe1ed7cf29dad01a2c69594ceb6b0ca523977f24d2767d3ef13de6f6b9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131563af08c9fd291fd2f7c813846125fe715f006a3d396bde57881e1cc0a186`

```dockerfile
```

-	Layers:
	-	`sha256:0c0d39bebfbb0c7af2b65758f081a44f9b9d036cb843b36bf3d346a568b44c6b`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 14.9 MB (14866904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e11d0d508b78947bc35881c46c4902ec23e4a3e0154d972b7b3bbd47d11d51c`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 34.6 KB (34553 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:8a685d21a4ebc7e8e6541115b8fef17a872d669184b8100c4c180e6498d09a6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:600242f3651fd71af32573d613dc98870ac61237714ea230ea784615ae56ad87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170977378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c9538bbb34e2fa4804bc95b61014dc154906a3923898531804e280e89f361b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48db9f7ea45e51212dd1767f5624cc179e510fd2336cb21366b52bddfd0c834`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57907e4cc4f2f352e028caad5c77b978b85227de33b70e0d1568b5abc8dbb858`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c10ebc08f661c8844aedb2a0d2a6031bbf4c89a7a2f5647e42b2ceb572c2948`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 6.9 MB (6902535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e3773858ad48aca220a5cfe56df146822d1bf920234c249d7c6d3fc936fe85`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a9291ccc131f35749bacacffcec55a5f1001ceefafbac00603fddd2cb07ffe`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afebf85e09ce9df2a3ec0c97256101d165835fd531a0bfeb04065b8d7845ef2`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 49.6 MB (49622114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9247a49c1f0b18ac2cc953ef93c10cdf24efe6227e4cc93d0c657dd84cd25742`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aff87c766172bf423aba5677dc35af0bcb8b91988cc3a224a674ebc5a74a004`  
		Last Modified: Thu, 21 Nov 2024 00:24:59 GMT  
		Size: 64.4 MB (64360958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cc72d643da6df2bd14e2b233ed0c2fddc9ff336f52d7451f9fbcaa7b03b939`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e23f27309a673d21df4d6b5f3dbf8331050dc00dea09f0159794c735bb50114`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:08555608f0ba44fdd231e4cf9f5cb977fcbd2d5b648a2a1959d5503a6c339313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14799183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea94bd97b65774e0422766f801f49ea4277aac2e7346159dc6a4171fd62ee10`

```dockerfile
```

-	Layers:
	-	`sha256:1174e925b3a4bf1c77c5afd35cb0a7b9e99fe494d1cb4b1de725327bdf2ae371`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 14.8 MB (14764233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5f477512a8770433ae872d8713e19c78da10c07deb95a448a6ba86928c32302`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 35.0 KB (34950 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6cee01d37675de33f46215162c641e54718f1ac37475571cbcaf7b6e2142c36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175477229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35859c321b65726b5b1c462dcd17649ce2df7772d6fb423362652722deae796`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6451580cceb6ab22e40316ff10f58ef0812032136a662d3f4c7a1ea47d97211e`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbb151ca502c2ff3727bca04b55f14c0eb91ad908a6f58473165a2f64994287`  
		Last Modified: Thu, 21 Nov 2024 00:28:06 GMT  
		Size: 48.5 MB (48485082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98634756c7a23cca4e16c16a3cbfc031532faf5947ec95bff16c1d3eca9ba253`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b92de65da79c3100d476e31d6aa125963ee5644d05e292c3f7ab8e708b8878`  
		Last Modified: Thu, 21 Nov 2024 00:28:07 GMT  
		Size: 71.9 MB (71906406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd198337bce0efd5f21deeb19858c1f39c65213fb91e8ef95de67e5f32e0e1c`  
		Last Modified: Thu, 21 Nov 2024 00:28:05 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7833aab7712665108fb352f9ba6db2718d608fda4d2d5a7fc7848c6fe78926ae`  
		Last Modified: Thu, 21 Nov 2024 00:28:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:00361d32ec81c0398af6925d2ba0b589f93d1a4a7b441f1bab31e27384244bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14794510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b5a7c181fe7864b40d90f367527b322208f5bb2b1fb419de6eaecedc3fd7ed`

```dockerfile
```

-	Layers:
	-	`sha256:51cdbdeda1bdc7d8a8b437b8e6c31d5fdd9ec46d604440136948a49b24406592`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 14.8 MB (14759311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d05e7863b79f8aa99b3619a87bfc5b11c04f63c248ac93f17565e8cbb0a1af2`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 35.2 KB (35199 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:3a797469a0c936822c3cc93c1e94f96d91d854c5c81eac45840b31464409b4ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:ca94d886e43c0541f834572c6861097113aa71d98fbc9bcce8a44ad3ec81a5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184179467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c32752b103f2f64b80cbdeca13f1062b5ae4a9cd8cb09ed3ebaa003241f4064`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb40b74f92c54287c4079c439813da763527bb1ff50ac099ed2e73e03f64cff`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70616fc1634f61422208d4490a405cb911b0f625facb00442d02aff0431c0a8d`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 4.4 MB (4422768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6366761dde571e9b27a79630976f734a901c05aed3df475cafa24686195454c5`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 1.4 MB (1445956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d9fb32a0c8e449173648e78aa4643bc85863e6743f833589f5045901b60fc2`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6f55273db7e4976edde7e688b786fe49243f37da6418c2f870188dfa5f672e`  
		Last Modified: Tue, 12 Nov 2024 02:14:39 GMT  
		Size: 15.3 MB (15295550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e10f7d81b1219ea142bf958f5e509737d72e91b6dab6c79877c01ce1618941`  
		Last Modified: Tue, 12 Nov 2024 02:14:39 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7562d4a81907f8b99d8942e2cb3ce93817c8eb39f2a0b7261260a863d41ac0a`  
		Last Modified: Tue, 12 Nov 2024 02:14:39 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324695993a9ceb2cbe6f2c7404314809fab57047e516d36e84587f9c631154d1`  
		Last Modified: Tue, 12 Nov 2024 02:14:41 GMT  
		Size: 133.9 MB (133876931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f5177793182d807ab87d637bca9718d80c9bee31c6db5fed0aef303ea49a61`  
		Last Modified: Tue, 12 Nov 2024 02:14:40 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfbda283dc78b30ba1332df28dec334f96a6d8fb0184140fc7f4e9efd285b71`  
		Last Modified: Tue, 12 Nov 2024 02:14:40 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ea090265c5dfbd982fc6e82622350ebda57ae50a86e8e3c40722885188837f`  
		Last Modified: Tue, 12 Nov 2024 02:14:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:21188c8c9bd9f1cd9746572d5c0072e268888a686019f5532a678d99630a357c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4033593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e75c0557c8dc311b60f6392b62837d4c02812bccbb16d12f2ae194f24f13a93`

```dockerfile
```

-	Layers:
	-	`sha256:e82e8f27a7b0f650ddfb751e22a194104691519f383089be9a5dc3db77820931`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 4.0 MB (3999297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a45a9157f9b91778d4c525ef7ddca9057fbc93977c5647eb986bd8c6e949c01e`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:3a797469a0c936822c3cc93c1e94f96d91d854c5c81eac45840b31464409b4ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:ca94d886e43c0541f834572c6861097113aa71d98fbc9bcce8a44ad3ec81a5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184179467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c32752b103f2f64b80cbdeca13f1062b5ae4a9cd8cb09ed3ebaa003241f4064`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb40b74f92c54287c4079c439813da763527bb1ff50ac099ed2e73e03f64cff`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70616fc1634f61422208d4490a405cb911b0f625facb00442d02aff0431c0a8d`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 4.4 MB (4422768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6366761dde571e9b27a79630976f734a901c05aed3df475cafa24686195454c5`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 1.4 MB (1445956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d9fb32a0c8e449173648e78aa4643bc85863e6743f833589f5045901b60fc2`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6f55273db7e4976edde7e688b786fe49243f37da6418c2f870188dfa5f672e`  
		Last Modified: Tue, 12 Nov 2024 02:14:39 GMT  
		Size: 15.3 MB (15295550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e10f7d81b1219ea142bf958f5e509737d72e91b6dab6c79877c01ce1618941`  
		Last Modified: Tue, 12 Nov 2024 02:14:39 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7562d4a81907f8b99d8942e2cb3ce93817c8eb39f2a0b7261260a863d41ac0a`  
		Last Modified: Tue, 12 Nov 2024 02:14:39 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324695993a9ceb2cbe6f2c7404314809fab57047e516d36e84587f9c631154d1`  
		Last Modified: Tue, 12 Nov 2024 02:14:41 GMT  
		Size: 133.9 MB (133876931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f5177793182d807ab87d637bca9718d80c9bee31c6db5fed0aef303ea49a61`  
		Last Modified: Tue, 12 Nov 2024 02:14:40 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfbda283dc78b30ba1332df28dec334f96a6d8fb0184140fc7f4e9efd285b71`  
		Last Modified: Tue, 12 Nov 2024 02:14:40 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ea090265c5dfbd982fc6e82622350ebda57ae50a86e8e3c40722885188837f`  
		Last Modified: Tue, 12 Nov 2024 02:14:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:21188c8c9bd9f1cd9746572d5c0072e268888a686019f5532a678d99630a357c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4033593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e75c0557c8dc311b60f6392b62837d4c02812bccbb16d12f2ae194f24f13a93`

```dockerfile
```

-	Layers:
	-	`sha256:e82e8f27a7b0f650ddfb751e22a194104691519f383089be9a5dc3db77820931`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 4.0 MB (3999297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a45a9157f9b91778d4c525ef7ddca9057fbc93977c5647eb986bd8c6e949c01e`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:8a685d21a4ebc7e8e6541115b8fef17a872d669184b8100c4c180e6498d09a6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:600242f3651fd71af32573d613dc98870ac61237714ea230ea784615ae56ad87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170977378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c9538bbb34e2fa4804bc95b61014dc154906a3923898531804e280e89f361b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48db9f7ea45e51212dd1767f5624cc179e510fd2336cb21366b52bddfd0c834`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57907e4cc4f2f352e028caad5c77b978b85227de33b70e0d1568b5abc8dbb858`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c10ebc08f661c8844aedb2a0d2a6031bbf4c89a7a2f5647e42b2ceb572c2948`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 6.9 MB (6902535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e3773858ad48aca220a5cfe56df146822d1bf920234c249d7c6d3fc936fe85`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a9291ccc131f35749bacacffcec55a5f1001ceefafbac00603fddd2cb07ffe`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afebf85e09ce9df2a3ec0c97256101d165835fd531a0bfeb04065b8d7845ef2`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 49.6 MB (49622114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9247a49c1f0b18ac2cc953ef93c10cdf24efe6227e4cc93d0c657dd84cd25742`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aff87c766172bf423aba5677dc35af0bcb8b91988cc3a224a674ebc5a74a004`  
		Last Modified: Thu, 21 Nov 2024 00:24:59 GMT  
		Size: 64.4 MB (64360958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cc72d643da6df2bd14e2b233ed0c2fddc9ff336f52d7451f9fbcaa7b03b939`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e23f27309a673d21df4d6b5f3dbf8331050dc00dea09f0159794c735bb50114`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:08555608f0ba44fdd231e4cf9f5cb977fcbd2d5b648a2a1959d5503a6c339313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14799183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea94bd97b65774e0422766f801f49ea4277aac2e7346159dc6a4171fd62ee10`

```dockerfile
```

-	Layers:
	-	`sha256:1174e925b3a4bf1c77c5afd35cb0a7b9e99fe494d1cb4b1de725327bdf2ae371`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 14.8 MB (14764233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5f477512a8770433ae872d8713e19c78da10c07deb95a448a6ba86928c32302`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 35.0 KB (34950 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6cee01d37675de33f46215162c641e54718f1ac37475571cbcaf7b6e2142c36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175477229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35859c321b65726b5b1c462dcd17649ce2df7772d6fb423362652722deae796`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6451580cceb6ab22e40316ff10f58ef0812032136a662d3f4c7a1ea47d97211e`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbb151ca502c2ff3727bca04b55f14c0eb91ad908a6f58473165a2f64994287`  
		Last Modified: Thu, 21 Nov 2024 00:28:06 GMT  
		Size: 48.5 MB (48485082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98634756c7a23cca4e16c16a3cbfc031532faf5947ec95bff16c1d3eca9ba253`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b92de65da79c3100d476e31d6aa125963ee5644d05e292c3f7ab8e708b8878`  
		Last Modified: Thu, 21 Nov 2024 00:28:07 GMT  
		Size: 71.9 MB (71906406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd198337bce0efd5f21deeb19858c1f39c65213fb91e8ef95de67e5f32e0e1c`  
		Last Modified: Thu, 21 Nov 2024 00:28:05 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7833aab7712665108fb352f9ba6db2718d608fda4d2d5a7fc7848c6fe78926ae`  
		Last Modified: Thu, 21 Nov 2024 00:28:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:00361d32ec81c0398af6925d2ba0b589f93d1a4a7b441f1bab31e27384244bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14794510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b5a7c181fe7864b40d90f367527b322208f5bb2b1fb419de6eaecedc3fd7ed`

```dockerfile
```

-	Layers:
	-	`sha256:51cdbdeda1bdc7d8a8b437b8e6c31d5fdd9ec46d604440136948a49b24406592`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 14.8 MB (14759311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d05e7863b79f8aa99b3619a87bfc5b11c04f63c248ac93f17565e8cbb0a1af2`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 35.2 KB (35199 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:8a685d21a4ebc7e8e6541115b8fef17a872d669184b8100c4c180e6498d09a6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:600242f3651fd71af32573d613dc98870ac61237714ea230ea784615ae56ad87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170977378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c9538bbb34e2fa4804bc95b61014dc154906a3923898531804e280e89f361b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48db9f7ea45e51212dd1767f5624cc179e510fd2336cb21366b52bddfd0c834`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57907e4cc4f2f352e028caad5c77b978b85227de33b70e0d1568b5abc8dbb858`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c10ebc08f661c8844aedb2a0d2a6031bbf4c89a7a2f5647e42b2ceb572c2948`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 6.9 MB (6902535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e3773858ad48aca220a5cfe56df146822d1bf920234c249d7c6d3fc936fe85`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a9291ccc131f35749bacacffcec55a5f1001ceefafbac00603fddd2cb07ffe`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afebf85e09ce9df2a3ec0c97256101d165835fd531a0bfeb04065b8d7845ef2`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 49.6 MB (49622114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9247a49c1f0b18ac2cc953ef93c10cdf24efe6227e4cc93d0c657dd84cd25742`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aff87c766172bf423aba5677dc35af0bcb8b91988cc3a224a674ebc5a74a004`  
		Last Modified: Thu, 21 Nov 2024 00:24:59 GMT  
		Size: 64.4 MB (64360958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cc72d643da6df2bd14e2b233ed0c2fddc9ff336f52d7451f9fbcaa7b03b939`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e23f27309a673d21df4d6b5f3dbf8331050dc00dea09f0159794c735bb50114`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:08555608f0ba44fdd231e4cf9f5cb977fcbd2d5b648a2a1959d5503a6c339313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14799183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea94bd97b65774e0422766f801f49ea4277aac2e7346159dc6a4171fd62ee10`

```dockerfile
```

-	Layers:
	-	`sha256:1174e925b3a4bf1c77c5afd35cb0a7b9e99fe494d1cb4b1de725327bdf2ae371`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 14.8 MB (14764233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5f477512a8770433ae872d8713e19c78da10c07deb95a448a6ba86928c32302`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 35.0 KB (34950 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6cee01d37675de33f46215162c641e54718f1ac37475571cbcaf7b6e2142c36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175477229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35859c321b65726b5b1c462dcd17649ce2df7772d6fb423362652722deae796`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6451580cceb6ab22e40316ff10f58ef0812032136a662d3f4c7a1ea47d97211e`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbb151ca502c2ff3727bca04b55f14c0eb91ad908a6f58473165a2f64994287`  
		Last Modified: Thu, 21 Nov 2024 00:28:06 GMT  
		Size: 48.5 MB (48485082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98634756c7a23cca4e16c16a3cbfc031532faf5947ec95bff16c1d3eca9ba253`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b92de65da79c3100d476e31d6aa125963ee5644d05e292c3f7ab8e708b8878`  
		Last Modified: Thu, 21 Nov 2024 00:28:07 GMT  
		Size: 71.9 MB (71906406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd198337bce0efd5f21deeb19858c1f39c65213fb91e8ef95de67e5f32e0e1c`  
		Last Modified: Thu, 21 Nov 2024 00:28:05 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7833aab7712665108fb352f9ba6db2718d608fda4d2d5a7fc7848c6fe78926ae`  
		Last Modified: Thu, 21 Nov 2024 00:28:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:00361d32ec81c0398af6925d2ba0b589f93d1a4a7b441f1bab31e27384244bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14794510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b5a7c181fe7864b40d90f367527b322208f5bb2b1fb419de6eaecedc3fd7ed`

```dockerfile
```

-	Layers:
	-	`sha256:51cdbdeda1bdc7d8a8b437b8e6c31d5fdd9ec46d604440136948a49b24406592`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 14.8 MB (14759311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d05e7863b79f8aa99b3619a87bfc5b11c04f63c248ac93f17565e8cbb0a1af2`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 35.2 KB (35199 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40`

```console
$ docker pull mysql@sha256:8a685d21a4ebc7e8e6541115b8fef17a872d669184b8100c4c180e6498d09a6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.40` - linux; amd64

```console
$ docker pull mysql@sha256:600242f3651fd71af32573d613dc98870ac61237714ea230ea784615ae56ad87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170977378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c9538bbb34e2fa4804bc95b61014dc154906a3923898531804e280e89f361b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48db9f7ea45e51212dd1767f5624cc179e510fd2336cb21366b52bddfd0c834`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57907e4cc4f2f352e028caad5c77b978b85227de33b70e0d1568b5abc8dbb858`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c10ebc08f661c8844aedb2a0d2a6031bbf4c89a7a2f5647e42b2ceb572c2948`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 6.9 MB (6902535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e3773858ad48aca220a5cfe56df146822d1bf920234c249d7c6d3fc936fe85`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a9291ccc131f35749bacacffcec55a5f1001ceefafbac00603fddd2cb07ffe`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afebf85e09ce9df2a3ec0c97256101d165835fd531a0bfeb04065b8d7845ef2`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 49.6 MB (49622114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9247a49c1f0b18ac2cc953ef93c10cdf24efe6227e4cc93d0c657dd84cd25742`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aff87c766172bf423aba5677dc35af0bcb8b91988cc3a224a674ebc5a74a004`  
		Last Modified: Thu, 21 Nov 2024 00:24:59 GMT  
		Size: 64.4 MB (64360958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cc72d643da6df2bd14e2b233ed0c2fddc9ff336f52d7451f9fbcaa7b03b939`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e23f27309a673d21df4d6b5f3dbf8331050dc00dea09f0159794c735bb50114`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40` - unknown; unknown

```console
$ docker pull mysql@sha256:08555608f0ba44fdd231e4cf9f5cb977fcbd2d5b648a2a1959d5503a6c339313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14799183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea94bd97b65774e0422766f801f49ea4277aac2e7346159dc6a4171fd62ee10`

```dockerfile
```

-	Layers:
	-	`sha256:1174e925b3a4bf1c77c5afd35cb0a7b9e99fe494d1cb4b1de725327bdf2ae371`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 14.8 MB (14764233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5f477512a8770433ae872d8713e19c78da10c07deb95a448a6ba86928c32302`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 35.0 KB (34950 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.40` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6cee01d37675de33f46215162c641e54718f1ac37475571cbcaf7b6e2142c36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175477229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35859c321b65726b5b1c462dcd17649ce2df7772d6fb423362652722deae796`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6451580cceb6ab22e40316ff10f58ef0812032136a662d3f4c7a1ea47d97211e`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbb151ca502c2ff3727bca04b55f14c0eb91ad908a6f58473165a2f64994287`  
		Last Modified: Thu, 21 Nov 2024 00:28:06 GMT  
		Size: 48.5 MB (48485082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98634756c7a23cca4e16c16a3cbfc031532faf5947ec95bff16c1d3eca9ba253`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b92de65da79c3100d476e31d6aa125963ee5644d05e292c3f7ab8e708b8878`  
		Last Modified: Thu, 21 Nov 2024 00:28:07 GMT  
		Size: 71.9 MB (71906406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd198337bce0efd5f21deeb19858c1f39c65213fb91e8ef95de67e5f32e0e1c`  
		Last Modified: Thu, 21 Nov 2024 00:28:05 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7833aab7712665108fb352f9ba6db2718d608fda4d2d5a7fc7848c6fe78926ae`  
		Last Modified: Thu, 21 Nov 2024 00:28:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40` - unknown; unknown

```console
$ docker pull mysql@sha256:00361d32ec81c0398af6925d2ba0b589f93d1a4a7b441f1bab31e27384244bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14794510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b5a7c181fe7864b40d90f367527b322208f5bb2b1fb419de6eaecedc3fd7ed`

```dockerfile
```

-	Layers:
	-	`sha256:51cdbdeda1bdc7d8a8b437b8e6c31d5fdd9ec46d604440136948a49b24406592`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 14.8 MB (14759311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d05e7863b79f8aa99b3619a87bfc5b11c04f63c248ac93f17565e8cbb0a1af2`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 35.2 KB (35199 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40-bookworm`

```console
$ docker pull mysql@sha256:3a797469a0c936822c3cc93c1e94f96d91d854c5c81eac45840b31464409b4ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.40-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:ca94d886e43c0541f834572c6861097113aa71d98fbc9bcce8a44ad3ec81a5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184179467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c32752b103f2f64b80cbdeca13f1062b5ae4a9cd8cb09ed3ebaa003241f4064`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb40b74f92c54287c4079c439813da763527bb1ff50ac099ed2e73e03f64cff`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70616fc1634f61422208d4490a405cb911b0f625facb00442d02aff0431c0a8d`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 4.4 MB (4422768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6366761dde571e9b27a79630976f734a901c05aed3df475cafa24686195454c5`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 1.4 MB (1445956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d9fb32a0c8e449173648e78aa4643bc85863e6743f833589f5045901b60fc2`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6f55273db7e4976edde7e688b786fe49243f37da6418c2f870188dfa5f672e`  
		Last Modified: Tue, 12 Nov 2024 02:14:39 GMT  
		Size: 15.3 MB (15295550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e10f7d81b1219ea142bf958f5e509737d72e91b6dab6c79877c01ce1618941`  
		Last Modified: Tue, 12 Nov 2024 02:14:39 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7562d4a81907f8b99d8942e2cb3ce93817c8eb39f2a0b7261260a863d41ac0a`  
		Last Modified: Tue, 12 Nov 2024 02:14:39 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324695993a9ceb2cbe6f2c7404314809fab57047e516d36e84587f9c631154d1`  
		Last Modified: Tue, 12 Nov 2024 02:14:41 GMT  
		Size: 133.9 MB (133876931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f5177793182d807ab87d637bca9718d80c9bee31c6db5fed0aef303ea49a61`  
		Last Modified: Tue, 12 Nov 2024 02:14:40 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfbda283dc78b30ba1332df28dec334f96a6d8fb0184140fc7f4e9efd285b71`  
		Last Modified: Tue, 12 Nov 2024 02:14:40 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ea090265c5dfbd982fc6e82622350ebda57ae50a86e8e3c40722885188837f`  
		Last Modified: Tue, 12 Nov 2024 02:14:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:21188c8c9bd9f1cd9746572d5c0072e268888a686019f5532a678d99630a357c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4033593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e75c0557c8dc311b60f6392b62837d4c02812bccbb16d12f2ae194f24f13a93`

```dockerfile
```

-	Layers:
	-	`sha256:e82e8f27a7b0f650ddfb751e22a194104691519f383089be9a5dc3db77820931`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 4.0 MB (3999297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a45a9157f9b91778d4c525ef7ddca9057fbc93977c5647eb986bd8c6e949c01e`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40-debian`

```console
$ docker pull mysql@sha256:3a797469a0c936822c3cc93c1e94f96d91d854c5c81eac45840b31464409b4ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.40-debian` - linux; amd64

```console
$ docker pull mysql@sha256:ca94d886e43c0541f834572c6861097113aa71d98fbc9bcce8a44ad3ec81a5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184179467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c32752b103f2f64b80cbdeca13f1062b5ae4a9cd8cb09ed3ebaa003241f4064`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb40b74f92c54287c4079c439813da763527bb1ff50ac099ed2e73e03f64cff`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70616fc1634f61422208d4490a405cb911b0f625facb00442d02aff0431c0a8d`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 4.4 MB (4422768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6366761dde571e9b27a79630976f734a901c05aed3df475cafa24686195454c5`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 1.4 MB (1445956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d9fb32a0c8e449173648e78aa4643bc85863e6743f833589f5045901b60fc2`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6f55273db7e4976edde7e688b786fe49243f37da6418c2f870188dfa5f672e`  
		Last Modified: Tue, 12 Nov 2024 02:14:39 GMT  
		Size: 15.3 MB (15295550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e10f7d81b1219ea142bf958f5e509737d72e91b6dab6c79877c01ce1618941`  
		Last Modified: Tue, 12 Nov 2024 02:14:39 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7562d4a81907f8b99d8942e2cb3ce93817c8eb39f2a0b7261260a863d41ac0a`  
		Last Modified: Tue, 12 Nov 2024 02:14:39 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324695993a9ceb2cbe6f2c7404314809fab57047e516d36e84587f9c631154d1`  
		Last Modified: Tue, 12 Nov 2024 02:14:41 GMT  
		Size: 133.9 MB (133876931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f5177793182d807ab87d637bca9718d80c9bee31c6db5fed0aef303ea49a61`  
		Last Modified: Tue, 12 Nov 2024 02:14:40 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfbda283dc78b30ba1332df28dec334f96a6d8fb0184140fc7f4e9efd285b71`  
		Last Modified: Tue, 12 Nov 2024 02:14:40 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ea090265c5dfbd982fc6e82622350ebda57ae50a86e8e3c40722885188837f`  
		Last Modified: Tue, 12 Nov 2024 02:14:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:21188c8c9bd9f1cd9746572d5c0072e268888a686019f5532a678d99630a357c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4033593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e75c0557c8dc311b60f6392b62837d4c02812bccbb16d12f2ae194f24f13a93`

```dockerfile
```

-	Layers:
	-	`sha256:e82e8f27a7b0f650ddfb751e22a194104691519f383089be9a5dc3db77820931`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 4.0 MB (3999297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a45a9157f9b91778d4c525ef7ddca9057fbc93977c5647eb986bd8c6e949c01e`  
		Last Modified: Tue, 12 Nov 2024 02:14:38 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40-oracle`

```console
$ docker pull mysql@sha256:8a685d21a4ebc7e8e6541115b8fef17a872d669184b8100c4c180e6498d09a6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.40-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:600242f3651fd71af32573d613dc98870ac61237714ea230ea784615ae56ad87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170977378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c9538bbb34e2fa4804bc95b61014dc154906a3923898531804e280e89f361b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48db9f7ea45e51212dd1767f5624cc179e510fd2336cb21366b52bddfd0c834`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57907e4cc4f2f352e028caad5c77b978b85227de33b70e0d1568b5abc8dbb858`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c10ebc08f661c8844aedb2a0d2a6031bbf4c89a7a2f5647e42b2ceb572c2948`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 6.9 MB (6902535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e3773858ad48aca220a5cfe56df146822d1bf920234c249d7c6d3fc936fe85`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a9291ccc131f35749bacacffcec55a5f1001ceefafbac00603fddd2cb07ffe`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afebf85e09ce9df2a3ec0c97256101d165835fd531a0bfeb04065b8d7845ef2`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 49.6 MB (49622114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9247a49c1f0b18ac2cc953ef93c10cdf24efe6227e4cc93d0c657dd84cd25742`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aff87c766172bf423aba5677dc35af0bcb8b91988cc3a224a674ebc5a74a004`  
		Last Modified: Thu, 21 Nov 2024 00:24:59 GMT  
		Size: 64.4 MB (64360958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cc72d643da6df2bd14e2b233ed0c2fddc9ff336f52d7451f9fbcaa7b03b939`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e23f27309a673d21df4d6b5f3dbf8331050dc00dea09f0159794c735bb50114`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:08555608f0ba44fdd231e4cf9f5cb977fcbd2d5b648a2a1959d5503a6c339313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14799183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea94bd97b65774e0422766f801f49ea4277aac2e7346159dc6a4171fd62ee10`

```dockerfile
```

-	Layers:
	-	`sha256:1174e925b3a4bf1c77c5afd35cb0a7b9e99fe494d1cb4b1de725327bdf2ae371`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 14.8 MB (14764233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5f477512a8770433ae872d8713e19c78da10c07deb95a448a6ba86928c32302`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 35.0 KB (34950 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.40-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6cee01d37675de33f46215162c641e54718f1ac37475571cbcaf7b6e2142c36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175477229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35859c321b65726b5b1c462dcd17649ce2df7772d6fb423362652722deae796`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6451580cceb6ab22e40316ff10f58ef0812032136a662d3f4c7a1ea47d97211e`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbb151ca502c2ff3727bca04b55f14c0eb91ad908a6f58473165a2f64994287`  
		Last Modified: Thu, 21 Nov 2024 00:28:06 GMT  
		Size: 48.5 MB (48485082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98634756c7a23cca4e16c16a3cbfc031532faf5947ec95bff16c1d3eca9ba253`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b92de65da79c3100d476e31d6aa125963ee5644d05e292c3f7ab8e708b8878`  
		Last Modified: Thu, 21 Nov 2024 00:28:07 GMT  
		Size: 71.9 MB (71906406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd198337bce0efd5f21deeb19858c1f39c65213fb91e8ef95de67e5f32e0e1c`  
		Last Modified: Thu, 21 Nov 2024 00:28:05 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7833aab7712665108fb352f9ba6db2718d608fda4d2d5a7fc7848c6fe78926ae`  
		Last Modified: Thu, 21 Nov 2024 00:28:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:00361d32ec81c0398af6925d2ba0b589f93d1a4a7b441f1bab31e27384244bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14794510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b5a7c181fe7864b40d90f367527b322208f5bb2b1fb419de6eaecedc3fd7ed`

```dockerfile
```

-	Layers:
	-	`sha256:51cdbdeda1bdc7d8a8b437b8e6c31d5fdd9ec46d604440136948a49b24406592`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 14.8 MB (14759311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d05e7863b79f8aa99b3619a87bfc5b11c04f63c248ac93f17565e8cbb0a1af2`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 35.2 KB (35199 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40-oraclelinux9`

```console
$ docker pull mysql@sha256:8a685d21a4ebc7e8e6541115b8fef17a872d669184b8100c4c180e6498d09a6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.40-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:600242f3651fd71af32573d613dc98870ac61237714ea230ea784615ae56ad87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170977378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c9538bbb34e2fa4804bc95b61014dc154906a3923898531804e280e89f361b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48db9f7ea45e51212dd1767f5624cc179e510fd2336cb21366b52bddfd0c834`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57907e4cc4f2f352e028caad5c77b978b85227de33b70e0d1568b5abc8dbb858`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c10ebc08f661c8844aedb2a0d2a6031bbf4c89a7a2f5647e42b2ceb572c2948`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 6.9 MB (6902535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e3773858ad48aca220a5cfe56df146822d1bf920234c249d7c6d3fc936fe85`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a9291ccc131f35749bacacffcec55a5f1001ceefafbac00603fddd2cb07ffe`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afebf85e09ce9df2a3ec0c97256101d165835fd531a0bfeb04065b8d7845ef2`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 49.6 MB (49622114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9247a49c1f0b18ac2cc953ef93c10cdf24efe6227e4cc93d0c657dd84cd25742`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aff87c766172bf423aba5677dc35af0bcb8b91988cc3a224a674ebc5a74a004`  
		Last Modified: Thu, 21 Nov 2024 00:24:59 GMT  
		Size: 64.4 MB (64360958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cc72d643da6df2bd14e2b233ed0c2fddc9ff336f52d7451f9fbcaa7b03b939`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e23f27309a673d21df4d6b5f3dbf8331050dc00dea09f0159794c735bb50114`  
		Last Modified: Thu, 21 Nov 2024 00:24:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:08555608f0ba44fdd231e4cf9f5cb977fcbd2d5b648a2a1959d5503a6c339313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14799183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea94bd97b65774e0422766f801f49ea4277aac2e7346159dc6a4171fd62ee10`

```dockerfile
```

-	Layers:
	-	`sha256:1174e925b3a4bf1c77c5afd35cb0a7b9e99fe494d1cb4b1de725327bdf2ae371`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 14.8 MB (14764233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5f477512a8770433ae872d8713e19c78da10c07deb95a448a6ba86928c32302`  
		Last Modified: Thu, 21 Nov 2024 00:24:57 GMT  
		Size: 35.0 KB (34950 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.40-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6cee01d37675de33f46215162c641e54718f1ac37475571cbcaf7b6e2142c36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175477229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35859c321b65726b5b1c462dcd17649ce2df7772d6fb423362652722deae796`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6451580cceb6ab22e40316ff10f58ef0812032136a662d3f4c7a1ea47d97211e`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbb151ca502c2ff3727bca04b55f14c0eb91ad908a6f58473165a2f64994287`  
		Last Modified: Thu, 21 Nov 2024 00:28:06 GMT  
		Size: 48.5 MB (48485082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98634756c7a23cca4e16c16a3cbfc031532faf5947ec95bff16c1d3eca9ba253`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b92de65da79c3100d476e31d6aa125963ee5644d05e292c3f7ab8e708b8878`  
		Last Modified: Thu, 21 Nov 2024 00:28:07 GMT  
		Size: 71.9 MB (71906406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd198337bce0efd5f21deeb19858c1f39c65213fb91e8ef95de67e5f32e0e1c`  
		Last Modified: Thu, 21 Nov 2024 00:28:05 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7833aab7712665108fb352f9ba6db2718d608fda4d2d5a7fc7848c6fe78926ae`  
		Last Modified: Thu, 21 Nov 2024 00:28:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:00361d32ec81c0398af6925d2ba0b589f93d1a4a7b441f1bab31e27384244bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14794510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b5a7c181fe7864b40d90f367527b322208f5bb2b1fb419de6eaecedc3fd7ed`

```dockerfile
```

-	Layers:
	-	`sha256:51cdbdeda1bdc7d8a8b437b8e6c31d5fdd9ec46d604440136948a49b24406592`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 14.8 MB (14759311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d05e7863b79f8aa99b3619a87bfc5b11c04f63c248ac93f17565e8cbb0a1af2`  
		Last Modified: Thu, 21 Nov 2024 00:28:04 GMT  
		Size: 35.2 KB (35199 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:2bed89deaa6122df7e3bfdb3006d2f09251e2fa925bdd4f6a5ccff7badf070ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:8d111b535dbe6d9fbdaafcb0e3157aff64664ef5052ceae3c57f974166a6cff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171514588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bb57dc6b1d1f9bbd9ab9843af36264c74b6944360d37703fc8cdb932c1587f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5e9755d4041de874322937a7e4aba7eae546b110eaf21c99fd9ee849a31f0b`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6f939b5bdeb93950dd408d5e339b273a43e8129bb908aa25a492fd41925b5e`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4825be18a9da34ab830e99c285416149b22324acc5d70e0fe35719306a672a39`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 6.9 MB (6902532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d101851db8708b91cdb31331ed5fd7584d9109fd10ae799295f8e4b1c372ee`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e6fd8a5fc375e4c5061959d05b0c1727be47165db7fcf903582c94045798ff`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b46238a9af0862e613cea2905d7fa437227a27976fbfcac6e82db8164ba40d`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 47.6 MB (47559393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13a1e3aee9ee85855737c1af5191eef5fbf6d612b81b87f12fcd6dd59d7594a`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444e8e4164f357b6d69d3d1932320dbd2f6e3f0970bf6ee1cacb47a88e87780f`  
		Last Modified: Thu, 21 Nov 2024 00:24:51 GMT  
		Size: 67.0 MB (66961014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef40cced209d5affe747d3e62bcaef3f4800e24279555efd1d9a0a68d5902c1`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:d24e1e14db4144ad85299ee67329e83eab737d53eabb1c765795ef88d63f8d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97e864c12a8d34ccf20924c9821a42b95f8a22305076fb1ef870ab42aa83988`

```dockerfile
```

-	Layers:
	-	`sha256:978b2ae2ea66ace5f526e29cbe706f1d9b0139220749975cfb696fbcbc463daf`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 14.9 MB (14871754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade4558bfff869010112ad9fbb8710524f7b764f662ceaedb75071b90e9a9d7c`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 34.2 KB (34248 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2516a10a1ea246e0b9391b259194e9f0c6a0669dfd1fccc337e62450f657acc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168737549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6672c03fe2b69c64f378bc123bffddae0ceb6db9d80968d238151dffa2706c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd77c1317d3aa167ce525e562b4150ca934ca0a6931888f4facee3c2832b430`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6319ad690265786884f89a8528c43a7641f5ec4ee13646914915d4fbbeef78b`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 46.5 MB (46450201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e66d86f17d19ad1ee543340630050da5690d888f02bc186b07736702382eb09`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d04267626c09db36ba57db446ffa128a79b92b28e520e9bbb60d84c92b94c0`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 67.2 MB (67201722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58f7aad98ac58f55673caa5b917718391795ff9a3b1f479fc7b787d78f3a354`  
		Last Modified: Thu, 21 Nov 2024 00:26:32 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:3d5efe1ed7cf29dad01a2c69594ceb6b0ca523977f24d2767d3ef13de6f6b9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131563af08c9fd291fd2f7c813846125fe715f006a3d396bde57881e1cc0a186`

```dockerfile
```

-	Layers:
	-	`sha256:0c0d39bebfbb0c7af2b65758f081a44f9b9d036cb843b36bf3d346a568b44c6b`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 14.9 MB (14866904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e11d0d508b78947bc35881c46c4902ec23e4a3e0154d972b7b3bbd47d11d51c`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 34.6 KB (34553 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:2bed89deaa6122df7e3bfdb3006d2f09251e2fa925bdd4f6a5ccff7badf070ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8d111b535dbe6d9fbdaafcb0e3157aff64664ef5052ceae3c57f974166a6cff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171514588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bb57dc6b1d1f9bbd9ab9843af36264c74b6944360d37703fc8cdb932c1587f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5e9755d4041de874322937a7e4aba7eae546b110eaf21c99fd9ee849a31f0b`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6f939b5bdeb93950dd408d5e339b273a43e8129bb908aa25a492fd41925b5e`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4825be18a9da34ab830e99c285416149b22324acc5d70e0fe35719306a672a39`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 6.9 MB (6902532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d101851db8708b91cdb31331ed5fd7584d9109fd10ae799295f8e4b1c372ee`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e6fd8a5fc375e4c5061959d05b0c1727be47165db7fcf903582c94045798ff`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b46238a9af0862e613cea2905d7fa437227a27976fbfcac6e82db8164ba40d`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 47.6 MB (47559393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13a1e3aee9ee85855737c1af5191eef5fbf6d612b81b87f12fcd6dd59d7594a`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444e8e4164f357b6d69d3d1932320dbd2f6e3f0970bf6ee1cacb47a88e87780f`  
		Last Modified: Thu, 21 Nov 2024 00:24:51 GMT  
		Size: 67.0 MB (66961014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef40cced209d5affe747d3e62bcaef3f4800e24279555efd1d9a0a68d5902c1`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d24e1e14db4144ad85299ee67329e83eab737d53eabb1c765795ef88d63f8d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97e864c12a8d34ccf20924c9821a42b95f8a22305076fb1ef870ab42aa83988`

```dockerfile
```

-	Layers:
	-	`sha256:978b2ae2ea66ace5f526e29cbe706f1d9b0139220749975cfb696fbcbc463daf`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 14.9 MB (14871754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade4558bfff869010112ad9fbb8710524f7b764f662ceaedb75071b90e9a9d7c`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 34.2 KB (34248 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2516a10a1ea246e0b9391b259194e9f0c6a0669dfd1fccc337e62450f657acc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168737549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6672c03fe2b69c64f378bc123bffddae0ceb6db9d80968d238151dffa2706c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd77c1317d3aa167ce525e562b4150ca934ca0a6931888f4facee3c2832b430`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6319ad690265786884f89a8528c43a7641f5ec4ee13646914915d4fbbeef78b`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 46.5 MB (46450201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e66d86f17d19ad1ee543340630050da5690d888f02bc186b07736702382eb09`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d04267626c09db36ba57db446ffa128a79b92b28e520e9bbb60d84c92b94c0`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 67.2 MB (67201722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58f7aad98ac58f55673caa5b917718391795ff9a3b1f479fc7b787d78f3a354`  
		Last Modified: Thu, 21 Nov 2024 00:26:32 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3d5efe1ed7cf29dad01a2c69594ceb6b0ca523977f24d2767d3ef13de6f6b9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131563af08c9fd291fd2f7c813846125fe715f006a3d396bde57881e1cc0a186`

```dockerfile
```

-	Layers:
	-	`sha256:0c0d39bebfbb0c7af2b65758f081a44f9b9d036cb843b36bf3d346a568b44c6b`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 14.9 MB (14866904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e11d0d508b78947bc35881c46c4902ec23e4a3e0154d972b7b3bbd47d11d51c`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 34.6 KB (34553 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:2bed89deaa6122df7e3bfdb3006d2f09251e2fa925bdd4f6a5ccff7badf070ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:8d111b535dbe6d9fbdaafcb0e3157aff64664ef5052ceae3c57f974166a6cff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171514588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bb57dc6b1d1f9bbd9ab9843af36264c74b6944360d37703fc8cdb932c1587f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5e9755d4041de874322937a7e4aba7eae546b110eaf21c99fd9ee849a31f0b`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6f939b5bdeb93950dd408d5e339b273a43e8129bb908aa25a492fd41925b5e`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4825be18a9da34ab830e99c285416149b22324acc5d70e0fe35719306a672a39`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 6.9 MB (6902532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d101851db8708b91cdb31331ed5fd7584d9109fd10ae799295f8e4b1c372ee`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e6fd8a5fc375e4c5061959d05b0c1727be47165db7fcf903582c94045798ff`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b46238a9af0862e613cea2905d7fa437227a27976fbfcac6e82db8164ba40d`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 47.6 MB (47559393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13a1e3aee9ee85855737c1af5191eef5fbf6d612b81b87f12fcd6dd59d7594a`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444e8e4164f357b6d69d3d1932320dbd2f6e3f0970bf6ee1cacb47a88e87780f`  
		Last Modified: Thu, 21 Nov 2024 00:24:51 GMT  
		Size: 67.0 MB (66961014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef40cced209d5affe747d3e62bcaef3f4800e24279555efd1d9a0a68d5902c1`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d24e1e14db4144ad85299ee67329e83eab737d53eabb1c765795ef88d63f8d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97e864c12a8d34ccf20924c9821a42b95f8a22305076fb1ef870ab42aa83988`

```dockerfile
```

-	Layers:
	-	`sha256:978b2ae2ea66ace5f526e29cbe706f1d9b0139220749975cfb696fbcbc463daf`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 14.9 MB (14871754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade4558bfff869010112ad9fbb8710524f7b764f662ceaedb75071b90e9a9d7c`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 34.2 KB (34248 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2516a10a1ea246e0b9391b259194e9f0c6a0669dfd1fccc337e62450f657acc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168737549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6672c03fe2b69c64f378bc123bffddae0ceb6db9d80968d238151dffa2706c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd77c1317d3aa167ce525e562b4150ca934ca0a6931888f4facee3c2832b430`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6319ad690265786884f89a8528c43a7641f5ec4ee13646914915d4fbbeef78b`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 46.5 MB (46450201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e66d86f17d19ad1ee543340630050da5690d888f02bc186b07736702382eb09`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d04267626c09db36ba57db446ffa128a79b92b28e520e9bbb60d84c92b94c0`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 67.2 MB (67201722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58f7aad98ac58f55673caa5b917718391795ff9a3b1f479fc7b787d78f3a354`  
		Last Modified: Thu, 21 Nov 2024 00:26:32 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3d5efe1ed7cf29dad01a2c69594ceb6b0ca523977f24d2767d3ef13de6f6b9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131563af08c9fd291fd2f7c813846125fe715f006a3d396bde57881e1cc0a186`

```dockerfile
```

-	Layers:
	-	`sha256:0c0d39bebfbb0c7af2b65758f081a44f9b9d036cb843b36bf3d346a568b44c6b`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 14.9 MB (14866904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e11d0d508b78947bc35881c46c4902ec23e4a3e0154d972b7b3bbd47d11d51c`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 34.6 KB (34553 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.3`

```console
$ docker pull mysql@sha256:2bed89deaa6122df7e3bfdb3006d2f09251e2fa925bdd4f6a5ccff7badf070ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.3` - linux; amd64

```console
$ docker pull mysql@sha256:8d111b535dbe6d9fbdaafcb0e3157aff64664ef5052ceae3c57f974166a6cff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171514588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bb57dc6b1d1f9bbd9ab9843af36264c74b6944360d37703fc8cdb932c1587f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5e9755d4041de874322937a7e4aba7eae546b110eaf21c99fd9ee849a31f0b`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6f939b5bdeb93950dd408d5e339b273a43e8129bb908aa25a492fd41925b5e`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4825be18a9da34ab830e99c285416149b22324acc5d70e0fe35719306a672a39`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 6.9 MB (6902532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d101851db8708b91cdb31331ed5fd7584d9109fd10ae799295f8e4b1c372ee`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e6fd8a5fc375e4c5061959d05b0c1727be47165db7fcf903582c94045798ff`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b46238a9af0862e613cea2905d7fa437227a27976fbfcac6e82db8164ba40d`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 47.6 MB (47559393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13a1e3aee9ee85855737c1af5191eef5fbf6d612b81b87f12fcd6dd59d7594a`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444e8e4164f357b6d69d3d1932320dbd2f6e3f0970bf6ee1cacb47a88e87780f`  
		Last Modified: Thu, 21 Nov 2024 00:24:51 GMT  
		Size: 67.0 MB (66961014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef40cced209d5affe747d3e62bcaef3f4800e24279555efd1d9a0a68d5902c1`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3` - unknown; unknown

```console
$ docker pull mysql@sha256:d24e1e14db4144ad85299ee67329e83eab737d53eabb1c765795ef88d63f8d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97e864c12a8d34ccf20924c9821a42b95f8a22305076fb1ef870ab42aa83988`

```dockerfile
```

-	Layers:
	-	`sha256:978b2ae2ea66ace5f526e29cbe706f1d9b0139220749975cfb696fbcbc463daf`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 14.9 MB (14871754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade4558bfff869010112ad9fbb8710524f7b764f662ceaedb75071b90e9a9d7c`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 34.2 KB (34248 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.3` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2516a10a1ea246e0b9391b259194e9f0c6a0669dfd1fccc337e62450f657acc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168737549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6672c03fe2b69c64f378bc123bffddae0ceb6db9d80968d238151dffa2706c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd77c1317d3aa167ce525e562b4150ca934ca0a6931888f4facee3c2832b430`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6319ad690265786884f89a8528c43a7641f5ec4ee13646914915d4fbbeef78b`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 46.5 MB (46450201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e66d86f17d19ad1ee543340630050da5690d888f02bc186b07736702382eb09`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d04267626c09db36ba57db446ffa128a79b92b28e520e9bbb60d84c92b94c0`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 67.2 MB (67201722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58f7aad98ac58f55673caa5b917718391795ff9a3b1f479fc7b787d78f3a354`  
		Last Modified: Thu, 21 Nov 2024 00:26:32 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3` - unknown; unknown

```console
$ docker pull mysql@sha256:3d5efe1ed7cf29dad01a2c69594ceb6b0ca523977f24d2767d3ef13de6f6b9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131563af08c9fd291fd2f7c813846125fe715f006a3d396bde57881e1cc0a186`

```dockerfile
```

-	Layers:
	-	`sha256:0c0d39bebfbb0c7af2b65758f081a44f9b9d036cb843b36bf3d346a568b44c6b`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 14.9 MB (14866904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e11d0d508b78947bc35881c46c4902ec23e4a3e0154d972b7b3bbd47d11d51c`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 34.6 KB (34553 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.3-oracle`

```console
$ docker pull mysql@sha256:2bed89deaa6122df7e3bfdb3006d2f09251e2fa925bdd4f6a5ccff7badf070ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.3-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8d111b535dbe6d9fbdaafcb0e3157aff64664ef5052ceae3c57f974166a6cff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171514588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bb57dc6b1d1f9bbd9ab9843af36264c74b6944360d37703fc8cdb932c1587f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5e9755d4041de874322937a7e4aba7eae546b110eaf21c99fd9ee849a31f0b`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6f939b5bdeb93950dd408d5e339b273a43e8129bb908aa25a492fd41925b5e`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4825be18a9da34ab830e99c285416149b22324acc5d70e0fe35719306a672a39`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 6.9 MB (6902532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d101851db8708b91cdb31331ed5fd7584d9109fd10ae799295f8e4b1c372ee`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e6fd8a5fc375e4c5061959d05b0c1727be47165db7fcf903582c94045798ff`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b46238a9af0862e613cea2905d7fa437227a27976fbfcac6e82db8164ba40d`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 47.6 MB (47559393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13a1e3aee9ee85855737c1af5191eef5fbf6d612b81b87f12fcd6dd59d7594a`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444e8e4164f357b6d69d3d1932320dbd2f6e3f0970bf6ee1cacb47a88e87780f`  
		Last Modified: Thu, 21 Nov 2024 00:24:51 GMT  
		Size: 67.0 MB (66961014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef40cced209d5affe747d3e62bcaef3f4800e24279555efd1d9a0a68d5902c1`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d24e1e14db4144ad85299ee67329e83eab737d53eabb1c765795ef88d63f8d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97e864c12a8d34ccf20924c9821a42b95f8a22305076fb1ef870ab42aa83988`

```dockerfile
```

-	Layers:
	-	`sha256:978b2ae2ea66ace5f526e29cbe706f1d9b0139220749975cfb696fbcbc463daf`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 14.9 MB (14871754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade4558bfff869010112ad9fbb8710524f7b764f662ceaedb75071b90e9a9d7c`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 34.2 KB (34248 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.3-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2516a10a1ea246e0b9391b259194e9f0c6a0669dfd1fccc337e62450f657acc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168737549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6672c03fe2b69c64f378bc123bffddae0ceb6db9d80968d238151dffa2706c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd77c1317d3aa167ce525e562b4150ca934ca0a6931888f4facee3c2832b430`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6319ad690265786884f89a8528c43a7641f5ec4ee13646914915d4fbbeef78b`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 46.5 MB (46450201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e66d86f17d19ad1ee543340630050da5690d888f02bc186b07736702382eb09`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d04267626c09db36ba57db446ffa128a79b92b28e520e9bbb60d84c92b94c0`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 67.2 MB (67201722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58f7aad98ac58f55673caa5b917718391795ff9a3b1f479fc7b787d78f3a354`  
		Last Modified: Thu, 21 Nov 2024 00:26:32 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3d5efe1ed7cf29dad01a2c69594ceb6b0ca523977f24d2767d3ef13de6f6b9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131563af08c9fd291fd2f7c813846125fe715f006a3d396bde57881e1cc0a186`

```dockerfile
```

-	Layers:
	-	`sha256:0c0d39bebfbb0c7af2b65758f081a44f9b9d036cb843b36bf3d346a568b44c6b`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 14.9 MB (14866904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e11d0d508b78947bc35881c46c4902ec23e4a3e0154d972b7b3bbd47d11d51c`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 34.6 KB (34553 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.3-oraclelinux9`

```console
$ docker pull mysql@sha256:2bed89deaa6122df7e3bfdb3006d2f09251e2fa925bdd4f6a5ccff7badf070ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.3-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:8d111b535dbe6d9fbdaafcb0e3157aff64664ef5052ceae3c57f974166a6cff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171514588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bb57dc6b1d1f9bbd9ab9843af36264c74b6944360d37703fc8cdb932c1587f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5e9755d4041de874322937a7e4aba7eae546b110eaf21c99fd9ee849a31f0b`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6f939b5bdeb93950dd408d5e339b273a43e8129bb908aa25a492fd41925b5e`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4825be18a9da34ab830e99c285416149b22324acc5d70e0fe35719306a672a39`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 6.9 MB (6902532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d101851db8708b91cdb31331ed5fd7584d9109fd10ae799295f8e4b1c372ee`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e6fd8a5fc375e4c5061959d05b0c1727be47165db7fcf903582c94045798ff`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b46238a9af0862e613cea2905d7fa437227a27976fbfcac6e82db8164ba40d`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 47.6 MB (47559393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13a1e3aee9ee85855737c1af5191eef5fbf6d612b81b87f12fcd6dd59d7594a`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444e8e4164f357b6d69d3d1932320dbd2f6e3f0970bf6ee1cacb47a88e87780f`  
		Last Modified: Thu, 21 Nov 2024 00:24:51 GMT  
		Size: 67.0 MB (66961014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef40cced209d5affe747d3e62bcaef3f4800e24279555efd1d9a0a68d5902c1`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d24e1e14db4144ad85299ee67329e83eab737d53eabb1c765795ef88d63f8d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97e864c12a8d34ccf20924c9821a42b95f8a22305076fb1ef870ab42aa83988`

```dockerfile
```

-	Layers:
	-	`sha256:978b2ae2ea66ace5f526e29cbe706f1d9b0139220749975cfb696fbcbc463daf`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 14.9 MB (14871754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade4558bfff869010112ad9fbb8710524f7b764f662ceaedb75071b90e9a9d7c`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 34.2 KB (34248 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.3-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2516a10a1ea246e0b9391b259194e9f0c6a0669dfd1fccc337e62450f657acc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168737549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6672c03fe2b69c64f378bc123bffddae0ceb6db9d80968d238151dffa2706c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd77c1317d3aa167ce525e562b4150ca934ca0a6931888f4facee3c2832b430`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6319ad690265786884f89a8528c43a7641f5ec4ee13646914915d4fbbeef78b`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 46.5 MB (46450201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e66d86f17d19ad1ee543340630050da5690d888f02bc186b07736702382eb09`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d04267626c09db36ba57db446ffa128a79b92b28e520e9bbb60d84c92b94c0`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 67.2 MB (67201722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58f7aad98ac58f55673caa5b917718391795ff9a3b1f479fc7b787d78f3a354`  
		Last Modified: Thu, 21 Nov 2024 00:26:32 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3d5efe1ed7cf29dad01a2c69594ceb6b0ca523977f24d2767d3ef13de6f6b9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131563af08c9fd291fd2f7c813846125fe715f006a3d396bde57881e1cc0a186`

```dockerfile
```

-	Layers:
	-	`sha256:0c0d39bebfbb0c7af2b65758f081a44f9b9d036cb843b36bf3d346a568b44c6b`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 14.9 MB (14866904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e11d0d508b78947bc35881c46c4902ec23e4a3e0154d972b7b3bbd47d11d51c`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 34.6 KB (34553 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:2e6739055511aed759dac119b0e41cf2fd44530d5568a1c8f7cbdba5fa9a4fef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:614c6a16ea109306c3e995a60abd1bab28e5f4cdab514d356472c6831e112d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede8426663b5b73ca266326540d860a1b4373ce2f17c123fa3db0f8e71258ba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7f01a1f057b2b5ad037007ac97f29f083655704acf8c2968205f65f26c5e0`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af7f259011cbb37fb5dce3345a4d293d4da2a765217d15487152687a88c799`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97a67e97e66b29535d2820481a78596cf40980fcf397cc207181331ee7a29f5`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 6.9 MB (6902539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa5bf8f003d5e0f4a14c1dbd8b6a201748d866c556049aa9d5e8001d8295292`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f438e53f82d49e9816b5fd0392c450d25d075d67bb7dd78cd7ca83bb6e84bc73`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698b8a4e4c39001876e80c1803d1a7e7b22f594ff3b2cc2d7e4bdd8e27830fb3`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 48.2 MB (48216795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c684c19ed723174982aa4f5fe3d7c186dda61bb0eea75a11855f3b07ca73fd4a`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d842b92c292f40a1b2fae5b54af6d883d02a8cf4ae8b0ec54c5ecb15a62a1be`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 69.1 MB (69090174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6216f14663c125c521d02adf1e2bb0a959a7978559a6eb08f5fedceeacb00`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:2cb108ee91f25a1ded70e40712ae8fb43c06a9e70e88444b9633ae46523ce756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb93187421706fac5240e55055ad54cb02c69e5488ed0eafbee18c78a33957ae`

```dockerfile
```

-	Layers:
	-	`sha256:a83848b53bd904283a24e288856be05c01ac866bcb5523964b847510d4ac9878`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 14.9 MB (14876213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633d68c46e114727ef7dea6b2e7f252948185e0c78bc38f4c4756cb132bb7975`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 35.3 KB (35315 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bba66e70d5e271e7f8196af4f1a557e33284a82e14c880fe9e64d4ba94875b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8142099d2b36ba2c2b4a5fa011872f5fff0a51e1d04337c7693c6f5e126653`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f511afaf35971ea3f8093ba2da28ace20fb31f48ef6eecef82dcd5c64ac7e9d`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc7c5c2a66b2cbe7e2799d797107fa0c6643fba56afcb0165748dedf321062a`  
		Last Modified: Thu, 21 Nov 2024 00:24:55 GMT  
		Size: 47.1 MB (47117085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff3e2db7492489a547c35665d5bdfa809da50c9d98e195cccbbdfa725cb5e34`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a473a60f19cad50d3d8739841ee41626150759acca6bed1bbe8b4bfa9345f0fc`  
		Last Modified: Thu, 21 Nov 2024 00:24:56 GMT  
		Size: 69.3 MB (69298550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569d66393be2aef8e99c59e37429480612ae1157cbd3f0c9f49fce34bb45cdce`  
		Last Modified: Thu, 21 Nov 2024 00:24:54 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:794e18033a443ed808c9fa1b30cc38f6f36b793b6e1d6a9f12096e0c4be4e6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717d777feb8b94e1f79413e9287de31d20580e91f93a15cdd45d0ae000197baa`

```dockerfile
```

-	Layers:
	-	`sha256:1bde0305f9f6bd446e9f44e9db2025f849aa6d75e8865c3f9d9ddd7838be8b20`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 14.9 MB (14871399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a18e74dab9e5f3249fdd430cbe82994f022192c79c5f46ad2a7d27a9efcf53`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:2e6739055511aed759dac119b0e41cf2fd44530d5568a1c8f7cbdba5fa9a4fef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:614c6a16ea109306c3e995a60abd1bab28e5f4cdab514d356472c6831e112d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede8426663b5b73ca266326540d860a1b4373ce2f17c123fa3db0f8e71258ba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7f01a1f057b2b5ad037007ac97f29f083655704acf8c2968205f65f26c5e0`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af7f259011cbb37fb5dce3345a4d293d4da2a765217d15487152687a88c799`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97a67e97e66b29535d2820481a78596cf40980fcf397cc207181331ee7a29f5`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 6.9 MB (6902539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa5bf8f003d5e0f4a14c1dbd8b6a201748d866c556049aa9d5e8001d8295292`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f438e53f82d49e9816b5fd0392c450d25d075d67bb7dd78cd7ca83bb6e84bc73`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698b8a4e4c39001876e80c1803d1a7e7b22f594ff3b2cc2d7e4bdd8e27830fb3`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 48.2 MB (48216795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c684c19ed723174982aa4f5fe3d7c186dda61bb0eea75a11855f3b07ca73fd4a`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d842b92c292f40a1b2fae5b54af6d883d02a8cf4ae8b0ec54c5ecb15a62a1be`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 69.1 MB (69090174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6216f14663c125c521d02adf1e2bb0a959a7978559a6eb08f5fedceeacb00`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2cb108ee91f25a1ded70e40712ae8fb43c06a9e70e88444b9633ae46523ce756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb93187421706fac5240e55055ad54cb02c69e5488ed0eafbee18c78a33957ae`

```dockerfile
```

-	Layers:
	-	`sha256:a83848b53bd904283a24e288856be05c01ac866bcb5523964b847510d4ac9878`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 14.9 MB (14876213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633d68c46e114727ef7dea6b2e7f252948185e0c78bc38f4c4756cb132bb7975`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 35.3 KB (35315 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bba66e70d5e271e7f8196af4f1a557e33284a82e14c880fe9e64d4ba94875b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8142099d2b36ba2c2b4a5fa011872f5fff0a51e1d04337c7693c6f5e126653`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f511afaf35971ea3f8093ba2da28ace20fb31f48ef6eecef82dcd5c64ac7e9d`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc7c5c2a66b2cbe7e2799d797107fa0c6643fba56afcb0165748dedf321062a`  
		Last Modified: Thu, 21 Nov 2024 00:24:55 GMT  
		Size: 47.1 MB (47117085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff3e2db7492489a547c35665d5bdfa809da50c9d98e195cccbbdfa725cb5e34`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a473a60f19cad50d3d8739841ee41626150759acca6bed1bbe8b4bfa9345f0fc`  
		Last Modified: Thu, 21 Nov 2024 00:24:56 GMT  
		Size: 69.3 MB (69298550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569d66393be2aef8e99c59e37429480612ae1157cbd3f0c9f49fce34bb45cdce`  
		Last Modified: Thu, 21 Nov 2024 00:24:54 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:794e18033a443ed808c9fa1b30cc38f6f36b793b6e1d6a9f12096e0c4be4e6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717d777feb8b94e1f79413e9287de31d20580e91f93a15cdd45d0ae000197baa`

```dockerfile
```

-	Layers:
	-	`sha256:1bde0305f9f6bd446e9f44e9db2025f849aa6d75e8865c3f9d9ddd7838be8b20`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 14.9 MB (14871399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a18e74dab9e5f3249fdd430cbe82994f022192c79c5f46ad2a7d27a9efcf53`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:2e6739055511aed759dac119b0e41cf2fd44530d5568a1c8f7cbdba5fa9a4fef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:614c6a16ea109306c3e995a60abd1bab28e5f4cdab514d356472c6831e112d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede8426663b5b73ca266326540d860a1b4373ce2f17c123fa3db0f8e71258ba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7f01a1f057b2b5ad037007ac97f29f083655704acf8c2968205f65f26c5e0`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af7f259011cbb37fb5dce3345a4d293d4da2a765217d15487152687a88c799`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97a67e97e66b29535d2820481a78596cf40980fcf397cc207181331ee7a29f5`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 6.9 MB (6902539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa5bf8f003d5e0f4a14c1dbd8b6a201748d866c556049aa9d5e8001d8295292`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f438e53f82d49e9816b5fd0392c450d25d075d67bb7dd78cd7ca83bb6e84bc73`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698b8a4e4c39001876e80c1803d1a7e7b22f594ff3b2cc2d7e4bdd8e27830fb3`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 48.2 MB (48216795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c684c19ed723174982aa4f5fe3d7c186dda61bb0eea75a11855f3b07ca73fd4a`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d842b92c292f40a1b2fae5b54af6d883d02a8cf4ae8b0ec54c5ecb15a62a1be`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 69.1 MB (69090174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6216f14663c125c521d02adf1e2bb0a959a7978559a6eb08f5fedceeacb00`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2cb108ee91f25a1ded70e40712ae8fb43c06a9e70e88444b9633ae46523ce756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb93187421706fac5240e55055ad54cb02c69e5488ed0eafbee18c78a33957ae`

```dockerfile
```

-	Layers:
	-	`sha256:a83848b53bd904283a24e288856be05c01ac866bcb5523964b847510d4ac9878`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 14.9 MB (14876213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633d68c46e114727ef7dea6b2e7f252948185e0c78bc38f4c4756cb132bb7975`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 35.3 KB (35315 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bba66e70d5e271e7f8196af4f1a557e33284a82e14c880fe9e64d4ba94875b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8142099d2b36ba2c2b4a5fa011872f5fff0a51e1d04337c7693c6f5e126653`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f511afaf35971ea3f8093ba2da28ace20fb31f48ef6eecef82dcd5c64ac7e9d`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc7c5c2a66b2cbe7e2799d797107fa0c6643fba56afcb0165748dedf321062a`  
		Last Modified: Thu, 21 Nov 2024 00:24:55 GMT  
		Size: 47.1 MB (47117085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff3e2db7492489a547c35665d5bdfa809da50c9d98e195cccbbdfa725cb5e34`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a473a60f19cad50d3d8739841ee41626150759acca6bed1bbe8b4bfa9345f0fc`  
		Last Modified: Thu, 21 Nov 2024 00:24:56 GMT  
		Size: 69.3 MB (69298550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569d66393be2aef8e99c59e37429480612ae1157cbd3f0c9f49fce34bb45cdce`  
		Last Modified: Thu, 21 Nov 2024 00:24:54 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:794e18033a443ed808c9fa1b30cc38f6f36b793b6e1d6a9f12096e0c4be4e6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717d777feb8b94e1f79413e9287de31d20580e91f93a15cdd45d0ae000197baa`

```dockerfile
```

-	Layers:
	-	`sha256:1bde0305f9f6bd446e9f44e9db2025f849aa6d75e8865c3f9d9ddd7838be8b20`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 14.9 MB (14871399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a18e74dab9e5f3249fdd430cbe82994f022192c79c5f46ad2a7d27a9efcf53`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1`

```console
$ docker pull mysql@sha256:2e6739055511aed759dac119b0e41cf2fd44530d5568a1c8f7cbdba5fa9a4fef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1` - linux; amd64

```console
$ docker pull mysql@sha256:614c6a16ea109306c3e995a60abd1bab28e5f4cdab514d356472c6831e112d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede8426663b5b73ca266326540d860a1b4373ce2f17c123fa3db0f8e71258ba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7f01a1f057b2b5ad037007ac97f29f083655704acf8c2968205f65f26c5e0`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af7f259011cbb37fb5dce3345a4d293d4da2a765217d15487152687a88c799`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97a67e97e66b29535d2820481a78596cf40980fcf397cc207181331ee7a29f5`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 6.9 MB (6902539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa5bf8f003d5e0f4a14c1dbd8b6a201748d866c556049aa9d5e8001d8295292`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f438e53f82d49e9816b5fd0392c450d25d075d67bb7dd78cd7ca83bb6e84bc73`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698b8a4e4c39001876e80c1803d1a7e7b22f594ff3b2cc2d7e4bdd8e27830fb3`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 48.2 MB (48216795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c684c19ed723174982aa4f5fe3d7c186dda61bb0eea75a11855f3b07ca73fd4a`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d842b92c292f40a1b2fae5b54af6d883d02a8cf4ae8b0ec54c5ecb15a62a1be`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 69.1 MB (69090174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6216f14663c125c521d02adf1e2bb0a959a7978559a6eb08f5fedceeacb00`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1` - unknown; unknown

```console
$ docker pull mysql@sha256:2cb108ee91f25a1ded70e40712ae8fb43c06a9e70e88444b9633ae46523ce756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb93187421706fac5240e55055ad54cb02c69e5488ed0eafbee18c78a33957ae`

```dockerfile
```

-	Layers:
	-	`sha256:a83848b53bd904283a24e288856be05c01ac866bcb5523964b847510d4ac9878`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 14.9 MB (14876213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633d68c46e114727ef7dea6b2e7f252948185e0c78bc38f4c4756cb132bb7975`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 35.3 KB (35315 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bba66e70d5e271e7f8196af4f1a557e33284a82e14c880fe9e64d4ba94875b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8142099d2b36ba2c2b4a5fa011872f5fff0a51e1d04337c7693c6f5e126653`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f511afaf35971ea3f8093ba2da28ace20fb31f48ef6eecef82dcd5c64ac7e9d`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc7c5c2a66b2cbe7e2799d797107fa0c6643fba56afcb0165748dedf321062a`  
		Last Modified: Thu, 21 Nov 2024 00:24:55 GMT  
		Size: 47.1 MB (47117085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff3e2db7492489a547c35665d5bdfa809da50c9d98e195cccbbdfa725cb5e34`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a473a60f19cad50d3d8739841ee41626150759acca6bed1bbe8b4bfa9345f0fc`  
		Last Modified: Thu, 21 Nov 2024 00:24:56 GMT  
		Size: 69.3 MB (69298550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569d66393be2aef8e99c59e37429480612ae1157cbd3f0c9f49fce34bb45cdce`  
		Last Modified: Thu, 21 Nov 2024 00:24:54 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1` - unknown; unknown

```console
$ docker pull mysql@sha256:794e18033a443ed808c9fa1b30cc38f6f36b793b6e1d6a9f12096e0c4be4e6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717d777feb8b94e1f79413e9287de31d20580e91f93a15cdd45d0ae000197baa`

```dockerfile
```

-	Layers:
	-	`sha256:1bde0305f9f6bd446e9f44e9db2025f849aa6d75e8865c3f9d9ddd7838be8b20`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 14.9 MB (14871399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a18e74dab9e5f3249fdd430cbe82994f022192c79c5f46ad2a7d27a9efcf53`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1-oracle`

```console
$ docker pull mysql@sha256:2e6739055511aed759dac119b0e41cf2fd44530d5568a1c8f7cbdba5fa9a4fef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:614c6a16ea109306c3e995a60abd1bab28e5f4cdab514d356472c6831e112d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede8426663b5b73ca266326540d860a1b4373ce2f17c123fa3db0f8e71258ba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7f01a1f057b2b5ad037007ac97f29f083655704acf8c2968205f65f26c5e0`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af7f259011cbb37fb5dce3345a4d293d4da2a765217d15487152687a88c799`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97a67e97e66b29535d2820481a78596cf40980fcf397cc207181331ee7a29f5`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 6.9 MB (6902539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa5bf8f003d5e0f4a14c1dbd8b6a201748d866c556049aa9d5e8001d8295292`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f438e53f82d49e9816b5fd0392c450d25d075d67bb7dd78cd7ca83bb6e84bc73`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698b8a4e4c39001876e80c1803d1a7e7b22f594ff3b2cc2d7e4bdd8e27830fb3`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 48.2 MB (48216795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c684c19ed723174982aa4f5fe3d7c186dda61bb0eea75a11855f3b07ca73fd4a`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d842b92c292f40a1b2fae5b54af6d883d02a8cf4ae8b0ec54c5ecb15a62a1be`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 69.1 MB (69090174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6216f14663c125c521d02adf1e2bb0a959a7978559a6eb08f5fedceeacb00`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2cb108ee91f25a1ded70e40712ae8fb43c06a9e70e88444b9633ae46523ce756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb93187421706fac5240e55055ad54cb02c69e5488ed0eafbee18c78a33957ae`

```dockerfile
```

-	Layers:
	-	`sha256:a83848b53bd904283a24e288856be05c01ac866bcb5523964b847510d4ac9878`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 14.9 MB (14876213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633d68c46e114727ef7dea6b2e7f252948185e0c78bc38f4c4756cb132bb7975`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 35.3 KB (35315 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bba66e70d5e271e7f8196af4f1a557e33284a82e14c880fe9e64d4ba94875b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8142099d2b36ba2c2b4a5fa011872f5fff0a51e1d04337c7693c6f5e126653`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f511afaf35971ea3f8093ba2da28ace20fb31f48ef6eecef82dcd5c64ac7e9d`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc7c5c2a66b2cbe7e2799d797107fa0c6643fba56afcb0165748dedf321062a`  
		Last Modified: Thu, 21 Nov 2024 00:24:55 GMT  
		Size: 47.1 MB (47117085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff3e2db7492489a547c35665d5bdfa809da50c9d98e195cccbbdfa725cb5e34`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a473a60f19cad50d3d8739841ee41626150759acca6bed1bbe8b4bfa9345f0fc`  
		Last Modified: Thu, 21 Nov 2024 00:24:56 GMT  
		Size: 69.3 MB (69298550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569d66393be2aef8e99c59e37429480612ae1157cbd3f0c9f49fce34bb45cdce`  
		Last Modified: Thu, 21 Nov 2024 00:24:54 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:794e18033a443ed808c9fa1b30cc38f6f36b793b6e1d6a9f12096e0c4be4e6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717d777feb8b94e1f79413e9287de31d20580e91f93a15cdd45d0ae000197baa`

```dockerfile
```

-	Layers:
	-	`sha256:1bde0305f9f6bd446e9f44e9db2025f849aa6d75e8865c3f9d9ddd7838be8b20`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 14.9 MB (14871399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a18e74dab9e5f3249fdd430cbe82994f022192c79c5f46ad2a7d27a9efcf53`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1-oraclelinux9`

```console
$ docker pull mysql@sha256:2e6739055511aed759dac119b0e41cf2fd44530d5568a1c8f7cbdba5fa9a4fef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:614c6a16ea109306c3e995a60abd1bab28e5f4cdab514d356472c6831e112d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede8426663b5b73ca266326540d860a1b4373ce2f17c123fa3db0f8e71258ba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7f01a1f057b2b5ad037007ac97f29f083655704acf8c2968205f65f26c5e0`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af7f259011cbb37fb5dce3345a4d293d4da2a765217d15487152687a88c799`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97a67e97e66b29535d2820481a78596cf40980fcf397cc207181331ee7a29f5`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 6.9 MB (6902539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa5bf8f003d5e0f4a14c1dbd8b6a201748d866c556049aa9d5e8001d8295292`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f438e53f82d49e9816b5fd0392c450d25d075d67bb7dd78cd7ca83bb6e84bc73`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698b8a4e4c39001876e80c1803d1a7e7b22f594ff3b2cc2d7e4bdd8e27830fb3`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 48.2 MB (48216795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c684c19ed723174982aa4f5fe3d7c186dda61bb0eea75a11855f3b07ca73fd4a`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d842b92c292f40a1b2fae5b54af6d883d02a8cf4ae8b0ec54c5ecb15a62a1be`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 69.1 MB (69090174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6216f14663c125c521d02adf1e2bb0a959a7978559a6eb08f5fedceeacb00`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2cb108ee91f25a1ded70e40712ae8fb43c06a9e70e88444b9633ae46523ce756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb93187421706fac5240e55055ad54cb02c69e5488ed0eafbee18c78a33957ae`

```dockerfile
```

-	Layers:
	-	`sha256:a83848b53bd904283a24e288856be05c01ac866bcb5523964b847510d4ac9878`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 14.9 MB (14876213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633d68c46e114727ef7dea6b2e7f252948185e0c78bc38f4c4756cb132bb7975`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 35.3 KB (35315 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bba66e70d5e271e7f8196af4f1a557e33284a82e14c880fe9e64d4ba94875b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8142099d2b36ba2c2b4a5fa011872f5fff0a51e1d04337c7693c6f5e126653`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f511afaf35971ea3f8093ba2da28ace20fb31f48ef6eecef82dcd5c64ac7e9d`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc7c5c2a66b2cbe7e2799d797107fa0c6643fba56afcb0165748dedf321062a`  
		Last Modified: Thu, 21 Nov 2024 00:24:55 GMT  
		Size: 47.1 MB (47117085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff3e2db7492489a547c35665d5bdfa809da50c9d98e195cccbbdfa725cb5e34`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a473a60f19cad50d3d8739841ee41626150759acca6bed1bbe8b4bfa9345f0fc`  
		Last Modified: Thu, 21 Nov 2024 00:24:56 GMT  
		Size: 69.3 MB (69298550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569d66393be2aef8e99c59e37429480612ae1157cbd3f0c9f49fce34bb45cdce`  
		Last Modified: Thu, 21 Nov 2024 00:24:54 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:794e18033a443ed808c9fa1b30cc38f6f36b793b6e1d6a9f12096e0c4be4e6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717d777feb8b94e1f79413e9287de31d20580e91f93a15cdd45d0ae000197baa`

```dockerfile
```

-	Layers:
	-	`sha256:1bde0305f9f6bd446e9f44e9db2025f849aa6d75e8865c3f9d9ddd7838be8b20`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 14.9 MB (14871399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a18e74dab9e5f3249fdd430cbe82994f022192c79c5f46ad2a7d27a9efcf53`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1.0`

```console
$ docker pull mysql@sha256:2e6739055511aed759dac119b0e41cf2fd44530d5568a1c8f7cbdba5fa9a4fef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1.0` - linux; amd64

```console
$ docker pull mysql@sha256:614c6a16ea109306c3e995a60abd1bab28e5f4cdab514d356472c6831e112d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede8426663b5b73ca266326540d860a1b4373ce2f17c123fa3db0f8e71258ba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7f01a1f057b2b5ad037007ac97f29f083655704acf8c2968205f65f26c5e0`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af7f259011cbb37fb5dce3345a4d293d4da2a765217d15487152687a88c799`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97a67e97e66b29535d2820481a78596cf40980fcf397cc207181331ee7a29f5`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 6.9 MB (6902539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa5bf8f003d5e0f4a14c1dbd8b6a201748d866c556049aa9d5e8001d8295292`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f438e53f82d49e9816b5fd0392c450d25d075d67bb7dd78cd7ca83bb6e84bc73`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698b8a4e4c39001876e80c1803d1a7e7b22f594ff3b2cc2d7e4bdd8e27830fb3`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 48.2 MB (48216795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c684c19ed723174982aa4f5fe3d7c186dda61bb0eea75a11855f3b07ca73fd4a`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d842b92c292f40a1b2fae5b54af6d883d02a8cf4ae8b0ec54c5ecb15a62a1be`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 69.1 MB (69090174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6216f14663c125c521d02adf1e2bb0a959a7978559a6eb08f5fedceeacb00`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0` - unknown; unknown

```console
$ docker pull mysql@sha256:2cb108ee91f25a1ded70e40712ae8fb43c06a9e70e88444b9633ae46523ce756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb93187421706fac5240e55055ad54cb02c69e5488ed0eafbee18c78a33957ae`

```dockerfile
```

-	Layers:
	-	`sha256:a83848b53bd904283a24e288856be05c01ac866bcb5523964b847510d4ac9878`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 14.9 MB (14876213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633d68c46e114727ef7dea6b2e7f252948185e0c78bc38f4c4756cb132bb7975`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 35.3 KB (35315 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bba66e70d5e271e7f8196af4f1a557e33284a82e14c880fe9e64d4ba94875b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8142099d2b36ba2c2b4a5fa011872f5fff0a51e1d04337c7693c6f5e126653`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f511afaf35971ea3f8093ba2da28ace20fb31f48ef6eecef82dcd5c64ac7e9d`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc7c5c2a66b2cbe7e2799d797107fa0c6643fba56afcb0165748dedf321062a`  
		Last Modified: Thu, 21 Nov 2024 00:24:55 GMT  
		Size: 47.1 MB (47117085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff3e2db7492489a547c35665d5bdfa809da50c9d98e195cccbbdfa725cb5e34`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a473a60f19cad50d3d8739841ee41626150759acca6bed1bbe8b4bfa9345f0fc`  
		Last Modified: Thu, 21 Nov 2024 00:24:56 GMT  
		Size: 69.3 MB (69298550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569d66393be2aef8e99c59e37429480612ae1157cbd3f0c9f49fce34bb45cdce`  
		Last Modified: Thu, 21 Nov 2024 00:24:54 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0` - unknown; unknown

```console
$ docker pull mysql@sha256:794e18033a443ed808c9fa1b30cc38f6f36b793b6e1d6a9f12096e0c4be4e6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717d777feb8b94e1f79413e9287de31d20580e91f93a15cdd45d0ae000197baa`

```dockerfile
```

-	Layers:
	-	`sha256:1bde0305f9f6bd446e9f44e9db2025f849aa6d75e8865c3f9d9ddd7838be8b20`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 14.9 MB (14871399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a18e74dab9e5f3249fdd430cbe82994f022192c79c5f46ad2a7d27a9efcf53`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1.0-oracle`

```console
$ docker pull mysql@sha256:2e6739055511aed759dac119b0e41cf2fd44530d5568a1c8f7cbdba5fa9a4fef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:614c6a16ea109306c3e995a60abd1bab28e5f4cdab514d356472c6831e112d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede8426663b5b73ca266326540d860a1b4373ce2f17c123fa3db0f8e71258ba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7f01a1f057b2b5ad037007ac97f29f083655704acf8c2968205f65f26c5e0`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af7f259011cbb37fb5dce3345a4d293d4da2a765217d15487152687a88c799`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97a67e97e66b29535d2820481a78596cf40980fcf397cc207181331ee7a29f5`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 6.9 MB (6902539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa5bf8f003d5e0f4a14c1dbd8b6a201748d866c556049aa9d5e8001d8295292`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f438e53f82d49e9816b5fd0392c450d25d075d67bb7dd78cd7ca83bb6e84bc73`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698b8a4e4c39001876e80c1803d1a7e7b22f594ff3b2cc2d7e4bdd8e27830fb3`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 48.2 MB (48216795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c684c19ed723174982aa4f5fe3d7c186dda61bb0eea75a11855f3b07ca73fd4a`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d842b92c292f40a1b2fae5b54af6d883d02a8cf4ae8b0ec54c5ecb15a62a1be`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 69.1 MB (69090174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6216f14663c125c521d02adf1e2bb0a959a7978559a6eb08f5fedceeacb00`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2cb108ee91f25a1ded70e40712ae8fb43c06a9e70e88444b9633ae46523ce756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb93187421706fac5240e55055ad54cb02c69e5488ed0eafbee18c78a33957ae`

```dockerfile
```

-	Layers:
	-	`sha256:a83848b53bd904283a24e288856be05c01ac866bcb5523964b847510d4ac9878`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 14.9 MB (14876213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633d68c46e114727ef7dea6b2e7f252948185e0c78bc38f4c4756cb132bb7975`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 35.3 KB (35315 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bba66e70d5e271e7f8196af4f1a557e33284a82e14c880fe9e64d4ba94875b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8142099d2b36ba2c2b4a5fa011872f5fff0a51e1d04337c7693c6f5e126653`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f511afaf35971ea3f8093ba2da28ace20fb31f48ef6eecef82dcd5c64ac7e9d`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc7c5c2a66b2cbe7e2799d797107fa0c6643fba56afcb0165748dedf321062a`  
		Last Modified: Thu, 21 Nov 2024 00:24:55 GMT  
		Size: 47.1 MB (47117085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff3e2db7492489a547c35665d5bdfa809da50c9d98e195cccbbdfa725cb5e34`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a473a60f19cad50d3d8739841ee41626150759acca6bed1bbe8b4bfa9345f0fc`  
		Last Modified: Thu, 21 Nov 2024 00:24:56 GMT  
		Size: 69.3 MB (69298550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569d66393be2aef8e99c59e37429480612ae1157cbd3f0c9f49fce34bb45cdce`  
		Last Modified: Thu, 21 Nov 2024 00:24:54 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:794e18033a443ed808c9fa1b30cc38f6f36b793b6e1d6a9f12096e0c4be4e6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717d777feb8b94e1f79413e9287de31d20580e91f93a15cdd45d0ae000197baa`

```dockerfile
```

-	Layers:
	-	`sha256:1bde0305f9f6bd446e9f44e9db2025f849aa6d75e8865c3f9d9ddd7838be8b20`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 14.9 MB (14871399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a18e74dab9e5f3249fdd430cbe82994f022192c79c5f46ad2a7d27a9efcf53`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1.0-oraclelinux9`

```console
$ docker pull mysql@sha256:2e6739055511aed759dac119b0e41cf2fd44530d5568a1c8f7cbdba5fa9a4fef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:614c6a16ea109306c3e995a60abd1bab28e5f4cdab514d356472c6831e112d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede8426663b5b73ca266326540d860a1b4373ce2f17c123fa3db0f8e71258ba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7f01a1f057b2b5ad037007ac97f29f083655704acf8c2968205f65f26c5e0`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af7f259011cbb37fb5dce3345a4d293d4da2a765217d15487152687a88c799`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97a67e97e66b29535d2820481a78596cf40980fcf397cc207181331ee7a29f5`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 6.9 MB (6902539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa5bf8f003d5e0f4a14c1dbd8b6a201748d866c556049aa9d5e8001d8295292`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f438e53f82d49e9816b5fd0392c450d25d075d67bb7dd78cd7ca83bb6e84bc73`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698b8a4e4c39001876e80c1803d1a7e7b22f594ff3b2cc2d7e4bdd8e27830fb3`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 48.2 MB (48216795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c684c19ed723174982aa4f5fe3d7c186dda61bb0eea75a11855f3b07ca73fd4a`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d842b92c292f40a1b2fae5b54af6d883d02a8cf4ae8b0ec54c5ecb15a62a1be`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 69.1 MB (69090174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6216f14663c125c521d02adf1e2bb0a959a7978559a6eb08f5fedceeacb00`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2cb108ee91f25a1ded70e40712ae8fb43c06a9e70e88444b9633ae46523ce756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb93187421706fac5240e55055ad54cb02c69e5488ed0eafbee18c78a33957ae`

```dockerfile
```

-	Layers:
	-	`sha256:a83848b53bd904283a24e288856be05c01ac866bcb5523964b847510d4ac9878`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 14.9 MB (14876213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633d68c46e114727ef7dea6b2e7f252948185e0c78bc38f4c4756cb132bb7975`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 35.3 KB (35315 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bba66e70d5e271e7f8196af4f1a557e33284a82e14c880fe9e64d4ba94875b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8142099d2b36ba2c2b4a5fa011872f5fff0a51e1d04337c7693c6f5e126653`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f511afaf35971ea3f8093ba2da28ace20fb31f48ef6eecef82dcd5c64ac7e9d`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc7c5c2a66b2cbe7e2799d797107fa0c6643fba56afcb0165748dedf321062a`  
		Last Modified: Thu, 21 Nov 2024 00:24:55 GMT  
		Size: 47.1 MB (47117085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff3e2db7492489a547c35665d5bdfa809da50c9d98e195cccbbdfa725cb5e34`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a473a60f19cad50d3d8739841ee41626150759acca6bed1bbe8b4bfa9345f0fc`  
		Last Modified: Thu, 21 Nov 2024 00:24:56 GMT  
		Size: 69.3 MB (69298550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569d66393be2aef8e99c59e37429480612ae1157cbd3f0c9f49fce34bb45cdce`  
		Last Modified: Thu, 21 Nov 2024 00:24:54 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:794e18033a443ed808c9fa1b30cc38f6f36b793b6e1d6a9f12096e0c4be4e6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717d777feb8b94e1f79413e9287de31d20580e91f93a15cdd45d0ae000197baa`

```dockerfile
```

-	Layers:
	-	`sha256:1bde0305f9f6bd446e9f44e9db2025f849aa6d75e8865c3f9d9ddd7838be8b20`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 14.9 MB (14871399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a18e74dab9e5f3249fdd430cbe82994f022192c79c5f46ad2a7d27a9efcf53`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:2e6739055511aed759dac119b0e41cf2fd44530d5568a1c8f7cbdba5fa9a4fef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:614c6a16ea109306c3e995a60abd1bab28e5f4cdab514d356472c6831e112d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede8426663b5b73ca266326540d860a1b4373ce2f17c123fa3db0f8e71258ba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7f01a1f057b2b5ad037007ac97f29f083655704acf8c2968205f65f26c5e0`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af7f259011cbb37fb5dce3345a4d293d4da2a765217d15487152687a88c799`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97a67e97e66b29535d2820481a78596cf40980fcf397cc207181331ee7a29f5`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 6.9 MB (6902539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa5bf8f003d5e0f4a14c1dbd8b6a201748d866c556049aa9d5e8001d8295292`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f438e53f82d49e9816b5fd0392c450d25d075d67bb7dd78cd7ca83bb6e84bc73`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698b8a4e4c39001876e80c1803d1a7e7b22f594ff3b2cc2d7e4bdd8e27830fb3`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 48.2 MB (48216795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c684c19ed723174982aa4f5fe3d7c186dda61bb0eea75a11855f3b07ca73fd4a`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d842b92c292f40a1b2fae5b54af6d883d02a8cf4ae8b0ec54c5ecb15a62a1be`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 69.1 MB (69090174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6216f14663c125c521d02adf1e2bb0a959a7978559a6eb08f5fedceeacb00`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:2cb108ee91f25a1ded70e40712ae8fb43c06a9e70e88444b9633ae46523ce756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb93187421706fac5240e55055ad54cb02c69e5488ed0eafbee18c78a33957ae`

```dockerfile
```

-	Layers:
	-	`sha256:a83848b53bd904283a24e288856be05c01ac866bcb5523964b847510d4ac9878`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 14.9 MB (14876213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633d68c46e114727ef7dea6b2e7f252948185e0c78bc38f4c4756cb132bb7975`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 35.3 KB (35315 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bba66e70d5e271e7f8196af4f1a557e33284a82e14c880fe9e64d4ba94875b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8142099d2b36ba2c2b4a5fa011872f5fff0a51e1d04337c7693c6f5e126653`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f511afaf35971ea3f8093ba2da28ace20fb31f48ef6eecef82dcd5c64ac7e9d`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc7c5c2a66b2cbe7e2799d797107fa0c6643fba56afcb0165748dedf321062a`  
		Last Modified: Thu, 21 Nov 2024 00:24:55 GMT  
		Size: 47.1 MB (47117085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff3e2db7492489a547c35665d5bdfa809da50c9d98e195cccbbdfa725cb5e34`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a473a60f19cad50d3d8739841ee41626150759acca6bed1bbe8b4bfa9345f0fc`  
		Last Modified: Thu, 21 Nov 2024 00:24:56 GMT  
		Size: 69.3 MB (69298550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569d66393be2aef8e99c59e37429480612ae1157cbd3f0c9f49fce34bb45cdce`  
		Last Modified: Thu, 21 Nov 2024 00:24:54 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:794e18033a443ed808c9fa1b30cc38f6f36b793b6e1d6a9f12096e0c4be4e6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717d777feb8b94e1f79413e9287de31d20580e91f93a15cdd45d0ae000197baa`

```dockerfile
```

-	Layers:
	-	`sha256:1bde0305f9f6bd446e9f44e9db2025f849aa6d75e8865c3f9d9ddd7838be8b20`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 14.9 MB (14871399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a18e74dab9e5f3249fdd430cbe82994f022192c79c5f46ad2a7d27a9efcf53`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:2e6739055511aed759dac119b0e41cf2fd44530d5568a1c8f7cbdba5fa9a4fef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:614c6a16ea109306c3e995a60abd1bab28e5f4cdab514d356472c6831e112d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede8426663b5b73ca266326540d860a1b4373ce2f17c123fa3db0f8e71258ba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7f01a1f057b2b5ad037007ac97f29f083655704acf8c2968205f65f26c5e0`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af7f259011cbb37fb5dce3345a4d293d4da2a765217d15487152687a88c799`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97a67e97e66b29535d2820481a78596cf40980fcf397cc207181331ee7a29f5`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 6.9 MB (6902539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa5bf8f003d5e0f4a14c1dbd8b6a201748d866c556049aa9d5e8001d8295292`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f438e53f82d49e9816b5fd0392c450d25d075d67bb7dd78cd7ca83bb6e84bc73`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698b8a4e4c39001876e80c1803d1a7e7b22f594ff3b2cc2d7e4bdd8e27830fb3`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 48.2 MB (48216795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c684c19ed723174982aa4f5fe3d7c186dda61bb0eea75a11855f3b07ca73fd4a`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d842b92c292f40a1b2fae5b54af6d883d02a8cf4ae8b0ec54c5ecb15a62a1be`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 69.1 MB (69090174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6216f14663c125c521d02adf1e2bb0a959a7978559a6eb08f5fedceeacb00`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2cb108ee91f25a1ded70e40712ae8fb43c06a9e70e88444b9633ae46523ce756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb93187421706fac5240e55055ad54cb02c69e5488ed0eafbee18c78a33957ae`

```dockerfile
```

-	Layers:
	-	`sha256:a83848b53bd904283a24e288856be05c01ac866bcb5523964b847510d4ac9878`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 14.9 MB (14876213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633d68c46e114727ef7dea6b2e7f252948185e0c78bc38f4c4756cb132bb7975`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 35.3 KB (35315 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bba66e70d5e271e7f8196af4f1a557e33284a82e14c880fe9e64d4ba94875b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8142099d2b36ba2c2b4a5fa011872f5fff0a51e1d04337c7693c6f5e126653`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f511afaf35971ea3f8093ba2da28ace20fb31f48ef6eecef82dcd5c64ac7e9d`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc7c5c2a66b2cbe7e2799d797107fa0c6643fba56afcb0165748dedf321062a`  
		Last Modified: Thu, 21 Nov 2024 00:24:55 GMT  
		Size: 47.1 MB (47117085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff3e2db7492489a547c35665d5bdfa809da50c9d98e195cccbbdfa725cb5e34`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a473a60f19cad50d3d8739841ee41626150759acca6bed1bbe8b4bfa9345f0fc`  
		Last Modified: Thu, 21 Nov 2024 00:24:56 GMT  
		Size: 69.3 MB (69298550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569d66393be2aef8e99c59e37429480612ae1157cbd3f0c9f49fce34bb45cdce`  
		Last Modified: Thu, 21 Nov 2024 00:24:54 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:794e18033a443ed808c9fa1b30cc38f6f36b793b6e1d6a9f12096e0c4be4e6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717d777feb8b94e1f79413e9287de31d20580e91f93a15cdd45d0ae000197baa`

```dockerfile
```

-	Layers:
	-	`sha256:1bde0305f9f6bd446e9f44e9db2025f849aa6d75e8865c3f9d9ddd7838be8b20`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 14.9 MB (14871399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a18e74dab9e5f3249fdd430cbe82994f022192c79c5f46ad2a7d27a9efcf53`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:2e6739055511aed759dac119b0e41cf2fd44530d5568a1c8f7cbdba5fa9a4fef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:614c6a16ea109306c3e995a60abd1bab28e5f4cdab514d356472c6831e112d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede8426663b5b73ca266326540d860a1b4373ce2f17c123fa3db0f8e71258ba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7f01a1f057b2b5ad037007ac97f29f083655704acf8c2968205f65f26c5e0`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af7f259011cbb37fb5dce3345a4d293d4da2a765217d15487152687a88c799`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97a67e97e66b29535d2820481a78596cf40980fcf397cc207181331ee7a29f5`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 6.9 MB (6902539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa5bf8f003d5e0f4a14c1dbd8b6a201748d866c556049aa9d5e8001d8295292`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f438e53f82d49e9816b5fd0392c450d25d075d67bb7dd78cd7ca83bb6e84bc73`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698b8a4e4c39001876e80c1803d1a7e7b22f594ff3b2cc2d7e4bdd8e27830fb3`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 48.2 MB (48216795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c684c19ed723174982aa4f5fe3d7c186dda61bb0eea75a11855f3b07ca73fd4a`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d842b92c292f40a1b2fae5b54af6d883d02a8cf4ae8b0ec54c5ecb15a62a1be`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 69.1 MB (69090174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6216f14663c125c521d02adf1e2bb0a959a7978559a6eb08f5fedceeacb00`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2cb108ee91f25a1ded70e40712ae8fb43c06a9e70e88444b9633ae46523ce756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb93187421706fac5240e55055ad54cb02c69e5488ed0eafbee18c78a33957ae`

```dockerfile
```

-	Layers:
	-	`sha256:a83848b53bd904283a24e288856be05c01ac866bcb5523964b847510d4ac9878`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 14.9 MB (14876213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633d68c46e114727ef7dea6b2e7f252948185e0c78bc38f4c4756cb132bb7975`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 35.3 KB (35315 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bba66e70d5e271e7f8196af4f1a557e33284a82e14c880fe9e64d4ba94875b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8142099d2b36ba2c2b4a5fa011872f5fff0a51e1d04337c7693c6f5e126653`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f511afaf35971ea3f8093ba2da28ace20fb31f48ef6eecef82dcd5c64ac7e9d`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc7c5c2a66b2cbe7e2799d797107fa0c6643fba56afcb0165748dedf321062a`  
		Last Modified: Thu, 21 Nov 2024 00:24:55 GMT  
		Size: 47.1 MB (47117085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff3e2db7492489a547c35665d5bdfa809da50c9d98e195cccbbdfa725cb5e34`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a473a60f19cad50d3d8739841ee41626150759acca6bed1bbe8b4bfa9345f0fc`  
		Last Modified: Thu, 21 Nov 2024 00:24:56 GMT  
		Size: 69.3 MB (69298550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569d66393be2aef8e99c59e37429480612ae1157cbd3f0c9f49fce34bb45cdce`  
		Last Modified: Thu, 21 Nov 2024 00:24:54 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:794e18033a443ed808c9fa1b30cc38f6f36b793b6e1d6a9f12096e0c4be4e6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717d777feb8b94e1f79413e9287de31d20580e91f93a15cdd45d0ae000197baa`

```dockerfile
```

-	Layers:
	-	`sha256:1bde0305f9f6bd446e9f44e9db2025f849aa6d75e8865c3f9d9ddd7838be8b20`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 14.9 MB (14871399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a18e74dab9e5f3249fdd430cbe82994f022192c79c5f46ad2a7d27a9efcf53`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:2e6739055511aed759dac119b0e41cf2fd44530d5568a1c8f7cbdba5fa9a4fef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:614c6a16ea109306c3e995a60abd1bab28e5f4cdab514d356472c6831e112d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede8426663b5b73ca266326540d860a1b4373ce2f17c123fa3db0f8e71258ba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7f01a1f057b2b5ad037007ac97f29f083655704acf8c2968205f65f26c5e0`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af7f259011cbb37fb5dce3345a4d293d4da2a765217d15487152687a88c799`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97a67e97e66b29535d2820481a78596cf40980fcf397cc207181331ee7a29f5`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 6.9 MB (6902539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa5bf8f003d5e0f4a14c1dbd8b6a201748d866c556049aa9d5e8001d8295292`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f438e53f82d49e9816b5fd0392c450d25d075d67bb7dd78cd7ca83bb6e84bc73`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698b8a4e4c39001876e80c1803d1a7e7b22f594ff3b2cc2d7e4bdd8e27830fb3`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 48.2 MB (48216795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c684c19ed723174982aa4f5fe3d7c186dda61bb0eea75a11855f3b07ca73fd4a`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d842b92c292f40a1b2fae5b54af6d883d02a8cf4ae8b0ec54c5ecb15a62a1be`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 69.1 MB (69090174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6216f14663c125c521d02adf1e2bb0a959a7978559a6eb08f5fedceeacb00`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:2cb108ee91f25a1ded70e40712ae8fb43c06a9e70e88444b9633ae46523ce756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb93187421706fac5240e55055ad54cb02c69e5488ed0eafbee18c78a33957ae`

```dockerfile
```

-	Layers:
	-	`sha256:a83848b53bd904283a24e288856be05c01ac866bcb5523964b847510d4ac9878`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 14.9 MB (14876213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633d68c46e114727ef7dea6b2e7f252948185e0c78bc38f4c4756cb132bb7975`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 35.3 KB (35315 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bba66e70d5e271e7f8196af4f1a557e33284a82e14c880fe9e64d4ba94875b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8142099d2b36ba2c2b4a5fa011872f5fff0a51e1d04337c7693c6f5e126653`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f511afaf35971ea3f8093ba2da28ace20fb31f48ef6eecef82dcd5c64ac7e9d`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc7c5c2a66b2cbe7e2799d797107fa0c6643fba56afcb0165748dedf321062a`  
		Last Modified: Thu, 21 Nov 2024 00:24:55 GMT  
		Size: 47.1 MB (47117085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff3e2db7492489a547c35665d5bdfa809da50c9d98e195cccbbdfa725cb5e34`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a473a60f19cad50d3d8739841ee41626150759acca6bed1bbe8b4bfa9345f0fc`  
		Last Modified: Thu, 21 Nov 2024 00:24:56 GMT  
		Size: 69.3 MB (69298550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569d66393be2aef8e99c59e37429480612ae1157cbd3f0c9f49fce34bb45cdce`  
		Last Modified: Thu, 21 Nov 2024 00:24:54 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:794e18033a443ed808c9fa1b30cc38f6f36b793b6e1d6a9f12096e0c4be4e6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717d777feb8b94e1f79413e9287de31d20580e91f93a15cdd45d0ae000197baa`

```dockerfile
```

-	Layers:
	-	`sha256:1bde0305f9f6bd446e9f44e9db2025f849aa6d75e8865c3f9d9ddd7838be8b20`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 14.9 MB (14871399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a18e74dab9e5f3249fdd430cbe82994f022192c79c5f46ad2a7d27a9efcf53`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:2bed89deaa6122df7e3bfdb3006d2f09251e2fa925bdd4f6a5ccff7badf070ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:8d111b535dbe6d9fbdaafcb0e3157aff64664ef5052ceae3c57f974166a6cff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171514588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bb57dc6b1d1f9bbd9ab9843af36264c74b6944360d37703fc8cdb932c1587f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5e9755d4041de874322937a7e4aba7eae546b110eaf21c99fd9ee849a31f0b`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6f939b5bdeb93950dd408d5e339b273a43e8129bb908aa25a492fd41925b5e`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4825be18a9da34ab830e99c285416149b22324acc5d70e0fe35719306a672a39`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 6.9 MB (6902532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d101851db8708b91cdb31331ed5fd7584d9109fd10ae799295f8e4b1c372ee`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e6fd8a5fc375e4c5061959d05b0c1727be47165db7fcf903582c94045798ff`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b46238a9af0862e613cea2905d7fa437227a27976fbfcac6e82db8164ba40d`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 47.6 MB (47559393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13a1e3aee9ee85855737c1af5191eef5fbf6d612b81b87f12fcd6dd59d7594a`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444e8e4164f357b6d69d3d1932320dbd2f6e3f0970bf6ee1cacb47a88e87780f`  
		Last Modified: Thu, 21 Nov 2024 00:24:51 GMT  
		Size: 67.0 MB (66961014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef40cced209d5affe747d3e62bcaef3f4800e24279555efd1d9a0a68d5902c1`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:d24e1e14db4144ad85299ee67329e83eab737d53eabb1c765795ef88d63f8d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97e864c12a8d34ccf20924c9821a42b95f8a22305076fb1ef870ab42aa83988`

```dockerfile
```

-	Layers:
	-	`sha256:978b2ae2ea66ace5f526e29cbe706f1d9b0139220749975cfb696fbcbc463daf`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 14.9 MB (14871754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade4558bfff869010112ad9fbb8710524f7b764f662ceaedb75071b90e9a9d7c`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 34.2 KB (34248 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2516a10a1ea246e0b9391b259194e9f0c6a0669dfd1fccc337e62450f657acc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168737549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6672c03fe2b69c64f378bc123bffddae0ceb6db9d80968d238151dffa2706c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd77c1317d3aa167ce525e562b4150ca934ca0a6931888f4facee3c2832b430`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6319ad690265786884f89a8528c43a7641f5ec4ee13646914915d4fbbeef78b`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 46.5 MB (46450201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e66d86f17d19ad1ee543340630050da5690d888f02bc186b07736702382eb09`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d04267626c09db36ba57db446ffa128a79b92b28e520e9bbb60d84c92b94c0`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 67.2 MB (67201722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58f7aad98ac58f55673caa5b917718391795ff9a3b1f479fc7b787d78f3a354`  
		Last Modified: Thu, 21 Nov 2024 00:26:32 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:3d5efe1ed7cf29dad01a2c69594ceb6b0ca523977f24d2767d3ef13de6f6b9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131563af08c9fd291fd2f7c813846125fe715f006a3d396bde57881e1cc0a186`

```dockerfile
```

-	Layers:
	-	`sha256:0c0d39bebfbb0c7af2b65758f081a44f9b9d036cb843b36bf3d346a568b44c6b`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 14.9 MB (14866904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e11d0d508b78947bc35881c46c4902ec23e4a3e0154d972b7b3bbd47d11d51c`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 34.6 KB (34553 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:2bed89deaa6122df7e3bfdb3006d2f09251e2fa925bdd4f6a5ccff7badf070ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8d111b535dbe6d9fbdaafcb0e3157aff64664ef5052ceae3c57f974166a6cff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171514588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bb57dc6b1d1f9bbd9ab9843af36264c74b6944360d37703fc8cdb932c1587f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5e9755d4041de874322937a7e4aba7eae546b110eaf21c99fd9ee849a31f0b`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6f939b5bdeb93950dd408d5e339b273a43e8129bb908aa25a492fd41925b5e`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4825be18a9da34ab830e99c285416149b22324acc5d70e0fe35719306a672a39`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 6.9 MB (6902532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d101851db8708b91cdb31331ed5fd7584d9109fd10ae799295f8e4b1c372ee`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e6fd8a5fc375e4c5061959d05b0c1727be47165db7fcf903582c94045798ff`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b46238a9af0862e613cea2905d7fa437227a27976fbfcac6e82db8164ba40d`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 47.6 MB (47559393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13a1e3aee9ee85855737c1af5191eef5fbf6d612b81b87f12fcd6dd59d7594a`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444e8e4164f357b6d69d3d1932320dbd2f6e3f0970bf6ee1cacb47a88e87780f`  
		Last Modified: Thu, 21 Nov 2024 00:24:51 GMT  
		Size: 67.0 MB (66961014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef40cced209d5affe747d3e62bcaef3f4800e24279555efd1d9a0a68d5902c1`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d24e1e14db4144ad85299ee67329e83eab737d53eabb1c765795ef88d63f8d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97e864c12a8d34ccf20924c9821a42b95f8a22305076fb1ef870ab42aa83988`

```dockerfile
```

-	Layers:
	-	`sha256:978b2ae2ea66ace5f526e29cbe706f1d9b0139220749975cfb696fbcbc463daf`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 14.9 MB (14871754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade4558bfff869010112ad9fbb8710524f7b764f662ceaedb75071b90e9a9d7c`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 34.2 KB (34248 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2516a10a1ea246e0b9391b259194e9f0c6a0669dfd1fccc337e62450f657acc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168737549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6672c03fe2b69c64f378bc123bffddae0ceb6db9d80968d238151dffa2706c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd77c1317d3aa167ce525e562b4150ca934ca0a6931888f4facee3c2832b430`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6319ad690265786884f89a8528c43a7641f5ec4ee13646914915d4fbbeef78b`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 46.5 MB (46450201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e66d86f17d19ad1ee543340630050da5690d888f02bc186b07736702382eb09`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d04267626c09db36ba57db446ffa128a79b92b28e520e9bbb60d84c92b94c0`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 67.2 MB (67201722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58f7aad98ac58f55673caa5b917718391795ff9a3b1f479fc7b787d78f3a354`  
		Last Modified: Thu, 21 Nov 2024 00:26:32 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3d5efe1ed7cf29dad01a2c69594ceb6b0ca523977f24d2767d3ef13de6f6b9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131563af08c9fd291fd2f7c813846125fe715f006a3d396bde57881e1cc0a186`

```dockerfile
```

-	Layers:
	-	`sha256:0c0d39bebfbb0c7af2b65758f081a44f9b9d036cb843b36bf3d346a568b44c6b`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 14.9 MB (14866904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e11d0d508b78947bc35881c46c4902ec23e4a3e0154d972b7b3bbd47d11d51c`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 34.6 KB (34553 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:2bed89deaa6122df7e3bfdb3006d2f09251e2fa925bdd4f6a5ccff7badf070ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:8d111b535dbe6d9fbdaafcb0e3157aff64664ef5052ceae3c57f974166a6cff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171514588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bb57dc6b1d1f9bbd9ab9843af36264c74b6944360d37703fc8cdb932c1587f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5e9755d4041de874322937a7e4aba7eae546b110eaf21c99fd9ee849a31f0b`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6f939b5bdeb93950dd408d5e339b273a43e8129bb908aa25a492fd41925b5e`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4825be18a9da34ab830e99c285416149b22324acc5d70e0fe35719306a672a39`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 6.9 MB (6902532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d101851db8708b91cdb31331ed5fd7584d9109fd10ae799295f8e4b1c372ee`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e6fd8a5fc375e4c5061959d05b0c1727be47165db7fcf903582c94045798ff`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b46238a9af0862e613cea2905d7fa437227a27976fbfcac6e82db8164ba40d`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 47.6 MB (47559393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13a1e3aee9ee85855737c1af5191eef5fbf6d612b81b87f12fcd6dd59d7594a`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444e8e4164f357b6d69d3d1932320dbd2f6e3f0970bf6ee1cacb47a88e87780f`  
		Last Modified: Thu, 21 Nov 2024 00:24:51 GMT  
		Size: 67.0 MB (66961014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef40cced209d5affe747d3e62bcaef3f4800e24279555efd1d9a0a68d5902c1`  
		Last Modified: Thu, 21 Nov 2024 00:24:50 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d24e1e14db4144ad85299ee67329e83eab737d53eabb1c765795ef88d63f8d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97e864c12a8d34ccf20924c9821a42b95f8a22305076fb1ef870ab42aa83988`

```dockerfile
```

-	Layers:
	-	`sha256:978b2ae2ea66ace5f526e29cbe706f1d9b0139220749975cfb696fbcbc463daf`  
		Last Modified: Thu, 21 Nov 2024 00:24:49 GMT  
		Size: 14.9 MB (14871754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade4558bfff869010112ad9fbb8710524f7b764f662ceaedb75071b90e9a9d7c`  
		Last Modified: Thu, 21 Nov 2024 00:24:48 GMT  
		Size: 34.2 KB (34248 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2516a10a1ea246e0b9391b259194e9f0c6a0669dfd1fccc337e62450f657acc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168737549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6672c03fe2b69c64f378bc123bffddae0ceb6db9d80968d238151dffa2706c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd77c1317d3aa167ce525e562b4150ca934ca0a6931888f4facee3c2832b430`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6319ad690265786884f89a8528c43a7641f5ec4ee13646914915d4fbbeef78b`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 46.5 MB (46450201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e66d86f17d19ad1ee543340630050da5690d888f02bc186b07736702382eb09`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d04267626c09db36ba57db446ffa128a79b92b28e520e9bbb60d84c92b94c0`  
		Last Modified: Thu, 21 Nov 2024 00:26:33 GMT  
		Size: 67.2 MB (67201722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58f7aad98ac58f55673caa5b917718391795ff9a3b1f479fc7b787d78f3a354`  
		Last Modified: Thu, 21 Nov 2024 00:26:32 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3d5efe1ed7cf29dad01a2c69594ceb6b0ca523977f24d2767d3ef13de6f6b9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131563af08c9fd291fd2f7c813846125fe715f006a3d396bde57881e1cc0a186`

```dockerfile
```

-	Layers:
	-	`sha256:0c0d39bebfbb0c7af2b65758f081a44f9b9d036cb843b36bf3d346a568b44c6b`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 14.9 MB (14866904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e11d0d508b78947bc35881c46c4902ec23e4a3e0154d972b7b3bbd47d11d51c`  
		Last Modified: Thu, 21 Nov 2024 00:26:31 GMT  
		Size: 34.6 KB (34553 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:2e6739055511aed759dac119b0e41cf2fd44530d5568a1c8f7cbdba5fa9a4fef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:614c6a16ea109306c3e995a60abd1bab28e5f4cdab514d356472c6831e112d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede8426663b5b73ca266326540d860a1b4373ce2f17c123fa3db0f8e71258ba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7f01a1f057b2b5ad037007ac97f29f083655704acf8c2968205f65f26c5e0`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af7f259011cbb37fb5dce3345a4d293d4da2a765217d15487152687a88c799`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97a67e97e66b29535d2820481a78596cf40980fcf397cc207181331ee7a29f5`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 6.9 MB (6902539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa5bf8f003d5e0f4a14c1dbd8b6a201748d866c556049aa9d5e8001d8295292`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f438e53f82d49e9816b5fd0392c450d25d075d67bb7dd78cd7ca83bb6e84bc73`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698b8a4e4c39001876e80c1803d1a7e7b22f594ff3b2cc2d7e4bdd8e27830fb3`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 48.2 MB (48216795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c684c19ed723174982aa4f5fe3d7c186dda61bb0eea75a11855f3b07ca73fd4a`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d842b92c292f40a1b2fae5b54af6d883d02a8cf4ae8b0ec54c5ecb15a62a1be`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 69.1 MB (69090174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6216f14663c125c521d02adf1e2bb0a959a7978559a6eb08f5fedceeacb00`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2cb108ee91f25a1ded70e40712ae8fb43c06a9e70e88444b9633ae46523ce756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb93187421706fac5240e55055ad54cb02c69e5488ed0eafbee18c78a33957ae`

```dockerfile
```

-	Layers:
	-	`sha256:a83848b53bd904283a24e288856be05c01ac866bcb5523964b847510d4ac9878`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 14.9 MB (14876213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633d68c46e114727ef7dea6b2e7f252948185e0c78bc38f4c4756cb132bb7975`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 35.3 KB (35315 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bba66e70d5e271e7f8196af4f1a557e33284a82e14c880fe9e64d4ba94875b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8142099d2b36ba2c2b4a5fa011872f5fff0a51e1d04337c7693c6f5e126653`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f511afaf35971ea3f8093ba2da28ace20fb31f48ef6eecef82dcd5c64ac7e9d`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc7c5c2a66b2cbe7e2799d797107fa0c6643fba56afcb0165748dedf321062a`  
		Last Modified: Thu, 21 Nov 2024 00:24:55 GMT  
		Size: 47.1 MB (47117085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff3e2db7492489a547c35665d5bdfa809da50c9d98e195cccbbdfa725cb5e34`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a473a60f19cad50d3d8739841ee41626150759acca6bed1bbe8b4bfa9345f0fc`  
		Last Modified: Thu, 21 Nov 2024 00:24:56 GMT  
		Size: 69.3 MB (69298550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569d66393be2aef8e99c59e37429480612ae1157cbd3f0c9f49fce34bb45cdce`  
		Last Modified: Thu, 21 Nov 2024 00:24:54 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:794e18033a443ed808c9fa1b30cc38f6f36b793b6e1d6a9f12096e0c4be4e6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717d777feb8b94e1f79413e9287de31d20580e91f93a15cdd45d0ae000197baa`

```dockerfile
```

-	Layers:
	-	`sha256:1bde0305f9f6bd446e9f44e9db2025f849aa6d75e8865c3f9d9ddd7838be8b20`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 14.9 MB (14871399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a18e74dab9e5f3249fdd430cbe82994f022192c79c5f46ad2a7d27a9efcf53`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:2e6739055511aed759dac119b0e41cf2fd44530d5568a1c8f7cbdba5fa9a4fef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:614c6a16ea109306c3e995a60abd1bab28e5f4cdab514d356472c6831e112d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede8426663b5b73ca266326540d860a1b4373ce2f17c123fa3db0f8e71258ba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7f01a1f057b2b5ad037007ac97f29f083655704acf8c2968205f65f26c5e0`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af7f259011cbb37fb5dce3345a4d293d4da2a765217d15487152687a88c799`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97a67e97e66b29535d2820481a78596cf40980fcf397cc207181331ee7a29f5`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 6.9 MB (6902539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa5bf8f003d5e0f4a14c1dbd8b6a201748d866c556049aa9d5e8001d8295292`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f438e53f82d49e9816b5fd0392c450d25d075d67bb7dd78cd7ca83bb6e84bc73`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698b8a4e4c39001876e80c1803d1a7e7b22f594ff3b2cc2d7e4bdd8e27830fb3`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 48.2 MB (48216795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c684c19ed723174982aa4f5fe3d7c186dda61bb0eea75a11855f3b07ca73fd4a`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d842b92c292f40a1b2fae5b54af6d883d02a8cf4ae8b0ec54c5ecb15a62a1be`  
		Last Modified: Thu, 21 Nov 2024 00:24:43 GMT  
		Size: 69.1 MB (69090174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6216f14663c125c521d02adf1e2bb0a959a7978559a6eb08f5fedceeacb00`  
		Last Modified: Thu, 21 Nov 2024 00:24:44 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2cb108ee91f25a1ded70e40712ae8fb43c06a9e70e88444b9633ae46523ce756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb93187421706fac5240e55055ad54cb02c69e5488ed0eafbee18c78a33957ae`

```dockerfile
```

-	Layers:
	-	`sha256:a83848b53bd904283a24e288856be05c01ac866bcb5523964b847510d4ac9878`  
		Last Modified: Thu, 21 Nov 2024 00:24:41 GMT  
		Size: 14.9 MB (14876213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633d68c46e114727ef7dea6b2e7f252948185e0c78bc38f4c4756cb132bb7975`  
		Last Modified: Thu, 21 Nov 2024 00:24:40 GMT  
		Size: 35.3 KB (35315 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:bba66e70d5e271e7f8196af4f1a557e33284a82e14c880fe9e64d4ba94875b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8142099d2b36ba2c2b4a5fa011872f5fff0a51e1d04337c7693c6f5e126653`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
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
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff3c9a8b32242b8299b4ffc47004819e612aef523b26191a58b15341d90a8e`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307980804ab3cee64dbdb1185f73d6696d1f364344a031653a737929f415732`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a907a14294342fd2e77f509e1d7139e536ed1f95fa84260113d9bfbc4ae28`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 6.5 MB (6494591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d177704cec71eac0eef28c2c60f68d0a47330f47d924cac69f88d4d5d775b82`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f511afaf35971ea3f8093ba2da28ace20fb31f48ef6eecef82dcd5c64ac7e9d`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc7c5c2a66b2cbe7e2799d797107fa0c6643fba56afcb0165748dedf321062a`  
		Last Modified: Thu, 21 Nov 2024 00:24:55 GMT  
		Size: 47.1 MB (47117085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff3e2db7492489a547c35665d5bdfa809da50c9d98e195cccbbdfa725cb5e34`  
		Last Modified: Thu, 21 Nov 2024 00:24:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a473a60f19cad50d3d8739841ee41626150759acca6bed1bbe8b4bfa9345f0fc`  
		Last Modified: Thu, 21 Nov 2024 00:24:56 GMT  
		Size: 69.3 MB (69298550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569d66393be2aef8e99c59e37429480612ae1157cbd3f0c9f49fce34bb45cdce`  
		Last Modified: Thu, 21 Nov 2024 00:24:54 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:794e18033a443ed808c9fa1b30cc38f6f36b793b6e1d6a9f12096e0c4be4e6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717d777feb8b94e1f79413e9287de31d20580e91f93a15cdd45d0ae000197baa`

```dockerfile
```

-	Layers:
	-	`sha256:1bde0305f9f6bd446e9f44e9db2025f849aa6d75e8865c3f9d9ddd7838be8b20`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 14.9 MB (14871399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a18e74dab9e5f3249fdd430cbe82994f022192c79c5f46ad2a7d27a9efcf53`  
		Last Modified: Thu, 21 Nov 2024 00:24:52 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json
