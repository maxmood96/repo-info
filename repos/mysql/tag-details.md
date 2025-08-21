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
-	[`mysql:8.0.43`](#mysql8043)
-	[`mysql:8.0.43-bookworm`](#mysql8043-bookworm)
-	[`mysql:8.0.43-debian`](#mysql8043-debian)
-	[`mysql:8.0.43-oracle`](#mysql8043-oracle)
-	[`mysql:8.0.43-oraclelinux9`](#mysql8043-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.6`](#mysql846)
-	[`mysql:8.4.6-oracle`](#mysql846-oracle)
-	[`mysql:8.4.6-oraclelinux9`](#mysql846-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.4`](#mysql94)
-	[`mysql:9.4-oracle`](#mysql94-oracle)
-	[`mysql:9.4-oraclelinux9`](#mysql94-oraclelinux9)
-	[`mysql:9.4.0`](#mysql940)
-	[`mysql:9.4.0-oracle`](#mysql940-oracle)
-	[`mysql:9.4.0-oraclelinux9`](#mysql940-oraclelinux9)
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
$ docker pull mysql@sha256:432966f3bdcbf834ef578226e4c196fab460f0727daa888b039854b5c185e8b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:5144a476c89ccd10123ed8a67754cecf50a3c3d32e7ec2e5b5e48c588e07c7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (237016226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f1b9da918eec3e2bd327cc44936b97a15d8705396efe23dfa4198656330dbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd66ec68b64f7f87b2a021e220dc67f8b4e1b902e33a79a92f58410f071efff6`  
		Last Modified: Thu, 21 Aug 2025 19:10:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df938959d2c414e200f0b9c573a1aee4c04e117929223e23508d8107ce1f92f0`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 983.0 KB (983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9348ee598b89aee26c72bb0ad652e10cc5e914f36d503492f0f5ab0252992b5`  
		Last Modified: Thu, 21 Aug 2025 19:10:09 GMT  
		Size: 6.8 MB (6818646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ff5eaaa3b2925ba1855ca2372101208fad8d49d7b82c630c5a5f9cbee5e1f`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d504a2807609c4e00c08619d2328929116183206e0cbefe142587a3db106c473`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbc662f10805e2e50d549d3af79d72079ab6f0c4e455a2692dd582d7c49dbe0`  
		Last Modified: Thu, 21 Aug 2025 19:10:12 GMT  
		Size: 47.8 MB (47767188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a933af802302536755646015b767e3c6513698ebf1ed3fc43966c7ec2aeb5d`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14223e8296d1b6d374cd7bfb5df152d3a272c55c48abbe53f12c1ee03c3ed517`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 131.9 MB (131940894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f9674f6b0df251b150ce3b812e83f53875328c1ec1501ec120e5a1b075e910`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:10abbc9aa70f9d12955b056a95912a42465e0a9ebd1243312fc69f24169b1a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b390d665638f7510c5c3c2971248fce249da79262921d5112b9a212434e106a`

```dockerfile
```

-	Layers:
	-	`sha256:cc2b22161c710488c7c85339e0d6e4983fd006586875ac2939cb23e3d36ad355`  
		Last Modified: Thu, 21 Aug 2025 21:02:20 GMT  
		Size: 14.8 MB (14804922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca3af286439898090aafbd2c70aa31da70701b3054681f22d90796f1fc6a505`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dc80dc8fb761af4c489607085ab973bfb5b286e554259fb0c1aa3570a37ee782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232452065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e2df3d226bacc2aae919ea834a0cc467836f51ee75a4a77a6e4318b6c28cd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc39bf601a8f38d3a3f8386fff1821a460baef80efd721aa299dad351d4835f`  
		Last Modified: Thu, 07 Aug 2025 23:57:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef658516113bc95ec87c99c1b2d4b9d336afe851893f9bfbb1d4945529e459b`  
		Last Modified: Fri, 08 Aug 2025 01:46:58 GMT  
		Size: 46.7 MB (46653469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd4c1e6baf03c096209eae8ddfd7414900ff578117fb867bf73d756bd7bd1fb`  
		Last Modified: Thu, 07 Aug 2025 23:57:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5688f8e7baa3ad3488ea7f0689a918efea096803d9caadc5714bf71ef1b36f36`  
		Last Modified: Fri, 08 Aug 2025 01:47:07 GMT  
		Size: 130.3 MB (130342114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c46015e74a3cb49be59fb76e2bced8cf5ddd337f1531307d0af78fb050e8ee`  
		Last Modified: Thu, 07 Aug 2025 23:57:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:a6e2a4424a2fdf5da85a5657e13df2e6d1990a199f94c21eb9bd6355d8fd0d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e01fa3bb50c6a0a4c4f259afd8355bc12963f461947fd9498aa39810efbb88`

```dockerfile
```

-	Layers:
	-	`sha256:6f92339c56022c949bbc1f028fe64c8252db1ed85a94e98d721e0945f4a08f65`  
		Last Modified: Fri, 08 Aug 2025 03:02:40 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0374db211c0cda7d4f3d824a08c11a1412692c328cf4700b1684c2307b2445d0`  
		Last Modified: Fri, 08 Aug 2025 03:02:41 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:432966f3bdcbf834ef578226e4c196fab460f0727daa888b039854b5c185e8b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5144a476c89ccd10123ed8a67754cecf50a3c3d32e7ec2e5b5e48c588e07c7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (237016226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f1b9da918eec3e2bd327cc44936b97a15d8705396efe23dfa4198656330dbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd66ec68b64f7f87b2a021e220dc67f8b4e1b902e33a79a92f58410f071efff6`  
		Last Modified: Thu, 21 Aug 2025 19:10:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df938959d2c414e200f0b9c573a1aee4c04e117929223e23508d8107ce1f92f0`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 983.0 KB (983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9348ee598b89aee26c72bb0ad652e10cc5e914f36d503492f0f5ab0252992b5`  
		Last Modified: Thu, 21 Aug 2025 19:10:09 GMT  
		Size: 6.8 MB (6818646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ff5eaaa3b2925ba1855ca2372101208fad8d49d7b82c630c5a5f9cbee5e1f`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d504a2807609c4e00c08619d2328929116183206e0cbefe142587a3db106c473`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbc662f10805e2e50d549d3af79d72079ab6f0c4e455a2692dd582d7c49dbe0`  
		Last Modified: Thu, 21 Aug 2025 19:10:12 GMT  
		Size: 47.8 MB (47767188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a933af802302536755646015b767e3c6513698ebf1ed3fc43966c7ec2aeb5d`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14223e8296d1b6d374cd7bfb5df152d3a272c55c48abbe53f12c1ee03c3ed517`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 131.9 MB (131940894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f9674f6b0df251b150ce3b812e83f53875328c1ec1501ec120e5a1b075e910`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:10abbc9aa70f9d12955b056a95912a42465e0a9ebd1243312fc69f24169b1a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b390d665638f7510c5c3c2971248fce249da79262921d5112b9a212434e106a`

```dockerfile
```

-	Layers:
	-	`sha256:cc2b22161c710488c7c85339e0d6e4983fd006586875ac2939cb23e3d36ad355`  
		Last Modified: Thu, 21 Aug 2025 21:02:20 GMT  
		Size: 14.8 MB (14804922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca3af286439898090aafbd2c70aa31da70701b3054681f22d90796f1fc6a505`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dc80dc8fb761af4c489607085ab973bfb5b286e554259fb0c1aa3570a37ee782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232452065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e2df3d226bacc2aae919ea834a0cc467836f51ee75a4a77a6e4318b6c28cd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc39bf601a8f38d3a3f8386fff1821a460baef80efd721aa299dad351d4835f`  
		Last Modified: Thu, 07 Aug 2025 23:57:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef658516113bc95ec87c99c1b2d4b9d336afe851893f9bfbb1d4945529e459b`  
		Last Modified: Fri, 08 Aug 2025 01:46:58 GMT  
		Size: 46.7 MB (46653469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd4c1e6baf03c096209eae8ddfd7414900ff578117fb867bf73d756bd7bd1fb`  
		Last Modified: Thu, 07 Aug 2025 23:57:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5688f8e7baa3ad3488ea7f0689a918efea096803d9caadc5714bf71ef1b36f36`  
		Last Modified: Fri, 08 Aug 2025 01:47:07 GMT  
		Size: 130.3 MB (130342114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c46015e74a3cb49be59fb76e2bced8cf5ddd337f1531307d0af78fb050e8ee`  
		Last Modified: Thu, 07 Aug 2025 23:57:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a6e2a4424a2fdf5da85a5657e13df2e6d1990a199f94c21eb9bd6355d8fd0d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e01fa3bb50c6a0a4c4f259afd8355bc12963f461947fd9498aa39810efbb88`

```dockerfile
```

-	Layers:
	-	`sha256:6f92339c56022c949bbc1f028fe64c8252db1ed85a94e98d721e0945f4a08f65`  
		Last Modified: Fri, 08 Aug 2025 03:02:40 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0374db211c0cda7d4f3d824a08c11a1412692c328cf4700b1684c2307b2445d0`  
		Last Modified: Fri, 08 Aug 2025 03:02:41 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:432966f3bdcbf834ef578226e4c196fab460f0727daa888b039854b5c185e8b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5144a476c89ccd10123ed8a67754cecf50a3c3d32e7ec2e5b5e48c588e07c7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (237016226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f1b9da918eec3e2bd327cc44936b97a15d8705396efe23dfa4198656330dbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd66ec68b64f7f87b2a021e220dc67f8b4e1b902e33a79a92f58410f071efff6`  
		Last Modified: Thu, 21 Aug 2025 19:10:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df938959d2c414e200f0b9c573a1aee4c04e117929223e23508d8107ce1f92f0`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 983.0 KB (983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9348ee598b89aee26c72bb0ad652e10cc5e914f36d503492f0f5ab0252992b5`  
		Last Modified: Thu, 21 Aug 2025 19:10:09 GMT  
		Size: 6.8 MB (6818646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ff5eaaa3b2925ba1855ca2372101208fad8d49d7b82c630c5a5f9cbee5e1f`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d504a2807609c4e00c08619d2328929116183206e0cbefe142587a3db106c473`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbc662f10805e2e50d549d3af79d72079ab6f0c4e455a2692dd582d7c49dbe0`  
		Last Modified: Thu, 21 Aug 2025 19:10:12 GMT  
		Size: 47.8 MB (47767188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a933af802302536755646015b767e3c6513698ebf1ed3fc43966c7ec2aeb5d`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14223e8296d1b6d374cd7bfb5df152d3a272c55c48abbe53f12c1ee03c3ed517`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 131.9 MB (131940894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f9674f6b0df251b150ce3b812e83f53875328c1ec1501ec120e5a1b075e910`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:10abbc9aa70f9d12955b056a95912a42465e0a9ebd1243312fc69f24169b1a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b390d665638f7510c5c3c2971248fce249da79262921d5112b9a212434e106a`

```dockerfile
```

-	Layers:
	-	`sha256:cc2b22161c710488c7c85339e0d6e4983fd006586875ac2939cb23e3d36ad355`  
		Last Modified: Thu, 21 Aug 2025 21:02:20 GMT  
		Size: 14.8 MB (14804922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca3af286439898090aafbd2c70aa31da70701b3054681f22d90796f1fc6a505`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dc80dc8fb761af4c489607085ab973bfb5b286e554259fb0c1aa3570a37ee782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232452065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e2df3d226bacc2aae919ea834a0cc467836f51ee75a4a77a6e4318b6c28cd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc39bf601a8f38d3a3f8386fff1821a460baef80efd721aa299dad351d4835f`  
		Last Modified: Thu, 07 Aug 2025 23:57:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef658516113bc95ec87c99c1b2d4b9d336afe851893f9bfbb1d4945529e459b`  
		Last Modified: Fri, 08 Aug 2025 01:46:58 GMT  
		Size: 46.7 MB (46653469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd4c1e6baf03c096209eae8ddfd7414900ff578117fb867bf73d756bd7bd1fb`  
		Last Modified: Thu, 07 Aug 2025 23:57:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5688f8e7baa3ad3488ea7f0689a918efea096803d9caadc5714bf71ef1b36f36`  
		Last Modified: Fri, 08 Aug 2025 01:47:07 GMT  
		Size: 130.3 MB (130342114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c46015e74a3cb49be59fb76e2bced8cf5ddd337f1531307d0af78fb050e8ee`  
		Last Modified: Thu, 07 Aug 2025 23:57:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a6e2a4424a2fdf5da85a5657e13df2e6d1990a199f94c21eb9bd6355d8fd0d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e01fa3bb50c6a0a4c4f259afd8355bc12963f461947fd9498aa39810efbb88`

```dockerfile
```

-	Layers:
	-	`sha256:6f92339c56022c949bbc1f028fe64c8252db1ed85a94e98d721e0945f4a08f65`  
		Last Modified: Fri, 08 Aug 2025 03:02:40 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0374db211c0cda7d4f3d824a08c11a1412692c328cf4700b1684c2307b2445d0`  
		Last Modified: Fri, 08 Aug 2025 03:02:41 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:6bb17264eab41dee107f8f53c7901550613c89540ade5681747b180b883832f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:f315ea10389cb76ad6597082b315321dcd2afccc131b35097f8e79e3df5f116b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236035123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c7595ac65f7dc0812ea3c974cea2c0c2820647508fa4eeaec49b070031f38e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd63fb67c1768de40b6eb705903ea934b03fa10f353f1240783c517ac4b1066`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9476b8faedbaf35f9ff71eb6c3e425c772342e1828b81f7ede0530148895c170`  
		Last Modified: Thu, 21 Aug 2025 19:10:42 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc6cc933381b62ada00330457d00c522e00c6895a207bbb456cc95e1f6743ad`  
		Last Modified: Thu, 21 Aug 2025 19:10:42 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789fa151603e5eef498d8b59191bb9c2b626de4f68e79cd5dc4d9ae595d9689d`  
		Last Modified: Thu, 21 Aug 2025 19:10:42 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1756a372d7967751f8d31a3fb4c4f1d1bd92113a88c1922461ef337c33d59549`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131412d69359f39586399f7402ef6fe3bf37e9a441d7a1cf42b3932a6170f7af`  
		Last Modified: Thu, 21 Aug 2025 19:10:50 GMT  
		Size: 49.8 MB (49819980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3eacc36b14e40f2173e01a538369d39b9361c716af6f813f8bc2f841d1fba0`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0f5543b4641547536c3a519ed069f02acf3d7e25096fbe09c6b15c1af6ef09`  
		Last Modified: Thu, 21 Aug 2025 21:02:27 GMT  
		Size: 128.9 MB (128906848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca01bc78d4e36db767cc0466c95d055fa4ef329635ef88ca89b1a5508eb4c7`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fa42a56901e932718beac3bbbd5f24996cce9fe05bf4e47afdc42c181d61bb`  
		Last Modified: Thu, 21 Aug 2025 19:10:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:2b6ba11c145f90b1180b8365a04eb268f8a246802855983c843b1f74f8fc08ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4115abb9f2a47f68d9a6f3a676a2711c5a2d5ff8a4bcd5f4b7bfa26ce6d8c922`

```dockerfile
```

-	Layers:
	-	`sha256:0c3207f1b8b19cacab05dbc7735c7667d7db7607ced2e1c90b4c04987a7330d5`  
		Last Modified: Thu, 21 Aug 2025 21:02:26 GMT  
		Size: 14.5 MB (14528101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc9e21ddb72667d9872d370b942000a675a2a193eae37f49e97b148b9751bd54`  
		Last Modified: Thu, 21 Aug 2025 21:02:27 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90d8ec290b431cd8b2259f57ff7843b18d1c62caec063d0587266eaab34c5375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231619861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219daf4d91a468dc7b95b897da073af72ae5a503ffc5d0518fd7ae7a97634a7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd0027b97057493afec90b8b34b114f7e749aefafad40d3bf6d8edec65449be`  
		Last Modified: Fri, 08 Aug 2025 00:02:15 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da0df221558b805090e033233d669e4343ca8f6d82c8154e84c8297c897e3cd`  
		Last Modified: Fri, 08 Aug 2025 00:16:16 GMT  
		Size: 48.7 MB (48674604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c055843e3f4c87a0eda1598f0314c0187c5f56c0159e34a84a91f683dd15ac67`  
		Last Modified: Fri, 08 Aug 2025 00:02:17 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6682c79ed3b0d4cc93aa496cb4bd8a37694f2a81c42b7d9bdab94eb3f9fc1c29`  
		Last Modified: Fri, 08 Aug 2025 00:16:24 GMT  
		Size: 127.5 MB (127488659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8583ecde44825194ec11f940147d91eb21dcc8ec62d7dd5331c3065debc8d220`  
		Last Modified: Fri, 08 Aug 2025 00:02:26 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c195b220f3914a615485a35ef15f7d2cb9b7962cd78c147a079a254781cb5850`  
		Last Modified: Fri, 08 Aug 2025 00:02:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:a62c9b956f6ed9066b3f20a45470a853e15dd037bcf45800d08f9285e29f641b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234e86aedc56be1bd89572c8a8ca6a64257caadcdf6231d9fb9a7aab4f41bc17`

```dockerfile
```

-	Layers:
	-	`sha256:843ce886f3d1cd8c62207b0fbc99f3386f46f335001e1ee4215ec2ce9e3b0fff`  
		Last Modified: Fri, 08 Aug 2025 03:02:50 GMT  
		Size: 14.5 MB (14526448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12d93a8268ad4fa3f7b071f9eeb402b4785e5fdbea5985bb41f2d46e7a8058d4`  
		Last Modified: Fri, 08 Aug 2025 03:02:51 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:22b2f54e172195985d0400916d723628748c65c1d4fc951d7306a7bc2eb1f866
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:130c9976cac16ce4b387d68df7f50ca4cdefbf6d4e3c169d79b908cc6b9d484b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183547518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a07f50d1519874c24a6399c233beaed2a5aad1151d0f99c0da0caf052b96c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 22 Jul 2025 22:15:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1debian12
# Tue, 22 Jul 2025 22:15:12 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ca11fc06c2e04581aa42408b151687c831716ed947189c5426119b2d7686b6`  
		Last Modified: Tue, 12 Aug 2025 21:24:33 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98fe1b6426d85fcca4cf4ef8e02a835573e71c038ac67ced6bd0e04e5e04edd`  
		Last Modified: Tue, 12 Aug 2025 21:24:36 GMT  
		Size: 4.4 MB (4422762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91378b6c8e27fea672e04f62220109b66b4868f39b99232fb770c097ec954351`  
		Last Modified: Tue, 12 Aug 2025 21:24:36 GMT  
		Size: 1.4 MB (1446050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558c74d0ee7eaea03f8fec8856bb2c2fd1b7077b8df76dc60fd6cefc6848bd1f`  
		Last Modified: Tue, 12 Aug 2025 21:24:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b301e44f9686bf83333d253018734a7a3995c2b85f4b029b34da01ad0ec7e2`  
		Last Modified: Tue, 12 Aug 2025 21:24:36 GMT  
		Size: 15.3 MB (15299349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab77016573aeb7dd1104aefbadc845d72f0dc90e68c5c8aeaa51f31d6eee9dde`  
		Last Modified: Tue, 12 Aug 2025 21:24:33 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10788b40cb4a4fedb70a6c0cdfa6b8052abc52fa9146dd7d8a2e1bbf3a93eccc`  
		Last Modified: Tue, 12 Aug 2025 21:24:34 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74bd1d36346fd5a7b1334e71fd62e35bf1d13c516661405ed4653423fc15b4`  
		Last Modified: Wed, 13 Aug 2025 00:02:31 GMT  
		Size: 134.1 MB (134138832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca1ac6091a7a77ad9029293795951a8ce8f55dc37557602ac1b8a3939a20f07`  
		Last Modified: Tue, 12 Aug 2025 21:24:34 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7b12ba77c535467afdb5c538dd5fbd6d7247d231241634b411b8dccf973d12`  
		Last Modified: Tue, 12 Aug 2025 21:24:33 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7cb6fe9c3ce887326994ccee0a026e883b7b259314665040a8099ad41ad08`  
		Last Modified: Tue, 12 Aug 2025 21:24:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:6e71baabaecc669be1287634dd5f34a3a91db215c18437001b8908afc48d2dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4195500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74c53be5c637ba5ffa4d5ad01cd85ecbd04cfe3e0d6f41106052a312e8839a9`

```dockerfile
```

-	Layers:
	-	`sha256:740b707944dfa1127006cffc64b3ec1fceb13c5a83d10425c2a0747821f0d0b8`  
		Last Modified: Wed, 13 Aug 2025 00:02:21 GMT  
		Size: 4.2 MB (4161204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a9a9db0bf433a325d91662014527bb07ea9833313b8e4ec91afce46dd9c5fce`  
		Last Modified: Wed, 13 Aug 2025 00:02:22 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:22b2f54e172195985d0400916d723628748c65c1d4fc951d7306a7bc2eb1f866
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:130c9976cac16ce4b387d68df7f50ca4cdefbf6d4e3c169d79b908cc6b9d484b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183547518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a07f50d1519874c24a6399c233beaed2a5aad1151d0f99c0da0caf052b96c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 22 Jul 2025 22:15:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1debian12
# Tue, 22 Jul 2025 22:15:12 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ca11fc06c2e04581aa42408b151687c831716ed947189c5426119b2d7686b6`  
		Last Modified: Tue, 12 Aug 2025 21:24:33 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98fe1b6426d85fcca4cf4ef8e02a835573e71c038ac67ced6bd0e04e5e04edd`  
		Last Modified: Tue, 12 Aug 2025 21:24:36 GMT  
		Size: 4.4 MB (4422762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91378b6c8e27fea672e04f62220109b66b4868f39b99232fb770c097ec954351`  
		Last Modified: Tue, 12 Aug 2025 21:24:36 GMT  
		Size: 1.4 MB (1446050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558c74d0ee7eaea03f8fec8856bb2c2fd1b7077b8df76dc60fd6cefc6848bd1f`  
		Last Modified: Tue, 12 Aug 2025 21:24:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b301e44f9686bf83333d253018734a7a3995c2b85f4b029b34da01ad0ec7e2`  
		Last Modified: Tue, 12 Aug 2025 21:24:36 GMT  
		Size: 15.3 MB (15299349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab77016573aeb7dd1104aefbadc845d72f0dc90e68c5c8aeaa51f31d6eee9dde`  
		Last Modified: Tue, 12 Aug 2025 21:24:33 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10788b40cb4a4fedb70a6c0cdfa6b8052abc52fa9146dd7d8a2e1bbf3a93eccc`  
		Last Modified: Tue, 12 Aug 2025 21:24:34 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74bd1d36346fd5a7b1334e71fd62e35bf1d13c516661405ed4653423fc15b4`  
		Last Modified: Wed, 13 Aug 2025 00:02:31 GMT  
		Size: 134.1 MB (134138832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca1ac6091a7a77ad9029293795951a8ce8f55dc37557602ac1b8a3939a20f07`  
		Last Modified: Tue, 12 Aug 2025 21:24:34 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7b12ba77c535467afdb5c538dd5fbd6d7247d231241634b411b8dccf973d12`  
		Last Modified: Tue, 12 Aug 2025 21:24:33 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7cb6fe9c3ce887326994ccee0a026e883b7b259314665040a8099ad41ad08`  
		Last Modified: Tue, 12 Aug 2025 21:24:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:6e71baabaecc669be1287634dd5f34a3a91db215c18437001b8908afc48d2dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4195500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74c53be5c637ba5ffa4d5ad01cd85ecbd04cfe3e0d6f41106052a312e8839a9`

```dockerfile
```

-	Layers:
	-	`sha256:740b707944dfa1127006cffc64b3ec1fceb13c5a83d10425c2a0747821f0d0b8`  
		Last Modified: Wed, 13 Aug 2025 00:02:21 GMT  
		Size: 4.2 MB (4161204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a9a9db0bf433a325d91662014527bb07ea9833313b8e4ec91afce46dd9c5fce`  
		Last Modified: Wed, 13 Aug 2025 00:02:22 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:6bb17264eab41dee107f8f53c7901550613c89540ade5681747b180b883832f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f315ea10389cb76ad6597082b315321dcd2afccc131b35097f8e79e3df5f116b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236035123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c7595ac65f7dc0812ea3c974cea2c0c2820647508fa4eeaec49b070031f38e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd63fb67c1768de40b6eb705903ea934b03fa10f353f1240783c517ac4b1066`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9476b8faedbaf35f9ff71eb6c3e425c772342e1828b81f7ede0530148895c170`  
		Last Modified: Thu, 21 Aug 2025 19:10:42 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc6cc933381b62ada00330457d00c522e00c6895a207bbb456cc95e1f6743ad`  
		Last Modified: Thu, 21 Aug 2025 19:10:42 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789fa151603e5eef498d8b59191bb9c2b626de4f68e79cd5dc4d9ae595d9689d`  
		Last Modified: Thu, 21 Aug 2025 19:10:42 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1756a372d7967751f8d31a3fb4c4f1d1bd92113a88c1922461ef337c33d59549`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131412d69359f39586399f7402ef6fe3bf37e9a441d7a1cf42b3932a6170f7af`  
		Last Modified: Thu, 21 Aug 2025 19:10:50 GMT  
		Size: 49.8 MB (49819980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3eacc36b14e40f2173e01a538369d39b9361c716af6f813f8bc2f841d1fba0`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0f5543b4641547536c3a519ed069f02acf3d7e25096fbe09c6b15c1af6ef09`  
		Last Modified: Thu, 21 Aug 2025 21:02:27 GMT  
		Size: 128.9 MB (128906848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca01bc78d4e36db767cc0466c95d055fa4ef329635ef88ca89b1a5508eb4c7`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fa42a56901e932718beac3bbbd5f24996cce9fe05bf4e47afdc42c181d61bb`  
		Last Modified: Thu, 21 Aug 2025 19:10:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2b6ba11c145f90b1180b8365a04eb268f8a246802855983c843b1f74f8fc08ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4115abb9f2a47f68d9a6f3a676a2711c5a2d5ff8a4bcd5f4b7bfa26ce6d8c922`

```dockerfile
```

-	Layers:
	-	`sha256:0c3207f1b8b19cacab05dbc7735c7667d7db7607ced2e1c90b4c04987a7330d5`  
		Last Modified: Thu, 21 Aug 2025 21:02:26 GMT  
		Size: 14.5 MB (14528101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc9e21ddb72667d9872d370b942000a675a2a193eae37f49e97b148b9751bd54`  
		Last Modified: Thu, 21 Aug 2025 21:02:27 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90d8ec290b431cd8b2259f57ff7843b18d1c62caec063d0587266eaab34c5375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231619861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219daf4d91a468dc7b95b897da073af72ae5a503ffc5d0518fd7ae7a97634a7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd0027b97057493afec90b8b34b114f7e749aefafad40d3bf6d8edec65449be`  
		Last Modified: Fri, 08 Aug 2025 00:02:15 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da0df221558b805090e033233d669e4343ca8f6d82c8154e84c8297c897e3cd`  
		Last Modified: Fri, 08 Aug 2025 00:16:16 GMT  
		Size: 48.7 MB (48674604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c055843e3f4c87a0eda1598f0314c0187c5f56c0159e34a84a91f683dd15ac67`  
		Last Modified: Fri, 08 Aug 2025 00:02:17 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6682c79ed3b0d4cc93aa496cb4bd8a37694f2a81c42b7d9bdab94eb3f9fc1c29`  
		Last Modified: Fri, 08 Aug 2025 00:16:24 GMT  
		Size: 127.5 MB (127488659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8583ecde44825194ec11f940147d91eb21dcc8ec62d7dd5331c3065debc8d220`  
		Last Modified: Fri, 08 Aug 2025 00:02:26 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c195b220f3914a615485a35ef15f7d2cb9b7962cd78c147a079a254781cb5850`  
		Last Modified: Fri, 08 Aug 2025 00:02:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a62c9b956f6ed9066b3f20a45470a853e15dd037bcf45800d08f9285e29f641b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234e86aedc56be1bd89572c8a8ca6a64257caadcdf6231d9fb9a7aab4f41bc17`

```dockerfile
```

-	Layers:
	-	`sha256:843ce886f3d1cd8c62207b0fbc99f3386f46f335001e1ee4215ec2ce9e3b0fff`  
		Last Modified: Fri, 08 Aug 2025 03:02:50 GMT  
		Size: 14.5 MB (14526448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12d93a8268ad4fa3f7b071f9eeb402b4785e5fdbea5985bb41f2d46e7a8058d4`  
		Last Modified: Fri, 08 Aug 2025 03:02:51 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:6bb17264eab41dee107f8f53c7901550613c89540ade5681747b180b883832f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f315ea10389cb76ad6597082b315321dcd2afccc131b35097f8e79e3df5f116b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236035123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c7595ac65f7dc0812ea3c974cea2c0c2820647508fa4eeaec49b070031f38e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd63fb67c1768de40b6eb705903ea934b03fa10f353f1240783c517ac4b1066`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9476b8faedbaf35f9ff71eb6c3e425c772342e1828b81f7ede0530148895c170`  
		Last Modified: Thu, 21 Aug 2025 19:10:42 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc6cc933381b62ada00330457d00c522e00c6895a207bbb456cc95e1f6743ad`  
		Last Modified: Thu, 21 Aug 2025 19:10:42 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789fa151603e5eef498d8b59191bb9c2b626de4f68e79cd5dc4d9ae595d9689d`  
		Last Modified: Thu, 21 Aug 2025 19:10:42 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1756a372d7967751f8d31a3fb4c4f1d1bd92113a88c1922461ef337c33d59549`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131412d69359f39586399f7402ef6fe3bf37e9a441d7a1cf42b3932a6170f7af`  
		Last Modified: Thu, 21 Aug 2025 19:10:50 GMT  
		Size: 49.8 MB (49819980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3eacc36b14e40f2173e01a538369d39b9361c716af6f813f8bc2f841d1fba0`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0f5543b4641547536c3a519ed069f02acf3d7e25096fbe09c6b15c1af6ef09`  
		Last Modified: Thu, 21 Aug 2025 21:02:27 GMT  
		Size: 128.9 MB (128906848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca01bc78d4e36db767cc0466c95d055fa4ef329635ef88ca89b1a5508eb4c7`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fa42a56901e932718beac3bbbd5f24996cce9fe05bf4e47afdc42c181d61bb`  
		Last Modified: Thu, 21 Aug 2025 19:10:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2b6ba11c145f90b1180b8365a04eb268f8a246802855983c843b1f74f8fc08ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4115abb9f2a47f68d9a6f3a676a2711c5a2d5ff8a4bcd5f4b7bfa26ce6d8c922`

```dockerfile
```

-	Layers:
	-	`sha256:0c3207f1b8b19cacab05dbc7735c7667d7db7607ced2e1c90b4c04987a7330d5`  
		Last Modified: Thu, 21 Aug 2025 21:02:26 GMT  
		Size: 14.5 MB (14528101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc9e21ddb72667d9872d370b942000a675a2a193eae37f49e97b148b9751bd54`  
		Last Modified: Thu, 21 Aug 2025 21:02:27 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90d8ec290b431cd8b2259f57ff7843b18d1c62caec063d0587266eaab34c5375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231619861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219daf4d91a468dc7b95b897da073af72ae5a503ffc5d0518fd7ae7a97634a7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd0027b97057493afec90b8b34b114f7e749aefafad40d3bf6d8edec65449be`  
		Last Modified: Fri, 08 Aug 2025 00:02:15 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da0df221558b805090e033233d669e4343ca8f6d82c8154e84c8297c897e3cd`  
		Last Modified: Fri, 08 Aug 2025 00:16:16 GMT  
		Size: 48.7 MB (48674604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c055843e3f4c87a0eda1598f0314c0187c5f56c0159e34a84a91f683dd15ac67`  
		Last Modified: Fri, 08 Aug 2025 00:02:17 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6682c79ed3b0d4cc93aa496cb4bd8a37694f2a81c42b7d9bdab94eb3f9fc1c29`  
		Last Modified: Fri, 08 Aug 2025 00:16:24 GMT  
		Size: 127.5 MB (127488659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8583ecde44825194ec11f940147d91eb21dcc8ec62d7dd5331c3065debc8d220`  
		Last Modified: Fri, 08 Aug 2025 00:02:26 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c195b220f3914a615485a35ef15f7d2cb9b7962cd78c147a079a254781cb5850`  
		Last Modified: Fri, 08 Aug 2025 00:02:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a62c9b956f6ed9066b3f20a45470a853e15dd037bcf45800d08f9285e29f641b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234e86aedc56be1bd89572c8a8ca6a64257caadcdf6231d9fb9a7aab4f41bc17`

```dockerfile
```

-	Layers:
	-	`sha256:843ce886f3d1cd8c62207b0fbc99f3386f46f335001e1ee4215ec2ce9e3b0fff`  
		Last Modified: Fri, 08 Aug 2025 03:02:50 GMT  
		Size: 14.5 MB (14526448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12d93a8268ad4fa3f7b071f9eeb402b4785e5fdbea5985bb41f2d46e7a8058d4`  
		Last Modified: Fri, 08 Aug 2025 03:02:51 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.43`

```console
$ docker pull mysql@sha256:6bb17264eab41dee107f8f53c7901550613c89540ade5681747b180b883832f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.43` - linux; amd64

```console
$ docker pull mysql@sha256:f315ea10389cb76ad6597082b315321dcd2afccc131b35097f8e79e3df5f116b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236035123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c7595ac65f7dc0812ea3c974cea2c0c2820647508fa4eeaec49b070031f38e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd63fb67c1768de40b6eb705903ea934b03fa10f353f1240783c517ac4b1066`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9476b8faedbaf35f9ff71eb6c3e425c772342e1828b81f7ede0530148895c170`  
		Last Modified: Thu, 21 Aug 2025 19:10:42 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc6cc933381b62ada00330457d00c522e00c6895a207bbb456cc95e1f6743ad`  
		Last Modified: Thu, 21 Aug 2025 19:10:42 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789fa151603e5eef498d8b59191bb9c2b626de4f68e79cd5dc4d9ae595d9689d`  
		Last Modified: Thu, 21 Aug 2025 19:10:42 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1756a372d7967751f8d31a3fb4c4f1d1bd92113a88c1922461ef337c33d59549`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131412d69359f39586399f7402ef6fe3bf37e9a441d7a1cf42b3932a6170f7af`  
		Last Modified: Thu, 21 Aug 2025 19:10:50 GMT  
		Size: 49.8 MB (49819980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3eacc36b14e40f2173e01a538369d39b9361c716af6f813f8bc2f841d1fba0`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0f5543b4641547536c3a519ed069f02acf3d7e25096fbe09c6b15c1af6ef09`  
		Last Modified: Thu, 21 Aug 2025 21:02:27 GMT  
		Size: 128.9 MB (128906848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca01bc78d4e36db767cc0466c95d055fa4ef329635ef88ca89b1a5508eb4c7`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fa42a56901e932718beac3bbbd5f24996cce9fe05bf4e47afdc42c181d61bb`  
		Last Modified: Thu, 21 Aug 2025 19:10:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43` - unknown; unknown

```console
$ docker pull mysql@sha256:2b6ba11c145f90b1180b8365a04eb268f8a246802855983c843b1f74f8fc08ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4115abb9f2a47f68d9a6f3a676a2711c5a2d5ff8a4bcd5f4b7bfa26ce6d8c922`

```dockerfile
```

-	Layers:
	-	`sha256:0c3207f1b8b19cacab05dbc7735c7667d7db7607ced2e1c90b4c04987a7330d5`  
		Last Modified: Thu, 21 Aug 2025 21:02:26 GMT  
		Size: 14.5 MB (14528101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc9e21ddb72667d9872d370b942000a675a2a193eae37f49e97b148b9751bd54`  
		Last Modified: Thu, 21 Aug 2025 21:02:27 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.43` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90d8ec290b431cd8b2259f57ff7843b18d1c62caec063d0587266eaab34c5375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231619861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219daf4d91a468dc7b95b897da073af72ae5a503ffc5d0518fd7ae7a97634a7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd0027b97057493afec90b8b34b114f7e749aefafad40d3bf6d8edec65449be`  
		Last Modified: Fri, 08 Aug 2025 00:02:15 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da0df221558b805090e033233d669e4343ca8f6d82c8154e84c8297c897e3cd`  
		Last Modified: Fri, 08 Aug 2025 00:16:16 GMT  
		Size: 48.7 MB (48674604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c055843e3f4c87a0eda1598f0314c0187c5f56c0159e34a84a91f683dd15ac67`  
		Last Modified: Fri, 08 Aug 2025 00:02:17 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6682c79ed3b0d4cc93aa496cb4bd8a37694f2a81c42b7d9bdab94eb3f9fc1c29`  
		Last Modified: Fri, 08 Aug 2025 00:16:24 GMT  
		Size: 127.5 MB (127488659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8583ecde44825194ec11f940147d91eb21dcc8ec62d7dd5331c3065debc8d220`  
		Last Modified: Fri, 08 Aug 2025 00:02:26 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c195b220f3914a615485a35ef15f7d2cb9b7962cd78c147a079a254781cb5850`  
		Last Modified: Fri, 08 Aug 2025 00:02:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43` - unknown; unknown

```console
$ docker pull mysql@sha256:a62c9b956f6ed9066b3f20a45470a853e15dd037bcf45800d08f9285e29f641b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234e86aedc56be1bd89572c8a8ca6a64257caadcdf6231d9fb9a7aab4f41bc17`

```dockerfile
```

-	Layers:
	-	`sha256:843ce886f3d1cd8c62207b0fbc99f3386f46f335001e1ee4215ec2ce9e3b0fff`  
		Last Modified: Fri, 08 Aug 2025 03:02:50 GMT  
		Size: 14.5 MB (14526448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12d93a8268ad4fa3f7b071f9eeb402b4785e5fdbea5985bb41f2d46e7a8058d4`  
		Last Modified: Fri, 08 Aug 2025 03:02:51 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.43-bookworm`

```console
$ docker pull mysql@sha256:22b2f54e172195985d0400916d723628748c65c1d4fc951d7306a7bc2eb1f866
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.43-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:130c9976cac16ce4b387d68df7f50ca4cdefbf6d4e3c169d79b908cc6b9d484b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183547518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a07f50d1519874c24a6399c233beaed2a5aad1151d0f99c0da0caf052b96c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 22 Jul 2025 22:15:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1debian12
# Tue, 22 Jul 2025 22:15:12 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ca11fc06c2e04581aa42408b151687c831716ed947189c5426119b2d7686b6`  
		Last Modified: Tue, 12 Aug 2025 21:24:33 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98fe1b6426d85fcca4cf4ef8e02a835573e71c038ac67ced6bd0e04e5e04edd`  
		Last Modified: Tue, 12 Aug 2025 21:24:36 GMT  
		Size: 4.4 MB (4422762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91378b6c8e27fea672e04f62220109b66b4868f39b99232fb770c097ec954351`  
		Last Modified: Tue, 12 Aug 2025 21:24:36 GMT  
		Size: 1.4 MB (1446050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558c74d0ee7eaea03f8fec8856bb2c2fd1b7077b8df76dc60fd6cefc6848bd1f`  
		Last Modified: Tue, 12 Aug 2025 21:24:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b301e44f9686bf83333d253018734a7a3995c2b85f4b029b34da01ad0ec7e2`  
		Last Modified: Tue, 12 Aug 2025 21:24:36 GMT  
		Size: 15.3 MB (15299349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab77016573aeb7dd1104aefbadc845d72f0dc90e68c5c8aeaa51f31d6eee9dde`  
		Last Modified: Tue, 12 Aug 2025 21:24:33 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10788b40cb4a4fedb70a6c0cdfa6b8052abc52fa9146dd7d8a2e1bbf3a93eccc`  
		Last Modified: Tue, 12 Aug 2025 21:24:34 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74bd1d36346fd5a7b1334e71fd62e35bf1d13c516661405ed4653423fc15b4`  
		Last Modified: Wed, 13 Aug 2025 00:02:31 GMT  
		Size: 134.1 MB (134138832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca1ac6091a7a77ad9029293795951a8ce8f55dc37557602ac1b8a3939a20f07`  
		Last Modified: Tue, 12 Aug 2025 21:24:34 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7b12ba77c535467afdb5c538dd5fbd6d7247d231241634b411b8dccf973d12`  
		Last Modified: Tue, 12 Aug 2025 21:24:33 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7cb6fe9c3ce887326994ccee0a026e883b7b259314665040a8099ad41ad08`  
		Last Modified: Tue, 12 Aug 2025 21:24:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:6e71baabaecc669be1287634dd5f34a3a91db215c18437001b8908afc48d2dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4195500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74c53be5c637ba5ffa4d5ad01cd85ecbd04cfe3e0d6f41106052a312e8839a9`

```dockerfile
```

-	Layers:
	-	`sha256:740b707944dfa1127006cffc64b3ec1fceb13c5a83d10425c2a0747821f0d0b8`  
		Last Modified: Wed, 13 Aug 2025 00:02:21 GMT  
		Size: 4.2 MB (4161204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a9a9db0bf433a325d91662014527bb07ea9833313b8e4ec91afce46dd9c5fce`  
		Last Modified: Wed, 13 Aug 2025 00:02:22 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.43-debian`

```console
$ docker pull mysql@sha256:22b2f54e172195985d0400916d723628748c65c1d4fc951d7306a7bc2eb1f866
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.43-debian` - linux; amd64

```console
$ docker pull mysql@sha256:130c9976cac16ce4b387d68df7f50ca4cdefbf6d4e3c169d79b908cc6b9d484b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183547518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a07f50d1519874c24a6399c233beaed2a5aad1151d0f99c0da0caf052b96c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 22 Jul 2025 22:15:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1debian12
# Tue, 22 Jul 2025 22:15:12 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ca11fc06c2e04581aa42408b151687c831716ed947189c5426119b2d7686b6`  
		Last Modified: Tue, 12 Aug 2025 21:24:33 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98fe1b6426d85fcca4cf4ef8e02a835573e71c038ac67ced6bd0e04e5e04edd`  
		Last Modified: Tue, 12 Aug 2025 21:24:36 GMT  
		Size: 4.4 MB (4422762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91378b6c8e27fea672e04f62220109b66b4868f39b99232fb770c097ec954351`  
		Last Modified: Tue, 12 Aug 2025 21:24:36 GMT  
		Size: 1.4 MB (1446050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558c74d0ee7eaea03f8fec8856bb2c2fd1b7077b8df76dc60fd6cefc6848bd1f`  
		Last Modified: Tue, 12 Aug 2025 21:24:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b301e44f9686bf83333d253018734a7a3995c2b85f4b029b34da01ad0ec7e2`  
		Last Modified: Tue, 12 Aug 2025 21:24:36 GMT  
		Size: 15.3 MB (15299349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab77016573aeb7dd1104aefbadc845d72f0dc90e68c5c8aeaa51f31d6eee9dde`  
		Last Modified: Tue, 12 Aug 2025 21:24:33 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10788b40cb4a4fedb70a6c0cdfa6b8052abc52fa9146dd7d8a2e1bbf3a93eccc`  
		Last Modified: Tue, 12 Aug 2025 21:24:34 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74bd1d36346fd5a7b1334e71fd62e35bf1d13c516661405ed4653423fc15b4`  
		Last Modified: Wed, 13 Aug 2025 00:02:31 GMT  
		Size: 134.1 MB (134138832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca1ac6091a7a77ad9029293795951a8ce8f55dc37557602ac1b8a3939a20f07`  
		Last Modified: Tue, 12 Aug 2025 21:24:34 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7b12ba77c535467afdb5c538dd5fbd6d7247d231241634b411b8dccf973d12`  
		Last Modified: Tue, 12 Aug 2025 21:24:33 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7cb6fe9c3ce887326994ccee0a026e883b7b259314665040a8099ad41ad08`  
		Last Modified: Tue, 12 Aug 2025 21:24:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:6e71baabaecc669be1287634dd5f34a3a91db215c18437001b8908afc48d2dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4195500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74c53be5c637ba5ffa4d5ad01cd85ecbd04cfe3e0d6f41106052a312e8839a9`

```dockerfile
```

-	Layers:
	-	`sha256:740b707944dfa1127006cffc64b3ec1fceb13c5a83d10425c2a0747821f0d0b8`  
		Last Modified: Wed, 13 Aug 2025 00:02:21 GMT  
		Size: 4.2 MB (4161204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a9a9db0bf433a325d91662014527bb07ea9833313b8e4ec91afce46dd9c5fce`  
		Last Modified: Wed, 13 Aug 2025 00:02:22 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.43-oracle`

```console
$ docker pull mysql@sha256:6bb17264eab41dee107f8f53c7901550613c89540ade5681747b180b883832f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.43-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f315ea10389cb76ad6597082b315321dcd2afccc131b35097f8e79e3df5f116b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236035123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c7595ac65f7dc0812ea3c974cea2c0c2820647508fa4eeaec49b070031f38e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd63fb67c1768de40b6eb705903ea934b03fa10f353f1240783c517ac4b1066`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9476b8faedbaf35f9ff71eb6c3e425c772342e1828b81f7ede0530148895c170`  
		Last Modified: Thu, 21 Aug 2025 19:10:42 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc6cc933381b62ada00330457d00c522e00c6895a207bbb456cc95e1f6743ad`  
		Last Modified: Thu, 21 Aug 2025 19:10:42 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789fa151603e5eef498d8b59191bb9c2b626de4f68e79cd5dc4d9ae595d9689d`  
		Last Modified: Thu, 21 Aug 2025 19:10:42 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1756a372d7967751f8d31a3fb4c4f1d1bd92113a88c1922461ef337c33d59549`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131412d69359f39586399f7402ef6fe3bf37e9a441d7a1cf42b3932a6170f7af`  
		Last Modified: Thu, 21 Aug 2025 19:10:50 GMT  
		Size: 49.8 MB (49819980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3eacc36b14e40f2173e01a538369d39b9361c716af6f813f8bc2f841d1fba0`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0f5543b4641547536c3a519ed069f02acf3d7e25096fbe09c6b15c1af6ef09`  
		Last Modified: Thu, 21 Aug 2025 21:02:27 GMT  
		Size: 128.9 MB (128906848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca01bc78d4e36db767cc0466c95d055fa4ef329635ef88ca89b1a5508eb4c7`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fa42a56901e932718beac3bbbd5f24996cce9fe05bf4e47afdc42c181d61bb`  
		Last Modified: Thu, 21 Aug 2025 19:10:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2b6ba11c145f90b1180b8365a04eb268f8a246802855983c843b1f74f8fc08ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4115abb9f2a47f68d9a6f3a676a2711c5a2d5ff8a4bcd5f4b7bfa26ce6d8c922`

```dockerfile
```

-	Layers:
	-	`sha256:0c3207f1b8b19cacab05dbc7735c7667d7db7607ced2e1c90b4c04987a7330d5`  
		Last Modified: Thu, 21 Aug 2025 21:02:26 GMT  
		Size: 14.5 MB (14528101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc9e21ddb72667d9872d370b942000a675a2a193eae37f49e97b148b9751bd54`  
		Last Modified: Thu, 21 Aug 2025 21:02:27 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.43-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90d8ec290b431cd8b2259f57ff7843b18d1c62caec063d0587266eaab34c5375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231619861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219daf4d91a468dc7b95b897da073af72ae5a503ffc5d0518fd7ae7a97634a7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd0027b97057493afec90b8b34b114f7e749aefafad40d3bf6d8edec65449be`  
		Last Modified: Fri, 08 Aug 2025 00:02:15 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da0df221558b805090e033233d669e4343ca8f6d82c8154e84c8297c897e3cd`  
		Last Modified: Fri, 08 Aug 2025 00:16:16 GMT  
		Size: 48.7 MB (48674604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c055843e3f4c87a0eda1598f0314c0187c5f56c0159e34a84a91f683dd15ac67`  
		Last Modified: Fri, 08 Aug 2025 00:02:17 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6682c79ed3b0d4cc93aa496cb4bd8a37694f2a81c42b7d9bdab94eb3f9fc1c29`  
		Last Modified: Fri, 08 Aug 2025 00:16:24 GMT  
		Size: 127.5 MB (127488659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8583ecde44825194ec11f940147d91eb21dcc8ec62d7dd5331c3065debc8d220`  
		Last Modified: Fri, 08 Aug 2025 00:02:26 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c195b220f3914a615485a35ef15f7d2cb9b7962cd78c147a079a254781cb5850`  
		Last Modified: Fri, 08 Aug 2025 00:02:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a62c9b956f6ed9066b3f20a45470a853e15dd037bcf45800d08f9285e29f641b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234e86aedc56be1bd89572c8a8ca6a64257caadcdf6231d9fb9a7aab4f41bc17`

```dockerfile
```

-	Layers:
	-	`sha256:843ce886f3d1cd8c62207b0fbc99f3386f46f335001e1ee4215ec2ce9e3b0fff`  
		Last Modified: Fri, 08 Aug 2025 03:02:50 GMT  
		Size: 14.5 MB (14526448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12d93a8268ad4fa3f7b071f9eeb402b4785e5fdbea5985bb41f2d46e7a8058d4`  
		Last Modified: Fri, 08 Aug 2025 03:02:51 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.43-oraclelinux9`

```console
$ docker pull mysql@sha256:6bb17264eab41dee107f8f53c7901550613c89540ade5681747b180b883832f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.43-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f315ea10389cb76ad6597082b315321dcd2afccc131b35097f8e79e3df5f116b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236035123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c7595ac65f7dc0812ea3c974cea2c0c2820647508fa4eeaec49b070031f38e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd63fb67c1768de40b6eb705903ea934b03fa10f353f1240783c517ac4b1066`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9476b8faedbaf35f9ff71eb6c3e425c772342e1828b81f7ede0530148895c170`  
		Last Modified: Thu, 21 Aug 2025 19:10:42 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc6cc933381b62ada00330457d00c522e00c6895a207bbb456cc95e1f6743ad`  
		Last Modified: Thu, 21 Aug 2025 19:10:42 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789fa151603e5eef498d8b59191bb9c2b626de4f68e79cd5dc4d9ae595d9689d`  
		Last Modified: Thu, 21 Aug 2025 19:10:42 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1756a372d7967751f8d31a3fb4c4f1d1bd92113a88c1922461ef337c33d59549`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131412d69359f39586399f7402ef6fe3bf37e9a441d7a1cf42b3932a6170f7af`  
		Last Modified: Thu, 21 Aug 2025 19:10:50 GMT  
		Size: 49.8 MB (49819980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3eacc36b14e40f2173e01a538369d39b9361c716af6f813f8bc2f841d1fba0`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0f5543b4641547536c3a519ed069f02acf3d7e25096fbe09c6b15c1af6ef09`  
		Last Modified: Thu, 21 Aug 2025 21:02:27 GMT  
		Size: 128.9 MB (128906848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca01bc78d4e36db767cc0466c95d055fa4ef329635ef88ca89b1a5508eb4c7`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fa42a56901e932718beac3bbbd5f24996cce9fe05bf4e47afdc42c181d61bb`  
		Last Modified: Thu, 21 Aug 2025 19:10:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2b6ba11c145f90b1180b8365a04eb268f8a246802855983c843b1f74f8fc08ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4115abb9f2a47f68d9a6f3a676a2711c5a2d5ff8a4bcd5f4b7bfa26ce6d8c922`

```dockerfile
```

-	Layers:
	-	`sha256:0c3207f1b8b19cacab05dbc7735c7667d7db7607ced2e1c90b4c04987a7330d5`  
		Last Modified: Thu, 21 Aug 2025 21:02:26 GMT  
		Size: 14.5 MB (14528101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc9e21ddb72667d9872d370b942000a675a2a193eae37f49e97b148b9751bd54`  
		Last Modified: Thu, 21 Aug 2025 21:02:27 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.43-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90d8ec290b431cd8b2259f57ff7843b18d1c62caec063d0587266eaab34c5375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231619861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219daf4d91a468dc7b95b897da073af72ae5a503ffc5d0518fd7ae7a97634a7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd0027b97057493afec90b8b34b114f7e749aefafad40d3bf6d8edec65449be`  
		Last Modified: Fri, 08 Aug 2025 00:02:15 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da0df221558b805090e033233d669e4343ca8f6d82c8154e84c8297c897e3cd`  
		Last Modified: Fri, 08 Aug 2025 00:16:16 GMT  
		Size: 48.7 MB (48674604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c055843e3f4c87a0eda1598f0314c0187c5f56c0159e34a84a91f683dd15ac67`  
		Last Modified: Fri, 08 Aug 2025 00:02:17 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6682c79ed3b0d4cc93aa496cb4bd8a37694f2a81c42b7d9bdab94eb3f9fc1c29`  
		Last Modified: Fri, 08 Aug 2025 00:16:24 GMT  
		Size: 127.5 MB (127488659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8583ecde44825194ec11f940147d91eb21dcc8ec62d7dd5331c3065debc8d220`  
		Last Modified: Fri, 08 Aug 2025 00:02:26 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c195b220f3914a615485a35ef15f7d2cb9b7962cd78c147a079a254781cb5850`  
		Last Modified: Fri, 08 Aug 2025 00:02:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a62c9b956f6ed9066b3f20a45470a853e15dd037bcf45800d08f9285e29f641b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234e86aedc56be1bd89572c8a8ca6a64257caadcdf6231d9fb9a7aab4f41bc17`

```dockerfile
```

-	Layers:
	-	`sha256:843ce886f3d1cd8c62207b0fbc99f3386f46f335001e1ee4215ec2ce9e3b0fff`  
		Last Modified: Fri, 08 Aug 2025 03:02:50 GMT  
		Size: 14.5 MB (14526448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12d93a8268ad4fa3f7b071f9eeb402b4785e5fdbea5985bb41f2d46e7a8058d4`  
		Last Modified: Fri, 08 Aug 2025 03:02:51 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:432966f3bdcbf834ef578226e4c196fab460f0727daa888b039854b5c185e8b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:5144a476c89ccd10123ed8a67754cecf50a3c3d32e7ec2e5b5e48c588e07c7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (237016226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f1b9da918eec3e2bd327cc44936b97a15d8705396efe23dfa4198656330dbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd66ec68b64f7f87b2a021e220dc67f8b4e1b902e33a79a92f58410f071efff6`  
		Last Modified: Thu, 21 Aug 2025 19:10:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df938959d2c414e200f0b9c573a1aee4c04e117929223e23508d8107ce1f92f0`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 983.0 KB (983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9348ee598b89aee26c72bb0ad652e10cc5e914f36d503492f0f5ab0252992b5`  
		Last Modified: Thu, 21 Aug 2025 19:10:09 GMT  
		Size: 6.8 MB (6818646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ff5eaaa3b2925ba1855ca2372101208fad8d49d7b82c630c5a5f9cbee5e1f`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d504a2807609c4e00c08619d2328929116183206e0cbefe142587a3db106c473`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbc662f10805e2e50d549d3af79d72079ab6f0c4e455a2692dd582d7c49dbe0`  
		Last Modified: Thu, 21 Aug 2025 19:10:12 GMT  
		Size: 47.8 MB (47767188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a933af802302536755646015b767e3c6513698ebf1ed3fc43966c7ec2aeb5d`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14223e8296d1b6d374cd7bfb5df152d3a272c55c48abbe53f12c1ee03c3ed517`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 131.9 MB (131940894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f9674f6b0df251b150ce3b812e83f53875328c1ec1501ec120e5a1b075e910`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:10abbc9aa70f9d12955b056a95912a42465e0a9ebd1243312fc69f24169b1a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b390d665638f7510c5c3c2971248fce249da79262921d5112b9a212434e106a`

```dockerfile
```

-	Layers:
	-	`sha256:cc2b22161c710488c7c85339e0d6e4983fd006586875ac2939cb23e3d36ad355`  
		Last Modified: Thu, 21 Aug 2025 21:02:20 GMT  
		Size: 14.8 MB (14804922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca3af286439898090aafbd2c70aa31da70701b3054681f22d90796f1fc6a505`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dc80dc8fb761af4c489607085ab973bfb5b286e554259fb0c1aa3570a37ee782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232452065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e2df3d226bacc2aae919ea834a0cc467836f51ee75a4a77a6e4318b6c28cd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc39bf601a8f38d3a3f8386fff1821a460baef80efd721aa299dad351d4835f`  
		Last Modified: Thu, 07 Aug 2025 23:57:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef658516113bc95ec87c99c1b2d4b9d336afe851893f9bfbb1d4945529e459b`  
		Last Modified: Fri, 08 Aug 2025 01:46:58 GMT  
		Size: 46.7 MB (46653469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd4c1e6baf03c096209eae8ddfd7414900ff578117fb867bf73d756bd7bd1fb`  
		Last Modified: Thu, 07 Aug 2025 23:57:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5688f8e7baa3ad3488ea7f0689a918efea096803d9caadc5714bf71ef1b36f36`  
		Last Modified: Fri, 08 Aug 2025 01:47:07 GMT  
		Size: 130.3 MB (130342114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c46015e74a3cb49be59fb76e2bced8cf5ddd337f1531307d0af78fb050e8ee`  
		Last Modified: Thu, 07 Aug 2025 23:57:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:a6e2a4424a2fdf5da85a5657e13df2e6d1990a199f94c21eb9bd6355d8fd0d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e01fa3bb50c6a0a4c4f259afd8355bc12963f461947fd9498aa39810efbb88`

```dockerfile
```

-	Layers:
	-	`sha256:6f92339c56022c949bbc1f028fe64c8252db1ed85a94e98d721e0945f4a08f65`  
		Last Modified: Fri, 08 Aug 2025 03:02:40 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0374db211c0cda7d4f3d824a08c11a1412692c328cf4700b1684c2307b2445d0`  
		Last Modified: Fri, 08 Aug 2025 03:02:41 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:432966f3bdcbf834ef578226e4c196fab460f0727daa888b039854b5c185e8b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5144a476c89ccd10123ed8a67754cecf50a3c3d32e7ec2e5b5e48c588e07c7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (237016226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f1b9da918eec3e2bd327cc44936b97a15d8705396efe23dfa4198656330dbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd66ec68b64f7f87b2a021e220dc67f8b4e1b902e33a79a92f58410f071efff6`  
		Last Modified: Thu, 21 Aug 2025 19:10:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df938959d2c414e200f0b9c573a1aee4c04e117929223e23508d8107ce1f92f0`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 983.0 KB (983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9348ee598b89aee26c72bb0ad652e10cc5e914f36d503492f0f5ab0252992b5`  
		Last Modified: Thu, 21 Aug 2025 19:10:09 GMT  
		Size: 6.8 MB (6818646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ff5eaaa3b2925ba1855ca2372101208fad8d49d7b82c630c5a5f9cbee5e1f`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d504a2807609c4e00c08619d2328929116183206e0cbefe142587a3db106c473`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbc662f10805e2e50d549d3af79d72079ab6f0c4e455a2692dd582d7c49dbe0`  
		Last Modified: Thu, 21 Aug 2025 19:10:12 GMT  
		Size: 47.8 MB (47767188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a933af802302536755646015b767e3c6513698ebf1ed3fc43966c7ec2aeb5d`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14223e8296d1b6d374cd7bfb5df152d3a272c55c48abbe53f12c1ee03c3ed517`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 131.9 MB (131940894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f9674f6b0df251b150ce3b812e83f53875328c1ec1501ec120e5a1b075e910`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:10abbc9aa70f9d12955b056a95912a42465e0a9ebd1243312fc69f24169b1a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b390d665638f7510c5c3c2971248fce249da79262921d5112b9a212434e106a`

```dockerfile
```

-	Layers:
	-	`sha256:cc2b22161c710488c7c85339e0d6e4983fd006586875ac2939cb23e3d36ad355`  
		Last Modified: Thu, 21 Aug 2025 21:02:20 GMT  
		Size: 14.8 MB (14804922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca3af286439898090aafbd2c70aa31da70701b3054681f22d90796f1fc6a505`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dc80dc8fb761af4c489607085ab973bfb5b286e554259fb0c1aa3570a37ee782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232452065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e2df3d226bacc2aae919ea834a0cc467836f51ee75a4a77a6e4318b6c28cd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc39bf601a8f38d3a3f8386fff1821a460baef80efd721aa299dad351d4835f`  
		Last Modified: Thu, 07 Aug 2025 23:57:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef658516113bc95ec87c99c1b2d4b9d336afe851893f9bfbb1d4945529e459b`  
		Last Modified: Fri, 08 Aug 2025 01:46:58 GMT  
		Size: 46.7 MB (46653469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd4c1e6baf03c096209eae8ddfd7414900ff578117fb867bf73d756bd7bd1fb`  
		Last Modified: Thu, 07 Aug 2025 23:57:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5688f8e7baa3ad3488ea7f0689a918efea096803d9caadc5714bf71ef1b36f36`  
		Last Modified: Fri, 08 Aug 2025 01:47:07 GMT  
		Size: 130.3 MB (130342114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c46015e74a3cb49be59fb76e2bced8cf5ddd337f1531307d0af78fb050e8ee`  
		Last Modified: Thu, 07 Aug 2025 23:57:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a6e2a4424a2fdf5da85a5657e13df2e6d1990a199f94c21eb9bd6355d8fd0d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e01fa3bb50c6a0a4c4f259afd8355bc12963f461947fd9498aa39810efbb88`

```dockerfile
```

-	Layers:
	-	`sha256:6f92339c56022c949bbc1f028fe64c8252db1ed85a94e98d721e0945f4a08f65`  
		Last Modified: Fri, 08 Aug 2025 03:02:40 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0374db211c0cda7d4f3d824a08c11a1412692c328cf4700b1684c2307b2445d0`  
		Last Modified: Fri, 08 Aug 2025 03:02:41 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:432966f3bdcbf834ef578226e4c196fab460f0727daa888b039854b5c185e8b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5144a476c89ccd10123ed8a67754cecf50a3c3d32e7ec2e5b5e48c588e07c7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (237016226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f1b9da918eec3e2bd327cc44936b97a15d8705396efe23dfa4198656330dbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd66ec68b64f7f87b2a021e220dc67f8b4e1b902e33a79a92f58410f071efff6`  
		Last Modified: Thu, 21 Aug 2025 19:10:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df938959d2c414e200f0b9c573a1aee4c04e117929223e23508d8107ce1f92f0`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 983.0 KB (983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9348ee598b89aee26c72bb0ad652e10cc5e914f36d503492f0f5ab0252992b5`  
		Last Modified: Thu, 21 Aug 2025 19:10:09 GMT  
		Size: 6.8 MB (6818646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ff5eaaa3b2925ba1855ca2372101208fad8d49d7b82c630c5a5f9cbee5e1f`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d504a2807609c4e00c08619d2328929116183206e0cbefe142587a3db106c473`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbc662f10805e2e50d549d3af79d72079ab6f0c4e455a2692dd582d7c49dbe0`  
		Last Modified: Thu, 21 Aug 2025 19:10:12 GMT  
		Size: 47.8 MB (47767188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a933af802302536755646015b767e3c6513698ebf1ed3fc43966c7ec2aeb5d`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14223e8296d1b6d374cd7bfb5df152d3a272c55c48abbe53f12c1ee03c3ed517`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 131.9 MB (131940894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f9674f6b0df251b150ce3b812e83f53875328c1ec1501ec120e5a1b075e910`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:10abbc9aa70f9d12955b056a95912a42465e0a9ebd1243312fc69f24169b1a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b390d665638f7510c5c3c2971248fce249da79262921d5112b9a212434e106a`

```dockerfile
```

-	Layers:
	-	`sha256:cc2b22161c710488c7c85339e0d6e4983fd006586875ac2939cb23e3d36ad355`  
		Last Modified: Thu, 21 Aug 2025 21:02:20 GMT  
		Size: 14.8 MB (14804922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca3af286439898090aafbd2c70aa31da70701b3054681f22d90796f1fc6a505`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dc80dc8fb761af4c489607085ab973bfb5b286e554259fb0c1aa3570a37ee782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232452065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e2df3d226bacc2aae919ea834a0cc467836f51ee75a4a77a6e4318b6c28cd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc39bf601a8f38d3a3f8386fff1821a460baef80efd721aa299dad351d4835f`  
		Last Modified: Thu, 07 Aug 2025 23:57:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef658516113bc95ec87c99c1b2d4b9d336afe851893f9bfbb1d4945529e459b`  
		Last Modified: Fri, 08 Aug 2025 01:46:58 GMT  
		Size: 46.7 MB (46653469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd4c1e6baf03c096209eae8ddfd7414900ff578117fb867bf73d756bd7bd1fb`  
		Last Modified: Thu, 07 Aug 2025 23:57:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5688f8e7baa3ad3488ea7f0689a918efea096803d9caadc5714bf71ef1b36f36`  
		Last Modified: Fri, 08 Aug 2025 01:47:07 GMT  
		Size: 130.3 MB (130342114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c46015e74a3cb49be59fb76e2bced8cf5ddd337f1531307d0af78fb050e8ee`  
		Last Modified: Thu, 07 Aug 2025 23:57:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a6e2a4424a2fdf5da85a5657e13df2e6d1990a199f94c21eb9bd6355d8fd0d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e01fa3bb50c6a0a4c4f259afd8355bc12963f461947fd9498aa39810efbb88`

```dockerfile
```

-	Layers:
	-	`sha256:6f92339c56022c949bbc1f028fe64c8252db1ed85a94e98d721e0945f4a08f65`  
		Last Modified: Fri, 08 Aug 2025 03:02:40 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0374db211c0cda7d4f3d824a08c11a1412692c328cf4700b1684c2307b2445d0`  
		Last Modified: Fri, 08 Aug 2025 03:02:41 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.6`

```console
$ docker pull mysql@sha256:432966f3bdcbf834ef578226e4c196fab460f0727daa888b039854b5c185e8b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.6` - linux; amd64

```console
$ docker pull mysql@sha256:5144a476c89ccd10123ed8a67754cecf50a3c3d32e7ec2e5b5e48c588e07c7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (237016226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f1b9da918eec3e2bd327cc44936b97a15d8705396efe23dfa4198656330dbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd66ec68b64f7f87b2a021e220dc67f8b4e1b902e33a79a92f58410f071efff6`  
		Last Modified: Thu, 21 Aug 2025 19:10:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df938959d2c414e200f0b9c573a1aee4c04e117929223e23508d8107ce1f92f0`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 983.0 KB (983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9348ee598b89aee26c72bb0ad652e10cc5e914f36d503492f0f5ab0252992b5`  
		Last Modified: Thu, 21 Aug 2025 19:10:09 GMT  
		Size: 6.8 MB (6818646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ff5eaaa3b2925ba1855ca2372101208fad8d49d7b82c630c5a5f9cbee5e1f`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d504a2807609c4e00c08619d2328929116183206e0cbefe142587a3db106c473`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbc662f10805e2e50d549d3af79d72079ab6f0c4e455a2692dd582d7c49dbe0`  
		Last Modified: Thu, 21 Aug 2025 19:10:12 GMT  
		Size: 47.8 MB (47767188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a933af802302536755646015b767e3c6513698ebf1ed3fc43966c7ec2aeb5d`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14223e8296d1b6d374cd7bfb5df152d3a272c55c48abbe53f12c1ee03c3ed517`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 131.9 MB (131940894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f9674f6b0df251b150ce3b812e83f53875328c1ec1501ec120e5a1b075e910`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6` - unknown; unknown

```console
$ docker pull mysql@sha256:10abbc9aa70f9d12955b056a95912a42465e0a9ebd1243312fc69f24169b1a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b390d665638f7510c5c3c2971248fce249da79262921d5112b9a212434e106a`

```dockerfile
```

-	Layers:
	-	`sha256:cc2b22161c710488c7c85339e0d6e4983fd006586875ac2939cb23e3d36ad355`  
		Last Modified: Thu, 21 Aug 2025 21:02:20 GMT  
		Size: 14.8 MB (14804922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca3af286439898090aafbd2c70aa31da70701b3054681f22d90796f1fc6a505`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.6` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dc80dc8fb761af4c489607085ab973bfb5b286e554259fb0c1aa3570a37ee782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232452065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e2df3d226bacc2aae919ea834a0cc467836f51ee75a4a77a6e4318b6c28cd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc39bf601a8f38d3a3f8386fff1821a460baef80efd721aa299dad351d4835f`  
		Last Modified: Thu, 07 Aug 2025 23:57:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef658516113bc95ec87c99c1b2d4b9d336afe851893f9bfbb1d4945529e459b`  
		Last Modified: Fri, 08 Aug 2025 01:46:58 GMT  
		Size: 46.7 MB (46653469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd4c1e6baf03c096209eae8ddfd7414900ff578117fb867bf73d756bd7bd1fb`  
		Last Modified: Thu, 07 Aug 2025 23:57:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5688f8e7baa3ad3488ea7f0689a918efea096803d9caadc5714bf71ef1b36f36`  
		Last Modified: Fri, 08 Aug 2025 01:47:07 GMT  
		Size: 130.3 MB (130342114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c46015e74a3cb49be59fb76e2bced8cf5ddd337f1531307d0af78fb050e8ee`  
		Last Modified: Thu, 07 Aug 2025 23:57:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6` - unknown; unknown

```console
$ docker pull mysql@sha256:a6e2a4424a2fdf5da85a5657e13df2e6d1990a199f94c21eb9bd6355d8fd0d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e01fa3bb50c6a0a4c4f259afd8355bc12963f461947fd9498aa39810efbb88`

```dockerfile
```

-	Layers:
	-	`sha256:6f92339c56022c949bbc1f028fe64c8252db1ed85a94e98d721e0945f4a08f65`  
		Last Modified: Fri, 08 Aug 2025 03:02:40 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0374db211c0cda7d4f3d824a08c11a1412692c328cf4700b1684c2307b2445d0`  
		Last Modified: Fri, 08 Aug 2025 03:02:41 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.6-oracle`

```console
$ docker pull mysql@sha256:432966f3bdcbf834ef578226e4c196fab460f0727daa888b039854b5c185e8b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.6-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5144a476c89ccd10123ed8a67754cecf50a3c3d32e7ec2e5b5e48c588e07c7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (237016226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f1b9da918eec3e2bd327cc44936b97a15d8705396efe23dfa4198656330dbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd66ec68b64f7f87b2a021e220dc67f8b4e1b902e33a79a92f58410f071efff6`  
		Last Modified: Thu, 21 Aug 2025 19:10:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df938959d2c414e200f0b9c573a1aee4c04e117929223e23508d8107ce1f92f0`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 983.0 KB (983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9348ee598b89aee26c72bb0ad652e10cc5e914f36d503492f0f5ab0252992b5`  
		Last Modified: Thu, 21 Aug 2025 19:10:09 GMT  
		Size: 6.8 MB (6818646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ff5eaaa3b2925ba1855ca2372101208fad8d49d7b82c630c5a5f9cbee5e1f`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d504a2807609c4e00c08619d2328929116183206e0cbefe142587a3db106c473`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbc662f10805e2e50d549d3af79d72079ab6f0c4e455a2692dd582d7c49dbe0`  
		Last Modified: Thu, 21 Aug 2025 19:10:12 GMT  
		Size: 47.8 MB (47767188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a933af802302536755646015b767e3c6513698ebf1ed3fc43966c7ec2aeb5d`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14223e8296d1b6d374cd7bfb5df152d3a272c55c48abbe53f12c1ee03c3ed517`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 131.9 MB (131940894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f9674f6b0df251b150ce3b812e83f53875328c1ec1501ec120e5a1b075e910`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:10abbc9aa70f9d12955b056a95912a42465e0a9ebd1243312fc69f24169b1a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b390d665638f7510c5c3c2971248fce249da79262921d5112b9a212434e106a`

```dockerfile
```

-	Layers:
	-	`sha256:cc2b22161c710488c7c85339e0d6e4983fd006586875ac2939cb23e3d36ad355`  
		Last Modified: Thu, 21 Aug 2025 21:02:20 GMT  
		Size: 14.8 MB (14804922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca3af286439898090aafbd2c70aa31da70701b3054681f22d90796f1fc6a505`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.6-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dc80dc8fb761af4c489607085ab973bfb5b286e554259fb0c1aa3570a37ee782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232452065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e2df3d226bacc2aae919ea834a0cc467836f51ee75a4a77a6e4318b6c28cd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc39bf601a8f38d3a3f8386fff1821a460baef80efd721aa299dad351d4835f`  
		Last Modified: Thu, 07 Aug 2025 23:57:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef658516113bc95ec87c99c1b2d4b9d336afe851893f9bfbb1d4945529e459b`  
		Last Modified: Fri, 08 Aug 2025 01:46:58 GMT  
		Size: 46.7 MB (46653469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd4c1e6baf03c096209eae8ddfd7414900ff578117fb867bf73d756bd7bd1fb`  
		Last Modified: Thu, 07 Aug 2025 23:57:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5688f8e7baa3ad3488ea7f0689a918efea096803d9caadc5714bf71ef1b36f36`  
		Last Modified: Fri, 08 Aug 2025 01:47:07 GMT  
		Size: 130.3 MB (130342114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c46015e74a3cb49be59fb76e2bced8cf5ddd337f1531307d0af78fb050e8ee`  
		Last Modified: Thu, 07 Aug 2025 23:57:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a6e2a4424a2fdf5da85a5657e13df2e6d1990a199f94c21eb9bd6355d8fd0d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e01fa3bb50c6a0a4c4f259afd8355bc12963f461947fd9498aa39810efbb88`

```dockerfile
```

-	Layers:
	-	`sha256:6f92339c56022c949bbc1f028fe64c8252db1ed85a94e98d721e0945f4a08f65`  
		Last Modified: Fri, 08 Aug 2025 03:02:40 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0374db211c0cda7d4f3d824a08c11a1412692c328cf4700b1684c2307b2445d0`  
		Last Modified: Fri, 08 Aug 2025 03:02:41 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.6-oraclelinux9`

```console
$ docker pull mysql@sha256:432966f3bdcbf834ef578226e4c196fab460f0727daa888b039854b5c185e8b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.6-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5144a476c89ccd10123ed8a67754cecf50a3c3d32e7ec2e5b5e48c588e07c7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (237016226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f1b9da918eec3e2bd327cc44936b97a15d8705396efe23dfa4198656330dbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd66ec68b64f7f87b2a021e220dc67f8b4e1b902e33a79a92f58410f071efff6`  
		Last Modified: Thu, 21 Aug 2025 19:10:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df938959d2c414e200f0b9c573a1aee4c04e117929223e23508d8107ce1f92f0`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 983.0 KB (983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9348ee598b89aee26c72bb0ad652e10cc5e914f36d503492f0f5ab0252992b5`  
		Last Modified: Thu, 21 Aug 2025 19:10:09 GMT  
		Size: 6.8 MB (6818646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ff5eaaa3b2925ba1855ca2372101208fad8d49d7b82c630c5a5f9cbee5e1f`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d504a2807609c4e00c08619d2328929116183206e0cbefe142587a3db106c473`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbc662f10805e2e50d549d3af79d72079ab6f0c4e455a2692dd582d7c49dbe0`  
		Last Modified: Thu, 21 Aug 2025 19:10:12 GMT  
		Size: 47.8 MB (47767188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a933af802302536755646015b767e3c6513698ebf1ed3fc43966c7ec2aeb5d`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14223e8296d1b6d374cd7bfb5df152d3a272c55c48abbe53f12c1ee03c3ed517`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 131.9 MB (131940894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f9674f6b0df251b150ce3b812e83f53875328c1ec1501ec120e5a1b075e910`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:10abbc9aa70f9d12955b056a95912a42465e0a9ebd1243312fc69f24169b1a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b390d665638f7510c5c3c2971248fce249da79262921d5112b9a212434e106a`

```dockerfile
```

-	Layers:
	-	`sha256:cc2b22161c710488c7c85339e0d6e4983fd006586875ac2939cb23e3d36ad355`  
		Last Modified: Thu, 21 Aug 2025 21:02:20 GMT  
		Size: 14.8 MB (14804922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca3af286439898090aafbd2c70aa31da70701b3054681f22d90796f1fc6a505`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.6-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dc80dc8fb761af4c489607085ab973bfb5b286e554259fb0c1aa3570a37ee782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232452065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e2df3d226bacc2aae919ea834a0cc467836f51ee75a4a77a6e4318b6c28cd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc39bf601a8f38d3a3f8386fff1821a460baef80efd721aa299dad351d4835f`  
		Last Modified: Thu, 07 Aug 2025 23:57:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef658516113bc95ec87c99c1b2d4b9d336afe851893f9bfbb1d4945529e459b`  
		Last Modified: Fri, 08 Aug 2025 01:46:58 GMT  
		Size: 46.7 MB (46653469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd4c1e6baf03c096209eae8ddfd7414900ff578117fb867bf73d756bd7bd1fb`  
		Last Modified: Thu, 07 Aug 2025 23:57:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5688f8e7baa3ad3488ea7f0689a918efea096803d9caadc5714bf71ef1b36f36`  
		Last Modified: Fri, 08 Aug 2025 01:47:07 GMT  
		Size: 130.3 MB (130342114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c46015e74a3cb49be59fb76e2bced8cf5ddd337f1531307d0af78fb050e8ee`  
		Last Modified: Thu, 07 Aug 2025 23:57:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a6e2a4424a2fdf5da85a5657e13df2e6d1990a199f94c21eb9bd6355d8fd0d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e01fa3bb50c6a0a4c4f259afd8355bc12963f461947fd9498aa39810efbb88`

```dockerfile
```

-	Layers:
	-	`sha256:6f92339c56022c949bbc1f028fe64c8252db1ed85a94e98d721e0945f4a08f65`  
		Last Modified: Fri, 08 Aug 2025 03:02:40 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0374db211c0cda7d4f3d824a08c11a1412692c328cf4700b1684c2307b2445d0`  
		Last Modified: Fri, 08 Aug 2025 03:02:41 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:4ff17910bdff29a899a4cc5c95ff524f505e10dba5e1f6d4b7bcf6c4c786bf4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:e85dc53b71c49afff2047f3ed2dd4ae454da462fcc3e523754e48e36aadd4e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275520924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5440daffa8102faf89239bc524701d914edc0f9cda329988d0c2239dcb356e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5138e880171452ecd094232cf3b75cc38ed7daab3d9cd6823e64fa02cc9c16`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b534c7c08c954e78178326e62146b3b4f6a3d89ce0d8d5bdbe079b63d2ed272e`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5525b1bd2d5dcdbce6b38a73246ae8e96161dee8be7e74d31287f04e4742e844`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9effc86d91a32525dd087d29d09f4eabcb1a2529dc49381c76949ea45fb94533`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bcea418c7c4be37981e06590947286f7c2242c18964d7db55a0e86e3a93e99`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3e1c37f699bde5a65af6ac76020310518d3e8daa0a722ae88e2c265ea3693c`  
		Last Modified: Thu, 21 Aug 2025 19:10:48 GMT  
		Size: 49.3 MB (49267213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e3c68e682cc1833bd8a3f99d0142a0a07798745b86d5dba5bae4f152a800dd`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50786f9db9d5db01fdb3e560fe3e49210288ff986151837b6725692f6e13e274`  
		Last Modified: Thu, 21 Aug 2025 19:16:19 GMT  
		Size: 168.9 MB (168945526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea0fa0ace0c37874b18e97a0b9d3cc46314883f4d9f85725b2406c36b9e1f04`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:6b97f0aeb85fffeea7f7d87054342e79b38cd334404dcb73807f83074eefb5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ad5312b51e6bb51743da931219a15467020e36950acf86796a7ad9a1e94196`

```dockerfile
```

-	Layers:
	-	`sha256:aa95e3138f21c9e045be692cc25ed60a4c43b97a87f35c443382ac4b5033db9f`  
		Last Modified: Thu, 21 Aug 2025 21:02:45 GMT  
		Size: 17.7 MB (17699289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604195bff17b4e5bd960ec49bbae21286f66089408833e1b3086ca7d41cd761b`  
		Last Modified: Thu, 21 Aug 2025 21:02:47 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8920eb635c2d5fd9cc83cb365632a64a8032286648395955701f76d566f7639a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270696808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7d52b6f8f700b14c8a5f3b5902e3f2fcc8dc3cf210c33348994d8ce62ddbc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aab55028fec17a260a2e6bce865fe3567b6c3398d227e78a4e1be5d1e469686`  
		Last Modified: Fri, 08 Aug 2025 00:11:51 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e4b6b957309d2e916ad9f42dd2408662062b35c9a35666d631a5f9116e1e2`  
		Last Modified: Fri, 08 Aug 2025 00:41:36 GMT  
		Size: 48.0 MB (48004052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5a6bb76bb1504b245ae15291e4e97e6ab464eaaf1405a24fad1823835422e`  
		Last Modified: Fri, 08 Aug 2025 00:11:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8792e39739497fbe4d0b7cccaa1b40466b937fc2f494fc925c1fa150fff94e8`  
		Last Modified: Fri, 08 Aug 2025 00:41:44 GMT  
		Size: 167.2 MB (167236264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a43a0d58dcd1f55d4c552dca62d95bbb328aa78db2439c4ddd524af84d7b99`  
		Last Modified: Fri, 08 Aug 2025 00:11:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:71f38ecaca1f5dea5ab8744d20107cb055a89622644134883b58f45b3d746371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dbf685b382fec4591c12109859a6490b484a08d31e8986df7dd55090b1356f`

```dockerfile
```

-	Layers:
	-	`sha256:9bc92f7f413104f0ad73673607eb4d4e8e1ba1b26cbe96138a63e4a22274b27e`  
		Last Modified: Fri, 08 Aug 2025 03:03:14 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcc3e4d2b4bd513c9a32e1986fe1364bfdb3093db6579dc7f1c826a227e6c17`  
		Last Modified: Fri, 08 Aug 2025 03:03:15 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:4ff17910bdff29a899a4cc5c95ff524f505e10dba5e1f6d4b7bcf6c4c786bf4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e85dc53b71c49afff2047f3ed2dd4ae454da462fcc3e523754e48e36aadd4e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275520924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5440daffa8102faf89239bc524701d914edc0f9cda329988d0c2239dcb356e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5138e880171452ecd094232cf3b75cc38ed7daab3d9cd6823e64fa02cc9c16`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b534c7c08c954e78178326e62146b3b4f6a3d89ce0d8d5bdbe079b63d2ed272e`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5525b1bd2d5dcdbce6b38a73246ae8e96161dee8be7e74d31287f04e4742e844`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9effc86d91a32525dd087d29d09f4eabcb1a2529dc49381c76949ea45fb94533`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bcea418c7c4be37981e06590947286f7c2242c18964d7db55a0e86e3a93e99`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3e1c37f699bde5a65af6ac76020310518d3e8daa0a722ae88e2c265ea3693c`  
		Last Modified: Thu, 21 Aug 2025 19:10:48 GMT  
		Size: 49.3 MB (49267213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e3c68e682cc1833bd8a3f99d0142a0a07798745b86d5dba5bae4f152a800dd`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50786f9db9d5db01fdb3e560fe3e49210288ff986151837b6725692f6e13e274`  
		Last Modified: Thu, 21 Aug 2025 19:16:19 GMT  
		Size: 168.9 MB (168945526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea0fa0ace0c37874b18e97a0b9d3cc46314883f4d9f85725b2406c36b9e1f04`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6b97f0aeb85fffeea7f7d87054342e79b38cd334404dcb73807f83074eefb5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ad5312b51e6bb51743da931219a15467020e36950acf86796a7ad9a1e94196`

```dockerfile
```

-	Layers:
	-	`sha256:aa95e3138f21c9e045be692cc25ed60a4c43b97a87f35c443382ac4b5033db9f`  
		Last Modified: Thu, 21 Aug 2025 21:02:45 GMT  
		Size: 17.7 MB (17699289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604195bff17b4e5bd960ec49bbae21286f66089408833e1b3086ca7d41cd761b`  
		Last Modified: Thu, 21 Aug 2025 21:02:47 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8920eb635c2d5fd9cc83cb365632a64a8032286648395955701f76d566f7639a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270696808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7d52b6f8f700b14c8a5f3b5902e3f2fcc8dc3cf210c33348994d8ce62ddbc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aab55028fec17a260a2e6bce865fe3567b6c3398d227e78a4e1be5d1e469686`  
		Last Modified: Fri, 08 Aug 2025 00:11:51 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e4b6b957309d2e916ad9f42dd2408662062b35c9a35666d631a5f9116e1e2`  
		Last Modified: Fri, 08 Aug 2025 00:41:36 GMT  
		Size: 48.0 MB (48004052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5a6bb76bb1504b245ae15291e4e97e6ab464eaaf1405a24fad1823835422e`  
		Last Modified: Fri, 08 Aug 2025 00:11:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8792e39739497fbe4d0b7cccaa1b40466b937fc2f494fc925c1fa150fff94e8`  
		Last Modified: Fri, 08 Aug 2025 00:41:44 GMT  
		Size: 167.2 MB (167236264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a43a0d58dcd1f55d4c552dca62d95bbb328aa78db2439c4ddd524af84d7b99`  
		Last Modified: Fri, 08 Aug 2025 00:11:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:71f38ecaca1f5dea5ab8744d20107cb055a89622644134883b58f45b3d746371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dbf685b382fec4591c12109859a6490b484a08d31e8986df7dd55090b1356f`

```dockerfile
```

-	Layers:
	-	`sha256:9bc92f7f413104f0ad73673607eb4d4e8e1ba1b26cbe96138a63e4a22274b27e`  
		Last Modified: Fri, 08 Aug 2025 03:03:14 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcc3e4d2b4bd513c9a32e1986fe1364bfdb3093db6579dc7f1c826a227e6c17`  
		Last Modified: Fri, 08 Aug 2025 03:03:15 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:4ff17910bdff29a899a4cc5c95ff524f505e10dba5e1f6d4b7bcf6c4c786bf4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e85dc53b71c49afff2047f3ed2dd4ae454da462fcc3e523754e48e36aadd4e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275520924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5440daffa8102faf89239bc524701d914edc0f9cda329988d0c2239dcb356e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5138e880171452ecd094232cf3b75cc38ed7daab3d9cd6823e64fa02cc9c16`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b534c7c08c954e78178326e62146b3b4f6a3d89ce0d8d5bdbe079b63d2ed272e`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5525b1bd2d5dcdbce6b38a73246ae8e96161dee8be7e74d31287f04e4742e844`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9effc86d91a32525dd087d29d09f4eabcb1a2529dc49381c76949ea45fb94533`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bcea418c7c4be37981e06590947286f7c2242c18964d7db55a0e86e3a93e99`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3e1c37f699bde5a65af6ac76020310518d3e8daa0a722ae88e2c265ea3693c`  
		Last Modified: Thu, 21 Aug 2025 19:10:48 GMT  
		Size: 49.3 MB (49267213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e3c68e682cc1833bd8a3f99d0142a0a07798745b86d5dba5bae4f152a800dd`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50786f9db9d5db01fdb3e560fe3e49210288ff986151837b6725692f6e13e274`  
		Last Modified: Thu, 21 Aug 2025 19:16:19 GMT  
		Size: 168.9 MB (168945526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea0fa0ace0c37874b18e97a0b9d3cc46314883f4d9f85725b2406c36b9e1f04`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6b97f0aeb85fffeea7f7d87054342e79b38cd334404dcb73807f83074eefb5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ad5312b51e6bb51743da931219a15467020e36950acf86796a7ad9a1e94196`

```dockerfile
```

-	Layers:
	-	`sha256:aa95e3138f21c9e045be692cc25ed60a4c43b97a87f35c443382ac4b5033db9f`  
		Last Modified: Thu, 21 Aug 2025 21:02:45 GMT  
		Size: 17.7 MB (17699289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604195bff17b4e5bd960ec49bbae21286f66089408833e1b3086ca7d41cd761b`  
		Last Modified: Thu, 21 Aug 2025 21:02:47 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8920eb635c2d5fd9cc83cb365632a64a8032286648395955701f76d566f7639a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270696808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7d52b6f8f700b14c8a5f3b5902e3f2fcc8dc3cf210c33348994d8ce62ddbc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aab55028fec17a260a2e6bce865fe3567b6c3398d227e78a4e1be5d1e469686`  
		Last Modified: Fri, 08 Aug 2025 00:11:51 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e4b6b957309d2e916ad9f42dd2408662062b35c9a35666d631a5f9116e1e2`  
		Last Modified: Fri, 08 Aug 2025 00:41:36 GMT  
		Size: 48.0 MB (48004052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5a6bb76bb1504b245ae15291e4e97e6ab464eaaf1405a24fad1823835422e`  
		Last Modified: Fri, 08 Aug 2025 00:11:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8792e39739497fbe4d0b7cccaa1b40466b937fc2f494fc925c1fa150fff94e8`  
		Last Modified: Fri, 08 Aug 2025 00:41:44 GMT  
		Size: 167.2 MB (167236264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a43a0d58dcd1f55d4c552dca62d95bbb328aa78db2439c4ddd524af84d7b99`  
		Last Modified: Fri, 08 Aug 2025 00:11:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:71f38ecaca1f5dea5ab8744d20107cb055a89622644134883b58f45b3d746371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dbf685b382fec4591c12109859a6490b484a08d31e8986df7dd55090b1356f`

```dockerfile
```

-	Layers:
	-	`sha256:9bc92f7f413104f0ad73673607eb4d4e8e1ba1b26cbe96138a63e4a22274b27e`  
		Last Modified: Fri, 08 Aug 2025 03:03:14 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcc3e4d2b4bd513c9a32e1986fe1364bfdb3093db6579dc7f1c826a227e6c17`  
		Last Modified: Fri, 08 Aug 2025 03:03:15 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4`

```console
$ docker pull mysql@sha256:4ff17910bdff29a899a4cc5c95ff524f505e10dba5e1f6d4b7bcf6c4c786bf4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4` - linux; amd64

```console
$ docker pull mysql@sha256:e85dc53b71c49afff2047f3ed2dd4ae454da462fcc3e523754e48e36aadd4e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275520924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5440daffa8102faf89239bc524701d914edc0f9cda329988d0c2239dcb356e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5138e880171452ecd094232cf3b75cc38ed7daab3d9cd6823e64fa02cc9c16`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b534c7c08c954e78178326e62146b3b4f6a3d89ce0d8d5bdbe079b63d2ed272e`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5525b1bd2d5dcdbce6b38a73246ae8e96161dee8be7e74d31287f04e4742e844`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9effc86d91a32525dd087d29d09f4eabcb1a2529dc49381c76949ea45fb94533`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bcea418c7c4be37981e06590947286f7c2242c18964d7db55a0e86e3a93e99`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3e1c37f699bde5a65af6ac76020310518d3e8daa0a722ae88e2c265ea3693c`  
		Last Modified: Thu, 21 Aug 2025 19:10:48 GMT  
		Size: 49.3 MB (49267213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e3c68e682cc1833bd8a3f99d0142a0a07798745b86d5dba5bae4f152a800dd`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50786f9db9d5db01fdb3e560fe3e49210288ff986151837b6725692f6e13e274`  
		Last Modified: Thu, 21 Aug 2025 19:16:19 GMT  
		Size: 168.9 MB (168945526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea0fa0ace0c37874b18e97a0b9d3cc46314883f4d9f85725b2406c36b9e1f04`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4` - unknown; unknown

```console
$ docker pull mysql@sha256:6b97f0aeb85fffeea7f7d87054342e79b38cd334404dcb73807f83074eefb5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ad5312b51e6bb51743da931219a15467020e36950acf86796a7ad9a1e94196`

```dockerfile
```

-	Layers:
	-	`sha256:aa95e3138f21c9e045be692cc25ed60a4c43b97a87f35c443382ac4b5033db9f`  
		Last Modified: Thu, 21 Aug 2025 21:02:45 GMT  
		Size: 17.7 MB (17699289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604195bff17b4e5bd960ec49bbae21286f66089408833e1b3086ca7d41cd761b`  
		Last Modified: Thu, 21 Aug 2025 21:02:47 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8920eb635c2d5fd9cc83cb365632a64a8032286648395955701f76d566f7639a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270696808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7d52b6f8f700b14c8a5f3b5902e3f2fcc8dc3cf210c33348994d8ce62ddbc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aab55028fec17a260a2e6bce865fe3567b6c3398d227e78a4e1be5d1e469686`  
		Last Modified: Fri, 08 Aug 2025 00:11:51 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e4b6b957309d2e916ad9f42dd2408662062b35c9a35666d631a5f9116e1e2`  
		Last Modified: Fri, 08 Aug 2025 00:41:36 GMT  
		Size: 48.0 MB (48004052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5a6bb76bb1504b245ae15291e4e97e6ab464eaaf1405a24fad1823835422e`  
		Last Modified: Fri, 08 Aug 2025 00:11:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8792e39739497fbe4d0b7cccaa1b40466b937fc2f494fc925c1fa150fff94e8`  
		Last Modified: Fri, 08 Aug 2025 00:41:44 GMT  
		Size: 167.2 MB (167236264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a43a0d58dcd1f55d4c552dca62d95bbb328aa78db2439c4ddd524af84d7b99`  
		Last Modified: Fri, 08 Aug 2025 00:11:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4` - unknown; unknown

```console
$ docker pull mysql@sha256:71f38ecaca1f5dea5ab8744d20107cb055a89622644134883b58f45b3d746371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dbf685b382fec4591c12109859a6490b484a08d31e8986df7dd55090b1356f`

```dockerfile
```

-	Layers:
	-	`sha256:9bc92f7f413104f0ad73673607eb4d4e8e1ba1b26cbe96138a63e4a22274b27e`  
		Last Modified: Fri, 08 Aug 2025 03:03:14 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcc3e4d2b4bd513c9a32e1986fe1364bfdb3093db6579dc7f1c826a227e6c17`  
		Last Modified: Fri, 08 Aug 2025 03:03:15 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4-oracle`

```console
$ docker pull mysql@sha256:4ff17910bdff29a899a4cc5c95ff524f505e10dba5e1f6d4b7bcf6c4c786bf4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e85dc53b71c49afff2047f3ed2dd4ae454da462fcc3e523754e48e36aadd4e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275520924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5440daffa8102faf89239bc524701d914edc0f9cda329988d0c2239dcb356e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5138e880171452ecd094232cf3b75cc38ed7daab3d9cd6823e64fa02cc9c16`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b534c7c08c954e78178326e62146b3b4f6a3d89ce0d8d5bdbe079b63d2ed272e`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5525b1bd2d5dcdbce6b38a73246ae8e96161dee8be7e74d31287f04e4742e844`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9effc86d91a32525dd087d29d09f4eabcb1a2529dc49381c76949ea45fb94533`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bcea418c7c4be37981e06590947286f7c2242c18964d7db55a0e86e3a93e99`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3e1c37f699bde5a65af6ac76020310518d3e8daa0a722ae88e2c265ea3693c`  
		Last Modified: Thu, 21 Aug 2025 19:10:48 GMT  
		Size: 49.3 MB (49267213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e3c68e682cc1833bd8a3f99d0142a0a07798745b86d5dba5bae4f152a800dd`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50786f9db9d5db01fdb3e560fe3e49210288ff986151837b6725692f6e13e274`  
		Last Modified: Thu, 21 Aug 2025 19:16:19 GMT  
		Size: 168.9 MB (168945526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea0fa0ace0c37874b18e97a0b9d3cc46314883f4d9f85725b2406c36b9e1f04`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6b97f0aeb85fffeea7f7d87054342e79b38cd334404dcb73807f83074eefb5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ad5312b51e6bb51743da931219a15467020e36950acf86796a7ad9a1e94196`

```dockerfile
```

-	Layers:
	-	`sha256:aa95e3138f21c9e045be692cc25ed60a4c43b97a87f35c443382ac4b5033db9f`  
		Last Modified: Thu, 21 Aug 2025 21:02:45 GMT  
		Size: 17.7 MB (17699289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604195bff17b4e5bd960ec49bbae21286f66089408833e1b3086ca7d41cd761b`  
		Last Modified: Thu, 21 Aug 2025 21:02:47 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8920eb635c2d5fd9cc83cb365632a64a8032286648395955701f76d566f7639a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270696808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7d52b6f8f700b14c8a5f3b5902e3f2fcc8dc3cf210c33348994d8ce62ddbc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aab55028fec17a260a2e6bce865fe3567b6c3398d227e78a4e1be5d1e469686`  
		Last Modified: Fri, 08 Aug 2025 00:11:51 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e4b6b957309d2e916ad9f42dd2408662062b35c9a35666d631a5f9116e1e2`  
		Last Modified: Fri, 08 Aug 2025 00:41:36 GMT  
		Size: 48.0 MB (48004052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5a6bb76bb1504b245ae15291e4e97e6ab464eaaf1405a24fad1823835422e`  
		Last Modified: Fri, 08 Aug 2025 00:11:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8792e39739497fbe4d0b7cccaa1b40466b937fc2f494fc925c1fa150fff94e8`  
		Last Modified: Fri, 08 Aug 2025 00:41:44 GMT  
		Size: 167.2 MB (167236264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a43a0d58dcd1f55d4c552dca62d95bbb328aa78db2439c4ddd524af84d7b99`  
		Last Modified: Fri, 08 Aug 2025 00:11:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:71f38ecaca1f5dea5ab8744d20107cb055a89622644134883b58f45b3d746371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dbf685b382fec4591c12109859a6490b484a08d31e8986df7dd55090b1356f`

```dockerfile
```

-	Layers:
	-	`sha256:9bc92f7f413104f0ad73673607eb4d4e8e1ba1b26cbe96138a63e4a22274b27e`  
		Last Modified: Fri, 08 Aug 2025 03:03:14 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcc3e4d2b4bd513c9a32e1986fe1364bfdb3093db6579dc7f1c826a227e6c17`  
		Last Modified: Fri, 08 Aug 2025 03:03:15 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4-oraclelinux9`

```console
$ docker pull mysql@sha256:4ff17910bdff29a899a4cc5c95ff524f505e10dba5e1f6d4b7bcf6c4c786bf4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e85dc53b71c49afff2047f3ed2dd4ae454da462fcc3e523754e48e36aadd4e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275520924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5440daffa8102faf89239bc524701d914edc0f9cda329988d0c2239dcb356e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5138e880171452ecd094232cf3b75cc38ed7daab3d9cd6823e64fa02cc9c16`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b534c7c08c954e78178326e62146b3b4f6a3d89ce0d8d5bdbe079b63d2ed272e`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5525b1bd2d5dcdbce6b38a73246ae8e96161dee8be7e74d31287f04e4742e844`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9effc86d91a32525dd087d29d09f4eabcb1a2529dc49381c76949ea45fb94533`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bcea418c7c4be37981e06590947286f7c2242c18964d7db55a0e86e3a93e99`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3e1c37f699bde5a65af6ac76020310518d3e8daa0a722ae88e2c265ea3693c`  
		Last Modified: Thu, 21 Aug 2025 19:10:48 GMT  
		Size: 49.3 MB (49267213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e3c68e682cc1833bd8a3f99d0142a0a07798745b86d5dba5bae4f152a800dd`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50786f9db9d5db01fdb3e560fe3e49210288ff986151837b6725692f6e13e274`  
		Last Modified: Thu, 21 Aug 2025 19:16:19 GMT  
		Size: 168.9 MB (168945526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea0fa0ace0c37874b18e97a0b9d3cc46314883f4d9f85725b2406c36b9e1f04`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6b97f0aeb85fffeea7f7d87054342e79b38cd334404dcb73807f83074eefb5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ad5312b51e6bb51743da931219a15467020e36950acf86796a7ad9a1e94196`

```dockerfile
```

-	Layers:
	-	`sha256:aa95e3138f21c9e045be692cc25ed60a4c43b97a87f35c443382ac4b5033db9f`  
		Last Modified: Thu, 21 Aug 2025 21:02:45 GMT  
		Size: 17.7 MB (17699289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604195bff17b4e5bd960ec49bbae21286f66089408833e1b3086ca7d41cd761b`  
		Last Modified: Thu, 21 Aug 2025 21:02:47 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8920eb635c2d5fd9cc83cb365632a64a8032286648395955701f76d566f7639a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270696808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7d52b6f8f700b14c8a5f3b5902e3f2fcc8dc3cf210c33348994d8ce62ddbc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aab55028fec17a260a2e6bce865fe3567b6c3398d227e78a4e1be5d1e469686`  
		Last Modified: Fri, 08 Aug 2025 00:11:51 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e4b6b957309d2e916ad9f42dd2408662062b35c9a35666d631a5f9116e1e2`  
		Last Modified: Fri, 08 Aug 2025 00:41:36 GMT  
		Size: 48.0 MB (48004052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5a6bb76bb1504b245ae15291e4e97e6ab464eaaf1405a24fad1823835422e`  
		Last Modified: Fri, 08 Aug 2025 00:11:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8792e39739497fbe4d0b7cccaa1b40466b937fc2f494fc925c1fa150fff94e8`  
		Last Modified: Fri, 08 Aug 2025 00:41:44 GMT  
		Size: 167.2 MB (167236264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a43a0d58dcd1f55d4c552dca62d95bbb328aa78db2439c4ddd524af84d7b99`  
		Last Modified: Fri, 08 Aug 2025 00:11:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:71f38ecaca1f5dea5ab8744d20107cb055a89622644134883b58f45b3d746371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dbf685b382fec4591c12109859a6490b484a08d31e8986df7dd55090b1356f`

```dockerfile
```

-	Layers:
	-	`sha256:9bc92f7f413104f0ad73673607eb4d4e8e1ba1b26cbe96138a63e4a22274b27e`  
		Last Modified: Fri, 08 Aug 2025 03:03:14 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcc3e4d2b4bd513c9a32e1986fe1364bfdb3093db6579dc7f1c826a227e6c17`  
		Last Modified: Fri, 08 Aug 2025 03:03:15 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4.0`

```console
$ docker pull mysql@sha256:4ff17910bdff29a899a4cc5c95ff524f505e10dba5e1f6d4b7bcf6c4c786bf4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4.0` - linux; amd64

```console
$ docker pull mysql@sha256:e85dc53b71c49afff2047f3ed2dd4ae454da462fcc3e523754e48e36aadd4e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275520924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5440daffa8102faf89239bc524701d914edc0f9cda329988d0c2239dcb356e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5138e880171452ecd094232cf3b75cc38ed7daab3d9cd6823e64fa02cc9c16`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b534c7c08c954e78178326e62146b3b4f6a3d89ce0d8d5bdbe079b63d2ed272e`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5525b1bd2d5dcdbce6b38a73246ae8e96161dee8be7e74d31287f04e4742e844`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9effc86d91a32525dd087d29d09f4eabcb1a2529dc49381c76949ea45fb94533`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bcea418c7c4be37981e06590947286f7c2242c18964d7db55a0e86e3a93e99`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3e1c37f699bde5a65af6ac76020310518d3e8daa0a722ae88e2c265ea3693c`  
		Last Modified: Thu, 21 Aug 2025 19:10:48 GMT  
		Size: 49.3 MB (49267213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e3c68e682cc1833bd8a3f99d0142a0a07798745b86d5dba5bae4f152a800dd`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50786f9db9d5db01fdb3e560fe3e49210288ff986151837b6725692f6e13e274`  
		Last Modified: Thu, 21 Aug 2025 19:16:19 GMT  
		Size: 168.9 MB (168945526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea0fa0ace0c37874b18e97a0b9d3cc46314883f4d9f85725b2406c36b9e1f04`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0` - unknown; unknown

```console
$ docker pull mysql@sha256:6b97f0aeb85fffeea7f7d87054342e79b38cd334404dcb73807f83074eefb5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ad5312b51e6bb51743da931219a15467020e36950acf86796a7ad9a1e94196`

```dockerfile
```

-	Layers:
	-	`sha256:aa95e3138f21c9e045be692cc25ed60a4c43b97a87f35c443382ac4b5033db9f`  
		Last Modified: Thu, 21 Aug 2025 21:02:45 GMT  
		Size: 17.7 MB (17699289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604195bff17b4e5bd960ec49bbae21286f66089408833e1b3086ca7d41cd761b`  
		Last Modified: Thu, 21 Aug 2025 21:02:47 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8920eb635c2d5fd9cc83cb365632a64a8032286648395955701f76d566f7639a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270696808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7d52b6f8f700b14c8a5f3b5902e3f2fcc8dc3cf210c33348994d8ce62ddbc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aab55028fec17a260a2e6bce865fe3567b6c3398d227e78a4e1be5d1e469686`  
		Last Modified: Fri, 08 Aug 2025 00:11:51 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e4b6b957309d2e916ad9f42dd2408662062b35c9a35666d631a5f9116e1e2`  
		Last Modified: Fri, 08 Aug 2025 00:41:36 GMT  
		Size: 48.0 MB (48004052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5a6bb76bb1504b245ae15291e4e97e6ab464eaaf1405a24fad1823835422e`  
		Last Modified: Fri, 08 Aug 2025 00:11:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8792e39739497fbe4d0b7cccaa1b40466b937fc2f494fc925c1fa150fff94e8`  
		Last Modified: Fri, 08 Aug 2025 00:41:44 GMT  
		Size: 167.2 MB (167236264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a43a0d58dcd1f55d4c552dca62d95bbb328aa78db2439c4ddd524af84d7b99`  
		Last Modified: Fri, 08 Aug 2025 00:11:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0` - unknown; unknown

```console
$ docker pull mysql@sha256:71f38ecaca1f5dea5ab8744d20107cb055a89622644134883b58f45b3d746371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dbf685b382fec4591c12109859a6490b484a08d31e8986df7dd55090b1356f`

```dockerfile
```

-	Layers:
	-	`sha256:9bc92f7f413104f0ad73673607eb4d4e8e1ba1b26cbe96138a63e4a22274b27e`  
		Last Modified: Fri, 08 Aug 2025 03:03:14 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcc3e4d2b4bd513c9a32e1986fe1364bfdb3093db6579dc7f1c826a227e6c17`  
		Last Modified: Fri, 08 Aug 2025 03:03:15 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4.0-oracle`

```console
$ docker pull mysql@sha256:4ff17910bdff29a899a4cc5c95ff524f505e10dba5e1f6d4b7bcf6c4c786bf4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e85dc53b71c49afff2047f3ed2dd4ae454da462fcc3e523754e48e36aadd4e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275520924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5440daffa8102faf89239bc524701d914edc0f9cda329988d0c2239dcb356e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5138e880171452ecd094232cf3b75cc38ed7daab3d9cd6823e64fa02cc9c16`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b534c7c08c954e78178326e62146b3b4f6a3d89ce0d8d5bdbe079b63d2ed272e`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5525b1bd2d5dcdbce6b38a73246ae8e96161dee8be7e74d31287f04e4742e844`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9effc86d91a32525dd087d29d09f4eabcb1a2529dc49381c76949ea45fb94533`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bcea418c7c4be37981e06590947286f7c2242c18964d7db55a0e86e3a93e99`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3e1c37f699bde5a65af6ac76020310518d3e8daa0a722ae88e2c265ea3693c`  
		Last Modified: Thu, 21 Aug 2025 19:10:48 GMT  
		Size: 49.3 MB (49267213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e3c68e682cc1833bd8a3f99d0142a0a07798745b86d5dba5bae4f152a800dd`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50786f9db9d5db01fdb3e560fe3e49210288ff986151837b6725692f6e13e274`  
		Last Modified: Thu, 21 Aug 2025 19:16:19 GMT  
		Size: 168.9 MB (168945526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea0fa0ace0c37874b18e97a0b9d3cc46314883f4d9f85725b2406c36b9e1f04`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6b97f0aeb85fffeea7f7d87054342e79b38cd334404dcb73807f83074eefb5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ad5312b51e6bb51743da931219a15467020e36950acf86796a7ad9a1e94196`

```dockerfile
```

-	Layers:
	-	`sha256:aa95e3138f21c9e045be692cc25ed60a4c43b97a87f35c443382ac4b5033db9f`  
		Last Modified: Thu, 21 Aug 2025 21:02:45 GMT  
		Size: 17.7 MB (17699289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604195bff17b4e5bd960ec49bbae21286f66089408833e1b3086ca7d41cd761b`  
		Last Modified: Thu, 21 Aug 2025 21:02:47 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8920eb635c2d5fd9cc83cb365632a64a8032286648395955701f76d566f7639a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270696808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7d52b6f8f700b14c8a5f3b5902e3f2fcc8dc3cf210c33348994d8ce62ddbc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aab55028fec17a260a2e6bce865fe3567b6c3398d227e78a4e1be5d1e469686`  
		Last Modified: Fri, 08 Aug 2025 00:11:51 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e4b6b957309d2e916ad9f42dd2408662062b35c9a35666d631a5f9116e1e2`  
		Last Modified: Fri, 08 Aug 2025 00:41:36 GMT  
		Size: 48.0 MB (48004052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5a6bb76bb1504b245ae15291e4e97e6ab464eaaf1405a24fad1823835422e`  
		Last Modified: Fri, 08 Aug 2025 00:11:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8792e39739497fbe4d0b7cccaa1b40466b937fc2f494fc925c1fa150fff94e8`  
		Last Modified: Fri, 08 Aug 2025 00:41:44 GMT  
		Size: 167.2 MB (167236264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a43a0d58dcd1f55d4c552dca62d95bbb328aa78db2439c4ddd524af84d7b99`  
		Last Modified: Fri, 08 Aug 2025 00:11:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:71f38ecaca1f5dea5ab8744d20107cb055a89622644134883b58f45b3d746371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dbf685b382fec4591c12109859a6490b484a08d31e8986df7dd55090b1356f`

```dockerfile
```

-	Layers:
	-	`sha256:9bc92f7f413104f0ad73673607eb4d4e8e1ba1b26cbe96138a63e4a22274b27e`  
		Last Modified: Fri, 08 Aug 2025 03:03:14 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcc3e4d2b4bd513c9a32e1986fe1364bfdb3093db6579dc7f1c826a227e6c17`  
		Last Modified: Fri, 08 Aug 2025 03:03:15 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4.0-oraclelinux9`

```console
$ docker pull mysql@sha256:4ff17910bdff29a899a4cc5c95ff524f505e10dba5e1f6d4b7bcf6c4c786bf4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e85dc53b71c49afff2047f3ed2dd4ae454da462fcc3e523754e48e36aadd4e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275520924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5440daffa8102faf89239bc524701d914edc0f9cda329988d0c2239dcb356e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5138e880171452ecd094232cf3b75cc38ed7daab3d9cd6823e64fa02cc9c16`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b534c7c08c954e78178326e62146b3b4f6a3d89ce0d8d5bdbe079b63d2ed272e`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5525b1bd2d5dcdbce6b38a73246ae8e96161dee8be7e74d31287f04e4742e844`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9effc86d91a32525dd087d29d09f4eabcb1a2529dc49381c76949ea45fb94533`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bcea418c7c4be37981e06590947286f7c2242c18964d7db55a0e86e3a93e99`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3e1c37f699bde5a65af6ac76020310518d3e8daa0a722ae88e2c265ea3693c`  
		Last Modified: Thu, 21 Aug 2025 19:10:48 GMT  
		Size: 49.3 MB (49267213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e3c68e682cc1833bd8a3f99d0142a0a07798745b86d5dba5bae4f152a800dd`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50786f9db9d5db01fdb3e560fe3e49210288ff986151837b6725692f6e13e274`  
		Last Modified: Thu, 21 Aug 2025 19:16:19 GMT  
		Size: 168.9 MB (168945526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea0fa0ace0c37874b18e97a0b9d3cc46314883f4d9f85725b2406c36b9e1f04`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6b97f0aeb85fffeea7f7d87054342e79b38cd334404dcb73807f83074eefb5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ad5312b51e6bb51743da931219a15467020e36950acf86796a7ad9a1e94196`

```dockerfile
```

-	Layers:
	-	`sha256:aa95e3138f21c9e045be692cc25ed60a4c43b97a87f35c443382ac4b5033db9f`  
		Last Modified: Thu, 21 Aug 2025 21:02:45 GMT  
		Size: 17.7 MB (17699289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604195bff17b4e5bd960ec49bbae21286f66089408833e1b3086ca7d41cd761b`  
		Last Modified: Thu, 21 Aug 2025 21:02:47 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8920eb635c2d5fd9cc83cb365632a64a8032286648395955701f76d566f7639a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270696808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7d52b6f8f700b14c8a5f3b5902e3f2fcc8dc3cf210c33348994d8ce62ddbc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aab55028fec17a260a2e6bce865fe3567b6c3398d227e78a4e1be5d1e469686`  
		Last Modified: Fri, 08 Aug 2025 00:11:51 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e4b6b957309d2e916ad9f42dd2408662062b35c9a35666d631a5f9116e1e2`  
		Last Modified: Fri, 08 Aug 2025 00:41:36 GMT  
		Size: 48.0 MB (48004052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5a6bb76bb1504b245ae15291e4e97e6ab464eaaf1405a24fad1823835422e`  
		Last Modified: Fri, 08 Aug 2025 00:11:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8792e39739497fbe4d0b7cccaa1b40466b937fc2f494fc925c1fa150fff94e8`  
		Last Modified: Fri, 08 Aug 2025 00:41:44 GMT  
		Size: 167.2 MB (167236264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a43a0d58dcd1f55d4c552dca62d95bbb328aa78db2439c4ddd524af84d7b99`  
		Last Modified: Fri, 08 Aug 2025 00:11:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:71f38ecaca1f5dea5ab8744d20107cb055a89622644134883b58f45b3d746371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dbf685b382fec4591c12109859a6490b484a08d31e8986df7dd55090b1356f`

```dockerfile
```

-	Layers:
	-	`sha256:9bc92f7f413104f0ad73673607eb4d4e8e1ba1b26cbe96138a63e4a22274b27e`  
		Last Modified: Fri, 08 Aug 2025 03:03:14 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcc3e4d2b4bd513c9a32e1986fe1364bfdb3093db6579dc7f1c826a227e6c17`  
		Last Modified: Fri, 08 Aug 2025 03:03:15 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:4ff17910bdff29a899a4cc5c95ff524f505e10dba5e1f6d4b7bcf6c4c786bf4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:e85dc53b71c49afff2047f3ed2dd4ae454da462fcc3e523754e48e36aadd4e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275520924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5440daffa8102faf89239bc524701d914edc0f9cda329988d0c2239dcb356e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5138e880171452ecd094232cf3b75cc38ed7daab3d9cd6823e64fa02cc9c16`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b534c7c08c954e78178326e62146b3b4f6a3d89ce0d8d5bdbe079b63d2ed272e`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5525b1bd2d5dcdbce6b38a73246ae8e96161dee8be7e74d31287f04e4742e844`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9effc86d91a32525dd087d29d09f4eabcb1a2529dc49381c76949ea45fb94533`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bcea418c7c4be37981e06590947286f7c2242c18964d7db55a0e86e3a93e99`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3e1c37f699bde5a65af6ac76020310518d3e8daa0a722ae88e2c265ea3693c`  
		Last Modified: Thu, 21 Aug 2025 19:10:48 GMT  
		Size: 49.3 MB (49267213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e3c68e682cc1833bd8a3f99d0142a0a07798745b86d5dba5bae4f152a800dd`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50786f9db9d5db01fdb3e560fe3e49210288ff986151837b6725692f6e13e274`  
		Last Modified: Thu, 21 Aug 2025 19:16:19 GMT  
		Size: 168.9 MB (168945526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea0fa0ace0c37874b18e97a0b9d3cc46314883f4d9f85725b2406c36b9e1f04`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:6b97f0aeb85fffeea7f7d87054342e79b38cd334404dcb73807f83074eefb5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ad5312b51e6bb51743da931219a15467020e36950acf86796a7ad9a1e94196`

```dockerfile
```

-	Layers:
	-	`sha256:aa95e3138f21c9e045be692cc25ed60a4c43b97a87f35c443382ac4b5033db9f`  
		Last Modified: Thu, 21 Aug 2025 21:02:45 GMT  
		Size: 17.7 MB (17699289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604195bff17b4e5bd960ec49bbae21286f66089408833e1b3086ca7d41cd761b`  
		Last Modified: Thu, 21 Aug 2025 21:02:47 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8920eb635c2d5fd9cc83cb365632a64a8032286648395955701f76d566f7639a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270696808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7d52b6f8f700b14c8a5f3b5902e3f2fcc8dc3cf210c33348994d8ce62ddbc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aab55028fec17a260a2e6bce865fe3567b6c3398d227e78a4e1be5d1e469686`  
		Last Modified: Fri, 08 Aug 2025 00:11:51 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e4b6b957309d2e916ad9f42dd2408662062b35c9a35666d631a5f9116e1e2`  
		Last Modified: Fri, 08 Aug 2025 00:41:36 GMT  
		Size: 48.0 MB (48004052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5a6bb76bb1504b245ae15291e4e97e6ab464eaaf1405a24fad1823835422e`  
		Last Modified: Fri, 08 Aug 2025 00:11:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8792e39739497fbe4d0b7cccaa1b40466b937fc2f494fc925c1fa150fff94e8`  
		Last Modified: Fri, 08 Aug 2025 00:41:44 GMT  
		Size: 167.2 MB (167236264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a43a0d58dcd1f55d4c552dca62d95bbb328aa78db2439c4ddd524af84d7b99`  
		Last Modified: Fri, 08 Aug 2025 00:11:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:71f38ecaca1f5dea5ab8744d20107cb055a89622644134883b58f45b3d746371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dbf685b382fec4591c12109859a6490b484a08d31e8986df7dd55090b1356f`

```dockerfile
```

-	Layers:
	-	`sha256:9bc92f7f413104f0ad73673607eb4d4e8e1ba1b26cbe96138a63e4a22274b27e`  
		Last Modified: Fri, 08 Aug 2025 03:03:14 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcc3e4d2b4bd513c9a32e1986fe1364bfdb3093db6579dc7f1c826a227e6c17`  
		Last Modified: Fri, 08 Aug 2025 03:03:15 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:4ff17910bdff29a899a4cc5c95ff524f505e10dba5e1f6d4b7bcf6c4c786bf4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e85dc53b71c49afff2047f3ed2dd4ae454da462fcc3e523754e48e36aadd4e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275520924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5440daffa8102faf89239bc524701d914edc0f9cda329988d0c2239dcb356e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5138e880171452ecd094232cf3b75cc38ed7daab3d9cd6823e64fa02cc9c16`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b534c7c08c954e78178326e62146b3b4f6a3d89ce0d8d5bdbe079b63d2ed272e`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5525b1bd2d5dcdbce6b38a73246ae8e96161dee8be7e74d31287f04e4742e844`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9effc86d91a32525dd087d29d09f4eabcb1a2529dc49381c76949ea45fb94533`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bcea418c7c4be37981e06590947286f7c2242c18964d7db55a0e86e3a93e99`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3e1c37f699bde5a65af6ac76020310518d3e8daa0a722ae88e2c265ea3693c`  
		Last Modified: Thu, 21 Aug 2025 19:10:48 GMT  
		Size: 49.3 MB (49267213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e3c68e682cc1833bd8a3f99d0142a0a07798745b86d5dba5bae4f152a800dd`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50786f9db9d5db01fdb3e560fe3e49210288ff986151837b6725692f6e13e274`  
		Last Modified: Thu, 21 Aug 2025 19:16:19 GMT  
		Size: 168.9 MB (168945526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea0fa0ace0c37874b18e97a0b9d3cc46314883f4d9f85725b2406c36b9e1f04`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6b97f0aeb85fffeea7f7d87054342e79b38cd334404dcb73807f83074eefb5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ad5312b51e6bb51743da931219a15467020e36950acf86796a7ad9a1e94196`

```dockerfile
```

-	Layers:
	-	`sha256:aa95e3138f21c9e045be692cc25ed60a4c43b97a87f35c443382ac4b5033db9f`  
		Last Modified: Thu, 21 Aug 2025 21:02:45 GMT  
		Size: 17.7 MB (17699289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604195bff17b4e5bd960ec49bbae21286f66089408833e1b3086ca7d41cd761b`  
		Last Modified: Thu, 21 Aug 2025 21:02:47 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8920eb635c2d5fd9cc83cb365632a64a8032286648395955701f76d566f7639a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270696808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7d52b6f8f700b14c8a5f3b5902e3f2fcc8dc3cf210c33348994d8ce62ddbc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aab55028fec17a260a2e6bce865fe3567b6c3398d227e78a4e1be5d1e469686`  
		Last Modified: Fri, 08 Aug 2025 00:11:51 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e4b6b957309d2e916ad9f42dd2408662062b35c9a35666d631a5f9116e1e2`  
		Last Modified: Fri, 08 Aug 2025 00:41:36 GMT  
		Size: 48.0 MB (48004052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5a6bb76bb1504b245ae15291e4e97e6ab464eaaf1405a24fad1823835422e`  
		Last Modified: Fri, 08 Aug 2025 00:11:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8792e39739497fbe4d0b7cccaa1b40466b937fc2f494fc925c1fa150fff94e8`  
		Last Modified: Fri, 08 Aug 2025 00:41:44 GMT  
		Size: 167.2 MB (167236264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a43a0d58dcd1f55d4c552dca62d95bbb328aa78db2439c4ddd524af84d7b99`  
		Last Modified: Fri, 08 Aug 2025 00:11:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:71f38ecaca1f5dea5ab8744d20107cb055a89622644134883b58f45b3d746371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dbf685b382fec4591c12109859a6490b484a08d31e8986df7dd55090b1356f`

```dockerfile
```

-	Layers:
	-	`sha256:9bc92f7f413104f0ad73673607eb4d4e8e1ba1b26cbe96138a63e4a22274b27e`  
		Last Modified: Fri, 08 Aug 2025 03:03:14 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcc3e4d2b4bd513c9a32e1986fe1364bfdb3093db6579dc7f1c826a227e6c17`  
		Last Modified: Fri, 08 Aug 2025 03:03:15 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:4ff17910bdff29a899a4cc5c95ff524f505e10dba5e1f6d4b7bcf6c4c786bf4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e85dc53b71c49afff2047f3ed2dd4ae454da462fcc3e523754e48e36aadd4e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275520924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5440daffa8102faf89239bc524701d914edc0f9cda329988d0c2239dcb356e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5138e880171452ecd094232cf3b75cc38ed7daab3d9cd6823e64fa02cc9c16`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b534c7c08c954e78178326e62146b3b4f6a3d89ce0d8d5bdbe079b63d2ed272e`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5525b1bd2d5dcdbce6b38a73246ae8e96161dee8be7e74d31287f04e4742e844`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9effc86d91a32525dd087d29d09f4eabcb1a2529dc49381c76949ea45fb94533`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bcea418c7c4be37981e06590947286f7c2242c18964d7db55a0e86e3a93e99`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3e1c37f699bde5a65af6ac76020310518d3e8daa0a722ae88e2c265ea3693c`  
		Last Modified: Thu, 21 Aug 2025 19:10:48 GMT  
		Size: 49.3 MB (49267213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e3c68e682cc1833bd8a3f99d0142a0a07798745b86d5dba5bae4f152a800dd`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50786f9db9d5db01fdb3e560fe3e49210288ff986151837b6725692f6e13e274`  
		Last Modified: Thu, 21 Aug 2025 19:16:19 GMT  
		Size: 168.9 MB (168945526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea0fa0ace0c37874b18e97a0b9d3cc46314883f4d9f85725b2406c36b9e1f04`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6b97f0aeb85fffeea7f7d87054342e79b38cd334404dcb73807f83074eefb5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ad5312b51e6bb51743da931219a15467020e36950acf86796a7ad9a1e94196`

```dockerfile
```

-	Layers:
	-	`sha256:aa95e3138f21c9e045be692cc25ed60a4c43b97a87f35c443382ac4b5033db9f`  
		Last Modified: Thu, 21 Aug 2025 21:02:45 GMT  
		Size: 17.7 MB (17699289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604195bff17b4e5bd960ec49bbae21286f66089408833e1b3086ca7d41cd761b`  
		Last Modified: Thu, 21 Aug 2025 21:02:47 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8920eb635c2d5fd9cc83cb365632a64a8032286648395955701f76d566f7639a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270696808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7d52b6f8f700b14c8a5f3b5902e3f2fcc8dc3cf210c33348994d8ce62ddbc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aab55028fec17a260a2e6bce865fe3567b6c3398d227e78a4e1be5d1e469686`  
		Last Modified: Fri, 08 Aug 2025 00:11:51 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e4b6b957309d2e916ad9f42dd2408662062b35c9a35666d631a5f9116e1e2`  
		Last Modified: Fri, 08 Aug 2025 00:41:36 GMT  
		Size: 48.0 MB (48004052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5a6bb76bb1504b245ae15291e4e97e6ab464eaaf1405a24fad1823835422e`  
		Last Modified: Fri, 08 Aug 2025 00:11:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8792e39739497fbe4d0b7cccaa1b40466b937fc2f494fc925c1fa150fff94e8`  
		Last Modified: Fri, 08 Aug 2025 00:41:44 GMT  
		Size: 167.2 MB (167236264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a43a0d58dcd1f55d4c552dca62d95bbb328aa78db2439c4ddd524af84d7b99`  
		Last Modified: Fri, 08 Aug 2025 00:11:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:71f38ecaca1f5dea5ab8744d20107cb055a89622644134883b58f45b3d746371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dbf685b382fec4591c12109859a6490b484a08d31e8986df7dd55090b1356f`

```dockerfile
```

-	Layers:
	-	`sha256:9bc92f7f413104f0ad73673607eb4d4e8e1ba1b26cbe96138a63e4a22274b27e`  
		Last Modified: Fri, 08 Aug 2025 03:03:14 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcc3e4d2b4bd513c9a32e1986fe1364bfdb3093db6579dc7f1c826a227e6c17`  
		Last Modified: Fri, 08 Aug 2025 03:03:15 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:4ff17910bdff29a899a4cc5c95ff524f505e10dba5e1f6d4b7bcf6c4c786bf4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:e85dc53b71c49afff2047f3ed2dd4ae454da462fcc3e523754e48e36aadd4e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275520924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5440daffa8102faf89239bc524701d914edc0f9cda329988d0c2239dcb356e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5138e880171452ecd094232cf3b75cc38ed7daab3d9cd6823e64fa02cc9c16`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b534c7c08c954e78178326e62146b3b4f6a3d89ce0d8d5bdbe079b63d2ed272e`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5525b1bd2d5dcdbce6b38a73246ae8e96161dee8be7e74d31287f04e4742e844`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9effc86d91a32525dd087d29d09f4eabcb1a2529dc49381c76949ea45fb94533`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bcea418c7c4be37981e06590947286f7c2242c18964d7db55a0e86e3a93e99`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3e1c37f699bde5a65af6ac76020310518d3e8daa0a722ae88e2c265ea3693c`  
		Last Modified: Thu, 21 Aug 2025 19:10:48 GMT  
		Size: 49.3 MB (49267213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e3c68e682cc1833bd8a3f99d0142a0a07798745b86d5dba5bae4f152a800dd`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50786f9db9d5db01fdb3e560fe3e49210288ff986151837b6725692f6e13e274`  
		Last Modified: Thu, 21 Aug 2025 19:16:19 GMT  
		Size: 168.9 MB (168945526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea0fa0ace0c37874b18e97a0b9d3cc46314883f4d9f85725b2406c36b9e1f04`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:6b97f0aeb85fffeea7f7d87054342e79b38cd334404dcb73807f83074eefb5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ad5312b51e6bb51743da931219a15467020e36950acf86796a7ad9a1e94196`

```dockerfile
```

-	Layers:
	-	`sha256:aa95e3138f21c9e045be692cc25ed60a4c43b97a87f35c443382ac4b5033db9f`  
		Last Modified: Thu, 21 Aug 2025 21:02:45 GMT  
		Size: 17.7 MB (17699289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604195bff17b4e5bd960ec49bbae21286f66089408833e1b3086ca7d41cd761b`  
		Last Modified: Thu, 21 Aug 2025 21:02:47 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8920eb635c2d5fd9cc83cb365632a64a8032286648395955701f76d566f7639a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270696808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7d52b6f8f700b14c8a5f3b5902e3f2fcc8dc3cf210c33348994d8ce62ddbc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aab55028fec17a260a2e6bce865fe3567b6c3398d227e78a4e1be5d1e469686`  
		Last Modified: Fri, 08 Aug 2025 00:11:51 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e4b6b957309d2e916ad9f42dd2408662062b35c9a35666d631a5f9116e1e2`  
		Last Modified: Fri, 08 Aug 2025 00:41:36 GMT  
		Size: 48.0 MB (48004052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5a6bb76bb1504b245ae15291e4e97e6ab464eaaf1405a24fad1823835422e`  
		Last Modified: Fri, 08 Aug 2025 00:11:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8792e39739497fbe4d0b7cccaa1b40466b937fc2f494fc925c1fa150fff94e8`  
		Last Modified: Fri, 08 Aug 2025 00:41:44 GMT  
		Size: 167.2 MB (167236264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a43a0d58dcd1f55d4c552dca62d95bbb328aa78db2439c4ddd524af84d7b99`  
		Last Modified: Fri, 08 Aug 2025 00:11:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:71f38ecaca1f5dea5ab8744d20107cb055a89622644134883b58f45b3d746371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dbf685b382fec4591c12109859a6490b484a08d31e8986df7dd55090b1356f`

```dockerfile
```

-	Layers:
	-	`sha256:9bc92f7f413104f0ad73673607eb4d4e8e1ba1b26cbe96138a63e4a22274b27e`  
		Last Modified: Fri, 08 Aug 2025 03:03:14 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcc3e4d2b4bd513c9a32e1986fe1364bfdb3093db6579dc7f1c826a227e6c17`  
		Last Modified: Fri, 08 Aug 2025 03:03:15 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:432966f3bdcbf834ef578226e4c196fab460f0727daa888b039854b5c185e8b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:5144a476c89ccd10123ed8a67754cecf50a3c3d32e7ec2e5b5e48c588e07c7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (237016226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f1b9da918eec3e2bd327cc44936b97a15d8705396efe23dfa4198656330dbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd66ec68b64f7f87b2a021e220dc67f8b4e1b902e33a79a92f58410f071efff6`  
		Last Modified: Thu, 21 Aug 2025 19:10:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df938959d2c414e200f0b9c573a1aee4c04e117929223e23508d8107ce1f92f0`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 983.0 KB (983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9348ee598b89aee26c72bb0ad652e10cc5e914f36d503492f0f5ab0252992b5`  
		Last Modified: Thu, 21 Aug 2025 19:10:09 GMT  
		Size: 6.8 MB (6818646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ff5eaaa3b2925ba1855ca2372101208fad8d49d7b82c630c5a5f9cbee5e1f`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d504a2807609c4e00c08619d2328929116183206e0cbefe142587a3db106c473`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbc662f10805e2e50d549d3af79d72079ab6f0c4e455a2692dd582d7c49dbe0`  
		Last Modified: Thu, 21 Aug 2025 19:10:12 GMT  
		Size: 47.8 MB (47767188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a933af802302536755646015b767e3c6513698ebf1ed3fc43966c7ec2aeb5d`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14223e8296d1b6d374cd7bfb5df152d3a272c55c48abbe53f12c1ee03c3ed517`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 131.9 MB (131940894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f9674f6b0df251b150ce3b812e83f53875328c1ec1501ec120e5a1b075e910`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:10abbc9aa70f9d12955b056a95912a42465e0a9ebd1243312fc69f24169b1a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b390d665638f7510c5c3c2971248fce249da79262921d5112b9a212434e106a`

```dockerfile
```

-	Layers:
	-	`sha256:cc2b22161c710488c7c85339e0d6e4983fd006586875ac2939cb23e3d36ad355`  
		Last Modified: Thu, 21 Aug 2025 21:02:20 GMT  
		Size: 14.8 MB (14804922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca3af286439898090aafbd2c70aa31da70701b3054681f22d90796f1fc6a505`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dc80dc8fb761af4c489607085ab973bfb5b286e554259fb0c1aa3570a37ee782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232452065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e2df3d226bacc2aae919ea834a0cc467836f51ee75a4a77a6e4318b6c28cd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc39bf601a8f38d3a3f8386fff1821a460baef80efd721aa299dad351d4835f`  
		Last Modified: Thu, 07 Aug 2025 23:57:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef658516113bc95ec87c99c1b2d4b9d336afe851893f9bfbb1d4945529e459b`  
		Last Modified: Fri, 08 Aug 2025 01:46:58 GMT  
		Size: 46.7 MB (46653469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd4c1e6baf03c096209eae8ddfd7414900ff578117fb867bf73d756bd7bd1fb`  
		Last Modified: Thu, 07 Aug 2025 23:57:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5688f8e7baa3ad3488ea7f0689a918efea096803d9caadc5714bf71ef1b36f36`  
		Last Modified: Fri, 08 Aug 2025 01:47:07 GMT  
		Size: 130.3 MB (130342114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c46015e74a3cb49be59fb76e2bced8cf5ddd337f1531307d0af78fb050e8ee`  
		Last Modified: Thu, 07 Aug 2025 23:57:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:a6e2a4424a2fdf5da85a5657e13df2e6d1990a199f94c21eb9bd6355d8fd0d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e01fa3bb50c6a0a4c4f259afd8355bc12963f461947fd9498aa39810efbb88`

```dockerfile
```

-	Layers:
	-	`sha256:6f92339c56022c949bbc1f028fe64c8252db1ed85a94e98d721e0945f4a08f65`  
		Last Modified: Fri, 08 Aug 2025 03:02:40 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0374db211c0cda7d4f3d824a08c11a1412692c328cf4700b1684c2307b2445d0`  
		Last Modified: Fri, 08 Aug 2025 03:02:41 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:432966f3bdcbf834ef578226e4c196fab460f0727daa888b039854b5c185e8b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5144a476c89ccd10123ed8a67754cecf50a3c3d32e7ec2e5b5e48c588e07c7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (237016226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f1b9da918eec3e2bd327cc44936b97a15d8705396efe23dfa4198656330dbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd66ec68b64f7f87b2a021e220dc67f8b4e1b902e33a79a92f58410f071efff6`  
		Last Modified: Thu, 21 Aug 2025 19:10:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df938959d2c414e200f0b9c573a1aee4c04e117929223e23508d8107ce1f92f0`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 983.0 KB (983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9348ee598b89aee26c72bb0ad652e10cc5e914f36d503492f0f5ab0252992b5`  
		Last Modified: Thu, 21 Aug 2025 19:10:09 GMT  
		Size: 6.8 MB (6818646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ff5eaaa3b2925ba1855ca2372101208fad8d49d7b82c630c5a5f9cbee5e1f`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d504a2807609c4e00c08619d2328929116183206e0cbefe142587a3db106c473`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbc662f10805e2e50d549d3af79d72079ab6f0c4e455a2692dd582d7c49dbe0`  
		Last Modified: Thu, 21 Aug 2025 19:10:12 GMT  
		Size: 47.8 MB (47767188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a933af802302536755646015b767e3c6513698ebf1ed3fc43966c7ec2aeb5d`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14223e8296d1b6d374cd7bfb5df152d3a272c55c48abbe53f12c1ee03c3ed517`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 131.9 MB (131940894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f9674f6b0df251b150ce3b812e83f53875328c1ec1501ec120e5a1b075e910`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:10abbc9aa70f9d12955b056a95912a42465e0a9ebd1243312fc69f24169b1a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b390d665638f7510c5c3c2971248fce249da79262921d5112b9a212434e106a`

```dockerfile
```

-	Layers:
	-	`sha256:cc2b22161c710488c7c85339e0d6e4983fd006586875ac2939cb23e3d36ad355`  
		Last Modified: Thu, 21 Aug 2025 21:02:20 GMT  
		Size: 14.8 MB (14804922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca3af286439898090aafbd2c70aa31da70701b3054681f22d90796f1fc6a505`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dc80dc8fb761af4c489607085ab973bfb5b286e554259fb0c1aa3570a37ee782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232452065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e2df3d226bacc2aae919ea834a0cc467836f51ee75a4a77a6e4318b6c28cd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc39bf601a8f38d3a3f8386fff1821a460baef80efd721aa299dad351d4835f`  
		Last Modified: Thu, 07 Aug 2025 23:57:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef658516113bc95ec87c99c1b2d4b9d336afe851893f9bfbb1d4945529e459b`  
		Last Modified: Fri, 08 Aug 2025 01:46:58 GMT  
		Size: 46.7 MB (46653469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd4c1e6baf03c096209eae8ddfd7414900ff578117fb867bf73d756bd7bd1fb`  
		Last Modified: Thu, 07 Aug 2025 23:57:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5688f8e7baa3ad3488ea7f0689a918efea096803d9caadc5714bf71ef1b36f36`  
		Last Modified: Fri, 08 Aug 2025 01:47:07 GMT  
		Size: 130.3 MB (130342114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c46015e74a3cb49be59fb76e2bced8cf5ddd337f1531307d0af78fb050e8ee`  
		Last Modified: Thu, 07 Aug 2025 23:57:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a6e2a4424a2fdf5da85a5657e13df2e6d1990a199f94c21eb9bd6355d8fd0d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e01fa3bb50c6a0a4c4f259afd8355bc12963f461947fd9498aa39810efbb88`

```dockerfile
```

-	Layers:
	-	`sha256:6f92339c56022c949bbc1f028fe64c8252db1ed85a94e98d721e0945f4a08f65`  
		Last Modified: Fri, 08 Aug 2025 03:02:40 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0374db211c0cda7d4f3d824a08c11a1412692c328cf4700b1684c2307b2445d0`  
		Last Modified: Fri, 08 Aug 2025 03:02:41 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:432966f3bdcbf834ef578226e4c196fab460f0727daa888b039854b5c185e8b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5144a476c89ccd10123ed8a67754cecf50a3c3d32e7ec2e5b5e48c588e07c7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (237016226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f1b9da918eec3e2bd327cc44936b97a15d8705396efe23dfa4198656330dbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd66ec68b64f7f87b2a021e220dc67f8b4e1b902e33a79a92f58410f071efff6`  
		Last Modified: Thu, 21 Aug 2025 19:10:07 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df938959d2c414e200f0b9c573a1aee4c04e117929223e23508d8107ce1f92f0`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 983.0 KB (983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9348ee598b89aee26c72bb0ad652e10cc5e914f36d503492f0f5ab0252992b5`  
		Last Modified: Thu, 21 Aug 2025 19:10:09 GMT  
		Size: 6.8 MB (6818646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ff5eaaa3b2925ba1855ca2372101208fad8d49d7b82c630c5a5f9cbee5e1f`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d504a2807609c4e00c08619d2328929116183206e0cbefe142587a3db106c473`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbc662f10805e2e50d549d3af79d72079ab6f0c4e455a2692dd582d7c49dbe0`  
		Last Modified: Thu, 21 Aug 2025 19:10:12 GMT  
		Size: 47.8 MB (47767188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a933af802302536755646015b767e3c6513698ebf1ed3fc43966c7ec2aeb5d`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14223e8296d1b6d374cd7bfb5df152d3a272c55c48abbe53f12c1ee03c3ed517`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 131.9 MB (131940894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f9674f6b0df251b150ce3b812e83f53875328c1ec1501ec120e5a1b075e910`  
		Last Modified: Thu, 21 Aug 2025 19:10:08 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:10abbc9aa70f9d12955b056a95912a42465e0a9ebd1243312fc69f24169b1a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b390d665638f7510c5c3c2971248fce249da79262921d5112b9a212434e106a`

```dockerfile
```

-	Layers:
	-	`sha256:cc2b22161c710488c7c85339e0d6e4983fd006586875ac2939cb23e3d36ad355`  
		Last Modified: Thu, 21 Aug 2025 21:02:20 GMT  
		Size: 14.8 MB (14804922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca3af286439898090aafbd2c70aa31da70701b3054681f22d90796f1fc6a505`  
		Last Modified: Thu, 21 Aug 2025 21:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dc80dc8fb761af4c489607085ab973bfb5b286e554259fb0c1aa3570a37ee782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232452065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e2df3d226bacc2aae919ea834a0cc467836f51ee75a4a77a6e4318b6c28cd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc39bf601a8f38d3a3f8386fff1821a460baef80efd721aa299dad351d4835f`  
		Last Modified: Thu, 07 Aug 2025 23:57:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef658516113bc95ec87c99c1b2d4b9d336afe851893f9bfbb1d4945529e459b`  
		Last Modified: Fri, 08 Aug 2025 01:46:58 GMT  
		Size: 46.7 MB (46653469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd4c1e6baf03c096209eae8ddfd7414900ff578117fb867bf73d756bd7bd1fb`  
		Last Modified: Thu, 07 Aug 2025 23:57:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5688f8e7baa3ad3488ea7f0689a918efea096803d9caadc5714bf71ef1b36f36`  
		Last Modified: Fri, 08 Aug 2025 01:47:07 GMT  
		Size: 130.3 MB (130342114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c46015e74a3cb49be59fb76e2bced8cf5ddd337f1531307d0af78fb050e8ee`  
		Last Modified: Thu, 07 Aug 2025 23:57:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a6e2a4424a2fdf5da85a5657e13df2e6d1990a199f94c21eb9bd6355d8fd0d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e01fa3bb50c6a0a4c4f259afd8355bc12963f461947fd9498aa39810efbb88`

```dockerfile
```

-	Layers:
	-	`sha256:6f92339c56022c949bbc1f028fe64c8252db1ed85a94e98d721e0945f4a08f65`  
		Last Modified: Fri, 08 Aug 2025 03:02:40 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0374db211c0cda7d4f3d824a08c11a1412692c328cf4700b1684c2307b2445d0`  
		Last Modified: Fri, 08 Aug 2025 03:02:41 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:4ff17910bdff29a899a4cc5c95ff524f505e10dba5e1f6d4b7bcf6c4c786bf4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e85dc53b71c49afff2047f3ed2dd4ae454da462fcc3e523754e48e36aadd4e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275520924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5440daffa8102faf89239bc524701d914edc0f9cda329988d0c2239dcb356e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5138e880171452ecd094232cf3b75cc38ed7daab3d9cd6823e64fa02cc9c16`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b534c7c08c954e78178326e62146b3b4f6a3d89ce0d8d5bdbe079b63d2ed272e`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5525b1bd2d5dcdbce6b38a73246ae8e96161dee8be7e74d31287f04e4742e844`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9effc86d91a32525dd087d29d09f4eabcb1a2529dc49381c76949ea45fb94533`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bcea418c7c4be37981e06590947286f7c2242c18964d7db55a0e86e3a93e99`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3e1c37f699bde5a65af6ac76020310518d3e8daa0a722ae88e2c265ea3693c`  
		Last Modified: Thu, 21 Aug 2025 19:10:48 GMT  
		Size: 49.3 MB (49267213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e3c68e682cc1833bd8a3f99d0142a0a07798745b86d5dba5bae4f152a800dd`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50786f9db9d5db01fdb3e560fe3e49210288ff986151837b6725692f6e13e274`  
		Last Modified: Thu, 21 Aug 2025 19:16:19 GMT  
		Size: 168.9 MB (168945526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea0fa0ace0c37874b18e97a0b9d3cc46314883f4d9f85725b2406c36b9e1f04`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6b97f0aeb85fffeea7f7d87054342e79b38cd334404dcb73807f83074eefb5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ad5312b51e6bb51743da931219a15467020e36950acf86796a7ad9a1e94196`

```dockerfile
```

-	Layers:
	-	`sha256:aa95e3138f21c9e045be692cc25ed60a4c43b97a87f35c443382ac4b5033db9f`  
		Last Modified: Thu, 21 Aug 2025 21:02:45 GMT  
		Size: 17.7 MB (17699289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604195bff17b4e5bd960ec49bbae21286f66089408833e1b3086ca7d41cd761b`  
		Last Modified: Thu, 21 Aug 2025 21:02:47 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8920eb635c2d5fd9cc83cb365632a64a8032286648395955701f76d566f7639a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270696808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7d52b6f8f700b14c8a5f3b5902e3f2fcc8dc3cf210c33348994d8ce62ddbc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aab55028fec17a260a2e6bce865fe3567b6c3398d227e78a4e1be5d1e469686`  
		Last Modified: Fri, 08 Aug 2025 00:11:51 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e4b6b957309d2e916ad9f42dd2408662062b35c9a35666d631a5f9116e1e2`  
		Last Modified: Fri, 08 Aug 2025 00:41:36 GMT  
		Size: 48.0 MB (48004052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5a6bb76bb1504b245ae15291e4e97e6ab464eaaf1405a24fad1823835422e`  
		Last Modified: Fri, 08 Aug 2025 00:11:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8792e39739497fbe4d0b7cccaa1b40466b937fc2f494fc925c1fa150fff94e8`  
		Last Modified: Fri, 08 Aug 2025 00:41:44 GMT  
		Size: 167.2 MB (167236264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a43a0d58dcd1f55d4c552dca62d95bbb328aa78db2439c4ddd524af84d7b99`  
		Last Modified: Fri, 08 Aug 2025 00:11:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:71f38ecaca1f5dea5ab8744d20107cb055a89622644134883b58f45b3d746371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dbf685b382fec4591c12109859a6490b484a08d31e8986df7dd55090b1356f`

```dockerfile
```

-	Layers:
	-	`sha256:9bc92f7f413104f0ad73673607eb4d4e8e1ba1b26cbe96138a63e4a22274b27e`  
		Last Modified: Fri, 08 Aug 2025 03:03:14 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcc3e4d2b4bd513c9a32e1986fe1364bfdb3093db6579dc7f1c826a227e6c17`  
		Last Modified: Fri, 08 Aug 2025 03:03:15 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:4ff17910bdff29a899a4cc5c95ff524f505e10dba5e1f6d4b7bcf6c4c786bf4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e85dc53b71c49afff2047f3ed2dd4ae454da462fcc3e523754e48e36aadd4e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275520924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5440daffa8102faf89239bc524701d914edc0f9cda329988d0c2239dcb356e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5138e880171452ecd094232cf3b75cc38ed7daab3d9cd6823e64fa02cc9c16`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b534c7c08c954e78178326e62146b3b4f6a3d89ce0d8d5bdbe079b63d2ed272e`  
		Last Modified: Thu, 21 Aug 2025 19:10:47 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5525b1bd2d5dcdbce6b38a73246ae8e96161dee8be7e74d31287f04e4742e844`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 6.8 MB (6818681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9effc86d91a32525dd087d29d09f4eabcb1a2529dc49381c76949ea45fb94533`  
		Last Modified: Thu, 21 Aug 2025 19:10:43 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bcea418c7c4be37981e06590947286f7c2242c18964d7db55a0e86e3a93e99`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3e1c37f699bde5a65af6ac76020310518d3e8daa0a722ae88e2c265ea3693c`  
		Last Modified: Thu, 21 Aug 2025 19:10:48 GMT  
		Size: 49.3 MB (49267213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e3c68e682cc1833bd8a3f99d0142a0a07798745b86d5dba5bae4f152a800dd`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50786f9db9d5db01fdb3e560fe3e49210288ff986151837b6725692f6e13e274`  
		Last Modified: Thu, 21 Aug 2025 19:16:19 GMT  
		Size: 168.9 MB (168945526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea0fa0ace0c37874b18e97a0b9d3cc46314883f4d9f85725b2406c36b9e1f04`  
		Last Modified: Thu, 21 Aug 2025 19:10:44 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6b97f0aeb85fffeea7f7d87054342e79b38cd334404dcb73807f83074eefb5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ad5312b51e6bb51743da931219a15467020e36950acf86796a7ad9a1e94196`

```dockerfile
```

-	Layers:
	-	`sha256:aa95e3138f21c9e045be692cc25ed60a4c43b97a87f35c443382ac4b5033db9f`  
		Last Modified: Thu, 21 Aug 2025 21:02:45 GMT  
		Size: 17.7 MB (17699289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604195bff17b4e5bd960ec49bbae21286f66089408833e1b3086ca7d41cd761b`  
		Last Modified: Thu, 21 Aug 2025 21:02:47 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8920eb635c2d5fd9cc83cb365632a64a8032286648395955701f76d566f7639a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270696808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7d52b6f8f700b14c8a5f3b5902e3f2fcc8dc3cf210c33348994d8ce62ddbc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aab55028fec17a260a2e6bce865fe3567b6c3398d227e78a4e1be5d1e469686`  
		Last Modified: Fri, 08 Aug 2025 00:11:51 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e4b6b957309d2e916ad9f42dd2408662062b35c9a35666d631a5f9116e1e2`  
		Last Modified: Fri, 08 Aug 2025 00:41:36 GMT  
		Size: 48.0 MB (48004052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5a6bb76bb1504b245ae15291e4e97e6ab464eaaf1405a24fad1823835422e`  
		Last Modified: Fri, 08 Aug 2025 00:11:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8792e39739497fbe4d0b7cccaa1b40466b937fc2f494fc925c1fa150fff94e8`  
		Last Modified: Fri, 08 Aug 2025 00:41:44 GMT  
		Size: 167.2 MB (167236264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a43a0d58dcd1f55d4c552dca62d95bbb328aa78db2439c4ddd524af84d7b99`  
		Last Modified: Fri, 08 Aug 2025 00:11:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:71f38ecaca1f5dea5ab8744d20107cb055a89622644134883b58f45b3d746371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dbf685b382fec4591c12109859a6490b484a08d31e8986df7dd55090b1356f`

```dockerfile
```

-	Layers:
	-	`sha256:9bc92f7f413104f0ad73673607eb4d4e8e1ba1b26cbe96138a63e4a22274b27e`  
		Last Modified: Fri, 08 Aug 2025 03:03:14 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcc3e4d2b4bd513c9a32e1986fe1364bfdb3093db6579dc7f1c826a227e6c17`  
		Last Modified: Fri, 08 Aug 2025 03:03:15 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json
