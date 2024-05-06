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
-	[`mysql:8.0.37`](#mysql8037)
-	[`mysql:8.0.37-bookworm`](#mysql8037-bookworm)
-	[`mysql:8.0.37-debian`](#mysql8037-debian)
-	[`mysql:8.0.37-oracle`](#mysql8037-oracle)
-	[`mysql:8.0.37-oraclelinux9`](#mysql8037-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.0`](#mysql840)
-	[`mysql:8.4.0-oracle`](#mysql840-oracle)
-	[`mysql:8.4.0-oraclelinux9`](#mysql840-oraclelinux9)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:lts`](#mysqllts)
-	[`mysql:lts-oracle`](#mysqllts-oracle)
-	[`mysql:lts-oraclelinux9`](#mysqllts-oraclelinux9)
-	[`mysql:oracle`](#mysqloracle)
-	[`mysql:oraclelinux9`](#mysqloraclelinux9)

## `mysql:8`

```console
$ docker pull mysql@sha256:f7a8e140a7d6d1e6e0c99eeb0489c50a186ee4ac44ff55323a176529b9a43d33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:53a71a83be1fcbb1489c0fe23d377297f55b77a6c6ce816ca8fa30225adfe2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179341247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8251f0669c6ec890f73deaaf7a7891d8f0cd80821d89b9122b950b679a331c05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:30 GMT
ADD file:c53be7373aad45b6ab1d0accc144396269617e0efcd2892e9521c25fe73fd71e in / 
# Tue, 16 Apr 2024 19:54:30 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd37f6d992035c9959b83f8f96b15cac9d66542a608f378e6e97c17830b72d80`  
		Last Modified: Tue, 16 Apr 2024 19:55:43 GMT  
		Size: 51.3 MB (51320403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafe9b2df4d05db3b7e249359d1e613682fa3f2c6b1a5425297826102fbef66b`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc98c884ffd9ded4226246ffc1dc788bc14b9f3d8b94a5218e1ceed16bbce6d7`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e0e3e0c511ea6802887fbd56ff5b94184ba87b65f3aff0204a6a03216bfcd`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 4.6 MB (4599789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64520c05a6b1b103b680e92e3d2f25bb616a6259a7631625de8a88083993b59c`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d3ebffe5345bf0b168246eb753a3824b01d85c353cdb26924d418de27322eb`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be2eca8f885426e56640bb42c1d5c0ac6be94ce24c5e763bfec7322a7bcc674`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 55.6 MB (55565648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810320f66957eced0dc72d3c938fbf3af47cbccf450ad5e80400ae6c1882e5d5`  
		Last Modified: Tue, 30 Apr 2024 23:51:46 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c425b59d0ec08ecb9ea47d38f9eeaa65c33e9718ffc91608a3556dcb8fc29e6`  
		Last Modified: Tue, 30 Apr 2024 23:51:48 GMT  
		Size: 66.9 MB (66863077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7387b81cae9182cd820343599b7b7432d2d71a707e84d62edc5e57da5955ce0b`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:1428fbc99fd757d0553e1f14e47379e2bece98a3b6973932fdaddc6dd33171e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14812465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76845e51122a392850911f26ed69146a0941ca077f4801a609072e495026fb5c`

```dockerfile
```

-	Layers:
	-	`sha256:317e850b1e19b8eafa1b0ceef34783d95fbb1f3f0b5d38965767570936d3ca23`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 14.8 MB (14777374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3f37eece2d2f368cff32246af89a9f298aec0374bb9047d61d3105a5c4186af`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cf99e569402db84ac017aa56d09059f0b226f9a9c5644de24cffd4266dbda62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177224730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc9b4335a45c26b4204202c74127df42d2a28b22180e37f261c3809eb462b6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:12:16 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 16 Apr 2024 19:12:17 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae691a8c1b16066cca244ed4ea39e9b5c9af6dbf8d0347ed9ceeade76a8e750b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe011e50abc101883db1ab22a9bb6244d829c9bbe68c05b6874c0c1ed124a87`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c88c8fbaa893a4e5b948f4691a54b78782bcf57f77b47feff2c928dbce7653`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 4.3 MB (4302741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d028b2b1f150e0aeb6bfeaa5b9a244f5e9603ab59991c75aa9e0d26af02482`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc284ef09f941151cf5166e86b07fcc19f66f26f235d7dc6f20913bb6b4de338`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00367d65ff8291d336c1e5f8d314f111717488b4657e5da52543c33b829504de`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 54.6 MB (54633231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d4b7ff3dc2fade4a92765d67a8c5ce7565bcdbf4c3d2c86d58790a732d37c1`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafe7641a560f53680cd7f1572d853f011df819bac82c80b1bc568446ecd6c28`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 67.3 MB (67283710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b85ac37bb0900dbd819827cfdb8ae885be535195d33bc2dfac13b79e9c534f`  
		Last Modified: Wed, 01 May 2024 00:29:01 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:b0701fac0befd17e4cdbdbb39fa07cb5237a6b439fb49f21cda49f39be1b7523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14810777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75308f5373963ad1bd230e3d4c9bfca49ac4dddbce1af270171bba973f5685a`

```dockerfile
```

-	Layers:
	-	`sha256:416437ab84a9e25108a8a94da095cb890a8d5158e2cb5719e340d4f946a58baa`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 14.8 MB (14775654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3324096fdc8f73215f25425dee83087e5e91b5eb863938333beced58a0b0d97b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:f7a8e140a7d6d1e6e0c99eeb0489c50a186ee4ac44ff55323a176529b9a43d33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:53a71a83be1fcbb1489c0fe23d377297f55b77a6c6ce816ca8fa30225adfe2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179341247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8251f0669c6ec890f73deaaf7a7891d8f0cd80821d89b9122b950b679a331c05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:30 GMT
ADD file:c53be7373aad45b6ab1d0accc144396269617e0efcd2892e9521c25fe73fd71e in / 
# Tue, 16 Apr 2024 19:54:30 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd37f6d992035c9959b83f8f96b15cac9d66542a608f378e6e97c17830b72d80`  
		Last Modified: Tue, 16 Apr 2024 19:55:43 GMT  
		Size: 51.3 MB (51320403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafe9b2df4d05db3b7e249359d1e613682fa3f2c6b1a5425297826102fbef66b`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc98c884ffd9ded4226246ffc1dc788bc14b9f3d8b94a5218e1ceed16bbce6d7`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e0e3e0c511ea6802887fbd56ff5b94184ba87b65f3aff0204a6a03216bfcd`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 4.6 MB (4599789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64520c05a6b1b103b680e92e3d2f25bb616a6259a7631625de8a88083993b59c`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d3ebffe5345bf0b168246eb753a3824b01d85c353cdb26924d418de27322eb`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be2eca8f885426e56640bb42c1d5c0ac6be94ce24c5e763bfec7322a7bcc674`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 55.6 MB (55565648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810320f66957eced0dc72d3c938fbf3af47cbccf450ad5e80400ae6c1882e5d5`  
		Last Modified: Tue, 30 Apr 2024 23:51:46 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c425b59d0ec08ecb9ea47d38f9eeaa65c33e9718ffc91608a3556dcb8fc29e6`  
		Last Modified: Tue, 30 Apr 2024 23:51:48 GMT  
		Size: 66.9 MB (66863077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7387b81cae9182cd820343599b7b7432d2d71a707e84d62edc5e57da5955ce0b`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1428fbc99fd757d0553e1f14e47379e2bece98a3b6973932fdaddc6dd33171e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14812465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76845e51122a392850911f26ed69146a0941ca077f4801a609072e495026fb5c`

```dockerfile
```

-	Layers:
	-	`sha256:317e850b1e19b8eafa1b0ceef34783d95fbb1f3f0b5d38965767570936d3ca23`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 14.8 MB (14777374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3f37eece2d2f368cff32246af89a9f298aec0374bb9047d61d3105a5c4186af`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cf99e569402db84ac017aa56d09059f0b226f9a9c5644de24cffd4266dbda62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177224730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc9b4335a45c26b4204202c74127df42d2a28b22180e37f261c3809eb462b6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:12:16 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 16 Apr 2024 19:12:17 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae691a8c1b16066cca244ed4ea39e9b5c9af6dbf8d0347ed9ceeade76a8e750b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe011e50abc101883db1ab22a9bb6244d829c9bbe68c05b6874c0c1ed124a87`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c88c8fbaa893a4e5b948f4691a54b78782bcf57f77b47feff2c928dbce7653`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 4.3 MB (4302741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d028b2b1f150e0aeb6bfeaa5b9a244f5e9603ab59991c75aa9e0d26af02482`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc284ef09f941151cf5166e86b07fcc19f66f26f235d7dc6f20913bb6b4de338`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00367d65ff8291d336c1e5f8d314f111717488b4657e5da52543c33b829504de`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 54.6 MB (54633231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d4b7ff3dc2fade4a92765d67a8c5ce7565bcdbf4c3d2c86d58790a732d37c1`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafe7641a560f53680cd7f1572d853f011df819bac82c80b1bc568446ecd6c28`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 67.3 MB (67283710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b85ac37bb0900dbd819827cfdb8ae885be535195d33bc2dfac13b79e9c534f`  
		Last Modified: Wed, 01 May 2024 00:29:01 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b0701fac0befd17e4cdbdbb39fa07cb5237a6b439fb49f21cda49f39be1b7523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14810777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75308f5373963ad1bd230e3d4c9bfca49ac4dddbce1af270171bba973f5685a`

```dockerfile
```

-	Layers:
	-	`sha256:416437ab84a9e25108a8a94da095cb890a8d5158e2cb5719e340d4f946a58baa`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 14.8 MB (14775654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3324096fdc8f73215f25425dee83087e5e91b5eb863938333beced58a0b0d97b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

**does not exist** (yet?)

## `mysql:8.0`

```console
$ docker pull mysql@sha256:0f90283199964e9cc2a45c73ed2991da6943f416368025433932ed81007235a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:9c83d1058a148b74ed596d79ec71e03bd9cd402f060c567176de8f1c2cdfd050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 MB (178086090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a3e526fca25ac53b29cb76ab0d61eef7f2febcfe769c3cc93166b756b13fcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:30 GMT
ADD file:c53be7373aad45b6ab1d0accc144396269617e0efcd2892e9521c25fe73fd71e in / 
# Tue, 16 Apr 2024 19:54:30 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd37f6d992035c9959b83f8f96b15cac9d66542a608f378e6e97c17830b72d80`  
		Last Modified: Tue, 16 Apr 2024 19:55:43 GMT  
		Size: 51.3 MB (51320403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efa407487171d286e76ea28a365ce5e6fa411f8b3c0b5a1e6f4d9dbe06f8b1d`  
		Last Modified: Tue, 30 Apr 2024 23:51:42 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc98c884ffd9ded4226246ffc1dc788bc14b9f3d8b94a5218e1ceed16bbce6d7`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cecce821c2c196d2132315c7c18d6e7068be17151bb3b94379f16a31dc18f1c`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 4.6 MB (4599656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8604755048f050e54972d0ab0f76fd3bcf96a0077697064b6c068e84d4610a73`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50ac7eb5d18a37df58ff959aad0695b54978bb863f45da28df864e9278680c3`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9d9ac48f89e0d3f6ea6100895fad08baaf3e0ce96b1f1dc50b1b087b5b657e`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 59.1 MB (59057442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cace423609706e7ab02b5998468586a21299e0c6d22dfe8fc7ae7f380cfdc8f`  
		Last Modified: Tue, 30 Apr 2024 23:51:44 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63f89d11629fb1b346fd6e49d5fb226ce810ddb40ddbe989c2585c8d6492cd5`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 62.1 MB (62116147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6d92a49124071a98ee8e70f9f60538cc0597766a9d1ba37f35225a6f488fc9`  
		Last Modified: Tue, 30 Apr 2024 23:51:44 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e955c058ffb5fde4b5348fb86ac5437cf45d1c1d8aeb06a300de2633c9746f3b`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:171d6bb41ef44f1e63f1d1d01221c312ea640a1240e1bf37a7b6a423ea13b0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14701356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab9a6d18c6c95cdf10a0d6a1a0618a1547d7f144f53534bb0ef94c74aba8c60`

```dockerfile
```

-	Layers:
	-	`sha256:477a78eef629b3ce02ca42384f45ecc5620887d1b4dd907ccd811a3c89c1f8d1`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 14.7 MB (14666457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdc12c340879ff72dde06dabdc18c92fff180c95128524a572dcda32d908848d`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 34.9 KB (34899 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f4360337f719defad09baa2b7903241df4fe10767bc3da7208cc9fb912b50e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176323852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8053e13c41910f7a256d1813b7f94389bb2037cdc6d5d4b1c227a4e964c587b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:12:16 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 16 Apr 2024 19:12:17 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae691a8c1b16066cca244ed4ea39e9b5c9af6dbf8d0347ed9ceeade76a8e750b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe011e50abc101883db1ab22a9bb6244d829c9bbe68c05b6874c0c1ed124a87`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c88c8fbaa893a4e5b948f4691a54b78782bcf57f77b47feff2c928dbce7653`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 4.3 MB (4302741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d028b2b1f150e0aeb6bfeaa5b9a244f5e9603ab59991c75aa9e0d26af02482`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cbeb759403d76c018dc9047dadc7a00c9a6bdb78d7664004ecf487631fce98`  
		Last Modified: Wed, 01 May 2024 00:30:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ceebeb4e87b339016212257a51b4182c29ec87324baf655e99d3514e2148b3`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 58.1 MB (58142450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70daaf3f7c42ba469d3b17a67f38fe65546ccd13c3d3b9e764773ef6564d4c75`  
		Last Modified: Wed, 01 May 2024 00:30:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f4c19f9b852bc18085d7a237f610b8d17e9ae3cf9df27dfcaedb17ad66989f`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 62.9 MB (62873495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c347df2d48aa6a0a13b204f922e3aa0d2a903a2141f7fec56e238827618f83c`  
		Last Modified: Wed, 01 May 2024 00:31:00 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8903dbcded2d02243b239de4f8e5856b1408a76d92a85ea8da3eadb51665215c`  
		Last Modified: Wed, 01 May 2024 00:31:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:f1be1d3c82c2db05575f68e30fa53a8013b4b7c5b8e89c755c34895dcc8bcbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14699465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5bd00c9bd1aec121e35b9fec92b8a58853f6285580685787191df7fefdd80c`

```dockerfile
```

-	Layers:
	-	`sha256:e8c0b935e4f2c33fbf4a4605b9a99a5e7e4a9926dd4c7745cc672cda56ae80e2`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 14.7 MB (14664719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3eff94985dd0ee34d72bc4ce77345aad13b06e0555aea06a2238c9b1154b6d7`  
		Last Modified: Wed, 01 May 2024 00:30:58 GMT  
		Size: 34.7 KB (34746 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:23e2890afb54aa00ea7ff4f4f657fc5a853e37d7d9a85d9d1ed8b1dbee7694e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:3d02aa81c903a42cebc6e6bb407e1694ab1818bda55bf15b61a2742624fb8054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184723578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bfd90cb949d20f852d49d5ad85491c93c1b9b91d45fe208e380321720f5899`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1debian12
# Tue, 30 Apr 2024 04:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9bde18031fe909f543254cc2e733160f72a752205a2949c6b40a4fb93b5019`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f5b132130169e78e654966bd3298ae5547afe735d026b6c503f9cd781578b3`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 4.4 MB (4422801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55afbcd0ee95b43da7f32cf64b89260ace0979ea80882f734ffa5d0c3b59312`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 1.4 MB (1449199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143e159e9ba53f9ab249e4dd23b8146c96256ec7429fd67b703970048d25410`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9824c3f585b77f8a653ef04d6f855bd4f083fc9c13ff653d2b1af5e3016162`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 15.3 MB (15281632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d8aed07a3abd808a32a1c8f93bb986712dcc84c94ce5595119523ccaad776`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3668217c0d32afdc03ae00ca9b951002c2712c6294d9428c48b34c1806db544b`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1222274583182e0fc12661ac9ce631dc065e4cc10dcda00a146d33f1fabe87`  
		Last Modified: Tue, 30 Apr 2024 23:50:29 GMT  
		Size: 134.4 MB (134409341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb93646b643b58c7717ff573c97f8732ea09bd6d616bf98ce13d1fe87e96531f`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7470a28f457e6deac3f34c84d6c8dbe20300497a2245d679d7dced2b8b7ad8`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a34841c68669377f766eee6f5b9fe388c30796c6ec46e96452fc5ad2d2ce592`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:d1ab433d5294c0fd73d3b0dbd930072a2b008063272b1535d23e5b2aac7f8825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a86630f43c05e4d6049f3171246f462c68e29f488209ee07adf1d9301375a6`

```dockerfile
```

-	Layers:
	-	`sha256:c80288de35aea4344988f230740a6e5e3d3d3d7c957084b23bd95c884ce4d68c`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 4.0 MB (3953561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ca3c8ebbcb5ff586f0a9c49e88b165735b31fed5b7bfeace4df33efb746cb2`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 34.3 KB (34255 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:23e2890afb54aa00ea7ff4f4f657fc5a853e37d7d9a85d9d1ed8b1dbee7694e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:3d02aa81c903a42cebc6e6bb407e1694ab1818bda55bf15b61a2742624fb8054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184723578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bfd90cb949d20f852d49d5ad85491c93c1b9b91d45fe208e380321720f5899`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1debian12
# Tue, 30 Apr 2024 04:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9bde18031fe909f543254cc2e733160f72a752205a2949c6b40a4fb93b5019`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f5b132130169e78e654966bd3298ae5547afe735d026b6c503f9cd781578b3`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 4.4 MB (4422801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55afbcd0ee95b43da7f32cf64b89260ace0979ea80882f734ffa5d0c3b59312`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 1.4 MB (1449199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143e159e9ba53f9ab249e4dd23b8146c96256ec7429fd67b703970048d25410`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9824c3f585b77f8a653ef04d6f855bd4f083fc9c13ff653d2b1af5e3016162`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 15.3 MB (15281632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d8aed07a3abd808a32a1c8f93bb986712dcc84c94ce5595119523ccaad776`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3668217c0d32afdc03ae00ca9b951002c2712c6294d9428c48b34c1806db544b`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1222274583182e0fc12661ac9ce631dc065e4cc10dcda00a146d33f1fabe87`  
		Last Modified: Tue, 30 Apr 2024 23:50:29 GMT  
		Size: 134.4 MB (134409341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb93646b643b58c7717ff573c97f8732ea09bd6d616bf98ce13d1fe87e96531f`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7470a28f457e6deac3f34c84d6c8dbe20300497a2245d679d7dced2b8b7ad8`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a34841c68669377f766eee6f5b9fe388c30796c6ec46e96452fc5ad2d2ce592`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:d1ab433d5294c0fd73d3b0dbd930072a2b008063272b1535d23e5b2aac7f8825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a86630f43c05e4d6049f3171246f462c68e29f488209ee07adf1d9301375a6`

```dockerfile
```

-	Layers:
	-	`sha256:c80288de35aea4344988f230740a6e5e3d3d3d7c957084b23bd95c884ce4d68c`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 4.0 MB (3953561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ca3c8ebbcb5ff586f0a9c49e88b165735b31fed5b7bfeace4df33efb746cb2`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 34.3 KB (34255 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:0f90283199964e9cc2a45c73ed2991da6943f416368025433932ed81007235a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:9c83d1058a148b74ed596d79ec71e03bd9cd402f060c567176de8f1c2cdfd050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 MB (178086090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a3e526fca25ac53b29cb76ab0d61eef7f2febcfe769c3cc93166b756b13fcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:30 GMT
ADD file:c53be7373aad45b6ab1d0accc144396269617e0efcd2892e9521c25fe73fd71e in / 
# Tue, 16 Apr 2024 19:54:30 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd37f6d992035c9959b83f8f96b15cac9d66542a608f378e6e97c17830b72d80`  
		Last Modified: Tue, 16 Apr 2024 19:55:43 GMT  
		Size: 51.3 MB (51320403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efa407487171d286e76ea28a365ce5e6fa411f8b3c0b5a1e6f4d9dbe06f8b1d`  
		Last Modified: Tue, 30 Apr 2024 23:51:42 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc98c884ffd9ded4226246ffc1dc788bc14b9f3d8b94a5218e1ceed16bbce6d7`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cecce821c2c196d2132315c7c18d6e7068be17151bb3b94379f16a31dc18f1c`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 4.6 MB (4599656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8604755048f050e54972d0ab0f76fd3bcf96a0077697064b6c068e84d4610a73`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50ac7eb5d18a37df58ff959aad0695b54978bb863f45da28df864e9278680c3`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9d9ac48f89e0d3f6ea6100895fad08baaf3e0ce96b1f1dc50b1b087b5b657e`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 59.1 MB (59057442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cace423609706e7ab02b5998468586a21299e0c6d22dfe8fc7ae7f380cfdc8f`  
		Last Modified: Tue, 30 Apr 2024 23:51:44 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63f89d11629fb1b346fd6e49d5fb226ce810ddb40ddbe989c2585c8d6492cd5`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 62.1 MB (62116147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6d92a49124071a98ee8e70f9f60538cc0597766a9d1ba37f35225a6f488fc9`  
		Last Modified: Tue, 30 Apr 2024 23:51:44 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e955c058ffb5fde4b5348fb86ac5437cf45d1c1d8aeb06a300de2633c9746f3b`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:171d6bb41ef44f1e63f1d1d01221c312ea640a1240e1bf37a7b6a423ea13b0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14701356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab9a6d18c6c95cdf10a0d6a1a0618a1547d7f144f53534bb0ef94c74aba8c60`

```dockerfile
```

-	Layers:
	-	`sha256:477a78eef629b3ce02ca42384f45ecc5620887d1b4dd907ccd811a3c89c1f8d1`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 14.7 MB (14666457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdc12c340879ff72dde06dabdc18c92fff180c95128524a572dcda32d908848d`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 34.9 KB (34899 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f4360337f719defad09baa2b7903241df4fe10767bc3da7208cc9fb912b50e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176323852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8053e13c41910f7a256d1813b7f94389bb2037cdc6d5d4b1c227a4e964c587b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:12:16 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 16 Apr 2024 19:12:17 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae691a8c1b16066cca244ed4ea39e9b5c9af6dbf8d0347ed9ceeade76a8e750b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe011e50abc101883db1ab22a9bb6244d829c9bbe68c05b6874c0c1ed124a87`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c88c8fbaa893a4e5b948f4691a54b78782bcf57f77b47feff2c928dbce7653`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 4.3 MB (4302741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d028b2b1f150e0aeb6bfeaa5b9a244f5e9603ab59991c75aa9e0d26af02482`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cbeb759403d76c018dc9047dadc7a00c9a6bdb78d7664004ecf487631fce98`  
		Last Modified: Wed, 01 May 2024 00:30:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ceebeb4e87b339016212257a51b4182c29ec87324baf655e99d3514e2148b3`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 58.1 MB (58142450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70daaf3f7c42ba469d3b17a67f38fe65546ccd13c3d3b9e764773ef6564d4c75`  
		Last Modified: Wed, 01 May 2024 00:30:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f4c19f9b852bc18085d7a237f610b8d17e9ae3cf9df27dfcaedb17ad66989f`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 62.9 MB (62873495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c347df2d48aa6a0a13b204f922e3aa0d2a903a2141f7fec56e238827618f83c`  
		Last Modified: Wed, 01 May 2024 00:31:00 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8903dbcded2d02243b239de4f8e5856b1408a76d92a85ea8da3eadb51665215c`  
		Last Modified: Wed, 01 May 2024 00:31:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f1be1d3c82c2db05575f68e30fa53a8013b4b7c5b8e89c755c34895dcc8bcbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14699465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5bd00c9bd1aec121e35b9fec92b8a58853f6285580685787191df7fefdd80c`

```dockerfile
```

-	Layers:
	-	`sha256:e8c0b935e4f2c33fbf4a4605b9a99a5e7e4a9926dd4c7745cc672cda56ae80e2`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 14.7 MB (14664719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3eff94985dd0ee34d72bc4ce77345aad13b06e0555aea06a2238c9b1154b6d7`  
		Last Modified: Wed, 01 May 2024 00:30:58 GMT  
		Size: 34.7 KB (34746 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

**does not exist** (yet?)

## `mysql:8.0.37`

```console
$ docker pull mysql@sha256:0f90283199964e9cc2a45c73ed2991da6943f416368025433932ed81007235a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.37` - linux; amd64

```console
$ docker pull mysql@sha256:9c83d1058a148b74ed596d79ec71e03bd9cd402f060c567176de8f1c2cdfd050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 MB (178086090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a3e526fca25ac53b29cb76ab0d61eef7f2febcfe769c3cc93166b756b13fcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:30 GMT
ADD file:c53be7373aad45b6ab1d0accc144396269617e0efcd2892e9521c25fe73fd71e in / 
# Tue, 16 Apr 2024 19:54:30 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd37f6d992035c9959b83f8f96b15cac9d66542a608f378e6e97c17830b72d80`  
		Last Modified: Tue, 16 Apr 2024 19:55:43 GMT  
		Size: 51.3 MB (51320403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efa407487171d286e76ea28a365ce5e6fa411f8b3c0b5a1e6f4d9dbe06f8b1d`  
		Last Modified: Tue, 30 Apr 2024 23:51:42 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc98c884ffd9ded4226246ffc1dc788bc14b9f3d8b94a5218e1ceed16bbce6d7`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cecce821c2c196d2132315c7c18d6e7068be17151bb3b94379f16a31dc18f1c`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 4.6 MB (4599656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8604755048f050e54972d0ab0f76fd3bcf96a0077697064b6c068e84d4610a73`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50ac7eb5d18a37df58ff959aad0695b54978bb863f45da28df864e9278680c3`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9d9ac48f89e0d3f6ea6100895fad08baaf3e0ce96b1f1dc50b1b087b5b657e`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 59.1 MB (59057442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cace423609706e7ab02b5998468586a21299e0c6d22dfe8fc7ae7f380cfdc8f`  
		Last Modified: Tue, 30 Apr 2024 23:51:44 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63f89d11629fb1b346fd6e49d5fb226ce810ddb40ddbe989c2585c8d6492cd5`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 62.1 MB (62116147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6d92a49124071a98ee8e70f9f60538cc0597766a9d1ba37f35225a6f488fc9`  
		Last Modified: Tue, 30 Apr 2024 23:51:44 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e955c058ffb5fde4b5348fb86ac5437cf45d1c1d8aeb06a300de2633c9746f3b`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37` - unknown; unknown

```console
$ docker pull mysql@sha256:171d6bb41ef44f1e63f1d1d01221c312ea640a1240e1bf37a7b6a423ea13b0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14701356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab9a6d18c6c95cdf10a0d6a1a0618a1547d7f144f53534bb0ef94c74aba8c60`

```dockerfile
```

-	Layers:
	-	`sha256:477a78eef629b3ce02ca42384f45ecc5620887d1b4dd907ccd811a3c89c1f8d1`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 14.7 MB (14666457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdc12c340879ff72dde06dabdc18c92fff180c95128524a572dcda32d908848d`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 34.9 KB (34899 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.37` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f4360337f719defad09baa2b7903241df4fe10767bc3da7208cc9fb912b50e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176323852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8053e13c41910f7a256d1813b7f94389bb2037cdc6d5d4b1c227a4e964c587b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:12:16 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 16 Apr 2024 19:12:17 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae691a8c1b16066cca244ed4ea39e9b5c9af6dbf8d0347ed9ceeade76a8e750b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe011e50abc101883db1ab22a9bb6244d829c9bbe68c05b6874c0c1ed124a87`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c88c8fbaa893a4e5b948f4691a54b78782bcf57f77b47feff2c928dbce7653`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 4.3 MB (4302741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d028b2b1f150e0aeb6bfeaa5b9a244f5e9603ab59991c75aa9e0d26af02482`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cbeb759403d76c018dc9047dadc7a00c9a6bdb78d7664004ecf487631fce98`  
		Last Modified: Wed, 01 May 2024 00:30:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ceebeb4e87b339016212257a51b4182c29ec87324baf655e99d3514e2148b3`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 58.1 MB (58142450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70daaf3f7c42ba469d3b17a67f38fe65546ccd13c3d3b9e764773ef6564d4c75`  
		Last Modified: Wed, 01 May 2024 00:30:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f4c19f9b852bc18085d7a237f610b8d17e9ae3cf9df27dfcaedb17ad66989f`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 62.9 MB (62873495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c347df2d48aa6a0a13b204f922e3aa0d2a903a2141f7fec56e238827618f83c`  
		Last Modified: Wed, 01 May 2024 00:31:00 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8903dbcded2d02243b239de4f8e5856b1408a76d92a85ea8da3eadb51665215c`  
		Last Modified: Wed, 01 May 2024 00:31:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37` - unknown; unknown

```console
$ docker pull mysql@sha256:f1be1d3c82c2db05575f68e30fa53a8013b4b7c5b8e89c755c34895dcc8bcbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14699465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5bd00c9bd1aec121e35b9fec92b8a58853f6285580685787191df7fefdd80c`

```dockerfile
```

-	Layers:
	-	`sha256:e8c0b935e4f2c33fbf4a4605b9a99a5e7e4a9926dd4c7745cc672cda56ae80e2`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 14.7 MB (14664719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3eff94985dd0ee34d72bc4ce77345aad13b06e0555aea06a2238c9b1154b6d7`  
		Last Modified: Wed, 01 May 2024 00:30:58 GMT  
		Size: 34.7 KB (34746 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.37-bookworm`

```console
$ docker pull mysql@sha256:23e2890afb54aa00ea7ff4f4f657fc5a853e37d7d9a85d9d1ed8b1dbee7694e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.37-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:3d02aa81c903a42cebc6e6bb407e1694ab1818bda55bf15b61a2742624fb8054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184723578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bfd90cb949d20f852d49d5ad85491c93c1b9b91d45fe208e380321720f5899`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1debian12
# Tue, 30 Apr 2024 04:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9bde18031fe909f543254cc2e733160f72a752205a2949c6b40a4fb93b5019`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f5b132130169e78e654966bd3298ae5547afe735d026b6c503f9cd781578b3`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 4.4 MB (4422801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55afbcd0ee95b43da7f32cf64b89260ace0979ea80882f734ffa5d0c3b59312`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 1.4 MB (1449199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143e159e9ba53f9ab249e4dd23b8146c96256ec7429fd67b703970048d25410`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9824c3f585b77f8a653ef04d6f855bd4f083fc9c13ff653d2b1af5e3016162`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 15.3 MB (15281632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d8aed07a3abd808a32a1c8f93bb986712dcc84c94ce5595119523ccaad776`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3668217c0d32afdc03ae00ca9b951002c2712c6294d9428c48b34c1806db544b`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1222274583182e0fc12661ac9ce631dc065e4cc10dcda00a146d33f1fabe87`  
		Last Modified: Tue, 30 Apr 2024 23:50:29 GMT  
		Size: 134.4 MB (134409341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb93646b643b58c7717ff573c97f8732ea09bd6d616bf98ce13d1fe87e96531f`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7470a28f457e6deac3f34c84d6c8dbe20300497a2245d679d7dced2b8b7ad8`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a34841c68669377f766eee6f5b9fe388c30796c6ec46e96452fc5ad2d2ce592`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:d1ab433d5294c0fd73d3b0dbd930072a2b008063272b1535d23e5b2aac7f8825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a86630f43c05e4d6049f3171246f462c68e29f488209ee07adf1d9301375a6`

```dockerfile
```

-	Layers:
	-	`sha256:c80288de35aea4344988f230740a6e5e3d3d3d7c957084b23bd95c884ce4d68c`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 4.0 MB (3953561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ca3c8ebbcb5ff586f0a9c49e88b165735b31fed5b7bfeace4df33efb746cb2`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 34.3 KB (34255 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.37-debian`

```console
$ docker pull mysql@sha256:23e2890afb54aa00ea7ff4f4f657fc5a853e37d7d9a85d9d1ed8b1dbee7694e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.37-debian` - linux; amd64

```console
$ docker pull mysql@sha256:3d02aa81c903a42cebc6e6bb407e1694ab1818bda55bf15b61a2742624fb8054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184723578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bfd90cb949d20f852d49d5ad85491c93c1b9b91d45fe208e380321720f5899`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1debian12
# Tue, 30 Apr 2024 04:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9bde18031fe909f543254cc2e733160f72a752205a2949c6b40a4fb93b5019`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f5b132130169e78e654966bd3298ae5547afe735d026b6c503f9cd781578b3`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 4.4 MB (4422801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55afbcd0ee95b43da7f32cf64b89260ace0979ea80882f734ffa5d0c3b59312`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 1.4 MB (1449199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143e159e9ba53f9ab249e4dd23b8146c96256ec7429fd67b703970048d25410`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9824c3f585b77f8a653ef04d6f855bd4f083fc9c13ff653d2b1af5e3016162`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 15.3 MB (15281632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d8aed07a3abd808a32a1c8f93bb986712dcc84c94ce5595119523ccaad776`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3668217c0d32afdc03ae00ca9b951002c2712c6294d9428c48b34c1806db544b`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1222274583182e0fc12661ac9ce631dc065e4cc10dcda00a146d33f1fabe87`  
		Last Modified: Tue, 30 Apr 2024 23:50:29 GMT  
		Size: 134.4 MB (134409341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb93646b643b58c7717ff573c97f8732ea09bd6d616bf98ce13d1fe87e96531f`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7470a28f457e6deac3f34c84d6c8dbe20300497a2245d679d7dced2b8b7ad8`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a34841c68669377f766eee6f5b9fe388c30796c6ec46e96452fc5ad2d2ce592`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:d1ab433d5294c0fd73d3b0dbd930072a2b008063272b1535d23e5b2aac7f8825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a86630f43c05e4d6049f3171246f462c68e29f488209ee07adf1d9301375a6`

```dockerfile
```

-	Layers:
	-	`sha256:c80288de35aea4344988f230740a6e5e3d3d3d7c957084b23bd95c884ce4d68c`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 4.0 MB (3953561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ca3c8ebbcb5ff586f0a9c49e88b165735b31fed5b7bfeace4df33efb746cb2`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 34.3 KB (34255 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.37-oracle`

```console
$ docker pull mysql@sha256:0f90283199964e9cc2a45c73ed2991da6943f416368025433932ed81007235a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.37-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:9c83d1058a148b74ed596d79ec71e03bd9cd402f060c567176de8f1c2cdfd050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 MB (178086090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a3e526fca25ac53b29cb76ab0d61eef7f2febcfe769c3cc93166b756b13fcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:30 GMT
ADD file:c53be7373aad45b6ab1d0accc144396269617e0efcd2892e9521c25fe73fd71e in / 
# Tue, 16 Apr 2024 19:54:30 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd37f6d992035c9959b83f8f96b15cac9d66542a608f378e6e97c17830b72d80`  
		Last Modified: Tue, 16 Apr 2024 19:55:43 GMT  
		Size: 51.3 MB (51320403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efa407487171d286e76ea28a365ce5e6fa411f8b3c0b5a1e6f4d9dbe06f8b1d`  
		Last Modified: Tue, 30 Apr 2024 23:51:42 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc98c884ffd9ded4226246ffc1dc788bc14b9f3d8b94a5218e1ceed16bbce6d7`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cecce821c2c196d2132315c7c18d6e7068be17151bb3b94379f16a31dc18f1c`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 4.6 MB (4599656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8604755048f050e54972d0ab0f76fd3bcf96a0077697064b6c068e84d4610a73`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50ac7eb5d18a37df58ff959aad0695b54978bb863f45da28df864e9278680c3`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9d9ac48f89e0d3f6ea6100895fad08baaf3e0ce96b1f1dc50b1b087b5b657e`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 59.1 MB (59057442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cace423609706e7ab02b5998468586a21299e0c6d22dfe8fc7ae7f380cfdc8f`  
		Last Modified: Tue, 30 Apr 2024 23:51:44 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63f89d11629fb1b346fd6e49d5fb226ce810ddb40ddbe989c2585c8d6492cd5`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 62.1 MB (62116147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6d92a49124071a98ee8e70f9f60538cc0597766a9d1ba37f35225a6f488fc9`  
		Last Modified: Tue, 30 Apr 2024 23:51:44 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e955c058ffb5fde4b5348fb86ac5437cf45d1c1d8aeb06a300de2633c9746f3b`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:171d6bb41ef44f1e63f1d1d01221c312ea640a1240e1bf37a7b6a423ea13b0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14701356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab9a6d18c6c95cdf10a0d6a1a0618a1547d7f144f53534bb0ef94c74aba8c60`

```dockerfile
```

-	Layers:
	-	`sha256:477a78eef629b3ce02ca42384f45ecc5620887d1b4dd907ccd811a3c89c1f8d1`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 14.7 MB (14666457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdc12c340879ff72dde06dabdc18c92fff180c95128524a572dcda32d908848d`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 34.9 KB (34899 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.37-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f4360337f719defad09baa2b7903241df4fe10767bc3da7208cc9fb912b50e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176323852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8053e13c41910f7a256d1813b7f94389bb2037cdc6d5d4b1c227a4e964c587b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:12:16 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 16 Apr 2024 19:12:17 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae691a8c1b16066cca244ed4ea39e9b5c9af6dbf8d0347ed9ceeade76a8e750b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe011e50abc101883db1ab22a9bb6244d829c9bbe68c05b6874c0c1ed124a87`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c88c8fbaa893a4e5b948f4691a54b78782bcf57f77b47feff2c928dbce7653`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 4.3 MB (4302741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d028b2b1f150e0aeb6bfeaa5b9a244f5e9603ab59991c75aa9e0d26af02482`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cbeb759403d76c018dc9047dadc7a00c9a6bdb78d7664004ecf487631fce98`  
		Last Modified: Wed, 01 May 2024 00:30:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ceebeb4e87b339016212257a51b4182c29ec87324baf655e99d3514e2148b3`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 58.1 MB (58142450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70daaf3f7c42ba469d3b17a67f38fe65546ccd13c3d3b9e764773ef6564d4c75`  
		Last Modified: Wed, 01 May 2024 00:30:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f4c19f9b852bc18085d7a237f610b8d17e9ae3cf9df27dfcaedb17ad66989f`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 62.9 MB (62873495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c347df2d48aa6a0a13b204f922e3aa0d2a903a2141f7fec56e238827618f83c`  
		Last Modified: Wed, 01 May 2024 00:31:00 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8903dbcded2d02243b239de4f8e5856b1408a76d92a85ea8da3eadb51665215c`  
		Last Modified: Wed, 01 May 2024 00:31:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f1be1d3c82c2db05575f68e30fa53a8013b4b7c5b8e89c755c34895dcc8bcbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14699465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5bd00c9bd1aec121e35b9fec92b8a58853f6285580685787191df7fefdd80c`

```dockerfile
```

-	Layers:
	-	`sha256:e8c0b935e4f2c33fbf4a4605b9a99a5e7e4a9926dd4c7745cc672cda56ae80e2`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 14.7 MB (14664719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3eff94985dd0ee34d72bc4ce77345aad13b06e0555aea06a2238c9b1154b6d7`  
		Last Modified: Wed, 01 May 2024 00:30:58 GMT  
		Size: 34.7 KB (34746 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.37-oraclelinux9`

**does not exist** (yet?)

## `mysql:8.4`

```console
$ docker pull mysql@sha256:f7a8e140a7d6d1e6e0c99eeb0489c50a186ee4ac44ff55323a176529b9a43d33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:53a71a83be1fcbb1489c0fe23d377297f55b77a6c6ce816ca8fa30225adfe2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179341247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8251f0669c6ec890f73deaaf7a7891d8f0cd80821d89b9122b950b679a331c05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:30 GMT
ADD file:c53be7373aad45b6ab1d0accc144396269617e0efcd2892e9521c25fe73fd71e in / 
# Tue, 16 Apr 2024 19:54:30 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd37f6d992035c9959b83f8f96b15cac9d66542a608f378e6e97c17830b72d80`  
		Last Modified: Tue, 16 Apr 2024 19:55:43 GMT  
		Size: 51.3 MB (51320403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafe9b2df4d05db3b7e249359d1e613682fa3f2c6b1a5425297826102fbef66b`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc98c884ffd9ded4226246ffc1dc788bc14b9f3d8b94a5218e1ceed16bbce6d7`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e0e3e0c511ea6802887fbd56ff5b94184ba87b65f3aff0204a6a03216bfcd`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 4.6 MB (4599789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64520c05a6b1b103b680e92e3d2f25bb616a6259a7631625de8a88083993b59c`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d3ebffe5345bf0b168246eb753a3824b01d85c353cdb26924d418de27322eb`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be2eca8f885426e56640bb42c1d5c0ac6be94ce24c5e763bfec7322a7bcc674`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 55.6 MB (55565648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810320f66957eced0dc72d3c938fbf3af47cbccf450ad5e80400ae6c1882e5d5`  
		Last Modified: Tue, 30 Apr 2024 23:51:46 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c425b59d0ec08ecb9ea47d38f9eeaa65c33e9718ffc91608a3556dcb8fc29e6`  
		Last Modified: Tue, 30 Apr 2024 23:51:48 GMT  
		Size: 66.9 MB (66863077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7387b81cae9182cd820343599b7b7432d2d71a707e84d62edc5e57da5955ce0b`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:1428fbc99fd757d0553e1f14e47379e2bece98a3b6973932fdaddc6dd33171e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14812465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76845e51122a392850911f26ed69146a0941ca077f4801a609072e495026fb5c`

```dockerfile
```

-	Layers:
	-	`sha256:317e850b1e19b8eafa1b0ceef34783d95fbb1f3f0b5d38965767570936d3ca23`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 14.8 MB (14777374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3f37eece2d2f368cff32246af89a9f298aec0374bb9047d61d3105a5c4186af`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cf99e569402db84ac017aa56d09059f0b226f9a9c5644de24cffd4266dbda62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177224730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc9b4335a45c26b4204202c74127df42d2a28b22180e37f261c3809eb462b6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:12:16 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 16 Apr 2024 19:12:17 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae691a8c1b16066cca244ed4ea39e9b5c9af6dbf8d0347ed9ceeade76a8e750b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe011e50abc101883db1ab22a9bb6244d829c9bbe68c05b6874c0c1ed124a87`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c88c8fbaa893a4e5b948f4691a54b78782bcf57f77b47feff2c928dbce7653`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 4.3 MB (4302741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d028b2b1f150e0aeb6bfeaa5b9a244f5e9603ab59991c75aa9e0d26af02482`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc284ef09f941151cf5166e86b07fcc19f66f26f235d7dc6f20913bb6b4de338`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00367d65ff8291d336c1e5f8d314f111717488b4657e5da52543c33b829504de`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 54.6 MB (54633231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d4b7ff3dc2fade4a92765d67a8c5ce7565bcdbf4c3d2c86d58790a732d37c1`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafe7641a560f53680cd7f1572d853f011df819bac82c80b1bc568446ecd6c28`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 67.3 MB (67283710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b85ac37bb0900dbd819827cfdb8ae885be535195d33bc2dfac13b79e9c534f`  
		Last Modified: Wed, 01 May 2024 00:29:01 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:b0701fac0befd17e4cdbdbb39fa07cb5237a6b439fb49f21cda49f39be1b7523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14810777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75308f5373963ad1bd230e3d4c9bfca49ac4dddbce1af270171bba973f5685a`

```dockerfile
```

-	Layers:
	-	`sha256:416437ab84a9e25108a8a94da095cb890a8d5158e2cb5719e340d4f946a58baa`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 14.8 MB (14775654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3324096fdc8f73215f25425dee83087e5e91b5eb863938333beced58a0b0d97b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:f7a8e140a7d6d1e6e0c99eeb0489c50a186ee4ac44ff55323a176529b9a43d33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:53a71a83be1fcbb1489c0fe23d377297f55b77a6c6ce816ca8fa30225adfe2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179341247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8251f0669c6ec890f73deaaf7a7891d8f0cd80821d89b9122b950b679a331c05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:30 GMT
ADD file:c53be7373aad45b6ab1d0accc144396269617e0efcd2892e9521c25fe73fd71e in / 
# Tue, 16 Apr 2024 19:54:30 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd37f6d992035c9959b83f8f96b15cac9d66542a608f378e6e97c17830b72d80`  
		Last Modified: Tue, 16 Apr 2024 19:55:43 GMT  
		Size: 51.3 MB (51320403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafe9b2df4d05db3b7e249359d1e613682fa3f2c6b1a5425297826102fbef66b`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc98c884ffd9ded4226246ffc1dc788bc14b9f3d8b94a5218e1ceed16bbce6d7`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e0e3e0c511ea6802887fbd56ff5b94184ba87b65f3aff0204a6a03216bfcd`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 4.6 MB (4599789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64520c05a6b1b103b680e92e3d2f25bb616a6259a7631625de8a88083993b59c`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d3ebffe5345bf0b168246eb753a3824b01d85c353cdb26924d418de27322eb`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be2eca8f885426e56640bb42c1d5c0ac6be94ce24c5e763bfec7322a7bcc674`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 55.6 MB (55565648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810320f66957eced0dc72d3c938fbf3af47cbccf450ad5e80400ae6c1882e5d5`  
		Last Modified: Tue, 30 Apr 2024 23:51:46 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c425b59d0ec08ecb9ea47d38f9eeaa65c33e9718ffc91608a3556dcb8fc29e6`  
		Last Modified: Tue, 30 Apr 2024 23:51:48 GMT  
		Size: 66.9 MB (66863077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7387b81cae9182cd820343599b7b7432d2d71a707e84d62edc5e57da5955ce0b`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1428fbc99fd757d0553e1f14e47379e2bece98a3b6973932fdaddc6dd33171e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14812465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76845e51122a392850911f26ed69146a0941ca077f4801a609072e495026fb5c`

```dockerfile
```

-	Layers:
	-	`sha256:317e850b1e19b8eafa1b0ceef34783d95fbb1f3f0b5d38965767570936d3ca23`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 14.8 MB (14777374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3f37eece2d2f368cff32246af89a9f298aec0374bb9047d61d3105a5c4186af`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cf99e569402db84ac017aa56d09059f0b226f9a9c5644de24cffd4266dbda62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177224730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc9b4335a45c26b4204202c74127df42d2a28b22180e37f261c3809eb462b6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:12:16 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 16 Apr 2024 19:12:17 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae691a8c1b16066cca244ed4ea39e9b5c9af6dbf8d0347ed9ceeade76a8e750b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe011e50abc101883db1ab22a9bb6244d829c9bbe68c05b6874c0c1ed124a87`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c88c8fbaa893a4e5b948f4691a54b78782bcf57f77b47feff2c928dbce7653`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 4.3 MB (4302741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d028b2b1f150e0aeb6bfeaa5b9a244f5e9603ab59991c75aa9e0d26af02482`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc284ef09f941151cf5166e86b07fcc19f66f26f235d7dc6f20913bb6b4de338`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00367d65ff8291d336c1e5f8d314f111717488b4657e5da52543c33b829504de`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 54.6 MB (54633231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d4b7ff3dc2fade4a92765d67a8c5ce7565bcdbf4c3d2c86d58790a732d37c1`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafe7641a560f53680cd7f1572d853f011df819bac82c80b1bc568446ecd6c28`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 67.3 MB (67283710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b85ac37bb0900dbd819827cfdb8ae885be535195d33bc2dfac13b79e9c534f`  
		Last Modified: Wed, 01 May 2024 00:29:01 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b0701fac0befd17e4cdbdbb39fa07cb5237a6b439fb49f21cda49f39be1b7523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14810777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75308f5373963ad1bd230e3d4c9bfca49ac4dddbce1af270171bba973f5685a`

```dockerfile
```

-	Layers:
	-	`sha256:416437ab84a9e25108a8a94da095cb890a8d5158e2cb5719e340d4f946a58baa`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 14.8 MB (14775654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3324096fdc8f73215f25425dee83087e5e91b5eb863938333beced58a0b0d97b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

**does not exist** (yet?)

## `mysql:8.4.0`

```console
$ docker pull mysql@sha256:f7a8e140a7d6d1e6e0c99eeb0489c50a186ee4ac44ff55323a176529b9a43d33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.0` - linux; amd64

```console
$ docker pull mysql@sha256:53a71a83be1fcbb1489c0fe23d377297f55b77a6c6ce816ca8fa30225adfe2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179341247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8251f0669c6ec890f73deaaf7a7891d8f0cd80821d89b9122b950b679a331c05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:30 GMT
ADD file:c53be7373aad45b6ab1d0accc144396269617e0efcd2892e9521c25fe73fd71e in / 
# Tue, 16 Apr 2024 19:54:30 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd37f6d992035c9959b83f8f96b15cac9d66542a608f378e6e97c17830b72d80`  
		Last Modified: Tue, 16 Apr 2024 19:55:43 GMT  
		Size: 51.3 MB (51320403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafe9b2df4d05db3b7e249359d1e613682fa3f2c6b1a5425297826102fbef66b`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc98c884ffd9ded4226246ffc1dc788bc14b9f3d8b94a5218e1ceed16bbce6d7`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e0e3e0c511ea6802887fbd56ff5b94184ba87b65f3aff0204a6a03216bfcd`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 4.6 MB (4599789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64520c05a6b1b103b680e92e3d2f25bb616a6259a7631625de8a88083993b59c`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d3ebffe5345bf0b168246eb753a3824b01d85c353cdb26924d418de27322eb`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be2eca8f885426e56640bb42c1d5c0ac6be94ce24c5e763bfec7322a7bcc674`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 55.6 MB (55565648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810320f66957eced0dc72d3c938fbf3af47cbccf450ad5e80400ae6c1882e5d5`  
		Last Modified: Tue, 30 Apr 2024 23:51:46 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c425b59d0ec08ecb9ea47d38f9eeaa65c33e9718ffc91608a3556dcb8fc29e6`  
		Last Modified: Tue, 30 Apr 2024 23:51:48 GMT  
		Size: 66.9 MB (66863077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7387b81cae9182cd820343599b7b7432d2d71a707e84d62edc5e57da5955ce0b`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0` - unknown; unknown

```console
$ docker pull mysql@sha256:1428fbc99fd757d0553e1f14e47379e2bece98a3b6973932fdaddc6dd33171e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14812465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76845e51122a392850911f26ed69146a0941ca077f4801a609072e495026fb5c`

```dockerfile
```

-	Layers:
	-	`sha256:317e850b1e19b8eafa1b0ceef34783d95fbb1f3f0b5d38965767570936d3ca23`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 14.8 MB (14777374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3f37eece2d2f368cff32246af89a9f298aec0374bb9047d61d3105a5c4186af`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cf99e569402db84ac017aa56d09059f0b226f9a9c5644de24cffd4266dbda62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177224730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc9b4335a45c26b4204202c74127df42d2a28b22180e37f261c3809eb462b6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:12:16 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 16 Apr 2024 19:12:17 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae691a8c1b16066cca244ed4ea39e9b5c9af6dbf8d0347ed9ceeade76a8e750b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe011e50abc101883db1ab22a9bb6244d829c9bbe68c05b6874c0c1ed124a87`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c88c8fbaa893a4e5b948f4691a54b78782bcf57f77b47feff2c928dbce7653`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 4.3 MB (4302741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d028b2b1f150e0aeb6bfeaa5b9a244f5e9603ab59991c75aa9e0d26af02482`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc284ef09f941151cf5166e86b07fcc19f66f26f235d7dc6f20913bb6b4de338`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00367d65ff8291d336c1e5f8d314f111717488b4657e5da52543c33b829504de`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 54.6 MB (54633231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d4b7ff3dc2fade4a92765d67a8c5ce7565bcdbf4c3d2c86d58790a732d37c1`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafe7641a560f53680cd7f1572d853f011df819bac82c80b1bc568446ecd6c28`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 67.3 MB (67283710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b85ac37bb0900dbd819827cfdb8ae885be535195d33bc2dfac13b79e9c534f`  
		Last Modified: Wed, 01 May 2024 00:29:01 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0` - unknown; unknown

```console
$ docker pull mysql@sha256:b0701fac0befd17e4cdbdbb39fa07cb5237a6b439fb49f21cda49f39be1b7523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14810777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75308f5373963ad1bd230e3d4c9bfca49ac4dddbce1af270171bba973f5685a`

```dockerfile
```

-	Layers:
	-	`sha256:416437ab84a9e25108a8a94da095cb890a8d5158e2cb5719e340d4f946a58baa`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 14.8 MB (14775654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3324096fdc8f73215f25425dee83087e5e91b5eb863938333beced58a0b0d97b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.0-oracle`

```console
$ docker pull mysql@sha256:f7a8e140a7d6d1e6e0c99eeb0489c50a186ee4ac44ff55323a176529b9a43d33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:53a71a83be1fcbb1489c0fe23d377297f55b77a6c6ce816ca8fa30225adfe2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179341247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8251f0669c6ec890f73deaaf7a7891d8f0cd80821d89b9122b950b679a331c05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:30 GMT
ADD file:c53be7373aad45b6ab1d0accc144396269617e0efcd2892e9521c25fe73fd71e in / 
# Tue, 16 Apr 2024 19:54:30 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd37f6d992035c9959b83f8f96b15cac9d66542a608f378e6e97c17830b72d80`  
		Last Modified: Tue, 16 Apr 2024 19:55:43 GMT  
		Size: 51.3 MB (51320403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafe9b2df4d05db3b7e249359d1e613682fa3f2c6b1a5425297826102fbef66b`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc98c884ffd9ded4226246ffc1dc788bc14b9f3d8b94a5218e1ceed16bbce6d7`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e0e3e0c511ea6802887fbd56ff5b94184ba87b65f3aff0204a6a03216bfcd`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 4.6 MB (4599789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64520c05a6b1b103b680e92e3d2f25bb616a6259a7631625de8a88083993b59c`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d3ebffe5345bf0b168246eb753a3824b01d85c353cdb26924d418de27322eb`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be2eca8f885426e56640bb42c1d5c0ac6be94ce24c5e763bfec7322a7bcc674`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 55.6 MB (55565648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810320f66957eced0dc72d3c938fbf3af47cbccf450ad5e80400ae6c1882e5d5`  
		Last Modified: Tue, 30 Apr 2024 23:51:46 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c425b59d0ec08ecb9ea47d38f9eeaa65c33e9718ffc91608a3556dcb8fc29e6`  
		Last Modified: Tue, 30 Apr 2024 23:51:48 GMT  
		Size: 66.9 MB (66863077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7387b81cae9182cd820343599b7b7432d2d71a707e84d62edc5e57da5955ce0b`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1428fbc99fd757d0553e1f14e47379e2bece98a3b6973932fdaddc6dd33171e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14812465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76845e51122a392850911f26ed69146a0941ca077f4801a609072e495026fb5c`

```dockerfile
```

-	Layers:
	-	`sha256:317e850b1e19b8eafa1b0ceef34783d95fbb1f3f0b5d38965767570936d3ca23`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 14.8 MB (14777374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3f37eece2d2f368cff32246af89a9f298aec0374bb9047d61d3105a5c4186af`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cf99e569402db84ac017aa56d09059f0b226f9a9c5644de24cffd4266dbda62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177224730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc9b4335a45c26b4204202c74127df42d2a28b22180e37f261c3809eb462b6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:12:16 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 16 Apr 2024 19:12:17 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae691a8c1b16066cca244ed4ea39e9b5c9af6dbf8d0347ed9ceeade76a8e750b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe011e50abc101883db1ab22a9bb6244d829c9bbe68c05b6874c0c1ed124a87`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c88c8fbaa893a4e5b948f4691a54b78782bcf57f77b47feff2c928dbce7653`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 4.3 MB (4302741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d028b2b1f150e0aeb6bfeaa5b9a244f5e9603ab59991c75aa9e0d26af02482`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc284ef09f941151cf5166e86b07fcc19f66f26f235d7dc6f20913bb6b4de338`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00367d65ff8291d336c1e5f8d314f111717488b4657e5da52543c33b829504de`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 54.6 MB (54633231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d4b7ff3dc2fade4a92765d67a8c5ce7565bcdbf4c3d2c86d58790a732d37c1`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafe7641a560f53680cd7f1572d853f011df819bac82c80b1bc568446ecd6c28`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 67.3 MB (67283710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b85ac37bb0900dbd819827cfdb8ae885be535195d33bc2dfac13b79e9c534f`  
		Last Modified: Wed, 01 May 2024 00:29:01 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b0701fac0befd17e4cdbdbb39fa07cb5237a6b439fb49f21cda49f39be1b7523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14810777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75308f5373963ad1bd230e3d4c9bfca49ac4dddbce1af270171bba973f5685a`

```dockerfile
```

-	Layers:
	-	`sha256:416437ab84a9e25108a8a94da095cb890a8d5158e2cb5719e340d4f946a58baa`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 14.8 MB (14775654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3324096fdc8f73215f25425dee83087e5e91b5eb863938333beced58a0b0d97b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.0-oraclelinux9`

**does not exist** (yet?)

## `mysql:latest`

```console
$ docker pull mysql@sha256:f7a8e140a7d6d1e6e0c99eeb0489c50a186ee4ac44ff55323a176529b9a43d33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:53a71a83be1fcbb1489c0fe23d377297f55b77a6c6ce816ca8fa30225adfe2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179341247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8251f0669c6ec890f73deaaf7a7891d8f0cd80821d89b9122b950b679a331c05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:30 GMT
ADD file:c53be7373aad45b6ab1d0accc144396269617e0efcd2892e9521c25fe73fd71e in / 
# Tue, 16 Apr 2024 19:54:30 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd37f6d992035c9959b83f8f96b15cac9d66542a608f378e6e97c17830b72d80`  
		Last Modified: Tue, 16 Apr 2024 19:55:43 GMT  
		Size: 51.3 MB (51320403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafe9b2df4d05db3b7e249359d1e613682fa3f2c6b1a5425297826102fbef66b`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc98c884ffd9ded4226246ffc1dc788bc14b9f3d8b94a5218e1ceed16bbce6d7`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e0e3e0c511ea6802887fbd56ff5b94184ba87b65f3aff0204a6a03216bfcd`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 4.6 MB (4599789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64520c05a6b1b103b680e92e3d2f25bb616a6259a7631625de8a88083993b59c`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d3ebffe5345bf0b168246eb753a3824b01d85c353cdb26924d418de27322eb`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be2eca8f885426e56640bb42c1d5c0ac6be94ce24c5e763bfec7322a7bcc674`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 55.6 MB (55565648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810320f66957eced0dc72d3c938fbf3af47cbccf450ad5e80400ae6c1882e5d5`  
		Last Modified: Tue, 30 Apr 2024 23:51:46 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c425b59d0ec08ecb9ea47d38f9eeaa65c33e9718ffc91608a3556dcb8fc29e6`  
		Last Modified: Tue, 30 Apr 2024 23:51:48 GMT  
		Size: 66.9 MB (66863077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7387b81cae9182cd820343599b7b7432d2d71a707e84d62edc5e57da5955ce0b`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:1428fbc99fd757d0553e1f14e47379e2bece98a3b6973932fdaddc6dd33171e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14812465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76845e51122a392850911f26ed69146a0941ca077f4801a609072e495026fb5c`

```dockerfile
```

-	Layers:
	-	`sha256:317e850b1e19b8eafa1b0ceef34783d95fbb1f3f0b5d38965767570936d3ca23`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 14.8 MB (14777374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3f37eece2d2f368cff32246af89a9f298aec0374bb9047d61d3105a5c4186af`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cf99e569402db84ac017aa56d09059f0b226f9a9c5644de24cffd4266dbda62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177224730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc9b4335a45c26b4204202c74127df42d2a28b22180e37f261c3809eb462b6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:12:16 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 16 Apr 2024 19:12:17 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae691a8c1b16066cca244ed4ea39e9b5c9af6dbf8d0347ed9ceeade76a8e750b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe011e50abc101883db1ab22a9bb6244d829c9bbe68c05b6874c0c1ed124a87`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c88c8fbaa893a4e5b948f4691a54b78782bcf57f77b47feff2c928dbce7653`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 4.3 MB (4302741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d028b2b1f150e0aeb6bfeaa5b9a244f5e9603ab59991c75aa9e0d26af02482`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc284ef09f941151cf5166e86b07fcc19f66f26f235d7dc6f20913bb6b4de338`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00367d65ff8291d336c1e5f8d314f111717488b4657e5da52543c33b829504de`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 54.6 MB (54633231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d4b7ff3dc2fade4a92765d67a8c5ce7565bcdbf4c3d2c86d58790a732d37c1`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafe7641a560f53680cd7f1572d853f011df819bac82c80b1bc568446ecd6c28`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 67.3 MB (67283710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b85ac37bb0900dbd819827cfdb8ae885be535195d33bc2dfac13b79e9c534f`  
		Last Modified: Wed, 01 May 2024 00:29:01 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:b0701fac0befd17e4cdbdbb39fa07cb5237a6b439fb49f21cda49f39be1b7523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14810777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75308f5373963ad1bd230e3d4c9bfca49ac4dddbce1af270171bba973f5685a`

```dockerfile
```

-	Layers:
	-	`sha256:416437ab84a9e25108a8a94da095cb890a8d5158e2cb5719e340d4f946a58baa`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 14.8 MB (14775654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3324096fdc8f73215f25425dee83087e5e91b5eb863938333beced58a0b0d97b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:f7a8e140a7d6d1e6e0c99eeb0489c50a186ee4ac44ff55323a176529b9a43d33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:53a71a83be1fcbb1489c0fe23d377297f55b77a6c6ce816ca8fa30225adfe2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179341247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8251f0669c6ec890f73deaaf7a7891d8f0cd80821d89b9122b950b679a331c05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:30 GMT
ADD file:c53be7373aad45b6ab1d0accc144396269617e0efcd2892e9521c25fe73fd71e in / 
# Tue, 16 Apr 2024 19:54:30 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd37f6d992035c9959b83f8f96b15cac9d66542a608f378e6e97c17830b72d80`  
		Last Modified: Tue, 16 Apr 2024 19:55:43 GMT  
		Size: 51.3 MB (51320403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafe9b2df4d05db3b7e249359d1e613682fa3f2c6b1a5425297826102fbef66b`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc98c884ffd9ded4226246ffc1dc788bc14b9f3d8b94a5218e1ceed16bbce6d7`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e0e3e0c511ea6802887fbd56ff5b94184ba87b65f3aff0204a6a03216bfcd`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 4.6 MB (4599789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64520c05a6b1b103b680e92e3d2f25bb616a6259a7631625de8a88083993b59c`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d3ebffe5345bf0b168246eb753a3824b01d85c353cdb26924d418de27322eb`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be2eca8f885426e56640bb42c1d5c0ac6be94ce24c5e763bfec7322a7bcc674`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 55.6 MB (55565648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810320f66957eced0dc72d3c938fbf3af47cbccf450ad5e80400ae6c1882e5d5`  
		Last Modified: Tue, 30 Apr 2024 23:51:46 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c425b59d0ec08ecb9ea47d38f9eeaa65c33e9718ffc91608a3556dcb8fc29e6`  
		Last Modified: Tue, 30 Apr 2024 23:51:48 GMT  
		Size: 66.9 MB (66863077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7387b81cae9182cd820343599b7b7432d2d71a707e84d62edc5e57da5955ce0b`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:1428fbc99fd757d0553e1f14e47379e2bece98a3b6973932fdaddc6dd33171e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14812465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76845e51122a392850911f26ed69146a0941ca077f4801a609072e495026fb5c`

```dockerfile
```

-	Layers:
	-	`sha256:317e850b1e19b8eafa1b0ceef34783d95fbb1f3f0b5d38965767570936d3ca23`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 14.8 MB (14777374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3f37eece2d2f368cff32246af89a9f298aec0374bb9047d61d3105a5c4186af`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cf99e569402db84ac017aa56d09059f0b226f9a9c5644de24cffd4266dbda62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177224730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc9b4335a45c26b4204202c74127df42d2a28b22180e37f261c3809eb462b6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:12:16 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 16 Apr 2024 19:12:17 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae691a8c1b16066cca244ed4ea39e9b5c9af6dbf8d0347ed9ceeade76a8e750b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe011e50abc101883db1ab22a9bb6244d829c9bbe68c05b6874c0c1ed124a87`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c88c8fbaa893a4e5b948f4691a54b78782bcf57f77b47feff2c928dbce7653`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 4.3 MB (4302741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d028b2b1f150e0aeb6bfeaa5b9a244f5e9603ab59991c75aa9e0d26af02482`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc284ef09f941151cf5166e86b07fcc19f66f26f235d7dc6f20913bb6b4de338`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00367d65ff8291d336c1e5f8d314f111717488b4657e5da52543c33b829504de`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 54.6 MB (54633231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d4b7ff3dc2fade4a92765d67a8c5ce7565bcdbf4c3d2c86d58790a732d37c1`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafe7641a560f53680cd7f1572d853f011df819bac82c80b1bc568446ecd6c28`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 67.3 MB (67283710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b85ac37bb0900dbd819827cfdb8ae885be535195d33bc2dfac13b79e9c534f`  
		Last Modified: Wed, 01 May 2024 00:29:01 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:b0701fac0befd17e4cdbdbb39fa07cb5237a6b439fb49f21cda49f39be1b7523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14810777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75308f5373963ad1bd230e3d4c9bfca49ac4dddbce1af270171bba973f5685a`

```dockerfile
```

-	Layers:
	-	`sha256:416437ab84a9e25108a8a94da095cb890a8d5158e2cb5719e340d4f946a58baa`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 14.8 MB (14775654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3324096fdc8f73215f25425dee83087e5e91b5eb863938333beced58a0b0d97b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:f7a8e140a7d6d1e6e0c99eeb0489c50a186ee4ac44ff55323a176529b9a43d33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:53a71a83be1fcbb1489c0fe23d377297f55b77a6c6ce816ca8fa30225adfe2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179341247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8251f0669c6ec890f73deaaf7a7891d8f0cd80821d89b9122b950b679a331c05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:30 GMT
ADD file:c53be7373aad45b6ab1d0accc144396269617e0efcd2892e9521c25fe73fd71e in / 
# Tue, 16 Apr 2024 19:54:30 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd37f6d992035c9959b83f8f96b15cac9d66542a608f378e6e97c17830b72d80`  
		Last Modified: Tue, 16 Apr 2024 19:55:43 GMT  
		Size: 51.3 MB (51320403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafe9b2df4d05db3b7e249359d1e613682fa3f2c6b1a5425297826102fbef66b`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc98c884ffd9ded4226246ffc1dc788bc14b9f3d8b94a5218e1ceed16bbce6d7`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e0e3e0c511ea6802887fbd56ff5b94184ba87b65f3aff0204a6a03216bfcd`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 4.6 MB (4599789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64520c05a6b1b103b680e92e3d2f25bb616a6259a7631625de8a88083993b59c`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d3ebffe5345bf0b168246eb753a3824b01d85c353cdb26924d418de27322eb`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be2eca8f885426e56640bb42c1d5c0ac6be94ce24c5e763bfec7322a7bcc674`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 55.6 MB (55565648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810320f66957eced0dc72d3c938fbf3af47cbccf450ad5e80400ae6c1882e5d5`  
		Last Modified: Tue, 30 Apr 2024 23:51:46 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c425b59d0ec08ecb9ea47d38f9eeaa65c33e9718ffc91608a3556dcb8fc29e6`  
		Last Modified: Tue, 30 Apr 2024 23:51:48 GMT  
		Size: 66.9 MB (66863077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7387b81cae9182cd820343599b7b7432d2d71a707e84d62edc5e57da5955ce0b`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1428fbc99fd757d0553e1f14e47379e2bece98a3b6973932fdaddc6dd33171e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14812465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76845e51122a392850911f26ed69146a0941ca077f4801a609072e495026fb5c`

```dockerfile
```

-	Layers:
	-	`sha256:317e850b1e19b8eafa1b0ceef34783d95fbb1f3f0b5d38965767570936d3ca23`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 14.8 MB (14777374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3f37eece2d2f368cff32246af89a9f298aec0374bb9047d61d3105a5c4186af`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cf99e569402db84ac017aa56d09059f0b226f9a9c5644de24cffd4266dbda62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177224730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc9b4335a45c26b4204202c74127df42d2a28b22180e37f261c3809eb462b6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:12:16 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 16 Apr 2024 19:12:17 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae691a8c1b16066cca244ed4ea39e9b5c9af6dbf8d0347ed9ceeade76a8e750b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe011e50abc101883db1ab22a9bb6244d829c9bbe68c05b6874c0c1ed124a87`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c88c8fbaa893a4e5b948f4691a54b78782bcf57f77b47feff2c928dbce7653`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 4.3 MB (4302741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d028b2b1f150e0aeb6bfeaa5b9a244f5e9603ab59991c75aa9e0d26af02482`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc284ef09f941151cf5166e86b07fcc19f66f26f235d7dc6f20913bb6b4de338`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00367d65ff8291d336c1e5f8d314f111717488b4657e5da52543c33b829504de`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 54.6 MB (54633231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d4b7ff3dc2fade4a92765d67a8c5ce7565bcdbf4c3d2c86d58790a732d37c1`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafe7641a560f53680cd7f1572d853f011df819bac82c80b1bc568446ecd6c28`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 67.3 MB (67283710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b85ac37bb0900dbd819827cfdb8ae885be535195d33bc2dfac13b79e9c534f`  
		Last Modified: Wed, 01 May 2024 00:29:01 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b0701fac0befd17e4cdbdbb39fa07cb5237a6b439fb49f21cda49f39be1b7523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14810777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75308f5373963ad1bd230e3d4c9bfca49ac4dddbce1af270171bba973f5685a`

```dockerfile
```

-	Layers:
	-	`sha256:416437ab84a9e25108a8a94da095cb890a8d5158e2cb5719e340d4f946a58baa`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 14.8 MB (14775654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3324096fdc8f73215f25425dee83087e5e91b5eb863938333beced58a0b0d97b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

**does not exist** (yet?)

## `mysql:oracle`

```console
$ docker pull mysql@sha256:f7a8e140a7d6d1e6e0c99eeb0489c50a186ee4ac44ff55323a176529b9a43d33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:53a71a83be1fcbb1489c0fe23d377297f55b77a6c6ce816ca8fa30225adfe2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179341247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8251f0669c6ec890f73deaaf7a7891d8f0cd80821d89b9122b950b679a331c05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:30 GMT
ADD file:c53be7373aad45b6ab1d0accc144396269617e0efcd2892e9521c25fe73fd71e in / 
# Tue, 16 Apr 2024 19:54:30 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd37f6d992035c9959b83f8f96b15cac9d66542a608f378e6e97c17830b72d80`  
		Last Modified: Tue, 16 Apr 2024 19:55:43 GMT  
		Size: 51.3 MB (51320403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafe9b2df4d05db3b7e249359d1e613682fa3f2c6b1a5425297826102fbef66b`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc98c884ffd9ded4226246ffc1dc788bc14b9f3d8b94a5218e1ceed16bbce6d7`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e0e3e0c511ea6802887fbd56ff5b94184ba87b65f3aff0204a6a03216bfcd`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 4.6 MB (4599789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64520c05a6b1b103b680e92e3d2f25bb616a6259a7631625de8a88083993b59c`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d3ebffe5345bf0b168246eb753a3824b01d85c353cdb26924d418de27322eb`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be2eca8f885426e56640bb42c1d5c0ac6be94ce24c5e763bfec7322a7bcc674`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 55.6 MB (55565648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810320f66957eced0dc72d3c938fbf3af47cbccf450ad5e80400ae6c1882e5d5`  
		Last Modified: Tue, 30 Apr 2024 23:51:46 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c425b59d0ec08ecb9ea47d38f9eeaa65c33e9718ffc91608a3556dcb8fc29e6`  
		Last Modified: Tue, 30 Apr 2024 23:51:48 GMT  
		Size: 66.9 MB (66863077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7387b81cae9182cd820343599b7b7432d2d71a707e84d62edc5e57da5955ce0b`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1428fbc99fd757d0553e1f14e47379e2bece98a3b6973932fdaddc6dd33171e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14812465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76845e51122a392850911f26ed69146a0941ca077f4801a609072e495026fb5c`

```dockerfile
```

-	Layers:
	-	`sha256:317e850b1e19b8eafa1b0ceef34783d95fbb1f3f0b5d38965767570936d3ca23`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 14.8 MB (14777374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3f37eece2d2f368cff32246af89a9f298aec0374bb9047d61d3105a5c4186af`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cf99e569402db84ac017aa56d09059f0b226f9a9c5644de24cffd4266dbda62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177224730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc9b4335a45c26b4204202c74127df42d2a28b22180e37f261c3809eb462b6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:12:16 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 16 Apr 2024 19:12:17 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae691a8c1b16066cca244ed4ea39e9b5c9af6dbf8d0347ed9ceeade76a8e750b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe011e50abc101883db1ab22a9bb6244d829c9bbe68c05b6874c0c1ed124a87`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c88c8fbaa893a4e5b948f4691a54b78782bcf57f77b47feff2c928dbce7653`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 4.3 MB (4302741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d028b2b1f150e0aeb6bfeaa5b9a244f5e9603ab59991c75aa9e0d26af02482`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc284ef09f941151cf5166e86b07fcc19f66f26f235d7dc6f20913bb6b4de338`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00367d65ff8291d336c1e5f8d314f111717488b4657e5da52543c33b829504de`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 54.6 MB (54633231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d4b7ff3dc2fade4a92765d67a8c5ce7565bcdbf4c3d2c86d58790a732d37c1`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafe7641a560f53680cd7f1572d853f011df819bac82c80b1bc568446ecd6c28`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 67.3 MB (67283710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b85ac37bb0900dbd819827cfdb8ae885be535195d33bc2dfac13b79e9c534f`  
		Last Modified: Wed, 01 May 2024 00:29:01 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b0701fac0befd17e4cdbdbb39fa07cb5237a6b439fb49f21cda49f39be1b7523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14810777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75308f5373963ad1bd230e3d4c9bfca49ac4dddbce1af270171bba973f5685a`

```dockerfile
```

-	Layers:
	-	`sha256:416437ab84a9e25108a8a94da095cb890a8d5158e2cb5719e340d4f946a58baa`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 14.8 MB (14775654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3324096fdc8f73215f25425dee83087e5e91b5eb863938333beced58a0b0d97b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

**does not exist** (yet?)
