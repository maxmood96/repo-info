## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:0093a60271558dcf0084bbfd683f4b94e56e07eb682c30bb074bb863bdba5b2b
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
$ docker pull mysql@sha256:871812bb5e91918c23410ecc4aa22c5e39b7c84e12cf52c231ef3dcca82c7490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233045781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a23f791babc29afc73f7aac77970fa302d5d219a30f7bd487875fac0fa61a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:09:00 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:09:00 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:09:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:09:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:09:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 21:10:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f1bc55eb16e754134bfba815453a74ba93ea6bbd9d27ac316b2b77850577bd`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2128c976b29d78f69a41ad76dc67cce8fd800a52d130d6f8293579fcd1eeda7`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b3bb1d63c466ebaa0fc2e8398cc873848a023facf67ba0dcccfc681aa5100f`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 5.8 MB (5790759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5425b0dd192e6ec77f0ad5828754df7a0c1a628f687c6403042a8fc57afe9526`  
		Last Modified: Mon, 04 May 2026 21:11:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c472e44f6b5ea3845f0e830eb674735904ec11a653cb994eb1a75e7c56ef91`  
		Last Modified: Mon, 04 May 2026 21:11:13 GMT  
		Size: 49.8 MB (49827931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bcfe4c9099b1ca747e6e5acb104014cb0296556d10ee53f5089cf1375fac04`  
		Last Modified: Mon, 04 May 2026 21:11:11 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a675bd3a34fe3e962a1f6831dac4f2a176cf88ef1c315ddf72c8ddfc4cf7cf`  
		Last Modified: Mon, 04 May 2026 21:11:14 GMT  
		Size: 130.8 MB (130781172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c228476154cbed5491d4e3a805938f4c9c72a02a71b23ba559be75b16d8353`  
		Last Modified: Mon, 04 May 2026 21:11:12 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:18c43f282a55b36187af012ed452a1d4e96c3285030f724f6b09f44a1fbb8def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49528778add127479f721d7f18c2e08febbe37f5966bcc0ed2e838f8839c90fa`

```dockerfile
```

-	Layers:
	-	`sha256:bf9d312db6bf9479e660fae507ac8fc00fa4b0e7c065fa2550a97941ff5cd192`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 15.7 MB (15708390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22236123f06da452f975f4518ee91c8b7e0af5875ec06e7f0cb73818131b00a2`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 33.6 KB (33567 bytes)  
		MIME: application/vnd.in-toto+json
