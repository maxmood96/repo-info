## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:56bf447e156cf9abcd862d140527647d25331cd18f3546849e684de1172c6b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:940fdfa3dc408fb792a8cceb21cafda4b7cd56ce4fbc32833766bdd2a57d6a4f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131636256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcfb2bcbf716a71cdb2dd51277575869547854e0c57519c03cd5d5cec58a9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Jun 2022 18:23:26 GMT
ADD file:837f6c6e7e20067b92edb72e78a8399e6cbbd72dab23db7b5b5a301c58d2a0de in / 
# Tue, 14 Jun 2022 18:23:26 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 18:39:39 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 14 Jun 2022 18:39:39 GMT
ENV GOSU_VERSION=1.14
# Tue, 14 Jun 2022 18:39:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 14 Jun 2022 18:40:04 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 14 Jun 2022 18:40:05 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 14 Jun 2022 18:40:06 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Jun 2022 18:40:06 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 14 Jun 2022 18:40:06 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 14 Jun 2022 18:40:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 14 Jun 2022 18:40:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 14 Jun 2022 18:40:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 14 Jun 2022 18:41:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 14 Jun 2022 18:41:10 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Jun 2022 18:41:10 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 14 Jun 2022 18:41:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Jun 2022 18:41:11 GMT
EXPOSE 3306 33060
# Tue, 14 Jun 2022 18:41:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5f160c0f6cac587a73883b48a8857f5cce0930112792cef25c62510e256e93dc`  
		Last Modified: Tue, 14 Jun 2022 18:24:18 GMT  
		Size: 39.2 MB (39219730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86c3d841d1984f858257755bdf734554725af4f926f3b1d1b22f119cce8bda9`  
		Last Modified: Tue, 14 Jun 2022 18:41:49 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f026b3ec1ed102cfe531d812e2063669bad08ac3a0ac68a31e44083d9b9a5f5d`  
		Last Modified: Tue, 14 Jun 2022 18:41:47 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80b2ddd662a38dbb423dbaa2be04afd41904253b436138b52f2a73aa46a5547`  
		Last Modified: Tue, 14 Jun 2022 18:41:48 GMT  
		Size: 4.5 MB (4535169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7724a6d28d1e789da86c89f0010caa7de0e4747dfcd360fa981a194850951f`  
		Last Modified: Tue, 14 Jun 2022 18:41:47 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8122570b85fec5c1d3bc0c08a48be2657da195b764c9a13b1a791a086c007368`  
		Last Modified: Tue, 14 Jun 2022 18:41:45 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea018df6cdc3d2aa821feb43a3035926c0c296b3c363e64ab0fa95f144f2e7b`  
		Last Modified: Tue, 14 Jun 2022 18:41:52 GMT  
		Size: 47.2 MB (47244178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8066c16abd2efdd49dd1fe3fab6fec9d250b699d9c0227f69c779c8da2c2acd6`  
		Last Modified: Tue, 14 Jun 2022 18:41:44 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd480e7da7ced7cfb1fb54d07fc5eb08057151be162150bd053f4eb89d9ba85f`  
		Last Modified: Tue, 14 Jun 2022 18:41:52 GMT  
		Size: 39.7 MB (39698832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b680e02f092e5330cf0200abf3ba02bddc3d440d02ebb11ec6ed8bf2ba3155`  
		Last Modified: Tue, 14 Jun 2022 18:41:45 GMT  
		Size: 5.2 KB (5158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0418232b74414d7e223da6fc26f47d9498abd72b4ca3bb1cd826f8f05ea55374
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138660393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0eef221ccdafeb4649e0af86a16d1bf826ed66807fd64248a212871c04c2a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Jun 2022 18:41:36 GMT
ADD file:4a6ee90ad73353bfb87b2f121e06bddaed6104536e485baa83fadbe7facc774c in / 
# Tue, 14 Jun 2022 18:41:37 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 19:17:17 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 14 Jun 2022 19:17:17 GMT
ENV GOSU_VERSION=1.14
# Tue, 14 Jun 2022 19:17:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 27 Jun 2022 23:40:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Mon, 27 Jun 2022 23:40:27 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Mon, 27 Jun 2022 23:40:28 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 27 Jun 2022 23:40:29 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Mon, 27 Jun 2022 23:40:30 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Mon, 27 Jun 2022 23:40:56 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Mon, 27 Jun 2022 23:40:56 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Mon, 27 Jun 2022 23:40:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Mon, 27 Jun 2022 23:41:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Mon, 27 Jun 2022 23:41:27 GMT
VOLUME [/var/lib/mysql]
# Mon, 27 Jun 2022 23:41:29 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Mon, 27 Jun 2022 23:41:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 23:41:30 GMT
EXPOSE 3306 33060
# Mon, 27 Jun 2022 23:41:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2bbc1bf883bd601c0da5735b538963308bcc17f90d36525ecc93456ffad79064`  
		Last Modified: Tue, 14 Jun 2022 18:42:39 GMT  
		Size: 38.0 MB (38012371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8428f9d18fc319262a774f75a5849d4819b5b44cbf07fbb5e3c262e5cf30c22d`  
		Last Modified: Tue, 14 Jun 2022 19:19:14 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69cba94044003680a99c76f187ea817c71b843de38bb7f28faf8ca6508efd45e`  
		Last Modified: Tue, 14 Jun 2022 19:19:12 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac1107eaf64ada9002dc0dbf73e0a8b8c2a3e2dfe557a59ee79ae5296dd6d35`  
		Last Modified: Mon, 27 Jun 2022 23:41:57 GMT  
		Size: 4.4 MB (4400369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287b497aedf9bf453ca624e6f7b036489fa7091918b209ff279b763cecaff56e`  
		Last Modified: Mon, 27 Jun 2022 23:41:56 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95691dcdde5f2ee25bddc7d7b86e909e83b4afb1e4df5fad18d9522c3f510579`  
		Last Modified: Mon, 27 Jun 2022 23:41:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5782ffaaa3341fdec1b0c7406c0492d5cff1a9970a6bd418392b7174e60bea6f`  
		Last Modified: Mon, 27 Jun 2022 23:42:01 GMT  
		Size: 53.3 MB (53324071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01dd932f22732278b472cba5572dc1447697a6c2ef0d4ad0fb6f0d9ae009d07`  
		Last Modified: Mon, 27 Jun 2022 23:41:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d729e5c05f924689961a0ec3f59e39b68696747fe8e84592e0c7d3466f264bef`  
		Last Modified: Mon, 27 Jun 2022 23:42:01 GMT  
		Size: 42.1 MB (42056996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abe7fac72065516d8f16acb9fddfb5df729c103afd883ab5c353157a60ae4be`  
		Last Modified: Mon, 27 Jun 2022 23:41:53 GMT  
		Size: 5.2 KB (5161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
