## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:9b9d0aab4860798acff13d2a0ece3bc26639fe18b83fa5cd3e3d0e16b3ed05dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:bdc7c5e6ce679435c74c161dfcd3bb317358e79602d71d828990e266404140b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241128175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa262c3a6564b46bbfebf1994f935c67fb48640604bf0159fab1dbc2523620fc`
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
	-	`sha256:804bb8ae89decacdf918af27c892df04e6f2d3038e3a7d1e34475eef6be9aba3`  
		Last Modified: Thu, 13 Mar 2025 17:46:19 GMT  
		Size: 49.1 MB (49091441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b515e7ceb6913e3aa10d7a9bf68accce7fcf9a53f43daf01a5eb83b38bc01d8`  
		Last Modified: Thu, 13 Mar 2025 17:53:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa11c0a9f081f411c22cc7f27f3d2fb276e40bedc65be91e4d0b698e7693edc`  
		Last Modified: Thu, 13 Mar 2025 17:53:20 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d18181893b850aac8c2484bae2c1ffbacb105e4ac6827822c32b9775e04a692`  
		Last Modified: Thu, 13 Mar 2025 17:53:20 GMT  
		Size: 6.9 MB (6893209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a910cc8604c8e526ab672da368a8cd60cd9ffecdbe8024608b8a3e8e924c8f`  
		Last Modified: Thu, 13 Mar 2025 17:53:20 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0c792ca0966cd01f94d320994eb139121e54d35c4e3a530d5e6f9fd99ba2c7`  
		Last Modified: Thu, 13 Mar 2025 17:53:21 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d73d2a7342529c37aded6aa3f18cbd1f5f18510837579c01b2497981884afce`  
		Last Modified: Thu, 13 Mar 2025 17:53:22 GMT  
		Size: 48.4 MB (48419680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7e00d873b9f2110505c7cced579ff61754b4673e205488445ab0fe27f5aab2`  
		Last Modified: Thu, 13 Mar 2025 17:53:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a2553d6a807f62f18803d04468fd111e6cf563bdb89d828a8612cbd7f2fce0`  
		Last Modified: Thu, 13 Mar 2025 17:53:24 GMT  
		Size: 135.7 MB (135731357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e76254f5025f1cfb7ebc97fa8d9f501508ac21cddd920bebac1bef1df97b85`  
		Last Modified: Thu, 13 Mar 2025 17:53:22 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:68528bf4ce8f3555e917290f37e37601ce4cc7a8b952a5e98af573d57226c726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7124380a54f9527e1f53c1f65d4950fca1b38323f958664eddd70378197e658`

```dockerfile
```

-	Layers:
	-	`sha256:afa3871c6f65dac1e248f7424fba1b6e8558126156f74892822597ab4e23161d`  
		Last Modified: Thu, 13 Mar 2025 17:53:21 GMT  
		Size: 14.1 MB (14084503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9280c3df3859e243083274627c385561a66d002de1d6b4948a69215cf916b542`  
		Last Modified: Thu, 13 Mar 2025 17:53:20 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0bb914a8c1b6257ee4208380369c567f6b1016eeb0982398c167f8320995808e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236500950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f28080e88370900bbe1d821c85ea3df9a0a31c6c3322f35354f06b6c09c978`
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
	-	`sha256:ce92cb0849370fbaafa6ab88c7b03cebc3063fa56835d9dbf7d0b47c679a0097`  
		Last Modified: Thu, 13 Mar 2025 18:10:14 GMT  
		Size: 47.7 MB (47668022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2303f4a62c55de3c5666d328252495ec3eb67947cc5d75d3d46ae3d8353badbc`  
		Last Modified: Thu, 13 Mar 2025 19:12:56 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d763704225c6d5b23348b25756defb363cf11fc94265a689a18a1509964c25f5`  
		Last Modified: Thu, 13 Mar 2025 19:12:56 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d056028b9c184a140e5804abd9168fd02c6fc091e4859ef66373837675ed4ec4`  
		Last Modified: Thu, 13 Mar 2025 19:12:56 GMT  
		Size: 6.5 MB (6486308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b1500def330ca832518ff9cda277c50a449359f5ffd9e3093f8b9e67671615`  
		Last Modified: Thu, 13 Mar 2025 19:12:56 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065a61ce0ce9ef402c14886e9409e7ace5c2356b090b7d190cbc9698010624de`  
		Last Modified: Thu, 13 Mar 2025 19:12:57 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c8f411b1fa832369ae96617de4398ff6bd698b82f6771f86a0b4af105a4e26`  
		Last Modified: Thu, 13 Mar 2025 19:12:59 GMT  
		Size: 47.3 MB (47295356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beffef775ec722ea5609aea29443bb6f275587c52841b71611485a5faa3d9542`  
		Last Modified: Thu, 13 Mar 2025 19:12:57 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7720939c9d72df4f34b9406209b59706af4c53a702f8cf02f4b73c6e29aa04`  
		Last Modified: Thu, 13 Mar 2025 19:13:00 GMT  
		Size: 134.1 MB (134128344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d921a3558c36c079b9b8a05270286bf6320e0cb263cf567485c48e435a08c378`  
		Last Modified: Thu, 13 Mar 2025 19:12:58 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:99bb7eb90fdcd3bbced1d5ddabceaf6bc7c6ba772b1faf3ceda6a188066a8cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14118618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a514e25ac78ca3dcbfafc2d69c53a58cc0a23b2b6b57fcdc97c5e3ba6b4c0b21`

```dockerfile
```

-	Layers:
	-	`sha256:6050c6197b134aaa91c08527a79bd5fadb5055b3943233fa42148c4883895f26`  
		Last Modified: Thu, 13 Mar 2025 19:12:56 GMT  
		Size: 14.1 MB (14082959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05d4cd92b607a8f348e5c0a8d21fc1ad3859170e6c910855b682210f6dcd0dd`  
		Last Modified: Thu, 13 Mar 2025 19:12:56 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json
