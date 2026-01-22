## `mysql:lts`

```console
$ docker pull mysql@sha256:cf6d1c8f2d31c73c878c6f5f60c2bec46701c41d5baf99100888bef5b6578b86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:cee2bcd7cfece021d2e13229e660e2072ed50c9dd4635d2797c8954154ed1739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233230172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3890a37ddb73dd2c66d963f1b2c0fe051ccd580564526e85ea0073d08e926369`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:48:19 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:48:19 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:48:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:49:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:49:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c9c940ed3326dbe75491b5c125f4e77409c20f1607b63e8d19a3c80b842f3e`  
		Last Modified: Thu, 22 Jan 2026 01:02:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcefadb1e23c809499894384898688261866d60eba933b77725f25e26c3e97ac`  
		Last Modified: Wed, 21 Jan 2026 22:49:49 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3751cab74b958e7f2a28d97747761761c9ca8dcb19db045bf8715e1c88b02a77`  
		Last Modified: Wed, 21 Jan 2026 22:49:49 GMT  
		Size: 6.2 MB (6175161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c365df7c813339968023fded5e9042d098bb834a37079c11cfe99c16056e452`  
		Last Modified: Wed, 21 Jan 2026 23:47:14 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d59e782af07065a94adad658374505a377347a587b0ea862c9caabfcd1215a`  
		Last Modified: Wed, 21 Jan 2026 22:49:50 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06c9b222c64ef602389ece95bb72bac5893dd58b6edb5345235ecefa8616907`  
		Last Modified: Wed, 21 Jan 2026 22:50:06 GMT  
		Size: 47.8 MB (47811670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba7f8d3ecf830b612dd6ec5f2c8203c6a17f663a77102f0ffb793c1a1d589be`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c069718c101f0277bc8229dd2590bcb63d96f97ac9813addffd1b74d0d370f`  
		Last Modified: Wed, 21 Jan 2026 22:49:53 GMT  
		Size: 131.1 MB (131135770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c156dd23b850679b32b7f01f7d6fdc723966e165960e36800e3bd87e4740de17`  
		Last Modified: Wed, 21 Jan 2026 22:49:51 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:be16c973ece26bb060d837d03f50d148f5ba91ac5626368218b8e3a845047488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82df3286018a1d6cd6af61b31d53c2001d7503a9d7019268bee01205d261d23`

```dockerfile
```

-	Layers:
	-	`sha256:3339e5486c0c4cc6a3b8d51d1b3345afe45209ee3e2c44b15834ea10ba988fde`  
		Last Modified: Thu, 22 Jan 2026 01:02:23 GMT  
		Size: 15.2 MB (15234290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9377b2f281254f96efd66320022665c8cd5568ad522938d3fe3898e62ae20660`  
		Last Modified: Thu, 22 Jan 2026 01:02:24 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:509287abcaa38a3d334cf61bd787d0d523504c684990042f62fa4bfbadd1cb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228698723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fc1f3b0c1ad069b3e2a75bbd8036e5104f668132ef18ef6d542d86b85e2b06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:53:20 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 21 Jan 2026 22:53:21 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:53:21 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:50 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 21 Jan 2026 22:54:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:54:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:54:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:54:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:29:32 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da72dcb236c1597383af262a9f45c86ca2b4b75d909507a3ac5b0eb6d7bd801`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9d33c81d6768ce0368969dfaf925fbf6624bdf9202a7fe6d15e54b846c0e13`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7699a954d9de859b4b92ab5459f58e582e3085a82e29fa85c372c885cbd75f06`  
		Last Modified: Wed, 21 Jan 2026 22:55:12 GMT  
		Size: 5.8 MB (5798064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccbceaa8cf24fa2833a2afe398ccde1f6ff2bbee670abd536c014c84fdcf94d`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f6521db4dbfdbb841dcd5d6d34f10bf9c3741fa4a8d009fbbd9703846ab0e1`  
		Last Modified: Wed, 21 Jan 2026 22:54:59 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b36f2667d57cda43bb84edc3e089860e2f0d619fe5cc7a4ca134f30df64ee`  
		Last Modified: Wed, 21 Jan 2026 22:55:00 GMT  
		Size: 46.7 MB (46699165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c61b1843fc9549819d2149bd4ff4fc0c9ec59f7a7f62116469dfe294bbfae2`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d81e4d2c7b063ca6af6c142014724fd25f4b78bd37fbbbccf582016aa124db`  
		Last Modified: Wed, 21 Jan 2026 22:55:03 GMT  
		Size: 129.6 MB (129552583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2eea1ca45c6c742395a1c8b5d7327e0a8ffb8246a250cd5211862ed87b5662c`  
		Last Modified: Wed, 21 Jan 2026 22:55:08 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:7fdb2d55797d9e264ef6ff6971dce8f068ad60acf77c245b9e2d7bf79c5d2e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ab615fb5da4e8f4d9be289b02378388973342472e21c5a103210f09f2a0e75`

```dockerfile
```

-	Layers:
	-	`sha256:7cb8424279707d32f1f981f563752532ae08ba2091882802e59162d842af3f95`  
		Last Modified: Wed, 21 Jan 2026 22:54:58 GMT  
		Size: 15.2 MB (15232710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3794e62c5aa6c87d503274951dc859252ccf0086cad9ebf25ffaf00b2d9fe472`  
		Last Modified: Thu, 22 Jan 2026 01:02:36 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json
