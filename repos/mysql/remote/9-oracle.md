## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:db32c8ec843c042a728efb0ac7aa814d6f010eaac8923e20ae0a849d09c5baf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:717d1e4b2352def1f05b40c3c16c470b57f320112a32e506d4548f9964853304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266357843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66b7a28811314e6a4dcafccd94c4be68006bc32ec970bf95deb46ba36faaaca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:19 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a384f12fc17c4a4345d1165feb19288c5437373be4ac09f162d08c68683b26`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3034072b44e63d1e79ea3e342fd12e97ca43901fd8b2906e210eae290c723f`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07617e6f14bd1f717d9551f5b325d7412b1ca9fe16f6130958b1911d5bc5ec2`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 6.2 MB (6174544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7dc27e1ddd2f888a1d6ad0cad0c55905bb5b2276a717cca00b0e9b4deb667`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b1ba0190807d166baef7098e86fe6204c122fae6772a54f1f35fc9d174c61e`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c2157be11ce559af0bc6b6d25eb94ef104993abedc0584fc94d62731fd5311`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 51.4 MB (51448952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9390a44189a01556582762353a051263135785885eb2e15147586d679667a`  
		Last Modified: Thu, 05 Feb 2026 22:10:17 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b95dea655397746f06b33bf365db15297f55c2345090a2823bc0c79874b9a4`  
		Last Modified: Thu, 05 Feb 2026 22:10:21 GMT  
		Size: 160.6 MB (160633758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44c8bf49c1d239b0eda62ea1c5ed07cc67057612dcca8831df4b67a83cc1f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d28c84384e7ddf32b134e617d8e0822e7f6d7095cc30579de46a1ee9d2768ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e177d6dc600e09c21080e1102e8a416e021c4a0525695f8053429294cf92caf2`

```dockerfile
```

-	Layers:
	-	`sha256:7e5a775ad22a51cb9a2257f84e44d71f2a18eb24914dc233ce465adf051f25c4`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 16.3 MB (16297420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8be4b9c0eb42b0ba27f1212994a66b32c067b642fe4e9d0954f857a6ca0812`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8da8ea39f953a1dc0a507576ba3289a6416caa5a195ecdeefb5ad34991fc648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bab0412e25056497796fd66a0e8a8ba88fd150ae0215a902ac40aec72e33b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:26 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:10:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc311b7141a81abc777678fce031f5f9d0e35f00fac0bc09149d034df7fb143`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2866f080bd66e1591ef99259b84bfce1897c9a1cc90704bbef47668c2cc91263`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9e9c3d0312fcc60a59444875726e7498141d132a2a5b691f8d010c93eb500a`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 5.8 MB (5791701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3308f5dc5a765736e142932bff2e7f514adacbf784323b1281d3bc75406f328`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823d80b302358df95e02d0ff68bd90af04955af6d39800c87ffffafef16f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c8f56b46ceb0491f6906a0dd4f6bf82d59a73f9a023c7e00ee74741b84d70f`  
		Last Modified: Thu, 05 Feb 2026 22:10:42 GMT  
		Size: 50.1 MB (50086840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b2b2e44e46310cc4b14e96034786d2aed014890bd99635ae0178641075038`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e577a10e09c5ae91c9924eae74caedacee1690b00ff2fc22bcfd550113218`  
		Last Modified: Thu, 05 Feb 2026 22:10:44 GMT  
		Size: 158.9 MB (158940066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad37a81ec0b0df85dfc6fa4d746388caf1533f0bfb64ee04f1c32601eabcb9ef`  
		Last Modified: Thu, 05 Feb 2026 22:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f65d1491a46324caebad462221004ac9e42e2a377e2c601ea502389b47e05a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992b8c30aee19df4cb17ae696682f32b0923a3eec31a06d8d8bde4992f250b27`

```dockerfile
```

-	Layers:
	-	`sha256:381b00c5f847ba4f949cafdcc0911c4eaf169d35cdf464ac47ef92670595b931`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 16.3 MB (16295876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c08a75f7468a7ab9c1aec376a6792433ca750a3fb5f6f80345a2bbe861919f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json
