## `mysql:lts`

```console
$ docker pull mysql@sha256:9206fc2d8849cb6ae7128c2dea8aabd6c88fc8163efd1286b3f9bb74e6219bd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:cd8ec80bddd4d6da7e22763e79efc7c63da19c3503b1f90987320d0e6d5cedaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169774555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f742bd39cd6b457c890bfb3761fe201d69508a68d832c0caebdb6bac3df5e60f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c33853069527a20d8702eb39a35923717fc03298126567889f0e743bbb364`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773855fa856dd0b9fac608e69963798f34746397caa3b47b955b6037c304cd22`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b5068022ec99e20b6d9730419a0d24c0b44222444ca5aa9ff3763c7f0a515e`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 6.7 MB (6733344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627a78504886fe803ea6c81b60a507b6dc2c4faae39e9da4840ff89270335c2d`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ce992a870e328aff157043f3dca1888f3e464a7ba8ed9e21afb36b0f04c719`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b702ee9d4615b556f3467a9886da20925b3db0256f30aba7239aaf866f3b24`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 47.2 MB (47248252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b30f90bce11f70386835f3faad14d11a4e6d8b451062fafd67f64482208008`  
		Last Modified: Fri, 20 Sep 2024 18:50:09 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed80156b17ce0172c5fdaa4436e4f2b84be974e00c1cc8fb7eee7d4524dd940`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 65.6 MB (65553540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850c36b0e995bdaad53c3ce5238f4f7aeac7fa60e390006c38f932431e26e606`  
		Last Modified: Fri, 20 Sep 2024 18:50:10 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:fbc9855d741ec4355d531fe01118b359d3767d7e02f6eec498cbbb425918d3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 KB (38898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d366ea8923cf86d05648497bf2343eac6a346b0c3a0f986b46155f9b7265938`

```dockerfile
```

-	Layers:
	-	`sha256:ab77b22499dae276d5f8afc4916bfda88ea6ca4f62d506450bffa580bb1155e1`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 4.7 KB (4683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52f95083791286233d23aab94979c00996cfb342ca6953c526ace569daff7d2`  
		Last Modified: Fri, 20 Sep 2024 18:50:08 GMT  
		Size: 34.2 KB (34215 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json
