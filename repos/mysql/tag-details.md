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
-	[`mysql:8.0.41`](#mysql8041)
-	[`mysql:8.0.41-bookworm`](#mysql8041-bookworm)
-	[`mysql:8.0.41-debian`](#mysql8041-debian)
-	[`mysql:8.0.41-oracle`](#mysql8041-oracle)
-	[`mysql:8.0.41-oraclelinux9`](#mysql8041-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.4`](#mysql844)
-	[`mysql:8.4.4-oracle`](#mysql844-oracle)
-	[`mysql:8.4.4-oraclelinux9`](#mysql844-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.2`](#mysql92)
-	[`mysql:9.2-oracle`](#mysql92-oracle)
-	[`mysql:9.2-oraclelinux9`](#mysql92-oraclelinux9)
-	[`mysql:9.2.0`](#mysql920)
-	[`mysql:9.2.0-oracle`](#mysql920-oracle)
-	[`mysql:9.2.0-oraclelinux9`](#mysql920-oraclelinux9)
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
$ docker pull mysql@sha256:b14b2b73fc1242bef8fc21cbd73f247396f353cf314734d3502d72eb1ed0d93b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:d50d35b5bd33e90185cf7c9752a8a9c4e322752d9d441aead65d55a5a7a9b0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232921620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03152aa0b71af6d9c2d3ce540cb012fbe4f2c902896c7572baa29e9c2c863d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953a4ccd23a81b87fee3f10c6f7b0f64a28cddf2b44ae4709ed11ba1ddce2801`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f496cf111703223486f94eab0e33c24d2f2d42e3048ade9f846bee4d2c216d78`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba398fbba1a319bb6b0e8072ab3967941541520c4ea0cc9de237fe0fb5c24bf`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 6.9 MB (6900797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612294d2b805abc144afdb56ea7c4c853afb0848da8ba320ded974bfea920c0d`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b72e8cade85158d043b1cc49db60f3192b21928519bd37effb9455ff838774`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16088fb0c0bc6fed09b5f1901cd8932898f9533922d16e2ea76ec6713d3a6e9f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 47.6 MB (47593441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1113808e87139e81bf5791ef5f9a4cfb6340d3744c071b06378e5dd4300cf2`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb634a27ea9af9512a616770be962abb004a69340d9293672318762c88e6f0da`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 128.3 MB (128337606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779e768d23c147ac6ff98cad8c97e9fd64ae88e6fa64c36af645e92f9760640`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:8e27ad713932c235a3a2ba33c8afaf2f24be95c06cf5581d42a16e27cc34902c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e722b0900dddd12a388283e5a5536b2d3136467cab0738958c593d01ae72c0`

```dockerfile
```

-	Layers:
	-	`sha256:a1e7f0e8c496cb14802c1bfd6677f68818d049e581b7a09366a16c80701e32ef`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 14.1 MB (14074192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07d6bfb3db9fb8c16f6075a18e084c2af417f5624c0d7a8e3173a3c498488a4`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b069ea7a6e799b97b7cda674dc14af372a3e819e8167ca7f9f2b25d271ba21c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228373891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143ee6a01dfafb0fc64201d822bf454604f2f23e7de391d6ded6bed4d0f10d2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6d58e993cc8f74278b7b31bc7d5c3a90f3a641fa669d7f9baa0c8bb3f22b99`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89597d03bec9a798d018a2da6d72618fd411ee3be7cfba13b6f84a54a2ff094e`  
		Last Modified: Wed, 05 Feb 2025 21:11:25 GMT  
		Size: 46.5 MB (46472784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b25528c202a2c51e7345274b2ba9194d3e40ad59c4564ca8bda7c62adc296d7`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5176c942bb7758f3748ca374a5f473ec23d3aa80f84498adb45b23c52246574`  
		Last Modified: Wed, 05 Feb 2025 21:11:26 GMT  
		Size: 126.8 MB (126811206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f10df86d743ce521a9a6df46866fb0db04ee299e86f50ebf6a1a9be951c4afa`  
		Last Modified: Wed, 05 Feb 2025 21:11:24 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:9f201d54b76a028b5603016be80583ff3ce499109d5e9b51b6b5c0297cbf4535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7090fba013cec374dc2272b28151f052a2618f48262644077be4d3447039c7`

```dockerfile
```

-	Layers:
	-	`sha256:976a24bbc9d8d48ab0628f1df0c95711404a4ef73eec2286b7e272fbe4c09e72`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 14.1 MB (14072612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9fcf77de5ba79f3b92a0c9269899881dddef44c3ad957f19afa19b2d763ddbc`  
		Last Modified: Wed, 05 Feb 2025 21:11:22 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:b14b2b73fc1242bef8fc21cbd73f247396f353cf314734d3502d72eb1ed0d93b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d50d35b5bd33e90185cf7c9752a8a9c4e322752d9d441aead65d55a5a7a9b0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232921620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03152aa0b71af6d9c2d3ce540cb012fbe4f2c902896c7572baa29e9c2c863d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953a4ccd23a81b87fee3f10c6f7b0f64a28cddf2b44ae4709ed11ba1ddce2801`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f496cf111703223486f94eab0e33c24d2f2d42e3048ade9f846bee4d2c216d78`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba398fbba1a319bb6b0e8072ab3967941541520c4ea0cc9de237fe0fb5c24bf`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 6.9 MB (6900797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612294d2b805abc144afdb56ea7c4c853afb0848da8ba320ded974bfea920c0d`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b72e8cade85158d043b1cc49db60f3192b21928519bd37effb9455ff838774`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16088fb0c0bc6fed09b5f1901cd8932898f9533922d16e2ea76ec6713d3a6e9f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 47.6 MB (47593441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1113808e87139e81bf5791ef5f9a4cfb6340d3744c071b06378e5dd4300cf2`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb634a27ea9af9512a616770be962abb004a69340d9293672318762c88e6f0da`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 128.3 MB (128337606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779e768d23c147ac6ff98cad8c97e9fd64ae88e6fa64c36af645e92f9760640`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:8e27ad713932c235a3a2ba33c8afaf2f24be95c06cf5581d42a16e27cc34902c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e722b0900dddd12a388283e5a5536b2d3136467cab0738958c593d01ae72c0`

```dockerfile
```

-	Layers:
	-	`sha256:a1e7f0e8c496cb14802c1bfd6677f68818d049e581b7a09366a16c80701e32ef`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 14.1 MB (14074192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07d6bfb3db9fb8c16f6075a18e084c2af417f5624c0d7a8e3173a3c498488a4`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b069ea7a6e799b97b7cda674dc14af372a3e819e8167ca7f9f2b25d271ba21c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228373891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143ee6a01dfafb0fc64201d822bf454604f2f23e7de391d6ded6bed4d0f10d2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6d58e993cc8f74278b7b31bc7d5c3a90f3a641fa669d7f9baa0c8bb3f22b99`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89597d03bec9a798d018a2da6d72618fd411ee3be7cfba13b6f84a54a2ff094e`  
		Last Modified: Wed, 05 Feb 2025 21:11:25 GMT  
		Size: 46.5 MB (46472784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b25528c202a2c51e7345274b2ba9194d3e40ad59c4564ca8bda7c62adc296d7`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5176c942bb7758f3748ca374a5f473ec23d3aa80f84498adb45b23c52246574`  
		Last Modified: Wed, 05 Feb 2025 21:11:26 GMT  
		Size: 126.8 MB (126811206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f10df86d743ce521a9a6df46866fb0db04ee299e86f50ebf6a1a9be951c4afa`  
		Last Modified: Wed, 05 Feb 2025 21:11:24 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9f201d54b76a028b5603016be80583ff3ce499109d5e9b51b6b5c0297cbf4535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7090fba013cec374dc2272b28151f052a2618f48262644077be4d3447039c7`

```dockerfile
```

-	Layers:
	-	`sha256:976a24bbc9d8d48ab0628f1df0c95711404a4ef73eec2286b7e272fbe4c09e72`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 14.1 MB (14072612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9fcf77de5ba79f3b92a0c9269899881dddef44c3ad957f19afa19b2d763ddbc`  
		Last Modified: Wed, 05 Feb 2025 21:11:22 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:b14b2b73fc1242bef8fc21cbd73f247396f353cf314734d3502d72eb1ed0d93b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d50d35b5bd33e90185cf7c9752a8a9c4e322752d9d441aead65d55a5a7a9b0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232921620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03152aa0b71af6d9c2d3ce540cb012fbe4f2c902896c7572baa29e9c2c863d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953a4ccd23a81b87fee3f10c6f7b0f64a28cddf2b44ae4709ed11ba1ddce2801`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f496cf111703223486f94eab0e33c24d2f2d42e3048ade9f846bee4d2c216d78`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba398fbba1a319bb6b0e8072ab3967941541520c4ea0cc9de237fe0fb5c24bf`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 6.9 MB (6900797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612294d2b805abc144afdb56ea7c4c853afb0848da8ba320ded974bfea920c0d`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b72e8cade85158d043b1cc49db60f3192b21928519bd37effb9455ff838774`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16088fb0c0bc6fed09b5f1901cd8932898f9533922d16e2ea76ec6713d3a6e9f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 47.6 MB (47593441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1113808e87139e81bf5791ef5f9a4cfb6340d3744c071b06378e5dd4300cf2`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb634a27ea9af9512a616770be962abb004a69340d9293672318762c88e6f0da`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 128.3 MB (128337606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779e768d23c147ac6ff98cad8c97e9fd64ae88e6fa64c36af645e92f9760640`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:8e27ad713932c235a3a2ba33c8afaf2f24be95c06cf5581d42a16e27cc34902c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e722b0900dddd12a388283e5a5536b2d3136467cab0738958c593d01ae72c0`

```dockerfile
```

-	Layers:
	-	`sha256:a1e7f0e8c496cb14802c1bfd6677f68818d049e581b7a09366a16c80701e32ef`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 14.1 MB (14074192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07d6bfb3db9fb8c16f6075a18e084c2af417f5624c0d7a8e3173a3c498488a4`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b069ea7a6e799b97b7cda674dc14af372a3e819e8167ca7f9f2b25d271ba21c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228373891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143ee6a01dfafb0fc64201d822bf454604f2f23e7de391d6ded6bed4d0f10d2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6d58e993cc8f74278b7b31bc7d5c3a90f3a641fa669d7f9baa0c8bb3f22b99`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89597d03bec9a798d018a2da6d72618fd411ee3be7cfba13b6f84a54a2ff094e`  
		Last Modified: Wed, 05 Feb 2025 21:11:25 GMT  
		Size: 46.5 MB (46472784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b25528c202a2c51e7345274b2ba9194d3e40ad59c4564ca8bda7c62adc296d7`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5176c942bb7758f3748ca374a5f473ec23d3aa80f84498adb45b23c52246574`  
		Last Modified: Wed, 05 Feb 2025 21:11:26 GMT  
		Size: 126.8 MB (126811206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f10df86d743ce521a9a6df46866fb0db04ee299e86f50ebf6a1a9be951c4afa`  
		Last Modified: Wed, 05 Feb 2025 21:11:24 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9f201d54b76a028b5603016be80583ff3ce499109d5e9b51b6b5c0297cbf4535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7090fba013cec374dc2272b28151f052a2618f48262644077be4d3447039c7`

```dockerfile
```

-	Layers:
	-	`sha256:976a24bbc9d8d48ab0628f1df0c95711404a4ef73eec2286b7e272fbe4c09e72`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 14.1 MB (14072612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9fcf77de5ba79f3b92a0c9269899881dddef44c3ad957f19afa19b2d763ddbc`  
		Last Modified: Wed, 05 Feb 2025 21:11:22 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:f0657322a50b735bf284dac26e3e3d99e24810ea13d37ef6b7ca6cdd0d54fcc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:ec81f1831771560bd7536a5f85eeefe27e55f5fb4fc23cd5a4fd45464f7d8dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231919727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081ade299f2e2869cda9aa4314b6801b8ddcf851b7b5012e03fa7fbed557fd6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3b09f953cc63439caf29ecc50c8f51b1c5ca3621669505de462d63732fb757`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69038e54211bdb7abde47f6447273edf0c06b28fb3eb63a363277554430145f`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e40652ce5a94d382a18ef147a475c17e7db11051e2f682c149b48d0e3fbc1e`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 6.9 MB (6900810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5c2da6bb37121e624450120b02c75378316291b74e67bbb19b595bd420a969`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6258a15df35b08168c4519b6348854701c13b9de0da12ec6fafdbd467e57c72`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483046b091213e7b6a949a7fbd2dd4adcc461e9fbb6ee9d4e580bfb8a9347608`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 49.6 MB (49634979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fc4435765883fc6ae940e5b638c40de5324b181f6f28fe86431eb53095d6`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4af1f1b7267addd138073877fb479aed3cd576fd2f97b6414aab29dcd06783b`  
		Last Modified: Wed, 05 Feb 2025 21:09:10 GMT  
		Size: 125.3 MB (125294045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef9232f14620df5ddd75c38e8536e2dc38aafbd54d2bfda6226a109f99f5299`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07884a1588134bb0a801117ef111cbb694c004ebf303c6c8dc32388fa419aa91`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:55d1d99c78ea7f695366e1f07ccc48922b3045caeca289b4e0767368eaa83f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48f348c4f2e0524eec7febd77aa518f9aa229dfc340dd6eab606dbdc9502bbd`

```dockerfile
```

-	Layers:
	-	`sha256:504aa0de3aae869d6114541f6c6ac7e726d7a4508a022d1ba00f4ac29d7535c9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 13.8 MB (13797371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dde2184bc66bd32204bce88cbc7371a99485196c0e43a95fa2d15fe341889fb`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:12f16f93578c8f27ef56573d8ebc37bbf4de07c25b3bf0ad512876828a19a56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227543471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0f588c0487b02be376314afde244a11084cd855d13e8ab3083fc5bb19795e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d773d0a52e6930fb6520ba17f3154d09b8f7b6ef6830f0ef72939705896c23`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a35c17ac366f0486a55551082beec0ea47f983ac55087f5dc827cfd6d30773`  
		Last Modified: Wed, 05 Feb 2025 21:12:57 GMT  
		Size: 48.5 MB (48511368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749f50233fb227a6c2eda3f0ce65dc48f0c3cf46a24bf2e955e3e8f445176ee4`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67be89c7530466361ccab3fff8fa1cf0d464b19d3f687e155eaff68c05961f1f`  
		Last Modified: Wed, 05 Feb 2025 21:12:58 GMT  
		Size: 123.9 MB (123942090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f615929e74558472742275f41cbd8f3db4b675d69eb6a69220fef7e80c9e82`  
		Last Modified: Wed, 05 Feb 2025 21:12:56 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f51ff414665b511fb1df435ee35ecc523ae78cba9312a0a2d8cafe8b39d2a2`  
		Last Modified: Wed, 05 Feb 2025 21:12:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:c4757b01939b2f7d8c201e0454ff35d447348082d356cbb90710216e95a65411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13830920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800a24ba3bb7be26ae15bd9e2c34310273d2646ff0e255df4e7c8884f715c7bc`

```dockerfile
```

-	Layers:
	-	`sha256:2bf1b6168bba34d4b301ed37dfdeb0d592ad023b69ed547b848c901274c574a5`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 13.8 MB (13795719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e09715807ca8afefc873ade818da47ce53efbb1f8759ffaa1067bec39c2d93`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 35.2 KB (35201 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:eb30abf07b526c96442fbe869f180ece3b6eeef8881464441753e1e3d3d7dec0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:fb32696af3913531215de3958774100c3c7c384c1a5f4affac88a9e07d53153f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183294388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084f0fcc8d8fa02c7e81d672f4a0d6fd686bc09e5aa37b84305fd4de37362d37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 21 Jan 2025 17:15:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1debian12
# Tue, 21 Jan 2025 17:15:14 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8aeb8e8831b179af32de08d2ce497329e90714ba6382ca0bd46aaf605f3522f`  
		Last Modified: Tue, 04 Feb 2025 04:25:28 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0126d6a22dc4a19ba3deda2b1912fd576100a3ccc887341288af61e591348989`  
		Last Modified: Tue, 04 Feb 2025 04:25:29 GMT  
		Size: 4.4 MB (4422795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201a1467d04f383400698a683b5fc55b82bede77ef54661096622829a8bab5d9`  
		Last Modified: Tue, 04 Feb 2025 04:25:29 GMT  
		Size: 1.4 MB (1445974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c268013712b6db1275a840d48ec6c05e810df169396222e3b63d4b4effbfb82`  
		Last Modified: Tue, 04 Feb 2025 04:25:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e857fb30e986a272b561ebf1c87ee0e2a5360f40cd1195d3c974d0024e2641ef`  
		Last Modified: Tue, 04 Feb 2025 04:25:30 GMT  
		Size: 15.3 MB (15296618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4cfc58d880fa41f9ee2b4776fee57a705c464764122b40d7cb0e6c0a38defa`  
		Last Modified: Tue, 04 Feb 2025 04:25:29 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16b9d91ee8cfa26f8c45c5b343f857a79354726f3518d9a8bd2399fa9ff417e`  
		Last Modified: Tue, 04 Feb 2025 04:25:30 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2191414566fd4a760766c3e653de96922d12949228950a623cfaa4b2d626db55`  
		Last Modified: Tue, 04 Feb 2025 04:25:33 GMT  
		Size: 133.9 MB (133906430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fec42382df1d16ad9d7c6e1745616cda351191fdc2ad7003d34e1a8a9e058eb`  
		Last Modified: Tue, 04 Feb 2025 04:25:30 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbfae223e0d1357edca541d03bff1861f6fc9b88144edd1dde0f5c2476e3b5b`  
		Last Modified: Tue, 04 Feb 2025 04:25:31 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af6dece696ad5497656969c9f34e0fef235ac48d50517fabb4f25828ee80906`  
		Last Modified: Tue, 04 Feb 2025 04:25:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:8c24c8124e7a0ede939508115705b0a9b6304f33bf3dc13d1ac01551301bab1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4634d88ca8a2c36ad582358e329ad5bb50cbca2df90c2e7f16e415bcae3e56c`

```dockerfile
```

-	Layers:
	-	`sha256:ebfd98eaf6a19b45589fc93ed71beb7e8df496b35582fe6a9c1cde9ae7a14b8d`  
		Last Modified: Tue, 04 Feb 2025 04:25:29 GMT  
		Size: 4.0 MB (3993808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e37d1fbe22a37f1c697571217087b3e05fbf4bc51f4fbfb518601fb26a87e75a`  
		Last Modified: Tue, 04 Feb 2025 04:25:28 GMT  
		Size: 34.3 KB (34294 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:eb30abf07b526c96442fbe869f180ece3b6eeef8881464441753e1e3d3d7dec0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:fb32696af3913531215de3958774100c3c7c384c1a5f4affac88a9e07d53153f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183294388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084f0fcc8d8fa02c7e81d672f4a0d6fd686bc09e5aa37b84305fd4de37362d37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 21 Jan 2025 17:15:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1debian12
# Tue, 21 Jan 2025 17:15:14 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8aeb8e8831b179af32de08d2ce497329e90714ba6382ca0bd46aaf605f3522f`  
		Last Modified: Tue, 04 Feb 2025 04:25:28 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0126d6a22dc4a19ba3deda2b1912fd576100a3ccc887341288af61e591348989`  
		Last Modified: Tue, 04 Feb 2025 04:25:29 GMT  
		Size: 4.4 MB (4422795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201a1467d04f383400698a683b5fc55b82bede77ef54661096622829a8bab5d9`  
		Last Modified: Tue, 04 Feb 2025 04:25:29 GMT  
		Size: 1.4 MB (1445974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c268013712b6db1275a840d48ec6c05e810df169396222e3b63d4b4effbfb82`  
		Last Modified: Tue, 04 Feb 2025 04:25:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e857fb30e986a272b561ebf1c87ee0e2a5360f40cd1195d3c974d0024e2641ef`  
		Last Modified: Tue, 04 Feb 2025 04:25:30 GMT  
		Size: 15.3 MB (15296618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4cfc58d880fa41f9ee2b4776fee57a705c464764122b40d7cb0e6c0a38defa`  
		Last Modified: Tue, 04 Feb 2025 04:25:29 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16b9d91ee8cfa26f8c45c5b343f857a79354726f3518d9a8bd2399fa9ff417e`  
		Last Modified: Tue, 04 Feb 2025 04:25:30 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2191414566fd4a760766c3e653de96922d12949228950a623cfaa4b2d626db55`  
		Last Modified: Tue, 04 Feb 2025 04:25:33 GMT  
		Size: 133.9 MB (133906430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fec42382df1d16ad9d7c6e1745616cda351191fdc2ad7003d34e1a8a9e058eb`  
		Last Modified: Tue, 04 Feb 2025 04:25:30 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbfae223e0d1357edca541d03bff1861f6fc9b88144edd1dde0f5c2476e3b5b`  
		Last Modified: Tue, 04 Feb 2025 04:25:31 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af6dece696ad5497656969c9f34e0fef235ac48d50517fabb4f25828ee80906`  
		Last Modified: Tue, 04 Feb 2025 04:25:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:8c24c8124e7a0ede939508115705b0a9b6304f33bf3dc13d1ac01551301bab1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4634d88ca8a2c36ad582358e329ad5bb50cbca2df90c2e7f16e415bcae3e56c`

```dockerfile
```

-	Layers:
	-	`sha256:ebfd98eaf6a19b45589fc93ed71beb7e8df496b35582fe6a9c1cde9ae7a14b8d`  
		Last Modified: Tue, 04 Feb 2025 04:25:29 GMT  
		Size: 4.0 MB (3993808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e37d1fbe22a37f1c697571217087b3e05fbf4bc51f4fbfb518601fb26a87e75a`  
		Last Modified: Tue, 04 Feb 2025 04:25:28 GMT  
		Size: 34.3 KB (34294 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:f0657322a50b735bf284dac26e3e3d99e24810ea13d37ef6b7ca6cdd0d54fcc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:ec81f1831771560bd7536a5f85eeefe27e55f5fb4fc23cd5a4fd45464f7d8dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231919727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081ade299f2e2869cda9aa4314b6801b8ddcf851b7b5012e03fa7fbed557fd6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3b09f953cc63439caf29ecc50c8f51b1c5ca3621669505de462d63732fb757`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69038e54211bdb7abde47f6447273edf0c06b28fb3eb63a363277554430145f`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e40652ce5a94d382a18ef147a475c17e7db11051e2f682c149b48d0e3fbc1e`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 6.9 MB (6900810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5c2da6bb37121e624450120b02c75378316291b74e67bbb19b595bd420a969`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6258a15df35b08168c4519b6348854701c13b9de0da12ec6fafdbd467e57c72`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483046b091213e7b6a949a7fbd2dd4adcc461e9fbb6ee9d4e580bfb8a9347608`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 49.6 MB (49634979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fc4435765883fc6ae940e5b638c40de5324b181f6f28fe86431eb53095d6`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4af1f1b7267addd138073877fb479aed3cd576fd2f97b6414aab29dcd06783b`  
		Last Modified: Wed, 05 Feb 2025 21:09:10 GMT  
		Size: 125.3 MB (125294045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef9232f14620df5ddd75c38e8536e2dc38aafbd54d2bfda6226a109f99f5299`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07884a1588134bb0a801117ef111cbb694c004ebf303c6c8dc32388fa419aa91`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:55d1d99c78ea7f695366e1f07ccc48922b3045caeca289b4e0767368eaa83f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48f348c4f2e0524eec7febd77aa518f9aa229dfc340dd6eab606dbdc9502bbd`

```dockerfile
```

-	Layers:
	-	`sha256:504aa0de3aae869d6114541f6c6ac7e726d7a4508a022d1ba00f4ac29d7535c9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 13.8 MB (13797371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dde2184bc66bd32204bce88cbc7371a99485196c0e43a95fa2d15fe341889fb`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:12f16f93578c8f27ef56573d8ebc37bbf4de07c25b3bf0ad512876828a19a56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227543471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0f588c0487b02be376314afde244a11084cd855d13e8ab3083fc5bb19795e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d773d0a52e6930fb6520ba17f3154d09b8f7b6ef6830f0ef72939705896c23`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a35c17ac366f0486a55551082beec0ea47f983ac55087f5dc827cfd6d30773`  
		Last Modified: Wed, 05 Feb 2025 21:12:57 GMT  
		Size: 48.5 MB (48511368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749f50233fb227a6c2eda3f0ce65dc48f0c3cf46a24bf2e955e3e8f445176ee4`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67be89c7530466361ccab3fff8fa1cf0d464b19d3f687e155eaff68c05961f1f`  
		Last Modified: Wed, 05 Feb 2025 21:12:58 GMT  
		Size: 123.9 MB (123942090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f615929e74558472742275f41cbd8f3db4b675d69eb6a69220fef7e80c9e82`  
		Last Modified: Wed, 05 Feb 2025 21:12:56 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f51ff414665b511fb1df435ee35ecc523ae78cba9312a0a2d8cafe8b39d2a2`  
		Last Modified: Wed, 05 Feb 2025 21:12:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:c4757b01939b2f7d8c201e0454ff35d447348082d356cbb90710216e95a65411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13830920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800a24ba3bb7be26ae15bd9e2c34310273d2646ff0e255df4e7c8884f715c7bc`

```dockerfile
```

-	Layers:
	-	`sha256:2bf1b6168bba34d4b301ed37dfdeb0d592ad023b69ed547b848c901274c574a5`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 13.8 MB (13795719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e09715807ca8afefc873ade818da47ce53efbb1f8759ffaa1067bec39c2d93`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 35.2 KB (35201 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:f0657322a50b735bf284dac26e3e3d99e24810ea13d37ef6b7ca6cdd0d54fcc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:ec81f1831771560bd7536a5f85eeefe27e55f5fb4fc23cd5a4fd45464f7d8dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231919727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081ade299f2e2869cda9aa4314b6801b8ddcf851b7b5012e03fa7fbed557fd6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3b09f953cc63439caf29ecc50c8f51b1c5ca3621669505de462d63732fb757`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69038e54211bdb7abde47f6447273edf0c06b28fb3eb63a363277554430145f`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e40652ce5a94d382a18ef147a475c17e7db11051e2f682c149b48d0e3fbc1e`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 6.9 MB (6900810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5c2da6bb37121e624450120b02c75378316291b74e67bbb19b595bd420a969`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6258a15df35b08168c4519b6348854701c13b9de0da12ec6fafdbd467e57c72`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483046b091213e7b6a949a7fbd2dd4adcc461e9fbb6ee9d4e580bfb8a9347608`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 49.6 MB (49634979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fc4435765883fc6ae940e5b638c40de5324b181f6f28fe86431eb53095d6`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4af1f1b7267addd138073877fb479aed3cd576fd2f97b6414aab29dcd06783b`  
		Last Modified: Wed, 05 Feb 2025 21:09:10 GMT  
		Size: 125.3 MB (125294045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef9232f14620df5ddd75c38e8536e2dc38aafbd54d2bfda6226a109f99f5299`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07884a1588134bb0a801117ef111cbb694c004ebf303c6c8dc32388fa419aa91`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:55d1d99c78ea7f695366e1f07ccc48922b3045caeca289b4e0767368eaa83f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48f348c4f2e0524eec7febd77aa518f9aa229dfc340dd6eab606dbdc9502bbd`

```dockerfile
```

-	Layers:
	-	`sha256:504aa0de3aae869d6114541f6c6ac7e726d7a4508a022d1ba00f4ac29d7535c9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 13.8 MB (13797371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dde2184bc66bd32204bce88cbc7371a99485196c0e43a95fa2d15fe341889fb`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:12f16f93578c8f27ef56573d8ebc37bbf4de07c25b3bf0ad512876828a19a56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227543471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0f588c0487b02be376314afde244a11084cd855d13e8ab3083fc5bb19795e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d773d0a52e6930fb6520ba17f3154d09b8f7b6ef6830f0ef72939705896c23`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a35c17ac366f0486a55551082beec0ea47f983ac55087f5dc827cfd6d30773`  
		Last Modified: Wed, 05 Feb 2025 21:12:57 GMT  
		Size: 48.5 MB (48511368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749f50233fb227a6c2eda3f0ce65dc48f0c3cf46a24bf2e955e3e8f445176ee4`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67be89c7530466361ccab3fff8fa1cf0d464b19d3f687e155eaff68c05961f1f`  
		Last Modified: Wed, 05 Feb 2025 21:12:58 GMT  
		Size: 123.9 MB (123942090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f615929e74558472742275f41cbd8f3db4b675d69eb6a69220fef7e80c9e82`  
		Last Modified: Wed, 05 Feb 2025 21:12:56 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f51ff414665b511fb1df435ee35ecc523ae78cba9312a0a2d8cafe8b39d2a2`  
		Last Modified: Wed, 05 Feb 2025 21:12:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:c4757b01939b2f7d8c201e0454ff35d447348082d356cbb90710216e95a65411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13830920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800a24ba3bb7be26ae15bd9e2c34310273d2646ff0e255df4e7c8884f715c7bc`

```dockerfile
```

-	Layers:
	-	`sha256:2bf1b6168bba34d4b301ed37dfdeb0d592ad023b69ed547b848c901274c574a5`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 13.8 MB (13795719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e09715807ca8afefc873ade818da47ce53efbb1f8759ffaa1067bec39c2d93`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 35.2 KB (35201 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.41`

```console
$ docker pull mysql@sha256:f0657322a50b735bf284dac26e3e3d99e24810ea13d37ef6b7ca6cdd0d54fcc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.41` - linux; amd64

```console
$ docker pull mysql@sha256:ec81f1831771560bd7536a5f85eeefe27e55f5fb4fc23cd5a4fd45464f7d8dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231919727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081ade299f2e2869cda9aa4314b6801b8ddcf851b7b5012e03fa7fbed557fd6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3b09f953cc63439caf29ecc50c8f51b1c5ca3621669505de462d63732fb757`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69038e54211bdb7abde47f6447273edf0c06b28fb3eb63a363277554430145f`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e40652ce5a94d382a18ef147a475c17e7db11051e2f682c149b48d0e3fbc1e`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 6.9 MB (6900810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5c2da6bb37121e624450120b02c75378316291b74e67bbb19b595bd420a969`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6258a15df35b08168c4519b6348854701c13b9de0da12ec6fafdbd467e57c72`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483046b091213e7b6a949a7fbd2dd4adcc461e9fbb6ee9d4e580bfb8a9347608`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 49.6 MB (49634979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fc4435765883fc6ae940e5b638c40de5324b181f6f28fe86431eb53095d6`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4af1f1b7267addd138073877fb479aed3cd576fd2f97b6414aab29dcd06783b`  
		Last Modified: Wed, 05 Feb 2025 21:09:10 GMT  
		Size: 125.3 MB (125294045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef9232f14620df5ddd75c38e8536e2dc38aafbd54d2bfda6226a109f99f5299`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07884a1588134bb0a801117ef111cbb694c004ebf303c6c8dc32388fa419aa91`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41` - unknown; unknown

```console
$ docker pull mysql@sha256:55d1d99c78ea7f695366e1f07ccc48922b3045caeca289b4e0767368eaa83f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48f348c4f2e0524eec7febd77aa518f9aa229dfc340dd6eab606dbdc9502bbd`

```dockerfile
```

-	Layers:
	-	`sha256:504aa0de3aae869d6114541f6c6ac7e726d7a4508a022d1ba00f4ac29d7535c9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 13.8 MB (13797371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dde2184bc66bd32204bce88cbc7371a99485196c0e43a95fa2d15fe341889fb`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.41` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:12f16f93578c8f27ef56573d8ebc37bbf4de07c25b3bf0ad512876828a19a56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227543471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0f588c0487b02be376314afde244a11084cd855d13e8ab3083fc5bb19795e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d773d0a52e6930fb6520ba17f3154d09b8f7b6ef6830f0ef72939705896c23`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a35c17ac366f0486a55551082beec0ea47f983ac55087f5dc827cfd6d30773`  
		Last Modified: Wed, 05 Feb 2025 21:12:57 GMT  
		Size: 48.5 MB (48511368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749f50233fb227a6c2eda3f0ce65dc48f0c3cf46a24bf2e955e3e8f445176ee4`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67be89c7530466361ccab3fff8fa1cf0d464b19d3f687e155eaff68c05961f1f`  
		Last Modified: Wed, 05 Feb 2025 21:12:58 GMT  
		Size: 123.9 MB (123942090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f615929e74558472742275f41cbd8f3db4b675d69eb6a69220fef7e80c9e82`  
		Last Modified: Wed, 05 Feb 2025 21:12:56 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f51ff414665b511fb1df435ee35ecc523ae78cba9312a0a2d8cafe8b39d2a2`  
		Last Modified: Wed, 05 Feb 2025 21:12:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41` - unknown; unknown

```console
$ docker pull mysql@sha256:c4757b01939b2f7d8c201e0454ff35d447348082d356cbb90710216e95a65411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13830920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800a24ba3bb7be26ae15bd9e2c34310273d2646ff0e255df4e7c8884f715c7bc`

```dockerfile
```

-	Layers:
	-	`sha256:2bf1b6168bba34d4b301ed37dfdeb0d592ad023b69ed547b848c901274c574a5`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 13.8 MB (13795719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e09715807ca8afefc873ade818da47ce53efbb1f8759ffaa1067bec39c2d93`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 35.2 KB (35201 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.41-bookworm`

```console
$ docker pull mysql@sha256:eb30abf07b526c96442fbe869f180ece3b6eeef8881464441753e1e3d3d7dec0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.41-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:fb32696af3913531215de3958774100c3c7c384c1a5f4affac88a9e07d53153f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183294388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084f0fcc8d8fa02c7e81d672f4a0d6fd686bc09e5aa37b84305fd4de37362d37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 21 Jan 2025 17:15:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1debian12
# Tue, 21 Jan 2025 17:15:14 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8aeb8e8831b179af32de08d2ce497329e90714ba6382ca0bd46aaf605f3522f`  
		Last Modified: Tue, 04 Feb 2025 04:25:28 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0126d6a22dc4a19ba3deda2b1912fd576100a3ccc887341288af61e591348989`  
		Last Modified: Tue, 04 Feb 2025 04:25:29 GMT  
		Size: 4.4 MB (4422795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201a1467d04f383400698a683b5fc55b82bede77ef54661096622829a8bab5d9`  
		Last Modified: Tue, 04 Feb 2025 04:25:29 GMT  
		Size: 1.4 MB (1445974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c268013712b6db1275a840d48ec6c05e810df169396222e3b63d4b4effbfb82`  
		Last Modified: Tue, 04 Feb 2025 04:25:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e857fb30e986a272b561ebf1c87ee0e2a5360f40cd1195d3c974d0024e2641ef`  
		Last Modified: Tue, 04 Feb 2025 04:25:30 GMT  
		Size: 15.3 MB (15296618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4cfc58d880fa41f9ee2b4776fee57a705c464764122b40d7cb0e6c0a38defa`  
		Last Modified: Tue, 04 Feb 2025 04:25:29 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16b9d91ee8cfa26f8c45c5b343f857a79354726f3518d9a8bd2399fa9ff417e`  
		Last Modified: Tue, 04 Feb 2025 04:25:30 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2191414566fd4a760766c3e653de96922d12949228950a623cfaa4b2d626db55`  
		Last Modified: Tue, 04 Feb 2025 04:25:33 GMT  
		Size: 133.9 MB (133906430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fec42382df1d16ad9d7c6e1745616cda351191fdc2ad7003d34e1a8a9e058eb`  
		Last Modified: Tue, 04 Feb 2025 04:25:30 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbfae223e0d1357edca541d03bff1861f6fc9b88144edd1dde0f5c2476e3b5b`  
		Last Modified: Tue, 04 Feb 2025 04:25:31 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af6dece696ad5497656969c9f34e0fef235ac48d50517fabb4f25828ee80906`  
		Last Modified: Tue, 04 Feb 2025 04:25:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:8c24c8124e7a0ede939508115705b0a9b6304f33bf3dc13d1ac01551301bab1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4634d88ca8a2c36ad582358e329ad5bb50cbca2df90c2e7f16e415bcae3e56c`

```dockerfile
```

-	Layers:
	-	`sha256:ebfd98eaf6a19b45589fc93ed71beb7e8df496b35582fe6a9c1cde9ae7a14b8d`  
		Last Modified: Tue, 04 Feb 2025 04:25:29 GMT  
		Size: 4.0 MB (3993808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e37d1fbe22a37f1c697571217087b3e05fbf4bc51f4fbfb518601fb26a87e75a`  
		Last Modified: Tue, 04 Feb 2025 04:25:28 GMT  
		Size: 34.3 KB (34294 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.41-debian`

```console
$ docker pull mysql@sha256:eb30abf07b526c96442fbe869f180ece3b6eeef8881464441753e1e3d3d7dec0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.41-debian` - linux; amd64

```console
$ docker pull mysql@sha256:fb32696af3913531215de3958774100c3c7c384c1a5f4affac88a9e07d53153f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183294388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084f0fcc8d8fa02c7e81d672f4a0d6fd686bc09e5aa37b84305fd4de37362d37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 21 Jan 2025 17:15:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1debian12
# Tue, 21 Jan 2025 17:15:14 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8aeb8e8831b179af32de08d2ce497329e90714ba6382ca0bd46aaf605f3522f`  
		Last Modified: Tue, 04 Feb 2025 04:25:28 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0126d6a22dc4a19ba3deda2b1912fd576100a3ccc887341288af61e591348989`  
		Last Modified: Tue, 04 Feb 2025 04:25:29 GMT  
		Size: 4.4 MB (4422795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201a1467d04f383400698a683b5fc55b82bede77ef54661096622829a8bab5d9`  
		Last Modified: Tue, 04 Feb 2025 04:25:29 GMT  
		Size: 1.4 MB (1445974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c268013712b6db1275a840d48ec6c05e810df169396222e3b63d4b4effbfb82`  
		Last Modified: Tue, 04 Feb 2025 04:25:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e857fb30e986a272b561ebf1c87ee0e2a5360f40cd1195d3c974d0024e2641ef`  
		Last Modified: Tue, 04 Feb 2025 04:25:30 GMT  
		Size: 15.3 MB (15296618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4cfc58d880fa41f9ee2b4776fee57a705c464764122b40d7cb0e6c0a38defa`  
		Last Modified: Tue, 04 Feb 2025 04:25:29 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16b9d91ee8cfa26f8c45c5b343f857a79354726f3518d9a8bd2399fa9ff417e`  
		Last Modified: Tue, 04 Feb 2025 04:25:30 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2191414566fd4a760766c3e653de96922d12949228950a623cfaa4b2d626db55`  
		Last Modified: Tue, 04 Feb 2025 04:25:33 GMT  
		Size: 133.9 MB (133906430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fec42382df1d16ad9d7c6e1745616cda351191fdc2ad7003d34e1a8a9e058eb`  
		Last Modified: Tue, 04 Feb 2025 04:25:30 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbfae223e0d1357edca541d03bff1861f6fc9b88144edd1dde0f5c2476e3b5b`  
		Last Modified: Tue, 04 Feb 2025 04:25:31 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af6dece696ad5497656969c9f34e0fef235ac48d50517fabb4f25828ee80906`  
		Last Modified: Tue, 04 Feb 2025 04:25:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:8c24c8124e7a0ede939508115705b0a9b6304f33bf3dc13d1ac01551301bab1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4634d88ca8a2c36ad582358e329ad5bb50cbca2df90c2e7f16e415bcae3e56c`

```dockerfile
```

-	Layers:
	-	`sha256:ebfd98eaf6a19b45589fc93ed71beb7e8df496b35582fe6a9c1cde9ae7a14b8d`  
		Last Modified: Tue, 04 Feb 2025 04:25:29 GMT  
		Size: 4.0 MB (3993808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e37d1fbe22a37f1c697571217087b3e05fbf4bc51f4fbfb518601fb26a87e75a`  
		Last Modified: Tue, 04 Feb 2025 04:25:28 GMT  
		Size: 34.3 KB (34294 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.41-oracle`

```console
$ docker pull mysql@sha256:f0657322a50b735bf284dac26e3e3d99e24810ea13d37ef6b7ca6cdd0d54fcc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.41-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:ec81f1831771560bd7536a5f85eeefe27e55f5fb4fc23cd5a4fd45464f7d8dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231919727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081ade299f2e2869cda9aa4314b6801b8ddcf851b7b5012e03fa7fbed557fd6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3b09f953cc63439caf29ecc50c8f51b1c5ca3621669505de462d63732fb757`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69038e54211bdb7abde47f6447273edf0c06b28fb3eb63a363277554430145f`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e40652ce5a94d382a18ef147a475c17e7db11051e2f682c149b48d0e3fbc1e`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 6.9 MB (6900810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5c2da6bb37121e624450120b02c75378316291b74e67bbb19b595bd420a969`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6258a15df35b08168c4519b6348854701c13b9de0da12ec6fafdbd467e57c72`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483046b091213e7b6a949a7fbd2dd4adcc461e9fbb6ee9d4e580bfb8a9347608`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 49.6 MB (49634979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fc4435765883fc6ae940e5b638c40de5324b181f6f28fe86431eb53095d6`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4af1f1b7267addd138073877fb479aed3cd576fd2f97b6414aab29dcd06783b`  
		Last Modified: Wed, 05 Feb 2025 21:09:10 GMT  
		Size: 125.3 MB (125294045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef9232f14620df5ddd75c38e8536e2dc38aafbd54d2bfda6226a109f99f5299`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07884a1588134bb0a801117ef111cbb694c004ebf303c6c8dc32388fa419aa91`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:55d1d99c78ea7f695366e1f07ccc48922b3045caeca289b4e0767368eaa83f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48f348c4f2e0524eec7febd77aa518f9aa229dfc340dd6eab606dbdc9502bbd`

```dockerfile
```

-	Layers:
	-	`sha256:504aa0de3aae869d6114541f6c6ac7e726d7a4508a022d1ba00f4ac29d7535c9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 13.8 MB (13797371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dde2184bc66bd32204bce88cbc7371a99485196c0e43a95fa2d15fe341889fb`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.41-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:12f16f93578c8f27ef56573d8ebc37bbf4de07c25b3bf0ad512876828a19a56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227543471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0f588c0487b02be376314afde244a11084cd855d13e8ab3083fc5bb19795e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d773d0a52e6930fb6520ba17f3154d09b8f7b6ef6830f0ef72939705896c23`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a35c17ac366f0486a55551082beec0ea47f983ac55087f5dc827cfd6d30773`  
		Last Modified: Wed, 05 Feb 2025 21:12:57 GMT  
		Size: 48.5 MB (48511368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749f50233fb227a6c2eda3f0ce65dc48f0c3cf46a24bf2e955e3e8f445176ee4`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67be89c7530466361ccab3fff8fa1cf0d464b19d3f687e155eaff68c05961f1f`  
		Last Modified: Wed, 05 Feb 2025 21:12:58 GMT  
		Size: 123.9 MB (123942090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f615929e74558472742275f41cbd8f3db4b675d69eb6a69220fef7e80c9e82`  
		Last Modified: Wed, 05 Feb 2025 21:12:56 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f51ff414665b511fb1df435ee35ecc523ae78cba9312a0a2d8cafe8b39d2a2`  
		Last Modified: Wed, 05 Feb 2025 21:12:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:c4757b01939b2f7d8c201e0454ff35d447348082d356cbb90710216e95a65411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13830920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800a24ba3bb7be26ae15bd9e2c34310273d2646ff0e255df4e7c8884f715c7bc`

```dockerfile
```

-	Layers:
	-	`sha256:2bf1b6168bba34d4b301ed37dfdeb0d592ad023b69ed547b848c901274c574a5`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 13.8 MB (13795719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e09715807ca8afefc873ade818da47ce53efbb1f8759ffaa1067bec39c2d93`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 35.2 KB (35201 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.41-oraclelinux9`

```console
$ docker pull mysql@sha256:f0657322a50b735bf284dac26e3e3d99e24810ea13d37ef6b7ca6cdd0d54fcc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.41-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:ec81f1831771560bd7536a5f85eeefe27e55f5fb4fc23cd5a4fd45464f7d8dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231919727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081ade299f2e2869cda9aa4314b6801b8ddcf851b7b5012e03fa7fbed557fd6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3b09f953cc63439caf29ecc50c8f51b1c5ca3621669505de462d63732fb757`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69038e54211bdb7abde47f6447273edf0c06b28fb3eb63a363277554430145f`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e40652ce5a94d382a18ef147a475c17e7db11051e2f682c149b48d0e3fbc1e`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 6.9 MB (6900810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5c2da6bb37121e624450120b02c75378316291b74e67bbb19b595bd420a969`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6258a15df35b08168c4519b6348854701c13b9de0da12ec6fafdbd467e57c72`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483046b091213e7b6a949a7fbd2dd4adcc461e9fbb6ee9d4e580bfb8a9347608`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 49.6 MB (49634979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fc4435765883fc6ae940e5b638c40de5324b181f6f28fe86431eb53095d6`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4af1f1b7267addd138073877fb479aed3cd576fd2f97b6414aab29dcd06783b`  
		Last Modified: Wed, 05 Feb 2025 21:09:10 GMT  
		Size: 125.3 MB (125294045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef9232f14620df5ddd75c38e8536e2dc38aafbd54d2bfda6226a109f99f5299`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07884a1588134bb0a801117ef111cbb694c004ebf303c6c8dc32388fa419aa91`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:55d1d99c78ea7f695366e1f07ccc48922b3045caeca289b4e0767368eaa83f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48f348c4f2e0524eec7febd77aa518f9aa229dfc340dd6eab606dbdc9502bbd`

```dockerfile
```

-	Layers:
	-	`sha256:504aa0de3aae869d6114541f6c6ac7e726d7a4508a022d1ba00f4ac29d7535c9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 13.8 MB (13797371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dde2184bc66bd32204bce88cbc7371a99485196c0e43a95fa2d15fe341889fb`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.41-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:12f16f93578c8f27ef56573d8ebc37bbf4de07c25b3bf0ad512876828a19a56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227543471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0f588c0487b02be376314afde244a11084cd855d13e8ab3083fc5bb19795e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d773d0a52e6930fb6520ba17f3154d09b8f7b6ef6830f0ef72939705896c23`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a35c17ac366f0486a55551082beec0ea47f983ac55087f5dc827cfd6d30773`  
		Last Modified: Wed, 05 Feb 2025 21:12:57 GMT  
		Size: 48.5 MB (48511368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749f50233fb227a6c2eda3f0ce65dc48f0c3cf46a24bf2e955e3e8f445176ee4`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67be89c7530466361ccab3fff8fa1cf0d464b19d3f687e155eaff68c05961f1f`  
		Last Modified: Wed, 05 Feb 2025 21:12:58 GMT  
		Size: 123.9 MB (123942090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f615929e74558472742275f41cbd8f3db4b675d69eb6a69220fef7e80c9e82`  
		Last Modified: Wed, 05 Feb 2025 21:12:56 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f51ff414665b511fb1df435ee35ecc523ae78cba9312a0a2d8cafe8b39d2a2`  
		Last Modified: Wed, 05 Feb 2025 21:12:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:c4757b01939b2f7d8c201e0454ff35d447348082d356cbb90710216e95a65411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13830920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800a24ba3bb7be26ae15bd9e2c34310273d2646ff0e255df4e7c8884f715c7bc`

```dockerfile
```

-	Layers:
	-	`sha256:2bf1b6168bba34d4b301ed37dfdeb0d592ad023b69ed547b848c901274c574a5`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 13.8 MB (13795719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e09715807ca8afefc873ade818da47ce53efbb1f8759ffaa1067bec39c2d93`  
		Last Modified: Wed, 05 Feb 2025 21:12:55 GMT  
		Size: 35.2 KB (35201 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:b14b2b73fc1242bef8fc21cbd73f247396f353cf314734d3502d72eb1ed0d93b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:d50d35b5bd33e90185cf7c9752a8a9c4e322752d9d441aead65d55a5a7a9b0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232921620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03152aa0b71af6d9c2d3ce540cb012fbe4f2c902896c7572baa29e9c2c863d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953a4ccd23a81b87fee3f10c6f7b0f64a28cddf2b44ae4709ed11ba1ddce2801`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f496cf111703223486f94eab0e33c24d2f2d42e3048ade9f846bee4d2c216d78`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba398fbba1a319bb6b0e8072ab3967941541520c4ea0cc9de237fe0fb5c24bf`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 6.9 MB (6900797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612294d2b805abc144afdb56ea7c4c853afb0848da8ba320ded974bfea920c0d`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b72e8cade85158d043b1cc49db60f3192b21928519bd37effb9455ff838774`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16088fb0c0bc6fed09b5f1901cd8932898f9533922d16e2ea76ec6713d3a6e9f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 47.6 MB (47593441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1113808e87139e81bf5791ef5f9a4cfb6340d3744c071b06378e5dd4300cf2`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb634a27ea9af9512a616770be962abb004a69340d9293672318762c88e6f0da`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 128.3 MB (128337606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779e768d23c147ac6ff98cad8c97e9fd64ae88e6fa64c36af645e92f9760640`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:8e27ad713932c235a3a2ba33c8afaf2f24be95c06cf5581d42a16e27cc34902c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e722b0900dddd12a388283e5a5536b2d3136467cab0738958c593d01ae72c0`

```dockerfile
```

-	Layers:
	-	`sha256:a1e7f0e8c496cb14802c1bfd6677f68818d049e581b7a09366a16c80701e32ef`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 14.1 MB (14074192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07d6bfb3db9fb8c16f6075a18e084c2af417f5624c0d7a8e3173a3c498488a4`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b069ea7a6e799b97b7cda674dc14af372a3e819e8167ca7f9f2b25d271ba21c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228373891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143ee6a01dfafb0fc64201d822bf454604f2f23e7de391d6ded6bed4d0f10d2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6d58e993cc8f74278b7b31bc7d5c3a90f3a641fa669d7f9baa0c8bb3f22b99`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89597d03bec9a798d018a2da6d72618fd411ee3be7cfba13b6f84a54a2ff094e`  
		Last Modified: Wed, 05 Feb 2025 21:11:25 GMT  
		Size: 46.5 MB (46472784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b25528c202a2c51e7345274b2ba9194d3e40ad59c4564ca8bda7c62adc296d7`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5176c942bb7758f3748ca374a5f473ec23d3aa80f84498adb45b23c52246574`  
		Last Modified: Wed, 05 Feb 2025 21:11:26 GMT  
		Size: 126.8 MB (126811206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f10df86d743ce521a9a6df46866fb0db04ee299e86f50ebf6a1a9be951c4afa`  
		Last Modified: Wed, 05 Feb 2025 21:11:24 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:9f201d54b76a028b5603016be80583ff3ce499109d5e9b51b6b5c0297cbf4535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7090fba013cec374dc2272b28151f052a2618f48262644077be4d3447039c7`

```dockerfile
```

-	Layers:
	-	`sha256:976a24bbc9d8d48ab0628f1df0c95711404a4ef73eec2286b7e272fbe4c09e72`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 14.1 MB (14072612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9fcf77de5ba79f3b92a0c9269899881dddef44c3ad957f19afa19b2d763ddbc`  
		Last Modified: Wed, 05 Feb 2025 21:11:22 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:b14b2b73fc1242bef8fc21cbd73f247396f353cf314734d3502d72eb1ed0d93b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d50d35b5bd33e90185cf7c9752a8a9c4e322752d9d441aead65d55a5a7a9b0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232921620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03152aa0b71af6d9c2d3ce540cb012fbe4f2c902896c7572baa29e9c2c863d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953a4ccd23a81b87fee3f10c6f7b0f64a28cddf2b44ae4709ed11ba1ddce2801`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f496cf111703223486f94eab0e33c24d2f2d42e3048ade9f846bee4d2c216d78`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba398fbba1a319bb6b0e8072ab3967941541520c4ea0cc9de237fe0fb5c24bf`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 6.9 MB (6900797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612294d2b805abc144afdb56ea7c4c853afb0848da8ba320ded974bfea920c0d`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b72e8cade85158d043b1cc49db60f3192b21928519bd37effb9455ff838774`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16088fb0c0bc6fed09b5f1901cd8932898f9533922d16e2ea76ec6713d3a6e9f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 47.6 MB (47593441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1113808e87139e81bf5791ef5f9a4cfb6340d3744c071b06378e5dd4300cf2`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb634a27ea9af9512a616770be962abb004a69340d9293672318762c88e6f0da`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 128.3 MB (128337606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779e768d23c147ac6ff98cad8c97e9fd64ae88e6fa64c36af645e92f9760640`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:8e27ad713932c235a3a2ba33c8afaf2f24be95c06cf5581d42a16e27cc34902c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e722b0900dddd12a388283e5a5536b2d3136467cab0738958c593d01ae72c0`

```dockerfile
```

-	Layers:
	-	`sha256:a1e7f0e8c496cb14802c1bfd6677f68818d049e581b7a09366a16c80701e32ef`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 14.1 MB (14074192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07d6bfb3db9fb8c16f6075a18e084c2af417f5624c0d7a8e3173a3c498488a4`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b069ea7a6e799b97b7cda674dc14af372a3e819e8167ca7f9f2b25d271ba21c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228373891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143ee6a01dfafb0fc64201d822bf454604f2f23e7de391d6ded6bed4d0f10d2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6d58e993cc8f74278b7b31bc7d5c3a90f3a641fa669d7f9baa0c8bb3f22b99`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89597d03bec9a798d018a2da6d72618fd411ee3be7cfba13b6f84a54a2ff094e`  
		Last Modified: Wed, 05 Feb 2025 21:11:25 GMT  
		Size: 46.5 MB (46472784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b25528c202a2c51e7345274b2ba9194d3e40ad59c4564ca8bda7c62adc296d7`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5176c942bb7758f3748ca374a5f473ec23d3aa80f84498adb45b23c52246574`  
		Last Modified: Wed, 05 Feb 2025 21:11:26 GMT  
		Size: 126.8 MB (126811206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f10df86d743ce521a9a6df46866fb0db04ee299e86f50ebf6a1a9be951c4afa`  
		Last Modified: Wed, 05 Feb 2025 21:11:24 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9f201d54b76a028b5603016be80583ff3ce499109d5e9b51b6b5c0297cbf4535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7090fba013cec374dc2272b28151f052a2618f48262644077be4d3447039c7`

```dockerfile
```

-	Layers:
	-	`sha256:976a24bbc9d8d48ab0628f1df0c95711404a4ef73eec2286b7e272fbe4c09e72`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 14.1 MB (14072612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9fcf77de5ba79f3b92a0c9269899881dddef44c3ad957f19afa19b2d763ddbc`  
		Last Modified: Wed, 05 Feb 2025 21:11:22 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:b14b2b73fc1242bef8fc21cbd73f247396f353cf314734d3502d72eb1ed0d93b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d50d35b5bd33e90185cf7c9752a8a9c4e322752d9d441aead65d55a5a7a9b0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232921620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03152aa0b71af6d9c2d3ce540cb012fbe4f2c902896c7572baa29e9c2c863d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953a4ccd23a81b87fee3f10c6f7b0f64a28cddf2b44ae4709ed11ba1ddce2801`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f496cf111703223486f94eab0e33c24d2f2d42e3048ade9f846bee4d2c216d78`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba398fbba1a319bb6b0e8072ab3967941541520c4ea0cc9de237fe0fb5c24bf`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 6.9 MB (6900797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612294d2b805abc144afdb56ea7c4c853afb0848da8ba320ded974bfea920c0d`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b72e8cade85158d043b1cc49db60f3192b21928519bd37effb9455ff838774`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16088fb0c0bc6fed09b5f1901cd8932898f9533922d16e2ea76ec6713d3a6e9f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 47.6 MB (47593441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1113808e87139e81bf5791ef5f9a4cfb6340d3744c071b06378e5dd4300cf2`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb634a27ea9af9512a616770be962abb004a69340d9293672318762c88e6f0da`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 128.3 MB (128337606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779e768d23c147ac6ff98cad8c97e9fd64ae88e6fa64c36af645e92f9760640`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:8e27ad713932c235a3a2ba33c8afaf2f24be95c06cf5581d42a16e27cc34902c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e722b0900dddd12a388283e5a5536b2d3136467cab0738958c593d01ae72c0`

```dockerfile
```

-	Layers:
	-	`sha256:a1e7f0e8c496cb14802c1bfd6677f68818d049e581b7a09366a16c80701e32ef`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 14.1 MB (14074192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07d6bfb3db9fb8c16f6075a18e084c2af417f5624c0d7a8e3173a3c498488a4`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b069ea7a6e799b97b7cda674dc14af372a3e819e8167ca7f9f2b25d271ba21c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228373891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143ee6a01dfafb0fc64201d822bf454604f2f23e7de391d6ded6bed4d0f10d2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6d58e993cc8f74278b7b31bc7d5c3a90f3a641fa669d7f9baa0c8bb3f22b99`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89597d03bec9a798d018a2da6d72618fd411ee3be7cfba13b6f84a54a2ff094e`  
		Last Modified: Wed, 05 Feb 2025 21:11:25 GMT  
		Size: 46.5 MB (46472784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b25528c202a2c51e7345274b2ba9194d3e40ad59c4564ca8bda7c62adc296d7`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5176c942bb7758f3748ca374a5f473ec23d3aa80f84498adb45b23c52246574`  
		Last Modified: Wed, 05 Feb 2025 21:11:26 GMT  
		Size: 126.8 MB (126811206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f10df86d743ce521a9a6df46866fb0db04ee299e86f50ebf6a1a9be951c4afa`  
		Last Modified: Wed, 05 Feb 2025 21:11:24 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9f201d54b76a028b5603016be80583ff3ce499109d5e9b51b6b5c0297cbf4535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7090fba013cec374dc2272b28151f052a2618f48262644077be4d3447039c7`

```dockerfile
```

-	Layers:
	-	`sha256:976a24bbc9d8d48ab0628f1df0c95711404a4ef73eec2286b7e272fbe4c09e72`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 14.1 MB (14072612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9fcf77de5ba79f3b92a0c9269899881dddef44c3ad957f19afa19b2d763ddbc`  
		Last Modified: Wed, 05 Feb 2025 21:11:22 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.4`

```console
$ docker pull mysql@sha256:b14b2b73fc1242bef8fc21cbd73f247396f353cf314734d3502d72eb1ed0d93b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.4` - linux; amd64

```console
$ docker pull mysql@sha256:d50d35b5bd33e90185cf7c9752a8a9c4e322752d9d441aead65d55a5a7a9b0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232921620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03152aa0b71af6d9c2d3ce540cb012fbe4f2c902896c7572baa29e9c2c863d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953a4ccd23a81b87fee3f10c6f7b0f64a28cddf2b44ae4709ed11ba1ddce2801`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f496cf111703223486f94eab0e33c24d2f2d42e3048ade9f846bee4d2c216d78`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba398fbba1a319bb6b0e8072ab3967941541520c4ea0cc9de237fe0fb5c24bf`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 6.9 MB (6900797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612294d2b805abc144afdb56ea7c4c853afb0848da8ba320ded974bfea920c0d`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b72e8cade85158d043b1cc49db60f3192b21928519bd37effb9455ff838774`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16088fb0c0bc6fed09b5f1901cd8932898f9533922d16e2ea76ec6713d3a6e9f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 47.6 MB (47593441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1113808e87139e81bf5791ef5f9a4cfb6340d3744c071b06378e5dd4300cf2`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb634a27ea9af9512a616770be962abb004a69340d9293672318762c88e6f0da`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 128.3 MB (128337606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779e768d23c147ac6ff98cad8c97e9fd64ae88e6fa64c36af645e92f9760640`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4` - unknown; unknown

```console
$ docker pull mysql@sha256:8e27ad713932c235a3a2ba33c8afaf2f24be95c06cf5581d42a16e27cc34902c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e722b0900dddd12a388283e5a5536b2d3136467cab0738958c593d01ae72c0`

```dockerfile
```

-	Layers:
	-	`sha256:a1e7f0e8c496cb14802c1bfd6677f68818d049e581b7a09366a16c80701e32ef`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 14.1 MB (14074192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07d6bfb3db9fb8c16f6075a18e084c2af417f5624c0d7a8e3173a3c498488a4`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b069ea7a6e799b97b7cda674dc14af372a3e819e8167ca7f9f2b25d271ba21c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228373891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143ee6a01dfafb0fc64201d822bf454604f2f23e7de391d6ded6bed4d0f10d2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6d58e993cc8f74278b7b31bc7d5c3a90f3a641fa669d7f9baa0c8bb3f22b99`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89597d03bec9a798d018a2da6d72618fd411ee3be7cfba13b6f84a54a2ff094e`  
		Last Modified: Wed, 05 Feb 2025 21:11:25 GMT  
		Size: 46.5 MB (46472784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b25528c202a2c51e7345274b2ba9194d3e40ad59c4564ca8bda7c62adc296d7`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5176c942bb7758f3748ca374a5f473ec23d3aa80f84498adb45b23c52246574`  
		Last Modified: Wed, 05 Feb 2025 21:11:26 GMT  
		Size: 126.8 MB (126811206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f10df86d743ce521a9a6df46866fb0db04ee299e86f50ebf6a1a9be951c4afa`  
		Last Modified: Wed, 05 Feb 2025 21:11:24 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4` - unknown; unknown

```console
$ docker pull mysql@sha256:9f201d54b76a028b5603016be80583ff3ce499109d5e9b51b6b5c0297cbf4535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7090fba013cec374dc2272b28151f052a2618f48262644077be4d3447039c7`

```dockerfile
```

-	Layers:
	-	`sha256:976a24bbc9d8d48ab0628f1df0c95711404a4ef73eec2286b7e272fbe4c09e72`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 14.1 MB (14072612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9fcf77de5ba79f3b92a0c9269899881dddef44c3ad957f19afa19b2d763ddbc`  
		Last Modified: Wed, 05 Feb 2025 21:11:22 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.4-oracle`

```console
$ docker pull mysql@sha256:b14b2b73fc1242bef8fc21cbd73f247396f353cf314734d3502d72eb1ed0d93b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d50d35b5bd33e90185cf7c9752a8a9c4e322752d9d441aead65d55a5a7a9b0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232921620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03152aa0b71af6d9c2d3ce540cb012fbe4f2c902896c7572baa29e9c2c863d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953a4ccd23a81b87fee3f10c6f7b0f64a28cddf2b44ae4709ed11ba1ddce2801`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f496cf111703223486f94eab0e33c24d2f2d42e3048ade9f846bee4d2c216d78`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba398fbba1a319bb6b0e8072ab3967941541520c4ea0cc9de237fe0fb5c24bf`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 6.9 MB (6900797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612294d2b805abc144afdb56ea7c4c853afb0848da8ba320ded974bfea920c0d`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b72e8cade85158d043b1cc49db60f3192b21928519bd37effb9455ff838774`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16088fb0c0bc6fed09b5f1901cd8932898f9533922d16e2ea76ec6713d3a6e9f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 47.6 MB (47593441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1113808e87139e81bf5791ef5f9a4cfb6340d3744c071b06378e5dd4300cf2`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb634a27ea9af9512a616770be962abb004a69340d9293672318762c88e6f0da`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 128.3 MB (128337606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779e768d23c147ac6ff98cad8c97e9fd64ae88e6fa64c36af645e92f9760640`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:8e27ad713932c235a3a2ba33c8afaf2f24be95c06cf5581d42a16e27cc34902c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e722b0900dddd12a388283e5a5536b2d3136467cab0738958c593d01ae72c0`

```dockerfile
```

-	Layers:
	-	`sha256:a1e7f0e8c496cb14802c1bfd6677f68818d049e581b7a09366a16c80701e32ef`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 14.1 MB (14074192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07d6bfb3db9fb8c16f6075a18e084c2af417f5624c0d7a8e3173a3c498488a4`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b069ea7a6e799b97b7cda674dc14af372a3e819e8167ca7f9f2b25d271ba21c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228373891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143ee6a01dfafb0fc64201d822bf454604f2f23e7de391d6ded6bed4d0f10d2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6d58e993cc8f74278b7b31bc7d5c3a90f3a641fa669d7f9baa0c8bb3f22b99`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89597d03bec9a798d018a2da6d72618fd411ee3be7cfba13b6f84a54a2ff094e`  
		Last Modified: Wed, 05 Feb 2025 21:11:25 GMT  
		Size: 46.5 MB (46472784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b25528c202a2c51e7345274b2ba9194d3e40ad59c4564ca8bda7c62adc296d7`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5176c942bb7758f3748ca374a5f473ec23d3aa80f84498adb45b23c52246574`  
		Last Modified: Wed, 05 Feb 2025 21:11:26 GMT  
		Size: 126.8 MB (126811206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f10df86d743ce521a9a6df46866fb0db04ee299e86f50ebf6a1a9be951c4afa`  
		Last Modified: Wed, 05 Feb 2025 21:11:24 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9f201d54b76a028b5603016be80583ff3ce499109d5e9b51b6b5c0297cbf4535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7090fba013cec374dc2272b28151f052a2618f48262644077be4d3447039c7`

```dockerfile
```

-	Layers:
	-	`sha256:976a24bbc9d8d48ab0628f1df0c95711404a4ef73eec2286b7e272fbe4c09e72`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 14.1 MB (14072612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9fcf77de5ba79f3b92a0c9269899881dddef44c3ad957f19afa19b2d763ddbc`  
		Last Modified: Wed, 05 Feb 2025 21:11:22 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.4-oraclelinux9`

```console
$ docker pull mysql@sha256:b14b2b73fc1242bef8fc21cbd73f247396f353cf314734d3502d72eb1ed0d93b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d50d35b5bd33e90185cf7c9752a8a9c4e322752d9d441aead65d55a5a7a9b0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232921620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03152aa0b71af6d9c2d3ce540cb012fbe4f2c902896c7572baa29e9c2c863d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953a4ccd23a81b87fee3f10c6f7b0f64a28cddf2b44ae4709ed11ba1ddce2801`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f496cf111703223486f94eab0e33c24d2f2d42e3048ade9f846bee4d2c216d78`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba398fbba1a319bb6b0e8072ab3967941541520c4ea0cc9de237fe0fb5c24bf`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 6.9 MB (6900797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612294d2b805abc144afdb56ea7c4c853afb0848da8ba320ded974bfea920c0d`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b72e8cade85158d043b1cc49db60f3192b21928519bd37effb9455ff838774`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16088fb0c0bc6fed09b5f1901cd8932898f9533922d16e2ea76ec6713d3a6e9f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 47.6 MB (47593441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1113808e87139e81bf5791ef5f9a4cfb6340d3744c071b06378e5dd4300cf2`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb634a27ea9af9512a616770be962abb004a69340d9293672318762c88e6f0da`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 128.3 MB (128337606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779e768d23c147ac6ff98cad8c97e9fd64ae88e6fa64c36af645e92f9760640`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:8e27ad713932c235a3a2ba33c8afaf2f24be95c06cf5581d42a16e27cc34902c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e722b0900dddd12a388283e5a5536b2d3136467cab0738958c593d01ae72c0`

```dockerfile
```

-	Layers:
	-	`sha256:a1e7f0e8c496cb14802c1bfd6677f68818d049e581b7a09366a16c80701e32ef`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 14.1 MB (14074192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07d6bfb3db9fb8c16f6075a18e084c2af417f5624c0d7a8e3173a3c498488a4`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b069ea7a6e799b97b7cda674dc14af372a3e819e8167ca7f9f2b25d271ba21c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228373891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143ee6a01dfafb0fc64201d822bf454604f2f23e7de391d6ded6bed4d0f10d2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6d58e993cc8f74278b7b31bc7d5c3a90f3a641fa669d7f9baa0c8bb3f22b99`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89597d03bec9a798d018a2da6d72618fd411ee3be7cfba13b6f84a54a2ff094e`  
		Last Modified: Wed, 05 Feb 2025 21:11:25 GMT  
		Size: 46.5 MB (46472784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b25528c202a2c51e7345274b2ba9194d3e40ad59c4564ca8bda7c62adc296d7`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5176c942bb7758f3748ca374a5f473ec23d3aa80f84498adb45b23c52246574`  
		Last Modified: Wed, 05 Feb 2025 21:11:26 GMT  
		Size: 126.8 MB (126811206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f10df86d743ce521a9a6df46866fb0db04ee299e86f50ebf6a1a9be951c4afa`  
		Last Modified: Wed, 05 Feb 2025 21:11:24 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9f201d54b76a028b5603016be80583ff3ce499109d5e9b51b6b5c0297cbf4535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7090fba013cec374dc2272b28151f052a2618f48262644077be4d3447039c7`

```dockerfile
```

-	Layers:
	-	`sha256:976a24bbc9d8d48ab0628f1df0c95711404a4ef73eec2286b7e272fbe4c09e72`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 14.1 MB (14072612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9fcf77de5ba79f3b92a0c9269899881dddef44c3ad957f19afa19b2d763ddbc`  
		Last Modified: Wed, 05 Feb 2025 21:11:22 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:d56d039139a7f3b71f6d1c9f07ca4ee9f977b0fca13acdd27a1b13bfd4a4e3be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:c5eb2eeec0f383a613a984912221b663b49b015badcddf7baed7bdf22b7ed8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241152697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e34946bc4c418b9083622074deea6115aebefb4557d998897162bea8433f083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e59b1e9b7fc9a9eb4fa1fa5fc8607972c2670dd75fc4c50a7205aafa69c500f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf87f630bc84600161859d58a329ef80f43f44bdd85f320a416ec93aaadcd19`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886200dd5e38fb52ed314896a9b344e554158dd919db3187dda896573bbf38cb`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 6.9 MB (6900832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49812044423fc2929b886ef6091fd13267cdabb96e896e6ebae63b5bec66bff`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48319207fe201d8999054f5f48f9aff4aa14c19b5c6c4585e59076b0b0e88c7`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4312bbe95c6f45e596d3da7932dccce0bcacfc7817c28b063aa53092ab3e156`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 48.4 MB (48427656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd0a00427a8af6fd510a7debec37d4c9a4ff8b06c0105cfedcb9006985779f9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4e973a399acea71133d05cca20b12cd764fc541d730141b2bfff3b22d163e0`  
		Last Modified: Wed, 05 Feb 2025 21:09:11 GMT  
		Size: 135.7 MB (135734421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274b57fed122cc63adc4c52fbb798ac3c05dc98f77234ac33a474d41e6ff0b8e`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:b0accdd2aa5646c134aa14b2c50110091a309a2341c90f4acdf18df087dc87e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7c86c3f0ebc620528bbce4a7d75a2881ef0ac6a08b6952b4e982d8ce51fc21`

```dockerfile
```

-	Layers:
	-	`sha256:a80ea3072404b2cfa11c0387192290373eb59794e4e4481b5d9f13223da5b84d`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 14.1 MB (14084479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c27537cf70b90e7ef9d57e2f874e8a70e6089c6a51f8d0cc5eaaceab0e6ed74`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:add44c19ad3a11160d69598c8f040f909be0ffd292009de81446ffca0faaa175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236525463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdc083700d09d1089086647e63601adb73c90cefee1921b21af6b86f5031bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08781f18c7788abfbf773236db8d818d48da0dcbf28916eb63ef529f986bc4d`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02e7cdef9c23061e5ac9d03b340af65eb24b3a33c1cf9a70740a32ba64524af`  
		Last Modified: Wed, 05 Feb 2025 21:09:46 GMT  
		Size: 47.3 MB (47297946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f9f0e2e076fedb14c415158459505fb8a5bcfd31aab654f292b23fb6e97059`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2573d09c11f17b9435be5eb631776a7d68d9a248f99cfb276a050ee8661c8d1`  
		Last Modified: Wed, 05 Feb 2025 21:09:47 GMT  
		Size: 134.1 MB (134137606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c94852e619669bf7826213e860b2708075544f6ca135a201f1241f268547e1`  
		Last Modified: Wed, 05 Feb 2025 21:09:45 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:98fb28dc948f91236782d2379af7aedceff05cb4e5b0820673aec6e6294406d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302e6333c3d9e3a4d6df79bb568f7ed9082d3d2eff77eea02136485ccf507677`

```dockerfile
```

-	Layers:
	-	`sha256:7e39c9983f6ae9190941e61cdbc7bdbf30a8881bb3d352479be40d368566a250`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 14.1 MB (14082935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927bc78ffb6e843d9fdce2978c8aca59771d8db387a9424a2399cea5d1665a66`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:d56d039139a7f3b71f6d1c9f07ca4ee9f977b0fca13acdd27a1b13bfd4a4e3be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c5eb2eeec0f383a613a984912221b663b49b015badcddf7baed7bdf22b7ed8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241152697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e34946bc4c418b9083622074deea6115aebefb4557d998897162bea8433f083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e59b1e9b7fc9a9eb4fa1fa5fc8607972c2670dd75fc4c50a7205aafa69c500f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf87f630bc84600161859d58a329ef80f43f44bdd85f320a416ec93aaadcd19`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886200dd5e38fb52ed314896a9b344e554158dd919db3187dda896573bbf38cb`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 6.9 MB (6900832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49812044423fc2929b886ef6091fd13267cdabb96e896e6ebae63b5bec66bff`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48319207fe201d8999054f5f48f9aff4aa14c19b5c6c4585e59076b0b0e88c7`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4312bbe95c6f45e596d3da7932dccce0bcacfc7817c28b063aa53092ab3e156`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 48.4 MB (48427656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd0a00427a8af6fd510a7debec37d4c9a4ff8b06c0105cfedcb9006985779f9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4e973a399acea71133d05cca20b12cd764fc541d730141b2bfff3b22d163e0`  
		Last Modified: Wed, 05 Feb 2025 21:09:11 GMT  
		Size: 135.7 MB (135734421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274b57fed122cc63adc4c52fbb798ac3c05dc98f77234ac33a474d41e6ff0b8e`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b0accdd2aa5646c134aa14b2c50110091a309a2341c90f4acdf18df087dc87e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7c86c3f0ebc620528bbce4a7d75a2881ef0ac6a08b6952b4e982d8ce51fc21`

```dockerfile
```

-	Layers:
	-	`sha256:a80ea3072404b2cfa11c0387192290373eb59794e4e4481b5d9f13223da5b84d`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 14.1 MB (14084479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c27537cf70b90e7ef9d57e2f874e8a70e6089c6a51f8d0cc5eaaceab0e6ed74`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:add44c19ad3a11160d69598c8f040f909be0ffd292009de81446ffca0faaa175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236525463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdc083700d09d1089086647e63601adb73c90cefee1921b21af6b86f5031bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08781f18c7788abfbf773236db8d818d48da0dcbf28916eb63ef529f986bc4d`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02e7cdef9c23061e5ac9d03b340af65eb24b3a33c1cf9a70740a32ba64524af`  
		Last Modified: Wed, 05 Feb 2025 21:09:46 GMT  
		Size: 47.3 MB (47297946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f9f0e2e076fedb14c415158459505fb8a5bcfd31aab654f292b23fb6e97059`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2573d09c11f17b9435be5eb631776a7d68d9a248f99cfb276a050ee8661c8d1`  
		Last Modified: Wed, 05 Feb 2025 21:09:47 GMT  
		Size: 134.1 MB (134137606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c94852e619669bf7826213e860b2708075544f6ca135a201f1241f268547e1`  
		Last Modified: Wed, 05 Feb 2025 21:09:45 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:98fb28dc948f91236782d2379af7aedceff05cb4e5b0820673aec6e6294406d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302e6333c3d9e3a4d6df79bb568f7ed9082d3d2eff77eea02136485ccf507677`

```dockerfile
```

-	Layers:
	-	`sha256:7e39c9983f6ae9190941e61cdbc7bdbf30a8881bb3d352479be40d368566a250`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 14.1 MB (14082935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927bc78ffb6e843d9fdce2978c8aca59771d8db387a9424a2399cea5d1665a66`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:d56d039139a7f3b71f6d1c9f07ca4ee9f977b0fca13acdd27a1b13bfd4a4e3be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c5eb2eeec0f383a613a984912221b663b49b015badcddf7baed7bdf22b7ed8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241152697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e34946bc4c418b9083622074deea6115aebefb4557d998897162bea8433f083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e59b1e9b7fc9a9eb4fa1fa5fc8607972c2670dd75fc4c50a7205aafa69c500f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf87f630bc84600161859d58a329ef80f43f44bdd85f320a416ec93aaadcd19`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886200dd5e38fb52ed314896a9b344e554158dd919db3187dda896573bbf38cb`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 6.9 MB (6900832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49812044423fc2929b886ef6091fd13267cdabb96e896e6ebae63b5bec66bff`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48319207fe201d8999054f5f48f9aff4aa14c19b5c6c4585e59076b0b0e88c7`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4312bbe95c6f45e596d3da7932dccce0bcacfc7817c28b063aa53092ab3e156`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 48.4 MB (48427656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd0a00427a8af6fd510a7debec37d4c9a4ff8b06c0105cfedcb9006985779f9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4e973a399acea71133d05cca20b12cd764fc541d730141b2bfff3b22d163e0`  
		Last Modified: Wed, 05 Feb 2025 21:09:11 GMT  
		Size: 135.7 MB (135734421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274b57fed122cc63adc4c52fbb798ac3c05dc98f77234ac33a474d41e6ff0b8e`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b0accdd2aa5646c134aa14b2c50110091a309a2341c90f4acdf18df087dc87e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7c86c3f0ebc620528bbce4a7d75a2881ef0ac6a08b6952b4e982d8ce51fc21`

```dockerfile
```

-	Layers:
	-	`sha256:a80ea3072404b2cfa11c0387192290373eb59794e4e4481b5d9f13223da5b84d`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 14.1 MB (14084479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c27537cf70b90e7ef9d57e2f874e8a70e6089c6a51f8d0cc5eaaceab0e6ed74`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:add44c19ad3a11160d69598c8f040f909be0ffd292009de81446ffca0faaa175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236525463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdc083700d09d1089086647e63601adb73c90cefee1921b21af6b86f5031bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08781f18c7788abfbf773236db8d818d48da0dcbf28916eb63ef529f986bc4d`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02e7cdef9c23061e5ac9d03b340af65eb24b3a33c1cf9a70740a32ba64524af`  
		Last Modified: Wed, 05 Feb 2025 21:09:46 GMT  
		Size: 47.3 MB (47297946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f9f0e2e076fedb14c415158459505fb8a5bcfd31aab654f292b23fb6e97059`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2573d09c11f17b9435be5eb631776a7d68d9a248f99cfb276a050ee8661c8d1`  
		Last Modified: Wed, 05 Feb 2025 21:09:47 GMT  
		Size: 134.1 MB (134137606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c94852e619669bf7826213e860b2708075544f6ca135a201f1241f268547e1`  
		Last Modified: Wed, 05 Feb 2025 21:09:45 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:98fb28dc948f91236782d2379af7aedceff05cb4e5b0820673aec6e6294406d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302e6333c3d9e3a4d6df79bb568f7ed9082d3d2eff77eea02136485ccf507677`

```dockerfile
```

-	Layers:
	-	`sha256:7e39c9983f6ae9190941e61cdbc7bdbf30a8881bb3d352479be40d368566a250`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 14.1 MB (14082935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927bc78ffb6e843d9fdce2978c8aca59771d8db387a9424a2399cea5d1665a66`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2`

```console
$ docker pull mysql@sha256:d56d039139a7f3b71f6d1c9f07ca4ee9f977b0fca13acdd27a1b13bfd4a4e3be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2` - linux; amd64

```console
$ docker pull mysql@sha256:c5eb2eeec0f383a613a984912221b663b49b015badcddf7baed7bdf22b7ed8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241152697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e34946bc4c418b9083622074deea6115aebefb4557d998897162bea8433f083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e59b1e9b7fc9a9eb4fa1fa5fc8607972c2670dd75fc4c50a7205aafa69c500f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf87f630bc84600161859d58a329ef80f43f44bdd85f320a416ec93aaadcd19`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886200dd5e38fb52ed314896a9b344e554158dd919db3187dda896573bbf38cb`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 6.9 MB (6900832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49812044423fc2929b886ef6091fd13267cdabb96e896e6ebae63b5bec66bff`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48319207fe201d8999054f5f48f9aff4aa14c19b5c6c4585e59076b0b0e88c7`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4312bbe95c6f45e596d3da7932dccce0bcacfc7817c28b063aa53092ab3e156`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 48.4 MB (48427656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd0a00427a8af6fd510a7debec37d4c9a4ff8b06c0105cfedcb9006985779f9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4e973a399acea71133d05cca20b12cd764fc541d730141b2bfff3b22d163e0`  
		Last Modified: Wed, 05 Feb 2025 21:09:11 GMT  
		Size: 135.7 MB (135734421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274b57fed122cc63adc4c52fbb798ac3c05dc98f77234ac33a474d41e6ff0b8e`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2` - unknown; unknown

```console
$ docker pull mysql@sha256:b0accdd2aa5646c134aa14b2c50110091a309a2341c90f4acdf18df087dc87e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7c86c3f0ebc620528bbce4a7d75a2881ef0ac6a08b6952b4e982d8ce51fc21`

```dockerfile
```

-	Layers:
	-	`sha256:a80ea3072404b2cfa11c0387192290373eb59794e4e4481b5d9f13223da5b84d`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 14.1 MB (14084479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c27537cf70b90e7ef9d57e2f874e8a70e6089c6a51f8d0cc5eaaceab0e6ed74`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:add44c19ad3a11160d69598c8f040f909be0ffd292009de81446ffca0faaa175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236525463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdc083700d09d1089086647e63601adb73c90cefee1921b21af6b86f5031bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08781f18c7788abfbf773236db8d818d48da0dcbf28916eb63ef529f986bc4d`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02e7cdef9c23061e5ac9d03b340af65eb24b3a33c1cf9a70740a32ba64524af`  
		Last Modified: Wed, 05 Feb 2025 21:09:46 GMT  
		Size: 47.3 MB (47297946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f9f0e2e076fedb14c415158459505fb8a5bcfd31aab654f292b23fb6e97059`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2573d09c11f17b9435be5eb631776a7d68d9a248f99cfb276a050ee8661c8d1`  
		Last Modified: Wed, 05 Feb 2025 21:09:47 GMT  
		Size: 134.1 MB (134137606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c94852e619669bf7826213e860b2708075544f6ca135a201f1241f268547e1`  
		Last Modified: Wed, 05 Feb 2025 21:09:45 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2` - unknown; unknown

```console
$ docker pull mysql@sha256:98fb28dc948f91236782d2379af7aedceff05cb4e5b0820673aec6e6294406d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302e6333c3d9e3a4d6df79bb568f7ed9082d3d2eff77eea02136485ccf507677`

```dockerfile
```

-	Layers:
	-	`sha256:7e39c9983f6ae9190941e61cdbc7bdbf30a8881bb3d352479be40d368566a250`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 14.1 MB (14082935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927bc78ffb6e843d9fdce2978c8aca59771d8db387a9424a2399cea5d1665a66`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2-oracle`

```console
$ docker pull mysql@sha256:d56d039139a7f3b71f6d1c9f07ca4ee9f977b0fca13acdd27a1b13bfd4a4e3be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c5eb2eeec0f383a613a984912221b663b49b015badcddf7baed7bdf22b7ed8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241152697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e34946bc4c418b9083622074deea6115aebefb4557d998897162bea8433f083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e59b1e9b7fc9a9eb4fa1fa5fc8607972c2670dd75fc4c50a7205aafa69c500f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf87f630bc84600161859d58a329ef80f43f44bdd85f320a416ec93aaadcd19`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886200dd5e38fb52ed314896a9b344e554158dd919db3187dda896573bbf38cb`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 6.9 MB (6900832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49812044423fc2929b886ef6091fd13267cdabb96e896e6ebae63b5bec66bff`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48319207fe201d8999054f5f48f9aff4aa14c19b5c6c4585e59076b0b0e88c7`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4312bbe95c6f45e596d3da7932dccce0bcacfc7817c28b063aa53092ab3e156`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 48.4 MB (48427656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd0a00427a8af6fd510a7debec37d4c9a4ff8b06c0105cfedcb9006985779f9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4e973a399acea71133d05cca20b12cd764fc541d730141b2bfff3b22d163e0`  
		Last Modified: Wed, 05 Feb 2025 21:09:11 GMT  
		Size: 135.7 MB (135734421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274b57fed122cc63adc4c52fbb798ac3c05dc98f77234ac33a474d41e6ff0b8e`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b0accdd2aa5646c134aa14b2c50110091a309a2341c90f4acdf18df087dc87e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7c86c3f0ebc620528bbce4a7d75a2881ef0ac6a08b6952b4e982d8ce51fc21`

```dockerfile
```

-	Layers:
	-	`sha256:a80ea3072404b2cfa11c0387192290373eb59794e4e4481b5d9f13223da5b84d`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 14.1 MB (14084479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c27537cf70b90e7ef9d57e2f874e8a70e6089c6a51f8d0cc5eaaceab0e6ed74`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:add44c19ad3a11160d69598c8f040f909be0ffd292009de81446ffca0faaa175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236525463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdc083700d09d1089086647e63601adb73c90cefee1921b21af6b86f5031bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08781f18c7788abfbf773236db8d818d48da0dcbf28916eb63ef529f986bc4d`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02e7cdef9c23061e5ac9d03b340af65eb24b3a33c1cf9a70740a32ba64524af`  
		Last Modified: Wed, 05 Feb 2025 21:09:46 GMT  
		Size: 47.3 MB (47297946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f9f0e2e076fedb14c415158459505fb8a5bcfd31aab654f292b23fb6e97059`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2573d09c11f17b9435be5eb631776a7d68d9a248f99cfb276a050ee8661c8d1`  
		Last Modified: Wed, 05 Feb 2025 21:09:47 GMT  
		Size: 134.1 MB (134137606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c94852e619669bf7826213e860b2708075544f6ca135a201f1241f268547e1`  
		Last Modified: Wed, 05 Feb 2025 21:09:45 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:98fb28dc948f91236782d2379af7aedceff05cb4e5b0820673aec6e6294406d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302e6333c3d9e3a4d6df79bb568f7ed9082d3d2eff77eea02136485ccf507677`

```dockerfile
```

-	Layers:
	-	`sha256:7e39c9983f6ae9190941e61cdbc7bdbf30a8881bb3d352479be40d368566a250`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 14.1 MB (14082935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927bc78ffb6e843d9fdce2978c8aca59771d8db387a9424a2399cea5d1665a66`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2-oraclelinux9`

```console
$ docker pull mysql@sha256:d56d039139a7f3b71f6d1c9f07ca4ee9f977b0fca13acdd27a1b13bfd4a4e3be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c5eb2eeec0f383a613a984912221b663b49b015badcddf7baed7bdf22b7ed8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241152697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e34946bc4c418b9083622074deea6115aebefb4557d998897162bea8433f083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e59b1e9b7fc9a9eb4fa1fa5fc8607972c2670dd75fc4c50a7205aafa69c500f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf87f630bc84600161859d58a329ef80f43f44bdd85f320a416ec93aaadcd19`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886200dd5e38fb52ed314896a9b344e554158dd919db3187dda896573bbf38cb`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 6.9 MB (6900832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49812044423fc2929b886ef6091fd13267cdabb96e896e6ebae63b5bec66bff`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48319207fe201d8999054f5f48f9aff4aa14c19b5c6c4585e59076b0b0e88c7`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4312bbe95c6f45e596d3da7932dccce0bcacfc7817c28b063aa53092ab3e156`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 48.4 MB (48427656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd0a00427a8af6fd510a7debec37d4c9a4ff8b06c0105cfedcb9006985779f9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4e973a399acea71133d05cca20b12cd764fc541d730141b2bfff3b22d163e0`  
		Last Modified: Wed, 05 Feb 2025 21:09:11 GMT  
		Size: 135.7 MB (135734421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274b57fed122cc63adc4c52fbb798ac3c05dc98f77234ac33a474d41e6ff0b8e`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b0accdd2aa5646c134aa14b2c50110091a309a2341c90f4acdf18df087dc87e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7c86c3f0ebc620528bbce4a7d75a2881ef0ac6a08b6952b4e982d8ce51fc21`

```dockerfile
```

-	Layers:
	-	`sha256:a80ea3072404b2cfa11c0387192290373eb59794e4e4481b5d9f13223da5b84d`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 14.1 MB (14084479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c27537cf70b90e7ef9d57e2f874e8a70e6089c6a51f8d0cc5eaaceab0e6ed74`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:add44c19ad3a11160d69598c8f040f909be0ffd292009de81446ffca0faaa175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236525463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdc083700d09d1089086647e63601adb73c90cefee1921b21af6b86f5031bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08781f18c7788abfbf773236db8d818d48da0dcbf28916eb63ef529f986bc4d`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02e7cdef9c23061e5ac9d03b340af65eb24b3a33c1cf9a70740a32ba64524af`  
		Last Modified: Wed, 05 Feb 2025 21:09:46 GMT  
		Size: 47.3 MB (47297946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f9f0e2e076fedb14c415158459505fb8a5bcfd31aab654f292b23fb6e97059`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2573d09c11f17b9435be5eb631776a7d68d9a248f99cfb276a050ee8661c8d1`  
		Last Modified: Wed, 05 Feb 2025 21:09:47 GMT  
		Size: 134.1 MB (134137606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c94852e619669bf7826213e860b2708075544f6ca135a201f1241f268547e1`  
		Last Modified: Wed, 05 Feb 2025 21:09:45 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:98fb28dc948f91236782d2379af7aedceff05cb4e5b0820673aec6e6294406d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302e6333c3d9e3a4d6df79bb568f7ed9082d3d2eff77eea02136485ccf507677`

```dockerfile
```

-	Layers:
	-	`sha256:7e39c9983f6ae9190941e61cdbc7bdbf30a8881bb3d352479be40d368566a250`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 14.1 MB (14082935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927bc78ffb6e843d9fdce2978c8aca59771d8db387a9424a2399cea5d1665a66`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2.0`

```console
$ docker pull mysql@sha256:d56d039139a7f3b71f6d1c9f07ca4ee9f977b0fca13acdd27a1b13bfd4a4e3be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2.0` - linux; amd64

```console
$ docker pull mysql@sha256:c5eb2eeec0f383a613a984912221b663b49b015badcddf7baed7bdf22b7ed8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241152697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e34946bc4c418b9083622074deea6115aebefb4557d998897162bea8433f083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e59b1e9b7fc9a9eb4fa1fa5fc8607972c2670dd75fc4c50a7205aafa69c500f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf87f630bc84600161859d58a329ef80f43f44bdd85f320a416ec93aaadcd19`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886200dd5e38fb52ed314896a9b344e554158dd919db3187dda896573bbf38cb`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 6.9 MB (6900832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49812044423fc2929b886ef6091fd13267cdabb96e896e6ebae63b5bec66bff`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48319207fe201d8999054f5f48f9aff4aa14c19b5c6c4585e59076b0b0e88c7`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4312bbe95c6f45e596d3da7932dccce0bcacfc7817c28b063aa53092ab3e156`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 48.4 MB (48427656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd0a00427a8af6fd510a7debec37d4c9a4ff8b06c0105cfedcb9006985779f9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4e973a399acea71133d05cca20b12cd764fc541d730141b2bfff3b22d163e0`  
		Last Modified: Wed, 05 Feb 2025 21:09:11 GMT  
		Size: 135.7 MB (135734421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274b57fed122cc63adc4c52fbb798ac3c05dc98f77234ac33a474d41e6ff0b8e`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0` - unknown; unknown

```console
$ docker pull mysql@sha256:b0accdd2aa5646c134aa14b2c50110091a309a2341c90f4acdf18df087dc87e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7c86c3f0ebc620528bbce4a7d75a2881ef0ac6a08b6952b4e982d8ce51fc21`

```dockerfile
```

-	Layers:
	-	`sha256:a80ea3072404b2cfa11c0387192290373eb59794e4e4481b5d9f13223da5b84d`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 14.1 MB (14084479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c27537cf70b90e7ef9d57e2f874e8a70e6089c6a51f8d0cc5eaaceab0e6ed74`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:add44c19ad3a11160d69598c8f040f909be0ffd292009de81446ffca0faaa175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236525463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdc083700d09d1089086647e63601adb73c90cefee1921b21af6b86f5031bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08781f18c7788abfbf773236db8d818d48da0dcbf28916eb63ef529f986bc4d`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02e7cdef9c23061e5ac9d03b340af65eb24b3a33c1cf9a70740a32ba64524af`  
		Last Modified: Wed, 05 Feb 2025 21:09:46 GMT  
		Size: 47.3 MB (47297946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f9f0e2e076fedb14c415158459505fb8a5bcfd31aab654f292b23fb6e97059`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2573d09c11f17b9435be5eb631776a7d68d9a248f99cfb276a050ee8661c8d1`  
		Last Modified: Wed, 05 Feb 2025 21:09:47 GMT  
		Size: 134.1 MB (134137606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c94852e619669bf7826213e860b2708075544f6ca135a201f1241f268547e1`  
		Last Modified: Wed, 05 Feb 2025 21:09:45 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0` - unknown; unknown

```console
$ docker pull mysql@sha256:98fb28dc948f91236782d2379af7aedceff05cb4e5b0820673aec6e6294406d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302e6333c3d9e3a4d6df79bb568f7ed9082d3d2eff77eea02136485ccf507677`

```dockerfile
```

-	Layers:
	-	`sha256:7e39c9983f6ae9190941e61cdbc7bdbf30a8881bb3d352479be40d368566a250`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 14.1 MB (14082935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927bc78ffb6e843d9fdce2978c8aca59771d8db387a9424a2399cea5d1665a66`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2.0-oracle`

```console
$ docker pull mysql@sha256:d56d039139a7f3b71f6d1c9f07ca4ee9f977b0fca13acdd27a1b13bfd4a4e3be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c5eb2eeec0f383a613a984912221b663b49b015badcddf7baed7bdf22b7ed8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241152697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e34946bc4c418b9083622074deea6115aebefb4557d998897162bea8433f083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e59b1e9b7fc9a9eb4fa1fa5fc8607972c2670dd75fc4c50a7205aafa69c500f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf87f630bc84600161859d58a329ef80f43f44bdd85f320a416ec93aaadcd19`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886200dd5e38fb52ed314896a9b344e554158dd919db3187dda896573bbf38cb`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 6.9 MB (6900832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49812044423fc2929b886ef6091fd13267cdabb96e896e6ebae63b5bec66bff`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48319207fe201d8999054f5f48f9aff4aa14c19b5c6c4585e59076b0b0e88c7`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4312bbe95c6f45e596d3da7932dccce0bcacfc7817c28b063aa53092ab3e156`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 48.4 MB (48427656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd0a00427a8af6fd510a7debec37d4c9a4ff8b06c0105cfedcb9006985779f9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4e973a399acea71133d05cca20b12cd764fc541d730141b2bfff3b22d163e0`  
		Last Modified: Wed, 05 Feb 2025 21:09:11 GMT  
		Size: 135.7 MB (135734421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274b57fed122cc63adc4c52fbb798ac3c05dc98f77234ac33a474d41e6ff0b8e`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b0accdd2aa5646c134aa14b2c50110091a309a2341c90f4acdf18df087dc87e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7c86c3f0ebc620528bbce4a7d75a2881ef0ac6a08b6952b4e982d8ce51fc21`

```dockerfile
```

-	Layers:
	-	`sha256:a80ea3072404b2cfa11c0387192290373eb59794e4e4481b5d9f13223da5b84d`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 14.1 MB (14084479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c27537cf70b90e7ef9d57e2f874e8a70e6089c6a51f8d0cc5eaaceab0e6ed74`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:add44c19ad3a11160d69598c8f040f909be0ffd292009de81446ffca0faaa175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236525463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdc083700d09d1089086647e63601adb73c90cefee1921b21af6b86f5031bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08781f18c7788abfbf773236db8d818d48da0dcbf28916eb63ef529f986bc4d`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02e7cdef9c23061e5ac9d03b340af65eb24b3a33c1cf9a70740a32ba64524af`  
		Last Modified: Wed, 05 Feb 2025 21:09:46 GMT  
		Size: 47.3 MB (47297946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f9f0e2e076fedb14c415158459505fb8a5bcfd31aab654f292b23fb6e97059`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2573d09c11f17b9435be5eb631776a7d68d9a248f99cfb276a050ee8661c8d1`  
		Last Modified: Wed, 05 Feb 2025 21:09:47 GMT  
		Size: 134.1 MB (134137606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c94852e619669bf7826213e860b2708075544f6ca135a201f1241f268547e1`  
		Last Modified: Wed, 05 Feb 2025 21:09:45 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:98fb28dc948f91236782d2379af7aedceff05cb4e5b0820673aec6e6294406d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302e6333c3d9e3a4d6df79bb568f7ed9082d3d2eff77eea02136485ccf507677`

```dockerfile
```

-	Layers:
	-	`sha256:7e39c9983f6ae9190941e61cdbc7bdbf30a8881bb3d352479be40d368566a250`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 14.1 MB (14082935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927bc78ffb6e843d9fdce2978c8aca59771d8db387a9424a2399cea5d1665a66`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2.0-oraclelinux9`

```console
$ docker pull mysql@sha256:d56d039139a7f3b71f6d1c9f07ca4ee9f977b0fca13acdd27a1b13bfd4a4e3be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c5eb2eeec0f383a613a984912221b663b49b015badcddf7baed7bdf22b7ed8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241152697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e34946bc4c418b9083622074deea6115aebefb4557d998897162bea8433f083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e59b1e9b7fc9a9eb4fa1fa5fc8607972c2670dd75fc4c50a7205aafa69c500f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf87f630bc84600161859d58a329ef80f43f44bdd85f320a416ec93aaadcd19`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886200dd5e38fb52ed314896a9b344e554158dd919db3187dda896573bbf38cb`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 6.9 MB (6900832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49812044423fc2929b886ef6091fd13267cdabb96e896e6ebae63b5bec66bff`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48319207fe201d8999054f5f48f9aff4aa14c19b5c6c4585e59076b0b0e88c7`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4312bbe95c6f45e596d3da7932dccce0bcacfc7817c28b063aa53092ab3e156`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 48.4 MB (48427656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd0a00427a8af6fd510a7debec37d4c9a4ff8b06c0105cfedcb9006985779f9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4e973a399acea71133d05cca20b12cd764fc541d730141b2bfff3b22d163e0`  
		Last Modified: Wed, 05 Feb 2025 21:09:11 GMT  
		Size: 135.7 MB (135734421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274b57fed122cc63adc4c52fbb798ac3c05dc98f77234ac33a474d41e6ff0b8e`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b0accdd2aa5646c134aa14b2c50110091a309a2341c90f4acdf18df087dc87e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7c86c3f0ebc620528bbce4a7d75a2881ef0ac6a08b6952b4e982d8ce51fc21`

```dockerfile
```

-	Layers:
	-	`sha256:a80ea3072404b2cfa11c0387192290373eb59794e4e4481b5d9f13223da5b84d`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 14.1 MB (14084479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c27537cf70b90e7ef9d57e2f874e8a70e6089c6a51f8d0cc5eaaceab0e6ed74`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:add44c19ad3a11160d69598c8f040f909be0ffd292009de81446ffca0faaa175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236525463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdc083700d09d1089086647e63601adb73c90cefee1921b21af6b86f5031bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08781f18c7788abfbf773236db8d818d48da0dcbf28916eb63ef529f986bc4d`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02e7cdef9c23061e5ac9d03b340af65eb24b3a33c1cf9a70740a32ba64524af`  
		Last Modified: Wed, 05 Feb 2025 21:09:46 GMT  
		Size: 47.3 MB (47297946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f9f0e2e076fedb14c415158459505fb8a5bcfd31aab654f292b23fb6e97059`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2573d09c11f17b9435be5eb631776a7d68d9a248f99cfb276a050ee8661c8d1`  
		Last Modified: Wed, 05 Feb 2025 21:09:47 GMT  
		Size: 134.1 MB (134137606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c94852e619669bf7826213e860b2708075544f6ca135a201f1241f268547e1`  
		Last Modified: Wed, 05 Feb 2025 21:09:45 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:98fb28dc948f91236782d2379af7aedceff05cb4e5b0820673aec6e6294406d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302e6333c3d9e3a4d6df79bb568f7ed9082d3d2eff77eea02136485ccf507677`

```dockerfile
```

-	Layers:
	-	`sha256:7e39c9983f6ae9190941e61cdbc7bdbf30a8881bb3d352479be40d368566a250`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 14.1 MB (14082935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927bc78ffb6e843d9fdce2978c8aca59771d8db387a9424a2399cea5d1665a66`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:d56d039139a7f3b71f6d1c9f07ca4ee9f977b0fca13acdd27a1b13bfd4a4e3be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:c5eb2eeec0f383a613a984912221b663b49b015badcddf7baed7bdf22b7ed8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241152697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e34946bc4c418b9083622074deea6115aebefb4557d998897162bea8433f083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e59b1e9b7fc9a9eb4fa1fa5fc8607972c2670dd75fc4c50a7205aafa69c500f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf87f630bc84600161859d58a329ef80f43f44bdd85f320a416ec93aaadcd19`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886200dd5e38fb52ed314896a9b344e554158dd919db3187dda896573bbf38cb`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 6.9 MB (6900832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49812044423fc2929b886ef6091fd13267cdabb96e896e6ebae63b5bec66bff`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48319207fe201d8999054f5f48f9aff4aa14c19b5c6c4585e59076b0b0e88c7`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4312bbe95c6f45e596d3da7932dccce0bcacfc7817c28b063aa53092ab3e156`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 48.4 MB (48427656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd0a00427a8af6fd510a7debec37d4c9a4ff8b06c0105cfedcb9006985779f9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4e973a399acea71133d05cca20b12cd764fc541d730141b2bfff3b22d163e0`  
		Last Modified: Wed, 05 Feb 2025 21:09:11 GMT  
		Size: 135.7 MB (135734421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274b57fed122cc63adc4c52fbb798ac3c05dc98f77234ac33a474d41e6ff0b8e`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:b0accdd2aa5646c134aa14b2c50110091a309a2341c90f4acdf18df087dc87e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7c86c3f0ebc620528bbce4a7d75a2881ef0ac6a08b6952b4e982d8ce51fc21`

```dockerfile
```

-	Layers:
	-	`sha256:a80ea3072404b2cfa11c0387192290373eb59794e4e4481b5d9f13223da5b84d`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 14.1 MB (14084479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c27537cf70b90e7ef9d57e2f874e8a70e6089c6a51f8d0cc5eaaceab0e6ed74`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:add44c19ad3a11160d69598c8f040f909be0ffd292009de81446ffca0faaa175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236525463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdc083700d09d1089086647e63601adb73c90cefee1921b21af6b86f5031bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08781f18c7788abfbf773236db8d818d48da0dcbf28916eb63ef529f986bc4d`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02e7cdef9c23061e5ac9d03b340af65eb24b3a33c1cf9a70740a32ba64524af`  
		Last Modified: Wed, 05 Feb 2025 21:09:46 GMT  
		Size: 47.3 MB (47297946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f9f0e2e076fedb14c415158459505fb8a5bcfd31aab654f292b23fb6e97059`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2573d09c11f17b9435be5eb631776a7d68d9a248f99cfb276a050ee8661c8d1`  
		Last Modified: Wed, 05 Feb 2025 21:09:47 GMT  
		Size: 134.1 MB (134137606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c94852e619669bf7826213e860b2708075544f6ca135a201f1241f268547e1`  
		Last Modified: Wed, 05 Feb 2025 21:09:45 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:98fb28dc948f91236782d2379af7aedceff05cb4e5b0820673aec6e6294406d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302e6333c3d9e3a4d6df79bb568f7ed9082d3d2eff77eea02136485ccf507677`

```dockerfile
```

-	Layers:
	-	`sha256:7e39c9983f6ae9190941e61cdbc7bdbf30a8881bb3d352479be40d368566a250`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 14.1 MB (14082935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927bc78ffb6e843d9fdce2978c8aca59771d8db387a9424a2399cea5d1665a66`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:d56d039139a7f3b71f6d1c9f07ca4ee9f977b0fca13acdd27a1b13bfd4a4e3be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c5eb2eeec0f383a613a984912221b663b49b015badcddf7baed7bdf22b7ed8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241152697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e34946bc4c418b9083622074deea6115aebefb4557d998897162bea8433f083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e59b1e9b7fc9a9eb4fa1fa5fc8607972c2670dd75fc4c50a7205aafa69c500f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf87f630bc84600161859d58a329ef80f43f44bdd85f320a416ec93aaadcd19`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886200dd5e38fb52ed314896a9b344e554158dd919db3187dda896573bbf38cb`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 6.9 MB (6900832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49812044423fc2929b886ef6091fd13267cdabb96e896e6ebae63b5bec66bff`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48319207fe201d8999054f5f48f9aff4aa14c19b5c6c4585e59076b0b0e88c7`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4312bbe95c6f45e596d3da7932dccce0bcacfc7817c28b063aa53092ab3e156`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 48.4 MB (48427656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd0a00427a8af6fd510a7debec37d4c9a4ff8b06c0105cfedcb9006985779f9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4e973a399acea71133d05cca20b12cd764fc541d730141b2bfff3b22d163e0`  
		Last Modified: Wed, 05 Feb 2025 21:09:11 GMT  
		Size: 135.7 MB (135734421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274b57fed122cc63adc4c52fbb798ac3c05dc98f77234ac33a474d41e6ff0b8e`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b0accdd2aa5646c134aa14b2c50110091a309a2341c90f4acdf18df087dc87e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7c86c3f0ebc620528bbce4a7d75a2881ef0ac6a08b6952b4e982d8ce51fc21`

```dockerfile
```

-	Layers:
	-	`sha256:a80ea3072404b2cfa11c0387192290373eb59794e4e4481b5d9f13223da5b84d`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 14.1 MB (14084479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c27537cf70b90e7ef9d57e2f874e8a70e6089c6a51f8d0cc5eaaceab0e6ed74`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:add44c19ad3a11160d69598c8f040f909be0ffd292009de81446ffca0faaa175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236525463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdc083700d09d1089086647e63601adb73c90cefee1921b21af6b86f5031bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08781f18c7788abfbf773236db8d818d48da0dcbf28916eb63ef529f986bc4d`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02e7cdef9c23061e5ac9d03b340af65eb24b3a33c1cf9a70740a32ba64524af`  
		Last Modified: Wed, 05 Feb 2025 21:09:46 GMT  
		Size: 47.3 MB (47297946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f9f0e2e076fedb14c415158459505fb8a5bcfd31aab654f292b23fb6e97059`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2573d09c11f17b9435be5eb631776a7d68d9a248f99cfb276a050ee8661c8d1`  
		Last Modified: Wed, 05 Feb 2025 21:09:47 GMT  
		Size: 134.1 MB (134137606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c94852e619669bf7826213e860b2708075544f6ca135a201f1241f268547e1`  
		Last Modified: Wed, 05 Feb 2025 21:09:45 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:98fb28dc948f91236782d2379af7aedceff05cb4e5b0820673aec6e6294406d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302e6333c3d9e3a4d6df79bb568f7ed9082d3d2eff77eea02136485ccf507677`

```dockerfile
```

-	Layers:
	-	`sha256:7e39c9983f6ae9190941e61cdbc7bdbf30a8881bb3d352479be40d368566a250`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 14.1 MB (14082935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927bc78ffb6e843d9fdce2978c8aca59771d8db387a9424a2399cea5d1665a66`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:d56d039139a7f3b71f6d1c9f07ca4ee9f977b0fca13acdd27a1b13bfd4a4e3be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c5eb2eeec0f383a613a984912221b663b49b015badcddf7baed7bdf22b7ed8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241152697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e34946bc4c418b9083622074deea6115aebefb4557d998897162bea8433f083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e59b1e9b7fc9a9eb4fa1fa5fc8607972c2670dd75fc4c50a7205aafa69c500f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf87f630bc84600161859d58a329ef80f43f44bdd85f320a416ec93aaadcd19`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886200dd5e38fb52ed314896a9b344e554158dd919db3187dda896573bbf38cb`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 6.9 MB (6900832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49812044423fc2929b886ef6091fd13267cdabb96e896e6ebae63b5bec66bff`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48319207fe201d8999054f5f48f9aff4aa14c19b5c6c4585e59076b0b0e88c7`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4312bbe95c6f45e596d3da7932dccce0bcacfc7817c28b063aa53092ab3e156`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 48.4 MB (48427656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd0a00427a8af6fd510a7debec37d4c9a4ff8b06c0105cfedcb9006985779f9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4e973a399acea71133d05cca20b12cd764fc541d730141b2bfff3b22d163e0`  
		Last Modified: Wed, 05 Feb 2025 21:09:11 GMT  
		Size: 135.7 MB (135734421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274b57fed122cc63adc4c52fbb798ac3c05dc98f77234ac33a474d41e6ff0b8e`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b0accdd2aa5646c134aa14b2c50110091a309a2341c90f4acdf18df087dc87e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7c86c3f0ebc620528bbce4a7d75a2881ef0ac6a08b6952b4e982d8ce51fc21`

```dockerfile
```

-	Layers:
	-	`sha256:a80ea3072404b2cfa11c0387192290373eb59794e4e4481b5d9f13223da5b84d`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 14.1 MB (14084479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c27537cf70b90e7ef9d57e2f874e8a70e6089c6a51f8d0cc5eaaceab0e6ed74`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:add44c19ad3a11160d69598c8f040f909be0ffd292009de81446ffca0faaa175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236525463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdc083700d09d1089086647e63601adb73c90cefee1921b21af6b86f5031bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08781f18c7788abfbf773236db8d818d48da0dcbf28916eb63ef529f986bc4d`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02e7cdef9c23061e5ac9d03b340af65eb24b3a33c1cf9a70740a32ba64524af`  
		Last Modified: Wed, 05 Feb 2025 21:09:46 GMT  
		Size: 47.3 MB (47297946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f9f0e2e076fedb14c415158459505fb8a5bcfd31aab654f292b23fb6e97059`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2573d09c11f17b9435be5eb631776a7d68d9a248f99cfb276a050ee8661c8d1`  
		Last Modified: Wed, 05 Feb 2025 21:09:47 GMT  
		Size: 134.1 MB (134137606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c94852e619669bf7826213e860b2708075544f6ca135a201f1241f268547e1`  
		Last Modified: Wed, 05 Feb 2025 21:09:45 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:98fb28dc948f91236782d2379af7aedceff05cb4e5b0820673aec6e6294406d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302e6333c3d9e3a4d6df79bb568f7ed9082d3d2eff77eea02136485ccf507677`

```dockerfile
```

-	Layers:
	-	`sha256:7e39c9983f6ae9190941e61cdbc7bdbf30a8881bb3d352479be40d368566a250`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 14.1 MB (14082935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927bc78ffb6e843d9fdce2978c8aca59771d8db387a9424a2399cea5d1665a66`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:d56d039139a7f3b71f6d1c9f07ca4ee9f977b0fca13acdd27a1b13bfd4a4e3be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:c5eb2eeec0f383a613a984912221b663b49b015badcddf7baed7bdf22b7ed8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241152697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e34946bc4c418b9083622074deea6115aebefb4557d998897162bea8433f083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e59b1e9b7fc9a9eb4fa1fa5fc8607972c2670dd75fc4c50a7205aafa69c500f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf87f630bc84600161859d58a329ef80f43f44bdd85f320a416ec93aaadcd19`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886200dd5e38fb52ed314896a9b344e554158dd919db3187dda896573bbf38cb`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 6.9 MB (6900832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49812044423fc2929b886ef6091fd13267cdabb96e896e6ebae63b5bec66bff`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48319207fe201d8999054f5f48f9aff4aa14c19b5c6c4585e59076b0b0e88c7`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4312bbe95c6f45e596d3da7932dccce0bcacfc7817c28b063aa53092ab3e156`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 48.4 MB (48427656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd0a00427a8af6fd510a7debec37d4c9a4ff8b06c0105cfedcb9006985779f9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4e973a399acea71133d05cca20b12cd764fc541d730141b2bfff3b22d163e0`  
		Last Modified: Wed, 05 Feb 2025 21:09:11 GMT  
		Size: 135.7 MB (135734421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274b57fed122cc63adc4c52fbb798ac3c05dc98f77234ac33a474d41e6ff0b8e`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:b0accdd2aa5646c134aa14b2c50110091a309a2341c90f4acdf18df087dc87e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7c86c3f0ebc620528bbce4a7d75a2881ef0ac6a08b6952b4e982d8ce51fc21`

```dockerfile
```

-	Layers:
	-	`sha256:a80ea3072404b2cfa11c0387192290373eb59794e4e4481b5d9f13223da5b84d`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 14.1 MB (14084479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c27537cf70b90e7ef9d57e2f874e8a70e6089c6a51f8d0cc5eaaceab0e6ed74`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:add44c19ad3a11160d69598c8f040f909be0ffd292009de81446ffca0faaa175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236525463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdc083700d09d1089086647e63601adb73c90cefee1921b21af6b86f5031bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08781f18c7788abfbf773236db8d818d48da0dcbf28916eb63ef529f986bc4d`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02e7cdef9c23061e5ac9d03b340af65eb24b3a33c1cf9a70740a32ba64524af`  
		Last Modified: Wed, 05 Feb 2025 21:09:46 GMT  
		Size: 47.3 MB (47297946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f9f0e2e076fedb14c415158459505fb8a5bcfd31aab654f292b23fb6e97059`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2573d09c11f17b9435be5eb631776a7d68d9a248f99cfb276a050ee8661c8d1`  
		Last Modified: Wed, 05 Feb 2025 21:09:47 GMT  
		Size: 134.1 MB (134137606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c94852e619669bf7826213e860b2708075544f6ca135a201f1241f268547e1`  
		Last Modified: Wed, 05 Feb 2025 21:09:45 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:98fb28dc948f91236782d2379af7aedceff05cb4e5b0820673aec6e6294406d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302e6333c3d9e3a4d6df79bb568f7ed9082d3d2eff77eea02136485ccf507677`

```dockerfile
```

-	Layers:
	-	`sha256:7e39c9983f6ae9190941e61cdbc7bdbf30a8881bb3d352479be40d368566a250`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 14.1 MB (14082935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927bc78ffb6e843d9fdce2978c8aca59771d8db387a9424a2399cea5d1665a66`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:b14b2b73fc1242bef8fc21cbd73f247396f353cf314734d3502d72eb1ed0d93b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:d50d35b5bd33e90185cf7c9752a8a9c4e322752d9d441aead65d55a5a7a9b0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232921620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03152aa0b71af6d9c2d3ce540cb012fbe4f2c902896c7572baa29e9c2c863d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953a4ccd23a81b87fee3f10c6f7b0f64a28cddf2b44ae4709ed11ba1ddce2801`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f496cf111703223486f94eab0e33c24d2f2d42e3048ade9f846bee4d2c216d78`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba398fbba1a319bb6b0e8072ab3967941541520c4ea0cc9de237fe0fb5c24bf`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 6.9 MB (6900797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612294d2b805abc144afdb56ea7c4c853afb0848da8ba320ded974bfea920c0d`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b72e8cade85158d043b1cc49db60f3192b21928519bd37effb9455ff838774`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16088fb0c0bc6fed09b5f1901cd8932898f9533922d16e2ea76ec6713d3a6e9f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 47.6 MB (47593441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1113808e87139e81bf5791ef5f9a4cfb6340d3744c071b06378e5dd4300cf2`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb634a27ea9af9512a616770be962abb004a69340d9293672318762c88e6f0da`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 128.3 MB (128337606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779e768d23c147ac6ff98cad8c97e9fd64ae88e6fa64c36af645e92f9760640`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:8e27ad713932c235a3a2ba33c8afaf2f24be95c06cf5581d42a16e27cc34902c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e722b0900dddd12a388283e5a5536b2d3136467cab0738958c593d01ae72c0`

```dockerfile
```

-	Layers:
	-	`sha256:a1e7f0e8c496cb14802c1bfd6677f68818d049e581b7a09366a16c80701e32ef`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 14.1 MB (14074192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07d6bfb3db9fb8c16f6075a18e084c2af417f5624c0d7a8e3173a3c498488a4`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b069ea7a6e799b97b7cda674dc14af372a3e819e8167ca7f9f2b25d271ba21c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228373891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143ee6a01dfafb0fc64201d822bf454604f2f23e7de391d6ded6bed4d0f10d2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6d58e993cc8f74278b7b31bc7d5c3a90f3a641fa669d7f9baa0c8bb3f22b99`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89597d03bec9a798d018a2da6d72618fd411ee3be7cfba13b6f84a54a2ff094e`  
		Last Modified: Wed, 05 Feb 2025 21:11:25 GMT  
		Size: 46.5 MB (46472784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b25528c202a2c51e7345274b2ba9194d3e40ad59c4564ca8bda7c62adc296d7`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5176c942bb7758f3748ca374a5f473ec23d3aa80f84498adb45b23c52246574`  
		Last Modified: Wed, 05 Feb 2025 21:11:26 GMT  
		Size: 126.8 MB (126811206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f10df86d743ce521a9a6df46866fb0db04ee299e86f50ebf6a1a9be951c4afa`  
		Last Modified: Wed, 05 Feb 2025 21:11:24 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:9f201d54b76a028b5603016be80583ff3ce499109d5e9b51b6b5c0297cbf4535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7090fba013cec374dc2272b28151f052a2618f48262644077be4d3447039c7`

```dockerfile
```

-	Layers:
	-	`sha256:976a24bbc9d8d48ab0628f1df0c95711404a4ef73eec2286b7e272fbe4c09e72`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 14.1 MB (14072612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9fcf77de5ba79f3b92a0c9269899881dddef44c3ad957f19afa19b2d763ddbc`  
		Last Modified: Wed, 05 Feb 2025 21:11:22 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:b14b2b73fc1242bef8fc21cbd73f247396f353cf314734d3502d72eb1ed0d93b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d50d35b5bd33e90185cf7c9752a8a9c4e322752d9d441aead65d55a5a7a9b0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232921620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03152aa0b71af6d9c2d3ce540cb012fbe4f2c902896c7572baa29e9c2c863d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953a4ccd23a81b87fee3f10c6f7b0f64a28cddf2b44ae4709ed11ba1ddce2801`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f496cf111703223486f94eab0e33c24d2f2d42e3048ade9f846bee4d2c216d78`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba398fbba1a319bb6b0e8072ab3967941541520c4ea0cc9de237fe0fb5c24bf`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 6.9 MB (6900797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612294d2b805abc144afdb56ea7c4c853afb0848da8ba320ded974bfea920c0d`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b72e8cade85158d043b1cc49db60f3192b21928519bd37effb9455ff838774`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16088fb0c0bc6fed09b5f1901cd8932898f9533922d16e2ea76ec6713d3a6e9f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 47.6 MB (47593441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1113808e87139e81bf5791ef5f9a4cfb6340d3744c071b06378e5dd4300cf2`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb634a27ea9af9512a616770be962abb004a69340d9293672318762c88e6f0da`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 128.3 MB (128337606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779e768d23c147ac6ff98cad8c97e9fd64ae88e6fa64c36af645e92f9760640`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:8e27ad713932c235a3a2ba33c8afaf2f24be95c06cf5581d42a16e27cc34902c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e722b0900dddd12a388283e5a5536b2d3136467cab0738958c593d01ae72c0`

```dockerfile
```

-	Layers:
	-	`sha256:a1e7f0e8c496cb14802c1bfd6677f68818d049e581b7a09366a16c80701e32ef`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 14.1 MB (14074192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07d6bfb3db9fb8c16f6075a18e084c2af417f5624c0d7a8e3173a3c498488a4`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b069ea7a6e799b97b7cda674dc14af372a3e819e8167ca7f9f2b25d271ba21c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228373891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143ee6a01dfafb0fc64201d822bf454604f2f23e7de391d6ded6bed4d0f10d2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6d58e993cc8f74278b7b31bc7d5c3a90f3a641fa669d7f9baa0c8bb3f22b99`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89597d03bec9a798d018a2da6d72618fd411ee3be7cfba13b6f84a54a2ff094e`  
		Last Modified: Wed, 05 Feb 2025 21:11:25 GMT  
		Size: 46.5 MB (46472784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b25528c202a2c51e7345274b2ba9194d3e40ad59c4564ca8bda7c62adc296d7`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5176c942bb7758f3748ca374a5f473ec23d3aa80f84498adb45b23c52246574`  
		Last Modified: Wed, 05 Feb 2025 21:11:26 GMT  
		Size: 126.8 MB (126811206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f10df86d743ce521a9a6df46866fb0db04ee299e86f50ebf6a1a9be951c4afa`  
		Last Modified: Wed, 05 Feb 2025 21:11:24 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9f201d54b76a028b5603016be80583ff3ce499109d5e9b51b6b5c0297cbf4535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7090fba013cec374dc2272b28151f052a2618f48262644077be4d3447039c7`

```dockerfile
```

-	Layers:
	-	`sha256:976a24bbc9d8d48ab0628f1df0c95711404a4ef73eec2286b7e272fbe4c09e72`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 14.1 MB (14072612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9fcf77de5ba79f3b92a0c9269899881dddef44c3ad957f19afa19b2d763ddbc`  
		Last Modified: Wed, 05 Feb 2025 21:11:22 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:b14b2b73fc1242bef8fc21cbd73f247396f353cf314734d3502d72eb1ed0d93b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d50d35b5bd33e90185cf7c9752a8a9c4e322752d9d441aead65d55a5a7a9b0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232921620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03152aa0b71af6d9c2d3ce540cb012fbe4f2c902896c7572baa29e9c2c863d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953a4ccd23a81b87fee3f10c6f7b0f64a28cddf2b44ae4709ed11ba1ddce2801`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f496cf111703223486f94eab0e33c24d2f2d42e3048ade9f846bee4d2c216d78`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba398fbba1a319bb6b0e8072ab3967941541520c4ea0cc9de237fe0fb5c24bf`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 6.9 MB (6900797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612294d2b805abc144afdb56ea7c4c853afb0848da8ba320ded974bfea920c0d`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b72e8cade85158d043b1cc49db60f3192b21928519bd37effb9455ff838774`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16088fb0c0bc6fed09b5f1901cd8932898f9533922d16e2ea76ec6713d3a6e9f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 47.6 MB (47593441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1113808e87139e81bf5791ef5f9a4cfb6340d3744c071b06378e5dd4300cf2`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb634a27ea9af9512a616770be962abb004a69340d9293672318762c88e6f0da`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 128.3 MB (128337606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779e768d23c147ac6ff98cad8c97e9fd64ae88e6fa64c36af645e92f9760640`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:8e27ad713932c235a3a2ba33c8afaf2f24be95c06cf5581d42a16e27cc34902c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e722b0900dddd12a388283e5a5536b2d3136467cab0738958c593d01ae72c0`

```dockerfile
```

-	Layers:
	-	`sha256:a1e7f0e8c496cb14802c1bfd6677f68818d049e581b7a09366a16c80701e32ef`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 14.1 MB (14074192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07d6bfb3db9fb8c16f6075a18e084c2af417f5624c0d7a8e3173a3c498488a4`  
		Last Modified: Wed, 05 Feb 2025 21:09:06 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b069ea7a6e799b97b7cda674dc14af372a3e819e8167ca7f9f2b25d271ba21c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228373891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143ee6a01dfafb0fc64201d822bf454604f2f23e7de391d6ded6bed4d0f10d2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6d58e993cc8f74278b7b31bc7d5c3a90f3a641fa669d7f9baa0c8bb3f22b99`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89597d03bec9a798d018a2da6d72618fd411ee3be7cfba13b6f84a54a2ff094e`  
		Last Modified: Wed, 05 Feb 2025 21:11:25 GMT  
		Size: 46.5 MB (46472784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b25528c202a2c51e7345274b2ba9194d3e40ad59c4564ca8bda7c62adc296d7`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5176c942bb7758f3748ca374a5f473ec23d3aa80f84498adb45b23c52246574`  
		Last Modified: Wed, 05 Feb 2025 21:11:26 GMT  
		Size: 126.8 MB (126811206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f10df86d743ce521a9a6df46866fb0db04ee299e86f50ebf6a1a9be951c4afa`  
		Last Modified: Wed, 05 Feb 2025 21:11:24 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9f201d54b76a028b5603016be80583ff3ce499109d5e9b51b6b5c0297cbf4535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7090fba013cec374dc2272b28151f052a2618f48262644077be4d3447039c7`

```dockerfile
```

-	Layers:
	-	`sha256:976a24bbc9d8d48ab0628f1df0c95711404a4ef73eec2286b7e272fbe4c09e72`  
		Last Modified: Wed, 05 Feb 2025 21:11:23 GMT  
		Size: 14.1 MB (14072612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9fcf77de5ba79f3b92a0c9269899881dddef44c3ad957f19afa19b2d763ddbc`  
		Last Modified: Wed, 05 Feb 2025 21:11:22 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:d56d039139a7f3b71f6d1c9f07ca4ee9f977b0fca13acdd27a1b13bfd4a4e3be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c5eb2eeec0f383a613a984912221b663b49b015badcddf7baed7bdf22b7ed8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241152697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e34946bc4c418b9083622074deea6115aebefb4557d998897162bea8433f083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e59b1e9b7fc9a9eb4fa1fa5fc8607972c2670dd75fc4c50a7205aafa69c500f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf87f630bc84600161859d58a329ef80f43f44bdd85f320a416ec93aaadcd19`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886200dd5e38fb52ed314896a9b344e554158dd919db3187dda896573bbf38cb`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 6.9 MB (6900832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49812044423fc2929b886ef6091fd13267cdabb96e896e6ebae63b5bec66bff`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48319207fe201d8999054f5f48f9aff4aa14c19b5c6c4585e59076b0b0e88c7`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4312bbe95c6f45e596d3da7932dccce0bcacfc7817c28b063aa53092ab3e156`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 48.4 MB (48427656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd0a00427a8af6fd510a7debec37d4c9a4ff8b06c0105cfedcb9006985779f9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4e973a399acea71133d05cca20b12cd764fc541d730141b2bfff3b22d163e0`  
		Last Modified: Wed, 05 Feb 2025 21:09:11 GMT  
		Size: 135.7 MB (135734421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274b57fed122cc63adc4c52fbb798ac3c05dc98f77234ac33a474d41e6ff0b8e`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b0accdd2aa5646c134aa14b2c50110091a309a2341c90f4acdf18df087dc87e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7c86c3f0ebc620528bbce4a7d75a2881ef0ac6a08b6952b4e982d8ce51fc21`

```dockerfile
```

-	Layers:
	-	`sha256:a80ea3072404b2cfa11c0387192290373eb59794e4e4481b5d9f13223da5b84d`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 14.1 MB (14084479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c27537cf70b90e7ef9d57e2f874e8a70e6089c6a51f8d0cc5eaaceab0e6ed74`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:add44c19ad3a11160d69598c8f040f909be0ffd292009de81446ffca0faaa175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236525463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdc083700d09d1089086647e63601adb73c90cefee1921b21af6b86f5031bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08781f18c7788abfbf773236db8d818d48da0dcbf28916eb63ef529f986bc4d`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02e7cdef9c23061e5ac9d03b340af65eb24b3a33c1cf9a70740a32ba64524af`  
		Last Modified: Wed, 05 Feb 2025 21:09:46 GMT  
		Size: 47.3 MB (47297946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f9f0e2e076fedb14c415158459505fb8a5bcfd31aab654f292b23fb6e97059`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2573d09c11f17b9435be5eb631776a7d68d9a248f99cfb276a050ee8661c8d1`  
		Last Modified: Wed, 05 Feb 2025 21:09:47 GMT  
		Size: 134.1 MB (134137606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c94852e619669bf7826213e860b2708075544f6ca135a201f1241f268547e1`  
		Last Modified: Wed, 05 Feb 2025 21:09:45 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:98fb28dc948f91236782d2379af7aedceff05cb4e5b0820673aec6e6294406d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302e6333c3d9e3a4d6df79bb568f7ed9082d3d2eff77eea02136485ccf507677`

```dockerfile
```

-	Layers:
	-	`sha256:7e39c9983f6ae9190941e61cdbc7bdbf30a8881bb3d352479be40d368566a250`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 14.1 MB (14082935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927bc78ffb6e843d9fdce2978c8aca59771d8db387a9424a2399cea5d1665a66`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:d56d039139a7f3b71f6d1c9f07ca4ee9f977b0fca13acdd27a1b13bfd4a4e3be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c5eb2eeec0f383a613a984912221b663b49b015badcddf7baed7bdf22b7ed8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241152697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e34946bc4c418b9083622074deea6115aebefb4557d998897162bea8433f083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e59b1e9b7fc9a9eb4fa1fa5fc8607972c2670dd75fc4c50a7205aafa69c500f`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf87f630bc84600161859d58a329ef80f43f44bdd85f320a416ec93aaadcd19`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886200dd5e38fb52ed314896a9b344e554158dd919db3187dda896573bbf38cb`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 6.9 MB (6900832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49812044423fc2929b886ef6091fd13267cdabb96e896e6ebae63b5bec66bff`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48319207fe201d8999054f5f48f9aff4aa14c19b5c6c4585e59076b0b0e88c7`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4312bbe95c6f45e596d3da7932dccce0bcacfc7817c28b063aa53092ab3e156`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 48.4 MB (48427656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd0a00427a8af6fd510a7debec37d4c9a4ff8b06c0105cfedcb9006985779f9`  
		Last Modified: Wed, 05 Feb 2025 21:09:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4e973a399acea71133d05cca20b12cd764fc541d730141b2bfff3b22d163e0`  
		Last Modified: Wed, 05 Feb 2025 21:09:11 GMT  
		Size: 135.7 MB (135734421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274b57fed122cc63adc4c52fbb798ac3c05dc98f77234ac33a474d41e6ff0b8e`  
		Last Modified: Wed, 05 Feb 2025 21:09:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b0accdd2aa5646c134aa14b2c50110091a309a2341c90f4acdf18df087dc87e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7c86c3f0ebc620528bbce4a7d75a2881ef0ac6a08b6952b4e982d8ce51fc21`

```dockerfile
```

-	Layers:
	-	`sha256:a80ea3072404b2cfa11c0387192290373eb59794e4e4481b5d9f13223da5b84d`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 14.1 MB (14084479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c27537cf70b90e7ef9d57e2f874e8a70e6089c6a51f8d0cc5eaaceab0e6ed74`  
		Last Modified: Wed, 05 Feb 2025 21:09:07 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:add44c19ad3a11160d69598c8f040f909be0ffd292009de81446ffca0faaa175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236525463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdc083700d09d1089086647e63601adb73c90cefee1921b21af6b86f5031bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442de84431c3686b1102db2f27bf5d6c5ad048f099fec39de3b5001646d2c983`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c62f89276b8734222476bc15003935540491265a445f668b3f30576a94b1a1`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad3b65bf344f8e2ea9115bb095589f61983bc18bc0f760e98dd93477ec0b502`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 6.5 MB (6497581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a82c4d3661ff0f155d0a2d74bf5566e906450c6dedfdb3cab59fe956d0b219`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08781f18c7788abfbf773236db8d818d48da0dcbf28916eb63ef529f986bc4d`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02e7cdef9c23061e5ac9d03b340af65eb24b3a33c1cf9a70740a32ba64524af`  
		Last Modified: Wed, 05 Feb 2025 21:09:46 GMT  
		Size: 47.3 MB (47297946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f9f0e2e076fedb14c415158459505fb8a5bcfd31aab654f292b23fb6e97059`  
		Last Modified: Wed, 05 Feb 2025 21:09:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2573d09c11f17b9435be5eb631776a7d68d9a248f99cfb276a050ee8661c8d1`  
		Last Modified: Wed, 05 Feb 2025 21:09:47 GMT  
		Size: 134.1 MB (134137606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c94852e619669bf7826213e860b2708075544f6ca135a201f1241f268547e1`  
		Last Modified: Wed, 05 Feb 2025 21:09:45 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:98fb28dc948f91236782d2379af7aedceff05cb4e5b0820673aec6e6294406d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302e6333c3d9e3a4d6df79bb568f7ed9082d3d2eff77eea02136485ccf507677`

```dockerfile
```

-	Layers:
	-	`sha256:7e39c9983f6ae9190941e61cdbc7bdbf30a8881bb3d352479be40d368566a250`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 14.1 MB (14082935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927bc78ffb6e843d9fdce2978c8aca59771d8db387a9424a2399cea5d1665a66`  
		Last Modified: Wed, 05 Feb 2025 21:09:43 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json
