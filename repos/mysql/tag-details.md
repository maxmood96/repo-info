<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:8`](#mysql8)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8-oraclelinux8`](#mysql8-oraclelinux8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-bookworm`](#mysql80-bookworm)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0-oraclelinux8`](#mysql80-oraclelinux8)
-	[`mysql:8.0.36`](#mysql8036)
-	[`mysql:8.0.36-bookworm`](#mysql8036-bookworm)
-	[`mysql:8.0.36-debian`](#mysql8036-debian)
-	[`mysql:8.0.36-oracle`](#mysql8036-oracle)
-	[`mysql:8.0.36-oraclelinux8`](#mysql8036-oraclelinux8)
-	[`mysql:8.3`](#mysql83)
-	[`mysql:8.3-oracle`](#mysql83-oracle)
-	[`mysql:8.3-oraclelinux8`](#mysql83-oraclelinux8)
-	[`mysql:8.3.0`](#mysql830)
-	[`mysql:8.3.0-oracle`](#mysql830-oracle)
-	[`mysql:8.3.0-oraclelinux8`](#mysql830-oraclelinux8)
-	[`mysql:innovation`](#mysqlinnovation)
-	[`mysql:innovation-oracle`](#mysqlinnovation-oracle)
-	[`mysql:innovation-oraclelinux8`](#mysqlinnovation-oraclelinux8)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:oracle`](#mysqloracle)
-	[`mysql:oraclelinux8`](#mysqloraclelinux8)

## `mysql:8`

```console
$ docker pull mysql@sha256:0f2e15fb8b47db2518b1428239ed3e3fe6a6693401b2cf19552063562cfc2fc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:076e3b41dfa9b184815b1239e37dd709bfddfdbf0e425eebb17c740705815b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183369525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f3f983cb088300e9fe51eb4d855c4c353f7afae9f035e9553148cfeb665e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1a4da808dd02e76718ff6f7ac40eb217687bd0fcd253d88238a39da21dc5f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3292fb4adf41458b3405e4fab39ac956e9b0f416e99d47965f29da3b5d9e69aa`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3811c45068ccd835ac871817eea43ac59bfe8495799508c3a2b14892d9a5293e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 4.6 MB (4592408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13320244c05a40c7dbd1a258b070d485426553b22eeba4859320d8d3908f327`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a34d702f2813fc3cf78dabf8d762fe3af066b682a2a968e6ffcfef9482588d4`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de90f448147740b877cd5a67ad605595d4cdea350ee3d1eee6ab9a09062f42b6`  
		Last Modified: Fri, 05 Apr 2024 18:52:46 GMT  
		Size: 63.1 MB (63081353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575200ae3755746a3740ff1224a9cabd56187b00a76f67a02b02d8ec2a8fc48`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea400be5707154f3b61c33ae937ff92fd75991ee6e4aa90a1aef9d83ba3087b`  
		Last Modified: Fri, 05 Apr 2024 18:52:47 GMT  
		Size: 63.4 MB (63385317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c930606a4f11cfa2329527166ba39c9ae607166fe9ea129f7f501c2a765d4a`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:afd54f6d52e541184ddd0522cea94c724320401234036637dd404ff594148530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc4a54be9d6a9e12e4eadfabaa3a5f1883f5ef666d7f24bf99bdacbd865c88`

```dockerfile
```

-	Layers:
	-	`sha256:3e4e8176a1027fd661e2e4f9aff7fc92493e62a67ed841753acc7f58269314f0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 14.3 MB (14251350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ca62fef5598e17a59bbdeeefdbf07fc28ad9834f1daffdbbd3c44a0ae8f8f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 35.3 KB (35253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:83d25ba05253e3b89e5fd85f9a66b7a7d9f1e89292895bf8b567cffbe6650942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181397527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6757ec48c5aed83bb14cfd0c24a34cdf2ca2597180159ebd3c7daf73dd7333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c48356cf7d6537dfe73a9a67bdb4c3c67a94fa8e1d9ba69d6e8fe6541bb3`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada74d40ba8731fad59fba17d8484ffb304270e6ded18761b6d4d96075117a66`  
		Last Modified: Fri, 05 Apr 2024 19:08:07 GMT  
		Size: 62.1 MB (62054534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7b27488bbeff273c6739f2e5c81234ff7de38b4b222cf1a1e83e0d424a1f27`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c89304473a0e288d42d8e9abd6448096f4481ef1b031f301ce81fe07a85cd37`  
		Last Modified: Fri, 05 Apr 2024 19:08:08 GMT  
		Size: 64.0 MB (64033838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be02980a71934f1f891ec7d50e9cbc507195cdfac6c41c041b9b8fc9bed14d1`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:7d2e413e81e1bf2fe47f80e4edd77b489a70f1a2fc71f40a35b1ba491c25eb6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1a155253ffcc40532a6b7c1a12fea4acac2c83c31cb89a12f4602c982699c4`

```dockerfile
```

-	Layers:
	-	`sha256:fedac3a3dba1e088509f54630da5c8a543c6af3a936e5a4197a991265262b645`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 14.2 MB (14249630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fccee5b98ccd310e92f31122c54cf83ff9ad788ff001cfb18f994fe3a48fedd1`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:0f2e15fb8b47db2518b1428239ed3e3fe6a6693401b2cf19552063562cfc2fc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:076e3b41dfa9b184815b1239e37dd709bfddfdbf0e425eebb17c740705815b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183369525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f3f983cb088300e9fe51eb4d855c4c353f7afae9f035e9553148cfeb665e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1a4da808dd02e76718ff6f7ac40eb217687bd0fcd253d88238a39da21dc5f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3292fb4adf41458b3405e4fab39ac956e9b0f416e99d47965f29da3b5d9e69aa`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3811c45068ccd835ac871817eea43ac59bfe8495799508c3a2b14892d9a5293e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 4.6 MB (4592408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13320244c05a40c7dbd1a258b070d485426553b22eeba4859320d8d3908f327`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a34d702f2813fc3cf78dabf8d762fe3af066b682a2a968e6ffcfef9482588d4`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de90f448147740b877cd5a67ad605595d4cdea350ee3d1eee6ab9a09062f42b6`  
		Last Modified: Fri, 05 Apr 2024 18:52:46 GMT  
		Size: 63.1 MB (63081353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575200ae3755746a3740ff1224a9cabd56187b00a76f67a02b02d8ec2a8fc48`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea400be5707154f3b61c33ae937ff92fd75991ee6e4aa90a1aef9d83ba3087b`  
		Last Modified: Fri, 05 Apr 2024 18:52:47 GMT  
		Size: 63.4 MB (63385317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c930606a4f11cfa2329527166ba39c9ae607166fe9ea129f7f501c2a765d4a`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:afd54f6d52e541184ddd0522cea94c724320401234036637dd404ff594148530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc4a54be9d6a9e12e4eadfabaa3a5f1883f5ef666d7f24bf99bdacbd865c88`

```dockerfile
```

-	Layers:
	-	`sha256:3e4e8176a1027fd661e2e4f9aff7fc92493e62a67ed841753acc7f58269314f0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 14.3 MB (14251350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ca62fef5598e17a59bbdeeefdbf07fc28ad9834f1daffdbbd3c44a0ae8f8f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 35.3 KB (35253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:83d25ba05253e3b89e5fd85f9a66b7a7d9f1e89292895bf8b567cffbe6650942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181397527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6757ec48c5aed83bb14cfd0c24a34cdf2ca2597180159ebd3c7daf73dd7333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c48356cf7d6537dfe73a9a67bdb4c3c67a94fa8e1d9ba69d6e8fe6541bb3`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada74d40ba8731fad59fba17d8484ffb304270e6ded18761b6d4d96075117a66`  
		Last Modified: Fri, 05 Apr 2024 19:08:07 GMT  
		Size: 62.1 MB (62054534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7b27488bbeff273c6739f2e5c81234ff7de38b4b222cf1a1e83e0d424a1f27`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c89304473a0e288d42d8e9abd6448096f4481ef1b031f301ce81fe07a85cd37`  
		Last Modified: Fri, 05 Apr 2024 19:08:08 GMT  
		Size: 64.0 MB (64033838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be02980a71934f1f891ec7d50e9cbc507195cdfac6c41c041b9b8fc9bed14d1`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7d2e413e81e1bf2fe47f80e4edd77b489a70f1a2fc71f40a35b1ba491c25eb6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1a155253ffcc40532a6b7c1a12fea4acac2c83c31cb89a12f4602c982699c4`

```dockerfile
```

-	Layers:
	-	`sha256:fedac3a3dba1e088509f54630da5c8a543c6af3a936e5a4197a991265262b645`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 14.2 MB (14249630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fccee5b98ccd310e92f31122c54cf83ff9ad788ff001cfb18f994fe3a48fedd1`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux8`

```console
$ docker pull mysql@sha256:0f2e15fb8b47db2518b1428239ed3e3fe6a6693401b2cf19552063562cfc2fc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:076e3b41dfa9b184815b1239e37dd709bfddfdbf0e425eebb17c740705815b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183369525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f3f983cb088300e9fe51eb4d855c4c353f7afae9f035e9553148cfeb665e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1a4da808dd02e76718ff6f7ac40eb217687bd0fcd253d88238a39da21dc5f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3292fb4adf41458b3405e4fab39ac956e9b0f416e99d47965f29da3b5d9e69aa`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3811c45068ccd835ac871817eea43ac59bfe8495799508c3a2b14892d9a5293e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 4.6 MB (4592408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13320244c05a40c7dbd1a258b070d485426553b22eeba4859320d8d3908f327`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a34d702f2813fc3cf78dabf8d762fe3af066b682a2a968e6ffcfef9482588d4`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de90f448147740b877cd5a67ad605595d4cdea350ee3d1eee6ab9a09062f42b6`  
		Last Modified: Fri, 05 Apr 2024 18:52:46 GMT  
		Size: 63.1 MB (63081353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575200ae3755746a3740ff1224a9cabd56187b00a76f67a02b02d8ec2a8fc48`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea400be5707154f3b61c33ae937ff92fd75991ee6e4aa90a1aef9d83ba3087b`  
		Last Modified: Fri, 05 Apr 2024 18:52:47 GMT  
		Size: 63.4 MB (63385317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c930606a4f11cfa2329527166ba39c9ae607166fe9ea129f7f501c2a765d4a`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:afd54f6d52e541184ddd0522cea94c724320401234036637dd404ff594148530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc4a54be9d6a9e12e4eadfabaa3a5f1883f5ef666d7f24bf99bdacbd865c88`

```dockerfile
```

-	Layers:
	-	`sha256:3e4e8176a1027fd661e2e4f9aff7fc92493e62a67ed841753acc7f58269314f0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 14.3 MB (14251350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ca62fef5598e17a59bbdeeefdbf07fc28ad9834f1daffdbbd3c44a0ae8f8f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 35.3 KB (35253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:83d25ba05253e3b89e5fd85f9a66b7a7d9f1e89292895bf8b567cffbe6650942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181397527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6757ec48c5aed83bb14cfd0c24a34cdf2ca2597180159ebd3c7daf73dd7333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c48356cf7d6537dfe73a9a67bdb4c3c67a94fa8e1d9ba69d6e8fe6541bb3`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada74d40ba8731fad59fba17d8484ffb304270e6ded18761b6d4d96075117a66`  
		Last Modified: Fri, 05 Apr 2024 19:08:07 GMT  
		Size: 62.1 MB (62054534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7b27488bbeff273c6739f2e5c81234ff7de38b4b222cf1a1e83e0d424a1f27`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c89304473a0e288d42d8e9abd6448096f4481ef1b031f301ce81fe07a85cd37`  
		Last Modified: Fri, 05 Apr 2024 19:08:08 GMT  
		Size: 64.0 MB (64033838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be02980a71934f1f891ec7d50e9cbc507195cdfac6c41c041b9b8fc9bed14d1`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:7d2e413e81e1bf2fe47f80e4edd77b489a70f1a2fc71f40a35b1ba491c25eb6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1a155253ffcc40532a6b7c1a12fea4acac2c83c31cb89a12f4602c982699c4`

```dockerfile
```

-	Layers:
	-	`sha256:fedac3a3dba1e088509f54630da5c8a543c6af3a936e5a4197a991265262b645`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 14.2 MB (14249630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fccee5b98ccd310e92f31122c54cf83ff9ad788ff001cfb18f994fe3a48fedd1`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:ce628295ff5aa269e4d0241e0552476fa0de3af263daedf196ccb6fc0834fa6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:6e444bff4d42bda9f1d6121859c58ee2c6515185849b1654e37345a6eea6a4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174718031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a15556a7dd66cd508ceaa083564bc7dbfbc0469fa587d92b2ec466f25b2d95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64073634efcc472fea7ee7a6cfbc9678807ecb255cd9db8a592211b2680773f9`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca025b52c77767226b123e41cdc082fac3eed53f51e1054075c3966359178cb6`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091a1e5789d410cbc663e77f407e57e3ef0f34e0b5f7eabbd2db5bdeae7201d3`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 4.6 MB (4592421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ab1febf12321f52a634824a7b1c4d4984c3a38f9c8d13714c4cc9c58f33020`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c05e4058de6fd2d75662003e71ef4be64f6cbe047955d25f4f192a0b5a1b3a`  
		Last Modified: Fri, 05 Apr 2024 18:52:43 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c6654d8546ef4e29491058869717a0b404cbb32bc7507713c469fd2104964e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 58.5 MB (58515054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972ceacaa396a23c63ad64dc25a6e6ae565329b5f27ffdd6df1ba01d8f88b2a5`  
		Last Modified: Fri, 05 Apr 2024 18:52:43 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cf75b54f0c97134cd3db85db5896492e33328e6324e082cd5ebaab32107450`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 59.3 MB (59300013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c407b83071d4001190f1de96238348b61559f81d0e37d1522be3f4d79ebb6b0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd699dd4735c2c0963e06c4e0114be1ec20f084acc185a5e81e3d4e31652ff6a`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:eb6b60ce6e817e31300d8716d4586c94d287cd1b96d9dc9f8f419cf0922febbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14283147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bfb26eb39fb012f4c6597115f510eec5321740393c07e302cfe18c40953210`

```dockerfile
```

-	Layers:
	-	`sha256:5359fab16f0c035a2d60383029e54f3df1d25bcc45de3ed813b71be18851b495`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 14.2 MB (14248252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eebe7c21f9fa7365c785348c3ca35c9a4ff3ccbe0a86a09fba6e7d2915ac62a9`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:669bf0ab62ceffd50f8e5a68111ba89e48b376d8ec66baf37cdce042112f3d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178501772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d56cc6c12046b23ea539b9b3e1d3b0f0355fed6652c41d7395653c610f6dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278337e747e9fe1fb2d0f48f5984719bdfabd6c3979e75a610b71b4cdfff0be4`  
		Last Modified: Fri, 05 Apr 2024 19:10:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eaf88539129c994346e7f57dd7cc2f18840977c58c9a385fd1344462579d31`  
		Last Modified: Fri, 05 Apr 2024 19:10:04 GMT  
		Size: 57.6 MB (57595809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a25bfe33e2c4573ec8d4f7c34c75b2f6cd038388a237fd1de9db802691fd36`  
		Last Modified: Fri, 05 Apr 2024 19:10:02 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0154a68c7d2e7bc03e7e8b9a1e9ff32680cbd999569fdb079b66f1b643a5976`  
		Last Modified: Fri, 05 Apr 2024 19:10:04 GMT  
		Size: 65.6 MB (65596699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bdd7b17194c6e971917d9eb8351280b9e546ab70d8a141fe49db3c6831602d`  
		Last Modified: Fri, 05 Apr 2024 19:10:02 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3042f2d5dd040865afa56a70e67ad02d7a9dced3e70401dbce0d6f46367860`  
		Last Modified: Fri, 05 Apr 2024 19:10:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:60b4795edaa62791a65fc2b9760340f9e0143f2b096d389ddf2f9a5447b8d6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14281256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9b4d1bf9ab37b4ee0d3ea2602159465e43daca4e811f2ca613e5c99329b112`

```dockerfile
```

-	Layers:
	-	`sha256:d659ceed129addf03908069fff59e9cc203d328c9ad9cf28e771ecb6ae1d7bcd`  
		Last Modified: Fri, 05 Apr 2024 19:10:02 GMT  
		Size: 14.2 MB (14246514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6943267177494b264e6d697d9073d25dfc2dbc82d8019c24ea87fa654578fc03`  
		Last Modified: Fri, 05 Apr 2024 19:10:01 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:16d4cc0bd9da6f4becc3de398aaf34b96accbd35d039e3922e0721c1b9e06572
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:213ce44455c81e75c643b257c8c889c032047cb1b78c7038eba94710a9eb16e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180828380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c0bd217d592f5c913bb4e8eda3921db943554ccd25db8fd01ee93e68b06b9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1debian12
# Tue, 26 Mar 2024 03:50:44 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855739933c65c8c908e6007663e7b6d55d53e3cb6376cf45df6b85c54bcfff20`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf9690b1837f808bd48ed89713c955a80eba82ececd080aa36df2f6cf60d0bc`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 4.4 MB (4422729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718c8cf9a6d02f8d2c46c809091849da3f8050180802855c1ee42051fcdcefa`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 1.4 MB (1445886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2caee2910c1ee555369371c5a9b4d2b66e1e389f68f31b7c848223ba83e167e`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acea30847068f38b75b2d0efeeedc446df290c605dd21162a8cde4ced9f43ef`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 15.3 MB (15281898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef35ffb4224fb7fd335d5847991b14bdd01628b0fbf33eca17435a59f939313`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6102610fd9d73cf7fb22e291506906aa302e9eb67425fa26ea9cb65f034ad2db`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bddd247177c165c022455fe81cee3a81cace56ba1466e32b4ad6a4d416cf72`  
		Last Modified: Wed, 27 Mar 2024 21:50:15 GMT  
		Size: 130.5 MB (130543565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a018e3f1556086e1e4d59fa9b183292f2a98745378a07045b720a9d085cbddea`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 841.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9421e59b2c9fcbaf696ac0b5c0507de0dcb53e61ce99d18b9091dbf466b68915`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afacd7c4aa583a91dafcc48ea2bd9a3f8ea7ddc85fcc67fe09d3a3d0d34a4a74`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:13244d86e6e07d8bbc2ac7332544ed89d5d3f4dd32c45007b0cd39f7e902b317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c29219d095a8667022ff4cfbc271efa73bc32718e7098ee397a91fb7591f1b`

```dockerfile
```

-	Layers:
	-	`sha256:8078c346d7f7342482b3ed469c68b15266c781f77e8b9d54c75b45e4bb30beaa`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 4.0 MB (3954709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4875492051ca452867fc4569d5b8dc5a2e0e1985097396a1cdbc8f5f854ce9bc`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:16d4cc0bd9da6f4becc3de398aaf34b96accbd35d039e3922e0721c1b9e06572
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:213ce44455c81e75c643b257c8c889c032047cb1b78c7038eba94710a9eb16e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180828380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c0bd217d592f5c913bb4e8eda3921db943554ccd25db8fd01ee93e68b06b9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1debian12
# Tue, 26 Mar 2024 03:50:44 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855739933c65c8c908e6007663e7b6d55d53e3cb6376cf45df6b85c54bcfff20`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf9690b1837f808bd48ed89713c955a80eba82ececd080aa36df2f6cf60d0bc`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 4.4 MB (4422729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718c8cf9a6d02f8d2c46c809091849da3f8050180802855c1ee42051fcdcefa`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 1.4 MB (1445886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2caee2910c1ee555369371c5a9b4d2b66e1e389f68f31b7c848223ba83e167e`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acea30847068f38b75b2d0efeeedc446df290c605dd21162a8cde4ced9f43ef`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 15.3 MB (15281898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef35ffb4224fb7fd335d5847991b14bdd01628b0fbf33eca17435a59f939313`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6102610fd9d73cf7fb22e291506906aa302e9eb67425fa26ea9cb65f034ad2db`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bddd247177c165c022455fe81cee3a81cace56ba1466e32b4ad6a4d416cf72`  
		Last Modified: Wed, 27 Mar 2024 21:50:15 GMT  
		Size: 130.5 MB (130543565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a018e3f1556086e1e4d59fa9b183292f2a98745378a07045b720a9d085cbddea`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 841.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9421e59b2c9fcbaf696ac0b5c0507de0dcb53e61ce99d18b9091dbf466b68915`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afacd7c4aa583a91dafcc48ea2bd9a3f8ea7ddc85fcc67fe09d3a3d0d34a4a74`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:13244d86e6e07d8bbc2ac7332544ed89d5d3f4dd32c45007b0cd39f7e902b317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c29219d095a8667022ff4cfbc271efa73bc32718e7098ee397a91fb7591f1b`

```dockerfile
```

-	Layers:
	-	`sha256:8078c346d7f7342482b3ed469c68b15266c781f77e8b9d54c75b45e4bb30beaa`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 4.0 MB (3954709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4875492051ca452867fc4569d5b8dc5a2e0e1985097396a1cdbc8f5f854ce9bc`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:ce628295ff5aa269e4d0241e0552476fa0de3af263daedf196ccb6fc0834fa6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6e444bff4d42bda9f1d6121859c58ee2c6515185849b1654e37345a6eea6a4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174718031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a15556a7dd66cd508ceaa083564bc7dbfbc0469fa587d92b2ec466f25b2d95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64073634efcc472fea7ee7a6cfbc9678807ecb255cd9db8a592211b2680773f9`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca025b52c77767226b123e41cdc082fac3eed53f51e1054075c3966359178cb6`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091a1e5789d410cbc663e77f407e57e3ef0f34e0b5f7eabbd2db5bdeae7201d3`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 4.6 MB (4592421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ab1febf12321f52a634824a7b1c4d4984c3a38f9c8d13714c4cc9c58f33020`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c05e4058de6fd2d75662003e71ef4be64f6cbe047955d25f4f192a0b5a1b3a`  
		Last Modified: Fri, 05 Apr 2024 18:52:43 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c6654d8546ef4e29491058869717a0b404cbb32bc7507713c469fd2104964e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 58.5 MB (58515054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972ceacaa396a23c63ad64dc25a6e6ae565329b5f27ffdd6df1ba01d8f88b2a5`  
		Last Modified: Fri, 05 Apr 2024 18:52:43 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cf75b54f0c97134cd3db85db5896492e33328e6324e082cd5ebaab32107450`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 59.3 MB (59300013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c407b83071d4001190f1de96238348b61559f81d0e37d1522be3f4d79ebb6b0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd699dd4735c2c0963e06c4e0114be1ec20f084acc185a5e81e3d4e31652ff6a`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:eb6b60ce6e817e31300d8716d4586c94d287cd1b96d9dc9f8f419cf0922febbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14283147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bfb26eb39fb012f4c6597115f510eec5321740393c07e302cfe18c40953210`

```dockerfile
```

-	Layers:
	-	`sha256:5359fab16f0c035a2d60383029e54f3df1d25bcc45de3ed813b71be18851b495`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 14.2 MB (14248252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eebe7c21f9fa7365c785348c3ca35c9a4ff3ccbe0a86a09fba6e7d2915ac62a9`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:669bf0ab62ceffd50f8e5a68111ba89e48b376d8ec66baf37cdce042112f3d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178501772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d56cc6c12046b23ea539b9b3e1d3b0f0355fed6652c41d7395653c610f6dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278337e747e9fe1fb2d0f48f5984719bdfabd6c3979e75a610b71b4cdfff0be4`  
		Last Modified: Fri, 05 Apr 2024 19:10:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eaf88539129c994346e7f57dd7cc2f18840977c58c9a385fd1344462579d31`  
		Last Modified: Fri, 05 Apr 2024 19:10:04 GMT  
		Size: 57.6 MB (57595809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a25bfe33e2c4573ec8d4f7c34c75b2f6cd038388a237fd1de9db802691fd36`  
		Last Modified: Fri, 05 Apr 2024 19:10:02 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0154a68c7d2e7bc03e7e8b9a1e9ff32680cbd999569fdb079b66f1b643a5976`  
		Last Modified: Fri, 05 Apr 2024 19:10:04 GMT  
		Size: 65.6 MB (65596699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bdd7b17194c6e971917d9eb8351280b9e546ab70d8a141fe49db3c6831602d`  
		Last Modified: Fri, 05 Apr 2024 19:10:02 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3042f2d5dd040865afa56a70e67ad02d7a9dced3e70401dbce0d6f46367860`  
		Last Modified: Fri, 05 Apr 2024 19:10:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:60b4795edaa62791a65fc2b9760340f9e0143f2b096d389ddf2f9a5447b8d6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14281256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9b4d1bf9ab37b4ee0d3ea2602159465e43daca4e811f2ca613e5c99329b112`

```dockerfile
```

-	Layers:
	-	`sha256:d659ceed129addf03908069fff59e9cc203d328c9ad9cf28e771ecb6ae1d7bcd`  
		Last Modified: Fri, 05 Apr 2024 19:10:02 GMT  
		Size: 14.2 MB (14246514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6943267177494b264e6d697d9073d25dfc2dbc82d8019c24ea87fa654578fc03`  
		Last Modified: Fri, 05 Apr 2024 19:10:01 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux8`

```console
$ docker pull mysql@sha256:ce628295ff5aa269e4d0241e0552476fa0de3af263daedf196ccb6fc0834fa6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:6e444bff4d42bda9f1d6121859c58ee2c6515185849b1654e37345a6eea6a4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174718031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a15556a7dd66cd508ceaa083564bc7dbfbc0469fa587d92b2ec466f25b2d95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64073634efcc472fea7ee7a6cfbc9678807ecb255cd9db8a592211b2680773f9`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca025b52c77767226b123e41cdc082fac3eed53f51e1054075c3966359178cb6`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091a1e5789d410cbc663e77f407e57e3ef0f34e0b5f7eabbd2db5bdeae7201d3`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 4.6 MB (4592421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ab1febf12321f52a634824a7b1c4d4984c3a38f9c8d13714c4cc9c58f33020`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c05e4058de6fd2d75662003e71ef4be64f6cbe047955d25f4f192a0b5a1b3a`  
		Last Modified: Fri, 05 Apr 2024 18:52:43 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c6654d8546ef4e29491058869717a0b404cbb32bc7507713c469fd2104964e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 58.5 MB (58515054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972ceacaa396a23c63ad64dc25a6e6ae565329b5f27ffdd6df1ba01d8f88b2a5`  
		Last Modified: Fri, 05 Apr 2024 18:52:43 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cf75b54f0c97134cd3db85db5896492e33328e6324e082cd5ebaab32107450`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 59.3 MB (59300013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c407b83071d4001190f1de96238348b61559f81d0e37d1522be3f4d79ebb6b0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd699dd4735c2c0963e06c4e0114be1ec20f084acc185a5e81e3d4e31652ff6a`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:eb6b60ce6e817e31300d8716d4586c94d287cd1b96d9dc9f8f419cf0922febbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14283147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bfb26eb39fb012f4c6597115f510eec5321740393c07e302cfe18c40953210`

```dockerfile
```

-	Layers:
	-	`sha256:5359fab16f0c035a2d60383029e54f3df1d25bcc45de3ed813b71be18851b495`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 14.2 MB (14248252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eebe7c21f9fa7365c785348c3ca35c9a4ff3ccbe0a86a09fba6e7d2915ac62a9`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:669bf0ab62ceffd50f8e5a68111ba89e48b376d8ec66baf37cdce042112f3d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178501772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d56cc6c12046b23ea539b9b3e1d3b0f0355fed6652c41d7395653c610f6dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278337e747e9fe1fb2d0f48f5984719bdfabd6c3979e75a610b71b4cdfff0be4`  
		Last Modified: Fri, 05 Apr 2024 19:10:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eaf88539129c994346e7f57dd7cc2f18840977c58c9a385fd1344462579d31`  
		Last Modified: Fri, 05 Apr 2024 19:10:04 GMT  
		Size: 57.6 MB (57595809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a25bfe33e2c4573ec8d4f7c34c75b2f6cd038388a237fd1de9db802691fd36`  
		Last Modified: Fri, 05 Apr 2024 19:10:02 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0154a68c7d2e7bc03e7e8b9a1e9ff32680cbd999569fdb079b66f1b643a5976`  
		Last Modified: Fri, 05 Apr 2024 19:10:04 GMT  
		Size: 65.6 MB (65596699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bdd7b17194c6e971917d9eb8351280b9e546ab70d8a141fe49db3c6831602d`  
		Last Modified: Fri, 05 Apr 2024 19:10:02 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3042f2d5dd040865afa56a70e67ad02d7a9dced3e70401dbce0d6f46367860`  
		Last Modified: Fri, 05 Apr 2024 19:10:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:60b4795edaa62791a65fc2b9760340f9e0143f2b096d389ddf2f9a5447b8d6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14281256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9b4d1bf9ab37b4ee0d3ea2602159465e43daca4e811f2ca613e5c99329b112`

```dockerfile
```

-	Layers:
	-	`sha256:d659ceed129addf03908069fff59e9cc203d328c9ad9cf28e771ecb6ae1d7bcd`  
		Last Modified: Fri, 05 Apr 2024 19:10:02 GMT  
		Size: 14.2 MB (14246514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6943267177494b264e6d697d9073d25dfc2dbc82d8019c24ea87fa654578fc03`  
		Last Modified: Fri, 05 Apr 2024 19:10:01 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36`

```console
$ docker pull mysql@sha256:ce628295ff5aa269e4d0241e0552476fa0de3af263daedf196ccb6fc0834fa6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.36` - linux; amd64

```console
$ docker pull mysql@sha256:6e444bff4d42bda9f1d6121859c58ee2c6515185849b1654e37345a6eea6a4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174718031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a15556a7dd66cd508ceaa083564bc7dbfbc0469fa587d92b2ec466f25b2d95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64073634efcc472fea7ee7a6cfbc9678807ecb255cd9db8a592211b2680773f9`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca025b52c77767226b123e41cdc082fac3eed53f51e1054075c3966359178cb6`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091a1e5789d410cbc663e77f407e57e3ef0f34e0b5f7eabbd2db5bdeae7201d3`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 4.6 MB (4592421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ab1febf12321f52a634824a7b1c4d4984c3a38f9c8d13714c4cc9c58f33020`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c05e4058de6fd2d75662003e71ef4be64f6cbe047955d25f4f192a0b5a1b3a`  
		Last Modified: Fri, 05 Apr 2024 18:52:43 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c6654d8546ef4e29491058869717a0b404cbb32bc7507713c469fd2104964e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 58.5 MB (58515054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972ceacaa396a23c63ad64dc25a6e6ae565329b5f27ffdd6df1ba01d8f88b2a5`  
		Last Modified: Fri, 05 Apr 2024 18:52:43 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cf75b54f0c97134cd3db85db5896492e33328e6324e082cd5ebaab32107450`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 59.3 MB (59300013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c407b83071d4001190f1de96238348b61559f81d0e37d1522be3f4d79ebb6b0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd699dd4735c2c0963e06c4e0114be1ec20f084acc185a5e81e3d4e31652ff6a`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36` - unknown; unknown

```console
$ docker pull mysql@sha256:eb6b60ce6e817e31300d8716d4586c94d287cd1b96d9dc9f8f419cf0922febbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14283147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bfb26eb39fb012f4c6597115f510eec5321740393c07e302cfe18c40953210`

```dockerfile
```

-	Layers:
	-	`sha256:5359fab16f0c035a2d60383029e54f3df1d25bcc45de3ed813b71be18851b495`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 14.2 MB (14248252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eebe7c21f9fa7365c785348c3ca35c9a4ff3ccbe0a86a09fba6e7d2915ac62a9`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.36` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:669bf0ab62ceffd50f8e5a68111ba89e48b376d8ec66baf37cdce042112f3d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178501772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d56cc6c12046b23ea539b9b3e1d3b0f0355fed6652c41d7395653c610f6dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278337e747e9fe1fb2d0f48f5984719bdfabd6c3979e75a610b71b4cdfff0be4`  
		Last Modified: Fri, 05 Apr 2024 19:10:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eaf88539129c994346e7f57dd7cc2f18840977c58c9a385fd1344462579d31`  
		Last Modified: Fri, 05 Apr 2024 19:10:04 GMT  
		Size: 57.6 MB (57595809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a25bfe33e2c4573ec8d4f7c34c75b2f6cd038388a237fd1de9db802691fd36`  
		Last Modified: Fri, 05 Apr 2024 19:10:02 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0154a68c7d2e7bc03e7e8b9a1e9ff32680cbd999569fdb079b66f1b643a5976`  
		Last Modified: Fri, 05 Apr 2024 19:10:04 GMT  
		Size: 65.6 MB (65596699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bdd7b17194c6e971917d9eb8351280b9e546ab70d8a141fe49db3c6831602d`  
		Last Modified: Fri, 05 Apr 2024 19:10:02 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3042f2d5dd040865afa56a70e67ad02d7a9dced3e70401dbce0d6f46367860`  
		Last Modified: Fri, 05 Apr 2024 19:10:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36` - unknown; unknown

```console
$ docker pull mysql@sha256:60b4795edaa62791a65fc2b9760340f9e0143f2b096d389ddf2f9a5447b8d6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14281256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9b4d1bf9ab37b4ee0d3ea2602159465e43daca4e811f2ca613e5c99329b112`

```dockerfile
```

-	Layers:
	-	`sha256:d659ceed129addf03908069fff59e9cc203d328c9ad9cf28e771ecb6ae1d7bcd`  
		Last Modified: Fri, 05 Apr 2024 19:10:02 GMT  
		Size: 14.2 MB (14246514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6943267177494b264e6d697d9073d25dfc2dbc82d8019c24ea87fa654578fc03`  
		Last Modified: Fri, 05 Apr 2024 19:10:01 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36-bookworm`

```console
$ docker pull mysql@sha256:16d4cc0bd9da6f4becc3de398aaf34b96accbd35d039e3922e0721c1b9e06572
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.36-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:213ce44455c81e75c643b257c8c889c032047cb1b78c7038eba94710a9eb16e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180828380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c0bd217d592f5c913bb4e8eda3921db943554ccd25db8fd01ee93e68b06b9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1debian12
# Tue, 26 Mar 2024 03:50:44 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855739933c65c8c908e6007663e7b6d55d53e3cb6376cf45df6b85c54bcfff20`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf9690b1837f808bd48ed89713c955a80eba82ececd080aa36df2f6cf60d0bc`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 4.4 MB (4422729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718c8cf9a6d02f8d2c46c809091849da3f8050180802855c1ee42051fcdcefa`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 1.4 MB (1445886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2caee2910c1ee555369371c5a9b4d2b66e1e389f68f31b7c848223ba83e167e`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acea30847068f38b75b2d0efeeedc446df290c605dd21162a8cde4ced9f43ef`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 15.3 MB (15281898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef35ffb4224fb7fd335d5847991b14bdd01628b0fbf33eca17435a59f939313`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6102610fd9d73cf7fb22e291506906aa302e9eb67425fa26ea9cb65f034ad2db`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bddd247177c165c022455fe81cee3a81cace56ba1466e32b4ad6a4d416cf72`  
		Last Modified: Wed, 27 Mar 2024 21:50:15 GMT  
		Size: 130.5 MB (130543565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a018e3f1556086e1e4d59fa9b183292f2a98745378a07045b720a9d085cbddea`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 841.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9421e59b2c9fcbaf696ac0b5c0507de0dcb53e61ce99d18b9091dbf466b68915`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afacd7c4aa583a91dafcc48ea2bd9a3f8ea7ddc85fcc67fe09d3a3d0d34a4a74`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:13244d86e6e07d8bbc2ac7332544ed89d5d3f4dd32c45007b0cd39f7e902b317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c29219d095a8667022ff4cfbc271efa73bc32718e7098ee397a91fb7591f1b`

```dockerfile
```

-	Layers:
	-	`sha256:8078c346d7f7342482b3ed469c68b15266c781f77e8b9d54c75b45e4bb30beaa`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 4.0 MB (3954709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4875492051ca452867fc4569d5b8dc5a2e0e1985097396a1cdbc8f5f854ce9bc`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36-debian`

```console
$ docker pull mysql@sha256:16d4cc0bd9da6f4becc3de398aaf34b96accbd35d039e3922e0721c1b9e06572
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.36-debian` - linux; amd64

```console
$ docker pull mysql@sha256:213ce44455c81e75c643b257c8c889c032047cb1b78c7038eba94710a9eb16e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180828380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c0bd217d592f5c913bb4e8eda3921db943554ccd25db8fd01ee93e68b06b9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1debian12
# Tue, 26 Mar 2024 03:50:44 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855739933c65c8c908e6007663e7b6d55d53e3cb6376cf45df6b85c54bcfff20`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf9690b1837f808bd48ed89713c955a80eba82ececd080aa36df2f6cf60d0bc`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 4.4 MB (4422729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718c8cf9a6d02f8d2c46c809091849da3f8050180802855c1ee42051fcdcefa`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 1.4 MB (1445886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2caee2910c1ee555369371c5a9b4d2b66e1e389f68f31b7c848223ba83e167e`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acea30847068f38b75b2d0efeeedc446df290c605dd21162a8cde4ced9f43ef`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 15.3 MB (15281898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef35ffb4224fb7fd335d5847991b14bdd01628b0fbf33eca17435a59f939313`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6102610fd9d73cf7fb22e291506906aa302e9eb67425fa26ea9cb65f034ad2db`  
		Last Modified: Wed, 27 Mar 2024 21:50:13 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bddd247177c165c022455fe81cee3a81cace56ba1466e32b4ad6a4d416cf72`  
		Last Modified: Wed, 27 Mar 2024 21:50:15 GMT  
		Size: 130.5 MB (130543565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a018e3f1556086e1e4d59fa9b183292f2a98745378a07045b720a9d085cbddea`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 841.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9421e59b2c9fcbaf696ac0b5c0507de0dcb53e61ce99d18b9091dbf466b68915`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afacd7c4aa583a91dafcc48ea2bd9a3f8ea7ddc85fcc67fe09d3a3d0d34a4a74`  
		Last Modified: Wed, 27 Mar 2024 21:50:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:13244d86e6e07d8bbc2ac7332544ed89d5d3f4dd32c45007b0cd39f7e902b317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c29219d095a8667022ff4cfbc271efa73bc32718e7098ee397a91fb7591f1b`

```dockerfile
```

-	Layers:
	-	`sha256:8078c346d7f7342482b3ed469c68b15266c781f77e8b9d54c75b45e4bb30beaa`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 4.0 MB (3954709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4875492051ca452867fc4569d5b8dc5a2e0e1985097396a1cdbc8f5f854ce9bc`  
		Last Modified: Wed, 27 Mar 2024 21:50:12 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36-oracle`

```console
$ docker pull mysql@sha256:ce628295ff5aa269e4d0241e0552476fa0de3af263daedf196ccb6fc0834fa6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.36-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6e444bff4d42bda9f1d6121859c58ee2c6515185849b1654e37345a6eea6a4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174718031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a15556a7dd66cd508ceaa083564bc7dbfbc0469fa587d92b2ec466f25b2d95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64073634efcc472fea7ee7a6cfbc9678807ecb255cd9db8a592211b2680773f9`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca025b52c77767226b123e41cdc082fac3eed53f51e1054075c3966359178cb6`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091a1e5789d410cbc663e77f407e57e3ef0f34e0b5f7eabbd2db5bdeae7201d3`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 4.6 MB (4592421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ab1febf12321f52a634824a7b1c4d4984c3a38f9c8d13714c4cc9c58f33020`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c05e4058de6fd2d75662003e71ef4be64f6cbe047955d25f4f192a0b5a1b3a`  
		Last Modified: Fri, 05 Apr 2024 18:52:43 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c6654d8546ef4e29491058869717a0b404cbb32bc7507713c469fd2104964e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 58.5 MB (58515054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972ceacaa396a23c63ad64dc25a6e6ae565329b5f27ffdd6df1ba01d8f88b2a5`  
		Last Modified: Fri, 05 Apr 2024 18:52:43 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cf75b54f0c97134cd3db85db5896492e33328e6324e082cd5ebaab32107450`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 59.3 MB (59300013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c407b83071d4001190f1de96238348b61559f81d0e37d1522be3f4d79ebb6b0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd699dd4735c2c0963e06c4e0114be1ec20f084acc185a5e81e3d4e31652ff6a`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:eb6b60ce6e817e31300d8716d4586c94d287cd1b96d9dc9f8f419cf0922febbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14283147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bfb26eb39fb012f4c6597115f510eec5321740393c07e302cfe18c40953210`

```dockerfile
```

-	Layers:
	-	`sha256:5359fab16f0c035a2d60383029e54f3df1d25bcc45de3ed813b71be18851b495`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 14.2 MB (14248252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eebe7c21f9fa7365c785348c3ca35c9a4ff3ccbe0a86a09fba6e7d2915ac62a9`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.36-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:669bf0ab62ceffd50f8e5a68111ba89e48b376d8ec66baf37cdce042112f3d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178501772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d56cc6c12046b23ea539b9b3e1d3b0f0355fed6652c41d7395653c610f6dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278337e747e9fe1fb2d0f48f5984719bdfabd6c3979e75a610b71b4cdfff0be4`  
		Last Modified: Fri, 05 Apr 2024 19:10:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eaf88539129c994346e7f57dd7cc2f18840977c58c9a385fd1344462579d31`  
		Last Modified: Fri, 05 Apr 2024 19:10:04 GMT  
		Size: 57.6 MB (57595809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a25bfe33e2c4573ec8d4f7c34c75b2f6cd038388a237fd1de9db802691fd36`  
		Last Modified: Fri, 05 Apr 2024 19:10:02 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0154a68c7d2e7bc03e7e8b9a1e9ff32680cbd999569fdb079b66f1b643a5976`  
		Last Modified: Fri, 05 Apr 2024 19:10:04 GMT  
		Size: 65.6 MB (65596699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bdd7b17194c6e971917d9eb8351280b9e546ab70d8a141fe49db3c6831602d`  
		Last Modified: Fri, 05 Apr 2024 19:10:02 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3042f2d5dd040865afa56a70e67ad02d7a9dced3e70401dbce0d6f46367860`  
		Last Modified: Fri, 05 Apr 2024 19:10:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:60b4795edaa62791a65fc2b9760340f9e0143f2b096d389ddf2f9a5447b8d6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14281256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9b4d1bf9ab37b4ee0d3ea2602159465e43daca4e811f2ca613e5c99329b112`

```dockerfile
```

-	Layers:
	-	`sha256:d659ceed129addf03908069fff59e9cc203d328c9ad9cf28e771ecb6ae1d7bcd`  
		Last Modified: Fri, 05 Apr 2024 19:10:02 GMT  
		Size: 14.2 MB (14246514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6943267177494b264e6d697d9073d25dfc2dbc82d8019c24ea87fa654578fc03`  
		Last Modified: Fri, 05 Apr 2024 19:10:01 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36-oraclelinux8`

```console
$ docker pull mysql@sha256:ce628295ff5aa269e4d0241e0552476fa0de3af263daedf196ccb6fc0834fa6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.36-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:6e444bff4d42bda9f1d6121859c58ee2c6515185849b1654e37345a6eea6a4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174718031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a15556a7dd66cd508ceaa083564bc7dbfbc0469fa587d92b2ec466f25b2d95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64073634efcc472fea7ee7a6cfbc9678807ecb255cd9db8a592211b2680773f9`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca025b52c77767226b123e41cdc082fac3eed53f51e1054075c3966359178cb6`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091a1e5789d410cbc663e77f407e57e3ef0f34e0b5f7eabbd2db5bdeae7201d3`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 4.6 MB (4592421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ab1febf12321f52a634824a7b1c4d4984c3a38f9c8d13714c4cc9c58f33020`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c05e4058de6fd2d75662003e71ef4be64f6cbe047955d25f4f192a0b5a1b3a`  
		Last Modified: Fri, 05 Apr 2024 18:52:43 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c6654d8546ef4e29491058869717a0b404cbb32bc7507713c469fd2104964e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 58.5 MB (58515054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972ceacaa396a23c63ad64dc25a6e6ae565329b5f27ffdd6df1ba01d8f88b2a5`  
		Last Modified: Fri, 05 Apr 2024 18:52:43 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cf75b54f0c97134cd3db85db5896492e33328e6324e082cd5ebaab32107450`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 59.3 MB (59300013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c407b83071d4001190f1de96238348b61559f81d0e37d1522be3f4d79ebb6b0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd699dd4735c2c0963e06c4e0114be1ec20f084acc185a5e81e3d4e31652ff6a`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:eb6b60ce6e817e31300d8716d4586c94d287cd1b96d9dc9f8f419cf0922febbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14283147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bfb26eb39fb012f4c6597115f510eec5321740393c07e302cfe18c40953210`

```dockerfile
```

-	Layers:
	-	`sha256:5359fab16f0c035a2d60383029e54f3df1d25bcc45de3ed813b71be18851b495`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 14.2 MB (14248252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eebe7c21f9fa7365c785348c3ca35c9a4ff3ccbe0a86a09fba6e7d2915ac62a9`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.36-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:669bf0ab62ceffd50f8e5a68111ba89e48b376d8ec66baf37cdce042112f3d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178501772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d56cc6c12046b23ea539b9b3e1d3b0f0355fed6652c41d7395653c610f6dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278337e747e9fe1fb2d0f48f5984719bdfabd6c3979e75a610b71b4cdfff0be4`  
		Last Modified: Fri, 05 Apr 2024 19:10:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eaf88539129c994346e7f57dd7cc2f18840977c58c9a385fd1344462579d31`  
		Last Modified: Fri, 05 Apr 2024 19:10:04 GMT  
		Size: 57.6 MB (57595809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a25bfe33e2c4573ec8d4f7c34c75b2f6cd038388a237fd1de9db802691fd36`  
		Last Modified: Fri, 05 Apr 2024 19:10:02 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0154a68c7d2e7bc03e7e8b9a1e9ff32680cbd999569fdb079b66f1b643a5976`  
		Last Modified: Fri, 05 Apr 2024 19:10:04 GMT  
		Size: 65.6 MB (65596699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bdd7b17194c6e971917d9eb8351280b9e546ab70d8a141fe49db3c6831602d`  
		Last Modified: Fri, 05 Apr 2024 19:10:02 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3042f2d5dd040865afa56a70e67ad02d7a9dced3e70401dbce0d6f46367860`  
		Last Modified: Fri, 05 Apr 2024 19:10:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:60b4795edaa62791a65fc2b9760340f9e0143f2b096d389ddf2f9a5447b8d6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14281256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9b4d1bf9ab37b4ee0d3ea2602159465e43daca4e811f2ca613e5c99329b112`

```dockerfile
```

-	Layers:
	-	`sha256:d659ceed129addf03908069fff59e9cc203d328c9ad9cf28e771ecb6ae1d7bcd`  
		Last Modified: Fri, 05 Apr 2024 19:10:02 GMT  
		Size: 14.2 MB (14246514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6943267177494b264e6d697d9073d25dfc2dbc82d8019c24ea87fa654578fc03`  
		Last Modified: Fri, 05 Apr 2024 19:10:01 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3`

```console
$ docker pull mysql@sha256:0f2e15fb8b47db2518b1428239ed3e3fe6a6693401b2cf19552063562cfc2fc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3` - linux; amd64

```console
$ docker pull mysql@sha256:076e3b41dfa9b184815b1239e37dd709bfddfdbf0e425eebb17c740705815b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183369525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f3f983cb088300e9fe51eb4d855c4c353f7afae9f035e9553148cfeb665e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1a4da808dd02e76718ff6f7ac40eb217687bd0fcd253d88238a39da21dc5f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3292fb4adf41458b3405e4fab39ac956e9b0f416e99d47965f29da3b5d9e69aa`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3811c45068ccd835ac871817eea43ac59bfe8495799508c3a2b14892d9a5293e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 4.6 MB (4592408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13320244c05a40c7dbd1a258b070d485426553b22eeba4859320d8d3908f327`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a34d702f2813fc3cf78dabf8d762fe3af066b682a2a968e6ffcfef9482588d4`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de90f448147740b877cd5a67ad605595d4cdea350ee3d1eee6ab9a09062f42b6`  
		Last Modified: Fri, 05 Apr 2024 18:52:46 GMT  
		Size: 63.1 MB (63081353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575200ae3755746a3740ff1224a9cabd56187b00a76f67a02b02d8ec2a8fc48`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea400be5707154f3b61c33ae937ff92fd75991ee6e4aa90a1aef9d83ba3087b`  
		Last Modified: Fri, 05 Apr 2024 18:52:47 GMT  
		Size: 63.4 MB (63385317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c930606a4f11cfa2329527166ba39c9ae607166fe9ea129f7f501c2a765d4a`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3` - unknown; unknown

```console
$ docker pull mysql@sha256:afd54f6d52e541184ddd0522cea94c724320401234036637dd404ff594148530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc4a54be9d6a9e12e4eadfabaa3a5f1883f5ef666d7f24bf99bdacbd865c88`

```dockerfile
```

-	Layers:
	-	`sha256:3e4e8176a1027fd661e2e4f9aff7fc92493e62a67ed841753acc7f58269314f0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 14.3 MB (14251350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ca62fef5598e17a59bbdeeefdbf07fc28ad9834f1daffdbbd3c44a0ae8f8f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 35.3 KB (35253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:83d25ba05253e3b89e5fd85f9a66b7a7d9f1e89292895bf8b567cffbe6650942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181397527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6757ec48c5aed83bb14cfd0c24a34cdf2ca2597180159ebd3c7daf73dd7333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c48356cf7d6537dfe73a9a67bdb4c3c67a94fa8e1d9ba69d6e8fe6541bb3`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada74d40ba8731fad59fba17d8484ffb304270e6ded18761b6d4d96075117a66`  
		Last Modified: Fri, 05 Apr 2024 19:08:07 GMT  
		Size: 62.1 MB (62054534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7b27488bbeff273c6739f2e5c81234ff7de38b4b222cf1a1e83e0d424a1f27`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c89304473a0e288d42d8e9abd6448096f4481ef1b031f301ce81fe07a85cd37`  
		Last Modified: Fri, 05 Apr 2024 19:08:08 GMT  
		Size: 64.0 MB (64033838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be02980a71934f1f891ec7d50e9cbc507195cdfac6c41c041b9b8fc9bed14d1`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3` - unknown; unknown

```console
$ docker pull mysql@sha256:7d2e413e81e1bf2fe47f80e4edd77b489a70f1a2fc71f40a35b1ba491c25eb6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1a155253ffcc40532a6b7c1a12fea4acac2c83c31cb89a12f4602c982699c4`

```dockerfile
```

-	Layers:
	-	`sha256:fedac3a3dba1e088509f54630da5c8a543c6af3a936e5a4197a991265262b645`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 14.2 MB (14249630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fccee5b98ccd310e92f31122c54cf83ff9ad788ff001cfb18f994fe3a48fedd1`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3-oracle`

```console
$ docker pull mysql@sha256:0f2e15fb8b47db2518b1428239ed3e3fe6a6693401b2cf19552063562cfc2fc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:076e3b41dfa9b184815b1239e37dd709bfddfdbf0e425eebb17c740705815b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183369525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f3f983cb088300e9fe51eb4d855c4c353f7afae9f035e9553148cfeb665e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1a4da808dd02e76718ff6f7ac40eb217687bd0fcd253d88238a39da21dc5f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3292fb4adf41458b3405e4fab39ac956e9b0f416e99d47965f29da3b5d9e69aa`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3811c45068ccd835ac871817eea43ac59bfe8495799508c3a2b14892d9a5293e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 4.6 MB (4592408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13320244c05a40c7dbd1a258b070d485426553b22eeba4859320d8d3908f327`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a34d702f2813fc3cf78dabf8d762fe3af066b682a2a968e6ffcfef9482588d4`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de90f448147740b877cd5a67ad605595d4cdea350ee3d1eee6ab9a09062f42b6`  
		Last Modified: Fri, 05 Apr 2024 18:52:46 GMT  
		Size: 63.1 MB (63081353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575200ae3755746a3740ff1224a9cabd56187b00a76f67a02b02d8ec2a8fc48`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea400be5707154f3b61c33ae937ff92fd75991ee6e4aa90a1aef9d83ba3087b`  
		Last Modified: Fri, 05 Apr 2024 18:52:47 GMT  
		Size: 63.4 MB (63385317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c930606a4f11cfa2329527166ba39c9ae607166fe9ea129f7f501c2a765d4a`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:afd54f6d52e541184ddd0522cea94c724320401234036637dd404ff594148530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc4a54be9d6a9e12e4eadfabaa3a5f1883f5ef666d7f24bf99bdacbd865c88`

```dockerfile
```

-	Layers:
	-	`sha256:3e4e8176a1027fd661e2e4f9aff7fc92493e62a67ed841753acc7f58269314f0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 14.3 MB (14251350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ca62fef5598e17a59bbdeeefdbf07fc28ad9834f1daffdbbd3c44a0ae8f8f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 35.3 KB (35253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:83d25ba05253e3b89e5fd85f9a66b7a7d9f1e89292895bf8b567cffbe6650942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181397527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6757ec48c5aed83bb14cfd0c24a34cdf2ca2597180159ebd3c7daf73dd7333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c48356cf7d6537dfe73a9a67bdb4c3c67a94fa8e1d9ba69d6e8fe6541bb3`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada74d40ba8731fad59fba17d8484ffb304270e6ded18761b6d4d96075117a66`  
		Last Modified: Fri, 05 Apr 2024 19:08:07 GMT  
		Size: 62.1 MB (62054534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7b27488bbeff273c6739f2e5c81234ff7de38b4b222cf1a1e83e0d424a1f27`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c89304473a0e288d42d8e9abd6448096f4481ef1b031f301ce81fe07a85cd37`  
		Last Modified: Fri, 05 Apr 2024 19:08:08 GMT  
		Size: 64.0 MB (64033838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be02980a71934f1f891ec7d50e9cbc507195cdfac6c41c041b9b8fc9bed14d1`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7d2e413e81e1bf2fe47f80e4edd77b489a70f1a2fc71f40a35b1ba491c25eb6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1a155253ffcc40532a6b7c1a12fea4acac2c83c31cb89a12f4602c982699c4`

```dockerfile
```

-	Layers:
	-	`sha256:fedac3a3dba1e088509f54630da5c8a543c6af3a936e5a4197a991265262b645`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 14.2 MB (14249630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fccee5b98ccd310e92f31122c54cf83ff9ad788ff001cfb18f994fe3a48fedd1`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3-oraclelinux8`

```console
$ docker pull mysql@sha256:0f2e15fb8b47db2518b1428239ed3e3fe6a6693401b2cf19552063562cfc2fc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:076e3b41dfa9b184815b1239e37dd709bfddfdbf0e425eebb17c740705815b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183369525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f3f983cb088300e9fe51eb4d855c4c353f7afae9f035e9553148cfeb665e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1a4da808dd02e76718ff6f7ac40eb217687bd0fcd253d88238a39da21dc5f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3292fb4adf41458b3405e4fab39ac956e9b0f416e99d47965f29da3b5d9e69aa`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3811c45068ccd835ac871817eea43ac59bfe8495799508c3a2b14892d9a5293e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 4.6 MB (4592408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13320244c05a40c7dbd1a258b070d485426553b22eeba4859320d8d3908f327`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a34d702f2813fc3cf78dabf8d762fe3af066b682a2a968e6ffcfef9482588d4`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de90f448147740b877cd5a67ad605595d4cdea350ee3d1eee6ab9a09062f42b6`  
		Last Modified: Fri, 05 Apr 2024 18:52:46 GMT  
		Size: 63.1 MB (63081353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575200ae3755746a3740ff1224a9cabd56187b00a76f67a02b02d8ec2a8fc48`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea400be5707154f3b61c33ae937ff92fd75991ee6e4aa90a1aef9d83ba3087b`  
		Last Modified: Fri, 05 Apr 2024 18:52:47 GMT  
		Size: 63.4 MB (63385317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c930606a4f11cfa2329527166ba39c9ae607166fe9ea129f7f501c2a765d4a`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:afd54f6d52e541184ddd0522cea94c724320401234036637dd404ff594148530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc4a54be9d6a9e12e4eadfabaa3a5f1883f5ef666d7f24bf99bdacbd865c88`

```dockerfile
```

-	Layers:
	-	`sha256:3e4e8176a1027fd661e2e4f9aff7fc92493e62a67ed841753acc7f58269314f0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 14.3 MB (14251350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ca62fef5598e17a59bbdeeefdbf07fc28ad9834f1daffdbbd3c44a0ae8f8f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 35.3 KB (35253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:83d25ba05253e3b89e5fd85f9a66b7a7d9f1e89292895bf8b567cffbe6650942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181397527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6757ec48c5aed83bb14cfd0c24a34cdf2ca2597180159ebd3c7daf73dd7333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c48356cf7d6537dfe73a9a67bdb4c3c67a94fa8e1d9ba69d6e8fe6541bb3`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada74d40ba8731fad59fba17d8484ffb304270e6ded18761b6d4d96075117a66`  
		Last Modified: Fri, 05 Apr 2024 19:08:07 GMT  
		Size: 62.1 MB (62054534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7b27488bbeff273c6739f2e5c81234ff7de38b4b222cf1a1e83e0d424a1f27`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c89304473a0e288d42d8e9abd6448096f4481ef1b031f301ce81fe07a85cd37`  
		Last Modified: Fri, 05 Apr 2024 19:08:08 GMT  
		Size: 64.0 MB (64033838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be02980a71934f1f891ec7d50e9cbc507195cdfac6c41c041b9b8fc9bed14d1`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:7d2e413e81e1bf2fe47f80e4edd77b489a70f1a2fc71f40a35b1ba491c25eb6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1a155253ffcc40532a6b7c1a12fea4acac2c83c31cb89a12f4602c982699c4`

```dockerfile
```

-	Layers:
	-	`sha256:fedac3a3dba1e088509f54630da5c8a543c6af3a936e5a4197a991265262b645`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 14.2 MB (14249630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fccee5b98ccd310e92f31122c54cf83ff9ad788ff001cfb18f994fe3a48fedd1`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3.0`

```console
$ docker pull mysql@sha256:0f2e15fb8b47db2518b1428239ed3e3fe6a6693401b2cf19552063562cfc2fc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3.0` - linux; amd64

```console
$ docker pull mysql@sha256:076e3b41dfa9b184815b1239e37dd709bfddfdbf0e425eebb17c740705815b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183369525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f3f983cb088300e9fe51eb4d855c4c353f7afae9f035e9553148cfeb665e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1a4da808dd02e76718ff6f7ac40eb217687bd0fcd253d88238a39da21dc5f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3292fb4adf41458b3405e4fab39ac956e9b0f416e99d47965f29da3b5d9e69aa`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3811c45068ccd835ac871817eea43ac59bfe8495799508c3a2b14892d9a5293e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 4.6 MB (4592408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13320244c05a40c7dbd1a258b070d485426553b22eeba4859320d8d3908f327`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a34d702f2813fc3cf78dabf8d762fe3af066b682a2a968e6ffcfef9482588d4`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de90f448147740b877cd5a67ad605595d4cdea350ee3d1eee6ab9a09062f42b6`  
		Last Modified: Fri, 05 Apr 2024 18:52:46 GMT  
		Size: 63.1 MB (63081353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575200ae3755746a3740ff1224a9cabd56187b00a76f67a02b02d8ec2a8fc48`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea400be5707154f3b61c33ae937ff92fd75991ee6e4aa90a1aef9d83ba3087b`  
		Last Modified: Fri, 05 Apr 2024 18:52:47 GMT  
		Size: 63.4 MB (63385317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c930606a4f11cfa2329527166ba39c9ae607166fe9ea129f7f501c2a765d4a`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0` - unknown; unknown

```console
$ docker pull mysql@sha256:afd54f6d52e541184ddd0522cea94c724320401234036637dd404ff594148530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc4a54be9d6a9e12e4eadfabaa3a5f1883f5ef666d7f24bf99bdacbd865c88`

```dockerfile
```

-	Layers:
	-	`sha256:3e4e8176a1027fd661e2e4f9aff7fc92493e62a67ed841753acc7f58269314f0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 14.3 MB (14251350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ca62fef5598e17a59bbdeeefdbf07fc28ad9834f1daffdbbd3c44a0ae8f8f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 35.3 KB (35253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:83d25ba05253e3b89e5fd85f9a66b7a7d9f1e89292895bf8b567cffbe6650942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181397527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6757ec48c5aed83bb14cfd0c24a34cdf2ca2597180159ebd3c7daf73dd7333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c48356cf7d6537dfe73a9a67bdb4c3c67a94fa8e1d9ba69d6e8fe6541bb3`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada74d40ba8731fad59fba17d8484ffb304270e6ded18761b6d4d96075117a66`  
		Last Modified: Fri, 05 Apr 2024 19:08:07 GMT  
		Size: 62.1 MB (62054534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7b27488bbeff273c6739f2e5c81234ff7de38b4b222cf1a1e83e0d424a1f27`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c89304473a0e288d42d8e9abd6448096f4481ef1b031f301ce81fe07a85cd37`  
		Last Modified: Fri, 05 Apr 2024 19:08:08 GMT  
		Size: 64.0 MB (64033838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be02980a71934f1f891ec7d50e9cbc507195cdfac6c41c041b9b8fc9bed14d1`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0` - unknown; unknown

```console
$ docker pull mysql@sha256:7d2e413e81e1bf2fe47f80e4edd77b489a70f1a2fc71f40a35b1ba491c25eb6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1a155253ffcc40532a6b7c1a12fea4acac2c83c31cb89a12f4602c982699c4`

```dockerfile
```

-	Layers:
	-	`sha256:fedac3a3dba1e088509f54630da5c8a543c6af3a936e5a4197a991265262b645`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 14.2 MB (14249630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fccee5b98ccd310e92f31122c54cf83ff9ad788ff001cfb18f994fe3a48fedd1`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3.0-oracle`

```console
$ docker pull mysql@sha256:0f2e15fb8b47db2518b1428239ed3e3fe6a6693401b2cf19552063562cfc2fc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:076e3b41dfa9b184815b1239e37dd709bfddfdbf0e425eebb17c740705815b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183369525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f3f983cb088300e9fe51eb4d855c4c353f7afae9f035e9553148cfeb665e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1a4da808dd02e76718ff6f7ac40eb217687bd0fcd253d88238a39da21dc5f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3292fb4adf41458b3405e4fab39ac956e9b0f416e99d47965f29da3b5d9e69aa`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3811c45068ccd835ac871817eea43ac59bfe8495799508c3a2b14892d9a5293e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 4.6 MB (4592408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13320244c05a40c7dbd1a258b070d485426553b22eeba4859320d8d3908f327`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a34d702f2813fc3cf78dabf8d762fe3af066b682a2a968e6ffcfef9482588d4`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de90f448147740b877cd5a67ad605595d4cdea350ee3d1eee6ab9a09062f42b6`  
		Last Modified: Fri, 05 Apr 2024 18:52:46 GMT  
		Size: 63.1 MB (63081353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575200ae3755746a3740ff1224a9cabd56187b00a76f67a02b02d8ec2a8fc48`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea400be5707154f3b61c33ae937ff92fd75991ee6e4aa90a1aef9d83ba3087b`  
		Last Modified: Fri, 05 Apr 2024 18:52:47 GMT  
		Size: 63.4 MB (63385317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c930606a4f11cfa2329527166ba39c9ae607166fe9ea129f7f501c2a765d4a`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:afd54f6d52e541184ddd0522cea94c724320401234036637dd404ff594148530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc4a54be9d6a9e12e4eadfabaa3a5f1883f5ef666d7f24bf99bdacbd865c88`

```dockerfile
```

-	Layers:
	-	`sha256:3e4e8176a1027fd661e2e4f9aff7fc92493e62a67ed841753acc7f58269314f0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 14.3 MB (14251350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ca62fef5598e17a59bbdeeefdbf07fc28ad9834f1daffdbbd3c44a0ae8f8f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 35.3 KB (35253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:83d25ba05253e3b89e5fd85f9a66b7a7d9f1e89292895bf8b567cffbe6650942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181397527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6757ec48c5aed83bb14cfd0c24a34cdf2ca2597180159ebd3c7daf73dd7333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c48356cf7d6537dfe73a9a67bdb4c3c67a94fa8e1d9ba69d6e8fe6541bb3`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada74d40ba8731fad59fba17d8484ffb304270e6ded18761b6d4d96075117a66`  
		Last Modified: Fri, 05 Apr 2024 19:08:07 GMT  
		Size: 62.1 MB (62054534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7b27488bbeff273c6739f2e5c81234ff7de38b4b222cf1a1e83e0d424a1f27`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c89304473a0e288d42d8e9abd6448096f4481ef1b031f301ce81fe07a85cd37`  
		Last Modified: Fri, 05 Apr 2024 19:08:08 GMT  
		Size: 64.0 MB (64033838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be02980a71934f1f891ec7d50e9cbc507195cdfac6c41c041b9b8fc9bed14d1`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7d2e413e81e1bf2fe47f80e4edd77b489a70f1a2fc71f40a35b1ba491c25eb6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1a155253ffcc40532a6b7c1a12fea4acac2c83c31cb89a12f4602c982699c4`

```dockerfile
```

-	Layers:
	-	`sha256:fedac3a3dba1e088509f54630da5c8a543c6af3a936e5a4197a991265262b645`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 14.2 MB (14249630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fccee5b98ccd310e92f31122c54cf83ff9ad788ff001cfb18f994fe3a48fedd1`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3.0-oraclelinux8`

```console
$ docker pull mysql@sha256:0f2e15fb8b47db2518b1428239ed3e3fe6a6693401b2cf19552063562cfc2fc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3.0-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:076e3b41dfa9b184815b1239e37dd709bfddfdbf0e425eebb17c740705815b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183369525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f3f983cb088300e9fe51eb4d855c4c353f7afae9f035e9553148cfeb665e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1a4da808dd02e76718ff6f7ac40eb217687bd0fcd253d88238a39da21dc5f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3292fb4adf41458b3405e4fab39ac956e9b0f416e99d47965f29da3b5d9e69aa`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3811c45068ccd835ac871817eea43ac59bfe8495799508c3a2b14892d9a5293e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 4.6 MB (4592408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13320244c05a40c7dbd1a258b070d485426553b22eeba4859320d8d3908f327`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a34d702f2813fc3cf78dabf8d762fe3af066b682a2a968e6ffcfef9482588d4`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de90f448147740b877cd5a67ad605595d4cdea350ee3d1eee6ab9a09062f42b6`  
		Last Modified: Fri, 05 Apr 2024 18:52:46 GMT  
		Size: 63.1 MB (63081353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575200ae3755746a3740ff1224a9cabd56187b00a76f67a02b02d8ec2a8fc48`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea400be5707154f3b61c33ae937ff92fd75991ee6e4aa90a1aef9d83ba3087b`  
		Last Modified: Fri, 05 Apr 2024 18:52:47 GMT  
		Size: 63.4 MB (63385317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c930606a4f11cfa2329527166ba39c9ae607166fe9ea129f7f501c2a765d4a`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:afd54f6d52e541184ddd0522cea94c724320401234036637dd404ff594148530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc4a54be9d6a9e12e4eadfabaa3a5f1883f5ef666d7f24bf99bdacbd865c88`

```dockerfile
```

-	Layers:
	-	`sha256:3e4e8176a1027fd661e2e4f9aff7fc92493e62a67ed841753acc7f58269314f0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 14.3 MB (14251350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ca62fef5598e17a59bbdeeefdbf07fc28ad9834f1daffdbbd3c44a0ae8f8f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 35.3 KB (35253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3.0-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:83d25ba05253e3b89e5fd85f9a66b7a7d9f1e89292895bf8b567cffbe6650942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181397527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6757ec48c5aed83bb14cfd0c24a34cdf2ca2597180159ebd3c7daf73dd7333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c48356cf7d6537dfe73a9a67bdb4c3c67a94fa8e1d9ba69d6e8fe6541bb3`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada74d40ba8731fad59fba17d8484ffb304270e6ded18761b6d4d96075117a66`  
		Last Modified: Fri, 05 Apr 2024 19:08:07 GMT  
		Size: 62.1 MB (62054534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7b27488bbeff273c6739f2e5c81234ff7de38b4b222cf1a1e83e0d424a1f27`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c89304473a0e288d42d8e9abd6448096f4481ef1b031f301ce81fe07a85cd37`  
		Last Modified: Fri, 05 Apr 2024 19:08:08 GMT  
		Size: 64.0 MB (64033838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be02980a71934f1f891ec7d50e9cbc507195cdfac6c41c041b9b8fc9bed14d1`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:7d2e413e81e1bf2fe47f80e4edd77b489a70f1a2fc71f40a35b1ba491c25eb6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1a155253ffcc40532a6b7c1a12fea4acac2c83c31cb89a12f4602c982699c4`

```dockerfile
```

-	Layers:
	-	`sha256:fedac3a3dba1e088509f54630da5c8a543c6af3a936e5a4197a991265262b645`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 14.2 MB (14249630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fccee5b98ccd310e92f31122c54cf83ff9ad788ff001cfb18f994fe3a48fedd1`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:0f2e15fb8b47db2518b1428239ed3e3fe6a6693401b2cf19552063562cfc2fc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:076e3b41dfa9b184815b1239e37dd709bfddfdbf0e425eebb17c740705815b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183369525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f3f983cb088300e9fe51eb4d855c4c353f7afae9f035e9553148cfeb665e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1a4da808dd02e76718ff6f7ac40eb217687bd0fcd253d88238a39da21dc5f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3292fb4adf41458b3405e4fab39ac956e9b0f416e99d47965f29da3b5d9e69aa`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3811c45068ccd835ac871817eea43ac59bfe8495799508c3a2b14892d9a5293e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 4.6 MB (4592408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13320244c05a40c7dbd1a258b070d485426553b22eeba4859320d8d3908f327`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a34d702f2813fc3cf78dabf8d762fe3af066b682a2a968e6ffcfef9482588d4`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de90f448147740b877cd5a67ad605595d4cdea350ee3d1eee6ab9a09062f42b6`  
		Last Modified: Fri, 05 Apr 2024 18:52:46 GMT  
		Size: 63.1 MB (63081353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575200ae3755746a3740ff1224a9cabd56187b00a76f67a02b02d8ec2a8fc48`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea400be5707154f3b61c33ae937ff92fd75991ee6e4aa90a1aef9d83ba3087b`  
		Last Modified: Fri, 05 Apr 2024 18:52:47 GMT  
		Size: 63.4 MB (63385317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c930606a4f11cfa2329527166ba39c9ae607166fe9ea129f7f501c2a765d4a`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:afd54f6d52e541184ddd0522cea94c724320401234036637dd404ff594148530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc4a54be9d6a9e12e4eadfabaa3a5f1883f5ef666d7f24bf99bdacbd865c88`

```dockerfile
```

-	Layers:
	-	`sha256:3e4e8176a1027fd661e2e4f9aff7fc92493e62a67ed841753acc7f58269314f0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 14.3 MB (14251350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ca62fef5598e17a59bbdeeefdbf07fc28ad9834f1daffdbbd3c44a0ae8f8f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 35.3 KB (35253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:83d25ba05253e3b89e5fd85f9a66b7a7d9f1e89292895bf8b567cffbe6650942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181397527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6757ec48c5aed83bb14cfd0c24a34cdf2ca2597180159ebd3c7daf73dd7333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c48356cf7d6537dfe73a9a67bdb4c3c67a94fa8e1d9ba69d6e8fe6541bb3`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada74d40ba8731fad59fba17d8484ffb304270e6ded18761b6d4d96075117a66`  
		Last Modified: Fri, 05 Apr 2024 19:08:07 GMT  
		Size: 62.1 MB (62054534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7b27488bbeff273c6739f2e5c81234ff7de38b4b222cf1a1e83e0d424a1f27`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c89304473a0e288d42d8e9abd6448096f4481ef1b031f301ce81fe07a85cd37`  
		Last Modified: Fri, 05 Apr 2024 19:08:08 GMT  
		Size: 64.0 MB (64033838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be02980a71934f1f891ec7d50e9cbc507195cdfac6c41c041b9b8fc9bed14d1`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:7d2e413e81e1bf2fe47f80e4edd77b489a70f1a2fc71f40a35b1ba491c25eb6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1a155253ffcc40532a6b7c1a12fea4acac2c83c31cb89a12f4602c982699c4`

```dockerfile
```

-	Layers:
	-	`sha256:fedac3a3dba1e088509f54630da5c8a543c6af3a936e5a4197a991265262b645`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 14.2 MB (14249630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fccee5b98ccd310e92f31122c54cf83ff9ad788ff001cfb18f994fe3a48fedd1`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:0f2e15fb8b47db2518b1428239ed3e3fe6a6693401b2cf19552063562cfc2fc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:076e3b41dfa9b184815b1239e37dd709bfddfdbf0e425eebb17c740705815b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183369525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f3f983cb088300e9fe51eb4d855c4c353f7afae9f035e9553148cfeb665e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1a4da808dd02e76718ff6f7ac40eb217687bd0fcd253d88238a39da21dc5f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3292fb4adf41458b3405e4fab39ac956e9b0f416e99d47965f29da3b5d9e69aa`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3811c45068ccd835ac871817eea43ac59bfe8495799508c3a2b14892d9a5293e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 4.6 MB (4592408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13320244c05a40c7dbd1a258b070d485426553b22eeba4859320d8d3908f327`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a34d702f2813fc3cf78dabf8d762fe3af066b682a2a968e6ffcfef9482588d4`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de90f448147740b877cd5a67ad605595d4cdea350ee3d1eee6ab9a09062f42b6`  
		Last Modified: Fri, 05 Apr 2024 18:52:46 GMT  
		Size: 63.1 MB (63081353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575200ae3755746a3740ff1224a9cabd56187b00a76f67a02b02d8ec2a8fc48`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea400be5707154f3b61c33ae937ff92fd75991ee6e4aa90a1aef9d83ba3087b`  
		Last Modified: Fri, 05 Apr 2024 18:52:47 GMT  
		Size: 63.4 MB (63385317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c930606a4f11cfa2329527166ba39c9ae607166fe9ea129f7f501c2a765d4a`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:afd54f6d52e541184ddd0522cea94c724320401234036637dd404ff594148530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc4a54be9d6a9e12e4eadfabaa3a5f1883f5ef666d7f24bf99bdacbd865c88`

```dockerfile
```

-	Layers:
	-	`sha256:3e4e8176a1027fd661e2e4f9aff7fc92493e62a67ed841753acc7f58269314f0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 14.3 MB (14251350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ca62fef5598e17a59bbdeeefdbf07fc28ad9834f1daffdbbd3c44a0ae8f8f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 35.3 KB (35253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:83d25ba05253e3b89e5fd85f9a66b7a7d9f1e89292895bf8b567cffbe6650942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181397527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6757ec48c5aed83bb14cfd0c24a34cdf2ca2597180159ebd3c7daf73dd7333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c48356cf7d6537dfe73a9a67bdb4c3c67a94fa8e1d9ba69d6e8fe6541bb3`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada74d40ba8731fad59fba17d8484ffb304270e6ded18761b6d4d96075117a66`  
		Last Modified: Fri, 05 Apr 2024 19:08:07 GMT  
		Size: 62.1 MB (62054534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7b27488bbeff273c6739f2e5c81234ff7de38b4b222cf1a1e83e0d424a1f27`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c89304473a0e288d42d8e9abd6448096f4481ef1b031f301ce81fe07a85cd37`  
		Last Modified: Fri, 05 Apr 2024 19:08:08 GMT  
		Size: 64.0 MB (64033838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be02980a71934f1f891ec7d50e9cbc507195cdfac6c41c041b9b8fc9bed14d1`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7d2e413e81e1bf2fe47f80e4edd77b489a70f1a2fc71f40a35b1ba491c25eb6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1a155253ffcc40532a6b7c1a12fea4acac2c83c31cb89a12f4602c982699c4`

```dockerfile
```

-	Layers:
	-	`sha256:fedac3a3dba1e088509f54630da5c8a543c6af3a936e5a4197a991265262b645`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 14.2 MB (14249630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fccee5b98ccd310e92f31122c54cf83ff9ad788ff001cfb18f994fe3a48fedd1`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux8`

```console
$ docker pull mysql@sha256:0f2e15fb8b47db2518b1428239ed3e3fe6a6693401b2cf19552063562cfc2fc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:076e3b41dfa9b184815b1239e37dd709bfddfdbf0e425eebb17c740705815b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183369525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f3f983cb088300e9fe51eb4d855c4c353f7afae9f035e9553148cfeb665e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1a4da808dd02e76718ff6f7ac40eb217687bd0fcd253d88238a39da21dc5f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3292fb4adf41458b3405e4fab39ac956e9b0f416e99d47965f29da3b5d9e69aa`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3811c45068ccd835ac871817eea43ac59bfe8495799508c3a2b14892d9a5293e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 4.6 MB (4592408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13320244c05a40c7dbd1a258b070d485426553b22eeba4859320d8d3908f327`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a34d702f2813fc3cf78dabf8d762fe3af066b682a2a968e6ffcfef9482588d4`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de90f448147740b877cd5a67ad605595d4cdea350ee3d1eee6ab9a09062f42b6`  
		Last Modified: Fri, 05 Apr 2024 18:52:46 GMT  
		Size: 63.1 MB (63081353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575200ae3755746a3740ff1224a9cabd56187b00a76f67a02b02d8ec2a8fc48`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea400be5707154f3b61c33ae937ff92fd75991ee6e4aa90a1aef9d83ba3087b`  
		Last Modified: Fri, 05 Apr 2024 18:52:47 GMT  
		Size: 63.4 MB (63385317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c930606a4f11cfa2329527166ba39c9ae607166fe9ea129f7f501c2a765d4a`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:afd54f6d52e541184ddd0522cea94c724320401234036637dd404ff594148530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc4a54be9d6a9e12e4eadfabaa3a5f1883f5ef666d7f24bf99bdacbd865c88`

```dockerfile
```

-	Layers:
	-	`sha256:3e4e8176a1027fd661e2e4f9aff7fc92493e62a67ed841753acc7f58269314f0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 14.3 MB (14251350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ca62fef5598e17a59bbdeeefdbf07fc28ad9834f1daffdbbd3c44a0ae8f8f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 35.3 KB (35253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:83d25ba05253e3b89e5fd85f9a66b7a7d9f1e89292895bf8b567cffbe6650942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181397527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6757ec48c5aed83bb14cfd0c24a34cdf2ca2597180159ebd3c7daf73dd7333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c48356cf7d6537dfe73a9a67bdb4c3c67a94fa8e1d9ba69d6e8fe6541bb3`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada74d40ba8731fad59fba17d8484ffb304270e6ded18761b6d4d96075117a66`  
		Last Modified: Fri, 05 Apr 2024 19:08:07 GMT  
		Size: 62.1 MB (62054534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7b27488bbeff273c6739f2e5c81234ff7de38b4b222cf1a1e83e0d424a1f27`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c89304473a0e288d42d8e9abd6448096f4481ef1b031f301ce81fe07a85cd37`  
		Last Modified: Fri, 05 Apr 2024 19:08:08 GMT  
		Size: 64.0 MB (64033838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be02980a71934f1f891ec7d50e9cbc507195cdfac6c41c041b9b8fc9bed14d1`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:7d2e413e81e1bf2fe47f80e4edd77b489a70f1a2fc71f40a35b1ba491c25eb6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1a155253ffcc40532a6b7c1a12fea4acac2c83c31cb89a12f4602c982699c4`

```dockerfile
```

-	Layers:
	-	`sha256:fedac3a3dba1e088509f54630da5c8a543c6af3a936e5a4197a991265262b645`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 14.2 MB (14249630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fccee5b98ccd310e92f31122c54cf83ff9ad788ff001cfb18f994fe3a48fedd1`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:0f2e15fb8b47db2518b1428239ed3e3fe6a6693401b2cf19552063562cfc2fc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:076e3b41dfa9b184815b1239e37dd709bfddfdbf0e425eebb17c740705815b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183369525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f3f983cb088300e9fe51eb4d855c4c353f7afae9f035e9553148cfeb665e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1a4da808dd02e76718ff6f7ac40eb217687bd0fcd253d88238a39da21dc5f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3292fb4adf41458b3405e4fab39ac956e9b0f416e99d47965f29da3b5d9e69aa`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3811c45068ccd835ac871817eea43ac59bfe8495799508c3a2b14892d9a5293e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 4.6 MB (4592408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13320244c05a40c7dbd1a258b070d485426553b22eeba4859320d8d3908f327`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a34d702f2813fc3cf78dabf8d762fe3af066b682a2a968e6ffcfef9482588d4`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de90f448147740b877cd5a67ad605595d4cdea350ee3d1eee6ab9a09062f42b6`  
		Last Modified: Fri, 05 Apr 2024 18:52:46 GMT  
		Size: 63.1 MB (63081353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575200ae3755746a3740ff1224a9cabd56187b00a76f67a02b02d8ec2a8fc48`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea400be5707154f3b61c33ae937ff92fd75991ee6e4aa90a1aef9d83ba3087b`  
		Last Modified: Fri, 05 Apr 2024 18:52:47 GMT  
		Size: 63.4 MB (63385317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c930606a4f11cfa2329527166ba39c9ae607166fe9ea129f7f501c2a765d4a`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:afd54f6d52e541184ddd0522cea94c724320401234036637dd404ff594148530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc4a54be9d6a9e12e4eadfabaa3a5f1883f5ef666d7f24bf99bdacbd865c88`

```dockerfile
```

-	Layers:
	-	`sha256:3e4e8176a1027fd661e2e4f9aff7fc92493e62a67ed841753acc7f58269314f0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 14.3 MB (14251350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ca62fef5598e17a59bbdeeefdbf07fc28ad9834f1daffdbbd3c44a0ae8f8f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 35.3 KB (35253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:83d25ba05253e3b89e5fd85f9a66b7a7d9f1e89292895bf8b567cffbe6650942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181397527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6757ec48c5aed83bb14cfd0c24a34cdf2ca2597180159ebd3c7daf73dd7333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c48356cf7d6537dfe73a9a67bdb4c3c67a94fa8e1d9ba69d6e8fe6541bb3`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada74d40ba8731fad59fba17d8484ffb304270e6ded18761b6d4d96075117a66`  
		Last Modified: Fri, 05 Apr 2024 19:08:07 GMT  
		Size: 62.1 MB (62054534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7b27488bbeff273c6739f2e5c81234ff7de38b4b222cf1a1e83e0d424a1f27`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c89304473a0e288d42d8e9abd6448096f4481ef1b031f301ce81fe07a85cd37`  
		Last Modified: Fri, 05 Apr 2024 19:08:08 GMT  
		Size: 64.0 MB (64033838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be02980a71934f1f891ec7d50e9cbc507195cdfac6c41c041b9b8fc9bed14d1`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:7d2e413e81e1bf2fe47f80e4edd77b489a70f1a2fc71f40a35b1ba491c25eb6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1a155253ffcc40532a6b7c1a12fea4acac2c83c31cb89a12f4602c982699c4`

```dockerfile
```

-	Layers:
	-	`sha256:fedac3a3dba1e088509f54630da5c8a543c6af3a936e5a4197a991265262b645`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 14.2 MB (14249630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fccee5b98ccd310e92f31122c54cf83ff9ad788ff001cfb18f994fe3a48fedd1`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:0f2e15fb8b47db2518b1428239ed3e3fe6a6693401b2cf19552063562cfc2fc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:076e3b41dfa9b184815b1239e37dd709bfddfdbf0e425eebb17c740705815b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183369525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f3f983cb088300e9fe51eb4d855c4c353f7afae9f035e9553148cfeb665e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1a4da808dd02e76718ff6f7ac40eb217687bd0fcd253d88238a39da21dc5f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3292fb4adf41458b3405e4fab39ac956e9b0f416e99d47965f29da3b5d9e69aa`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3811c45068ccd835ac871817eea43ac59bfe8495799508c3a2b14892d9a5293e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 4.6 MB (4592408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13320244c05a40c7dbd1a258b070d485426553b22eeba4859320d8d3908f327`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a34d702f2813fc3cf78dabf8d762fe3af066b682a2a968e6ffcfef9482588d4`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de90f448147740b877cd5a67ad605595d4cdea350ee3d1eee6ab9a09062f42b6`  
		Last Modified: Fri, 05 Apr 2024 18:52:46 GMT  
		Size: 63.1 MB (63081353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575200ae3755746a3740ff1224a9cabd56187b00a76f67a02b02d8ec2a8fc48`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea400be5707154f3b61c33ae937ff92fd75991ee6e4aa90a1aef9d83ba3087b`  
		Last Modified: Fri, 05 Apr 2024 18:52:47 GMT  
		Size: 63.4 MB (63385317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c930606a4f11cfa2329527166ba39c9ae607166fe9ea129f7f501c2a765d4a`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:afd54f6d52e541184ddd0522cea94c724320401234036637dd404ff594148530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc4a54be9d6a9e12e4eadfabaa3a5f1883f5ef666d7f24bf99bdacbd865c88`

```dockerfile
```

-	Layers:
	-	`sha256:3e4e8176a1027fd661e2e4f9aff7fc92493e62a67ed841753acc7f58269314f0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 14.3 MB (14251350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ca62fef5598e17a59bbdeeefdbf07fc28ad9834f1daffdbbd3c44a0ae8f8f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 35.3 KB (35253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:83d25ba05253e3b89e5fd85f9a66b7a7d9f1e89292895bf8b567cffbe6650942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181397527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6757ec48c5aed83bb14cfd0c24a34cdf2ca2597180159ebd3c7daf73dd7333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c48356cf7d6537dfe73a9a67bdb4c3c67a94fa8e1d9ba69d6e8fe6541bb3`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada74d40ba8731fad59fba17d8484ffb304270e6ded18761b6d4d96075117a66`  
		Last Modified: Fri, 05 Apr 2024 19:08:07 GMT  
		Size: 62.1 MB (62054534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7b27488bbeff273c6739f2e5c81234ff7de38b4b222cf1a1e83e0d424a1f27`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c89304473a0e288d42d8e9abd6448096f4481ef1b031f301ce81fe07a85cd37`  
		Last Modified: Fri, 05 Apr 2024 19:08:08 GMT  
		Size: 64.0 MB (64033838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be02980a71934f1f891ec7d50e9cbc507195cdfac6c41c041b9b8fc9bed14d1`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7d2e413e81e1bf2fe47f80e4edd77b489a70f1a2fc71f40a35b1ba491c25eb6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1a155253ffcc40532a6b7c1a12fea4acac2c83c31cb89a12f4602c982699c4`

```dockerfile
```

-	Layers:
	-	`sha256:fedac3a3dba1e088509f54630da5c8a543c6af3a936e5a4197a991265262b645`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 14.2 MB (14249630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fccee5b98ccd310e92f31122c54cf83ff9ad788ff001cfb18f994fe3a48fedd1`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux8`

```console
$ docker pull mysql@sha256:0f2e15fb8b47db2518b1428239ed3e3fe6a6693401b2cf19552063562cfc2fc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:076e3b41dfa9b184815b1239e37dd709bfddfdbf0e425eebb17c740705815b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183369525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f3f983cb088300e9fe51eb4d855c4c353f7afae9f035e9553148cfeb665e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1a4da808dd02e76718ff6f7ac40eb217687bd0fcd253d88238a39da21dc5f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3292fb4adf41458b3405e4fab39ac956e9b0f416e99d47965f29da3b5d9e69aa`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3811c45068ccd835ac871817eea43ac59bfe8495799508c3a2b14892d9a5293e`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 4.6 MB (4592408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13320244c05a40c7dbd1a258b070d485426553b22eeba4859320d8d3908f327`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a34d702f2813fc3cf78dabf8d762fe3af066b682a2a968e6ffcfef9482588d4`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de90f448147740b877cd5a67ad605595d4cdea350ee3d1eee6ab9a09062f42b6`  
		Last Modified: Fri, 05 Apr 2024 18:52:46 GMT  
		Size: 63.1 MB (63081353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575200ae3755746a3740ff1224a9cabd56187b00a76f67a02b02d8ec2a8fc48`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea400be5707154f3b61c33ae937ff92fd75991ee6e4aa90a1aef9d83ba3087b`  
		Last Modified: Fri, 05 Apr 2024 18:52:47 GMT  
		Size: 63.4 MB (63385317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c930606a4f11cfa2329527166ba39c9ae607166fe9ea129f7f501c2a765d4a`  
		Last Modified: Fri, 05 Apr 2024 18:52:45 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:afd54f6d52e541184ddd0522cea94c724320401234036637dd404ff594148530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc4a54be9d6a9e12e4eadfabaa3a5f1883f5ef666d7f24bf99bdacbd865c88`

```dockerfile
```

-	Layers:
	-	`sha256:3e4e8176a1027fd661e2e4f9aff7fc92493e62a67ed841753acc7f58269314f0`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 14.3 MB (14251350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ca62fef5598e17a59bbdeeefdbf07fc28ad9834f1daffdbbd3c44a0ae8f8f4`  
		Last Modified: Fri, 05 Apr 2024 18:52:44 GMT  
		Size: 35.3 KB (35253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:83d25ba05253e3b89e5fd85f9a66b7a7d9f1e89292895bf8b567cffbe6650942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181397527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6757ec48c5aed83bb14cfd0c24a34cdf2ca2597180159ebd3c7daf73dd7333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae022566edc67475dcecbe32db8dbfd8141be6266dd9ccf441a888940ece37`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd18f4775b21389158b3daef3ba91e01397cdb350038632c51c6aa516a3d1c`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfab8150e6b92c21c46a95fbf9263389ab13358cb9b2362d580aefcda6e60`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 4.3 MB (4301344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce811470e9cebbeb68b5839537cd75df098ffd97017acb8c20d62c74e5a5e56e`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c48356cf7d6537dfe73a9a67bdb4c3c67a94fa8e1d9ba69d6e8fe6541bb3`  
		Last Modified: Fri, 05 Apr 2024 19:08:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada74d40ba8731fad59fba17d8484ffb304270e6ded18761b6d4d96075117a66`  
		Last Modified: Fri, 05 Apr 2024 19:08:07 GMT  
		Size: 62.1 MB (62054534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7b27488bbeff273c6739f2e5c81234ff7de38b4b222cf1a1e83e0d424a1f27`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c89304473a0e288d42d8e9abd6448096f4481ef1b031f301ce81fe07a85cd37`  
		Last Modified: Fri, 05 Apr 2024 19:08:08 GMT  
		Size: 64.0 MB (64033838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be02980a71934f1f891ec7d50e9cbc507195cdfac6c41c041b9b8fc9bed14d1`  
		Last Modified: Fri, 05 Apr 2024 19:08:06 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:7d2e413e81e1bf2fe47f80e4edd77b489a70f1a2fc71f40a35b1ba491c25eb6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1a155253ffcc40532a6b7c1a12fea4acac2c83c31cb89a12f4602c982699c4`

```dockerfile
```

-	Layers:
	-	`sha256:fedac3a3dba1e088509f54630da5c8a543c6af3a936e5a4197a991265262b645`  
		Last Modified: Fri, 05 Apr 2024 19:08:04 GMT  
		Size: 14.2 MB (14249630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fccee5b98ccd310e92f31122c54cf83ff9ad788ff001cfb18f994fe3a48fedd1`  
		Last Modified: Fri, 05 Apr 2024 19:08:03 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json
