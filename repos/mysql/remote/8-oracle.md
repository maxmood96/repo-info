## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:7dfb7bd2124a1a99fb7d5cfced33d3a6fe2795e11ac9bd3a600c8ad22b352b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6964c211b5fadfc3b6a84986cbd3c78418b091c2fd44074f58d9c15d9b0f5f52
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132816933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70325c69f1fe76e7f4e62e62fb5ef4e76acb45935075cec7b4cb42a928fef78a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 26 Aug 2022 21:25:57 GMT
ADD file:923c2af16ef366fe4e85b8ba8979b8a31da0cdbc606c08148463849bf66c395b in / 
# Fri, 26 Aug 2022 21:25:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 21:55:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 26 Aug 2022 21:55:56 GMT
ENV GOSU_VERSION=1.14
# Fri, 26 Aug 2022 21:56:00 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 26 Aug 2022 21:56:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 26 Aug 2022 21:56:23 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 26 Aug 2022 21:56:23 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 26 Aug 2022 21:56:24 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Fri, 26 Aug 2022 21:56:24 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 26 Aug 2022 21:56:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 26 Aug 2022 21:56:54 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 26 Aug 2022 21:56:54 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Fri, 26 Aug 2022 21:57:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 26 Aug 2022 21:57:25 GMT
VOLUME [/var/lib/mysql]
# Fri, 26 Aug 2022 21:57:25 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Fri, 26 Aug 2022 21:57:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 26 Aug 2022 21:57:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Aug 2022 21:57:26 GMT
EXPOSE 3306 33060
# Fri, 26 Aug 2022 21:57:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ee4ca39e1b6ea333d785f1cbc6b64b874a4f16f1200dad9e17d2015c925d1d57`  
		Last Modified: Fri, 26 Aug 2022 21:27:39 GMT  
		Size: 39.5 MB (39520501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55731ee5cc27ced42a0ea701da6c01ea54436624a61249e930ac796f0d539a25`  
		Last Modified: Fri, 26 Aug 2022 21:58:10 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fd4ba8837dcaaf863ffc3ef194a0811c9a25271e9a6f8f97791f35311eb150`  
		Last Modified: Fri, 26 Aug 2022 21:58:10 GMT  
		Size: 928.8 KB (928832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdb35add3bdb652fb29883c67fc10bd46a3fb0be64298abc066a4a06bb37115`  
		Last Modified: Fri, 26 Aug 2022 21:58:09 GMT  
		Size: 4.6 MB (4613200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb34f3e592a8dea4241df25f68119b066f2c978dfeb6af0e57b637bebf3b1a4e`  
		Last Modified: Fri, 26 Aug 2022 21:58:08 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961390a73dd279bcd61e333bc0319200dfb88add6a01deb2159d608df495cc39`  
		Last Modified: Fri, 26 Aug 2022 21:58:08 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338d4f22364bc14c90f342e4cb8a945b9e0caf236cfec0b19cff3d702d7e01b2`  
		Last Modified: Fri, 26 Aug 2022 21:58:13 GMT  
		Size: 47.7 MB (47741816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633ee7c9891570f248e85d04fe735e5574693fbb615ee5c36dd743c96df097fa`  
		Last Modified: Fri, 26 Aug 2022 21:58:06 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961374a411ee16c47884f4887ba1ffce8e0bc51523a59ff121734a06ac8ca3a7`  
		Last Modified: Fri, 26 Aug 2022 21:58:13 GMT  
		Size: 40.0 MB (40002910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da93a12a127a0237fe8c07cb62f9228af9f799d0ef27e4825bf31914c52b276a`  
		Last Modified: Fri, 26 Aug 2022 21:58:06 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6931149ad6ae8c447dce56977bfe1173a2197f264f3ccdee1e2bff7700a48ced`  
		Last Modified: Fri, 26 Aug 2022 21:58:06 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7fe463a176858bbb882d302561344a5519fce58979d8dd2a627b0259d611b5c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141495395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddc4f9f115246d8cf8d7a10f6ef4b99e49f17f4179d37718fac9b7230505df4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Aug 2022 20:47:49 GMT
ADD file:4f53d93ae4bccd786d6beda6f0ec4a450fd23a8fff2786d9e5b024a64aad6bb1 in / 
# Tue, 30 Aug 2022 20:47:50 GMT
CMD ["/bin/bash"]
# Tue, 30 Aug 2022 21:04:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 30 Aug 2022 21:04:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 30 Aug 2022 21:04:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 30 Aug 2022 21:04:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 30 Aug 2022 21:04:57 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 30 Aug 2022 21:04:58 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Aug 2022 21:04:59 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:05:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 30 Aug 2022 21:05:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 30 Aug 2022 21:05:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 30 Aug 2022 21:05:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 30 Aug 2022 21:06:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 30 Aug 2022 21:06:01 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Aug 2022 21:06:03 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 30 Aug 2022 21:06:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 30 Aug 2022 21:06:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Aug 2022 21:06:05 GMT
EXPOSE 3306 33060
# Tue, 30 Aug 2022 21:06:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fe1dbcd3b09e2c1e850118728988d6907b2f43969fe81443f422984829c640ce`  
		Last Modified: Tue, 30 Aug 2022 20:48:58 GMT  
		Size: 38.3 MB (38321155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628eaa205e4b635ea4abf3ffc1a274715fb21c62c9b5c13aa64f85b69194e4d0`  
		Last Modified: Tue, 30 Aug 2022 21:06:42 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c86bcae889d228807ca84be5d984746905b9f13b54f3d9e24ad5ed5ff2ec2`  
		Last Modified: Tue, 30 Aug 2022 21:06:43 GMT  
		Size: 857.2 KB (857151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd832022692a0dcbf9d863e7eb7298414ea6eeaa9b6a161e6b1f78ed800d453d`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 4.4 MB (4418862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc8449c44525b800b41e95edd00ca97388523235c4fb10422f90a261cc8026c`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c599e7bb6ea36dd75b58157ad8fced435621da7e033b3ed09b66c284f11f4707`  
		Last Modified: Tue, 30 Aug 2022 21:06:40 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3bac2fb7b290eef8c30ea6c5e12306aaab34e63af0559f1a95529ab2582fea`  
		Last Modified: Tue, 30 Aug 2022 21:06:45 GMT  
		Size: 53.8 MB (53803331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00fc0afe35569e52d9133a93e8265a26a4e7d1dda0e751cf7167d453cdca6c0`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca167dc4dd6fb3c2307e7dac2bff332ab3e6fa4ac308ab4a6817fbc6fde70dd`  
		Last Modified: Tue, 30 Aug 2022 21:06:45 GMT  
		Size: 44.1 MB (44085250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55769c82e12ba04740e57c8c4799cb16f8f6feccf2b96594ffee842f8ea680ca`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9551073dcb49db8ce5058768ac09128d8ec9411565cede87d638791e7c35676`  
		Last Modified: Tue, 30 Aug 2022 21:06:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
