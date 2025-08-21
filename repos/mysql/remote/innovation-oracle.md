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
