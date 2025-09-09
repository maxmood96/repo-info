## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:6e60ad6d61d8e7f0a4fd07f6b14109331d66a2f0d089e4b7a1f485d671a29604
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:240dbdd43912fd39e8f3dc639089689b508b8483083dc76d4a03de3a3251a6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236815541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb72985bb938a89de9f49e38b08d864d5cd16a71d7cc2131bb5705759c3a8a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e0357662693308cd79d9dde75766c7976309ce39f1d5d7b8db58ab741819f0`  
		Last Modified: Mon, 08 Sep 2025 22:42:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328796243e0b1cda6ae546118a08fb6555779ed79af7e8b22327a7fafc6277bf`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 782.3 KB (782336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998cf6c9454cef74eac13b3c45401daf534b3f7295e487fa0f1ab46b477e50c9`  
		Last Modified: Tue, 09 Sep 2025 00:02:24 GMT  
		Size: 6.8 MB (6818672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702ebe6dd8f015a64244c42fecaf58c5dfac4e3b44be8b182f6b5b2ed098381`  
		Last Modified: Mon, 08 Sep 2025 22:42:57 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894cca000d1f780fcd7afd568bb62adc62ae7b286bd88f9ac6c9b65ade46513`  
		Last Modified: Mon, 08 Sep 2025 22:43:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b5340945f96d3728efd4a61c8935cc9b8b680f30a6651037f92fb99436804f`  
		Last Modified: Tue, 09 Sep 2025 00:02:27 GMT  
		Size: 47.8 MB (47767152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b274c62c3cff97bf3a765a1e0c19b485ed7249a60e9bc1d59a44ebfdd97233`  
		Last Modified: Mon, 08 Sep 2025 22:43:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318326631da0031d2bbbccca0fde7425b41bda05c874e2cacab41c91bc7113c3`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 131.9 MB (131940887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582874d217963084d072050a4cd73a3702f97fb909857815b4a26bfe765fb2a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:11 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1d439979703a61dcd0eb26e577f2c5b164f2187f5cc6013d1c00a9131dc9b0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f550ea22b18898ec61433d26b71c1c12d5021cc2403e4584a642ebc2d09263`

```dockerfile
```

-	Layers:
	-	`sha256:9902dbec45a944718eb9b3bada40ecc071ee9787df286b756a9b2f42c933ce79`  
		Last Modified: Tue, 09 Sep 2025 00:02:29 GMT  
		Size: 14.8 MB (14804918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8782c57399d622ecd87e8e979887d3871918bf441777e72556674d7c327a1993`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c5c75688e919d4da65f643c12277d28bfc7e629fb8b3d6363d40fb85b77107ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232273311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c2ef8c7e3b596011893d8b1ac77e434c5d88417a059478eaf85fd8343f9961`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:12:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:12:13 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc35fc071eba97c9a158f3645391887aa00f2e8083278e8dd01b62a169e64ac`  
		Last Modified: Tue, 09 Sep 2025 02:27:24 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093c6caa91a6f26ebc6b0579d66e736c1c0bad2cca530843e8fa2cf1f7dbbe8e`  
		Last Modified: Tue, 09 Sep 2025 02:27:23 GMT  
		Size: 736.8 KB (736808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfcb5bf761c5d2aaec9b8be8c8497785263fc072e135a268c9642d316ae3111`  
		Last Modified: Tue, 09 Sep 2025 02:31:16 GMT  
		Size: 6.4 MB (6445487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd280f528cff59d9a7d1b994029ce5e0cd11df7e0cf89a2a940fb777b775f36`  
		Last Modified: Tue, 09 Sep 2025 02:21:38 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da38a666f82b574b71b62e143ab925efa5496f11d34bba00054625a91751b32e`  
		Last Modified: Tue, 09 Sep 2025 02:27:24 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d536d3279c430d2fa7e015743456925cf755d5038d285a675167a52a461bb031`  
		Last Modified: Tue, 09 Sep 2025 02:30:21 GMT  
		Size: 46.7 MB (46653364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a41f413d2c666abf981a74d62c5cc263c8a17195db7ee0df0a8a2736cb3a80`  
		Last Modified: Tue, 09 Sep 2025 02:27:24 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e30c41c9f4ba737afa4914c73684a6293db127ef417227e32dbb9feedc062d3`  
		Last Modified: Tue, 09 Sep 2025 03:02:25 GMT  
		Size: 130.3 MB (130341442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9bfdcc6700c14b493e4c0235339742b19821d509bbbde276b3b3a22d59b3c7`  
		Last Modified: Tue, 09 Sep 2025 02:27:24 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:53c36c8d8f0505e34d9642f5305bddd83f0259c3747a20ec9f8e21f50a6372a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a51897ebf5bb83fe3b3a0a7b9ab23a1c162c5a82fbdad803cb2fc79e30f4e9a`

```dockerfile
```

-	Layers:
	-	`sha256:bfd40d9ad8ac9ee63de18e0f30ef99737eb387e38584420b88893c244dc3510f`  
		Last Modified: Tue, 09 Sep 2025 03:02:29 GMT  
		Size: 14.8 MB (14803337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ebc2e6c997ef89f6f00b907d0e2e610229ed44027b628e7b83142bbd9887bf3`  
		Last Modified: Tue, 09 Sep 2025 03:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json
