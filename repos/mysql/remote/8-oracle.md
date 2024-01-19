## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:c36dddae6248de8b0b430feb6c1d9cf1df4f486228aa8cfc515bdc4387746cf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6d5a11994be8ca5e4cfaf4d370219f6eb6ef8fb41d57f9ed1568a93ffd5471ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183362882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b21e040954f63d922725c2d049cf2a0dfbad5522e8d3e14c36f1823ab3f5e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb5a921059e3898005818f7f80347bafc9800da5d427517f0713d2db0d167a0`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85878fb9bb201455b25020f87c8a00ecd14a7ff7e95f5eac360609b47c40e34`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16f3fd26a8227c3566f7b9f27ec3ad511b3f28551ea9bc1a2decd885136709f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 4.6 MB (4590753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51b5329cbeda564171e38873f6afa0ed11eecc5be923170862f1be7dcff0f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374d2f7f3267229ec55c2bd4fc4ce43ab0e34aeb60c297c7e83da433cc260cc0`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1bb2c95740adb15e9e07fe75f7788e4f767c4048041b448b55fedd60d05cf`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.1 MB (63086154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c905405360553567280bcac35bbf3b613048ee32a9e8c43ef1f3690c8609de7`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79cd2da03be475c108253eb3d1f98e7567fde5455fe95af2d645cb2cfb99949`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.4 MB (63372101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1aa788d17b88e63b294e49ca7166003652f4df88db20739aa2a4847d32f9f`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d5e3a0efc9f1128ba5339dab74a16a3007b18a313556bd8e84274b3eb535964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d72ddd7e2fc867360cb0fc75731100509343832040c1772c6e9ea0c37b22f53`

```dockerfile
```

-	Layers:
	-	`sha256:f7a868c5536bc5b2a94aaad3135e4987c970721c5b00d2c683ab274e1c2c2c44`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 12.1 MB (12130335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1818f978b3af2b1b5f94ac03b4b6ea40fb7368e22dc876cc3d201c8031983ae3`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d4c783e85ef8647a4350cb7aa7a8ddc7ebfd7cb217de4c2d1643e212ba94fcbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185271864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76e521c029290a5e42acd182b67a66b8bf1c42045e4a6977ee21e46a5fe6083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 18 Dec 2023 23:06:09 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["/bin/bash"]
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV GOSU_VERSION=1.16
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Mon, 18 Dec 2023 23:06:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Dec 2023 23:06:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 23:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 23:06:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 18 Dec 2023 23:06:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bc09224ded2ba51f48c57c09a54abbae3a2d2fe77f98359b0f65b2b1949af1`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f841abaf84e70ea9adf8e87060661de9a640af2d078692da78e0f022957710`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9dd3d51c4258676b6273ca6eb441d416a5de0efd3c1816052c63eed92dea23`  
		Last Modified: Thu, 18 Jan 2024 10:39:22 GMT  
		Size: 61.6 MB (61601668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ba15636f68c911fd80cfe93399a28984e75f3ccc50cda32f28601aad810793`  
		Last Modified: Thu, 18 Jan 2024 10:39:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699bfb592109d89d03cb6ba239703eae068660a5e890dd9183f39c5ea98ec301`  
		Last Modified: Thu, 18 Jan 2024 10:39:23 GMT  
		Size: 68.4 MB (68364295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadd8706fc96f08ea21fa0043a0efd5d6c914c5f544b2a043b5962b78f8d9146`  
		Last Modified: Thu, 18 Jan 2024 10:39:21 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:8e1d247b0af44d8a6b915673bfa2a5b70a250b01b5b500432877ad7afb20c3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11606658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d851d89e0a70e75de4023803faa9ffaead0d3db93625a47df941d02617a30080`

```dockerfile
```

-	Layers:
	-	`sha256:1f51356b804bf1effb4156dff7fcff3e2a9b1ca4f09ea75ac201b1d0eab221bd`  
		Last Modified: Thu, 18 Jan 2024 10:39:20 GMT  
		Size: 11.6 MB (11571720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15071d7f0bb6d7f8b4a76426a2c72b510453e6de5348a46df979c21f8b7d18e5`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 34.9 KB (34938 bytes)  
		MIME: application/vnd.in-toto+json
