## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:8b879a3959bc59adcb7281a41950d39cf8c9b3fb23b87b9b62318ce884a7c383
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:32fb6694d3cf0467dbb4d3bb02de218775506335da7293bc8fb258f2470252db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e413dee93df7f89216bb2d198c66261e0ba690020c4c5674f5aca813ac0479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e1a23d747fe18085e089bcdb3ca9f3d0d157dc8fa1c102f3fb2a21b751c14`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28a4a1c472b30ae4c345429eb1af286f0c49d904d27bc3ebfbade41ab2a51b`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 913.5 KB (913450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6445e04f075a67c2690b732f479b7154d6ea98378a928987cadc017be50b9c34`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 6.3 MB (6314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed1698398538ee026eba55ffa523b27771286785309b5b813c41bb38ef5911`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165239427fb2d6569c5f45bbb9db9d25fc84f7a51f698a9761db535e78f02ff9`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38fffb73a4211a25400f7d2309137384b9fde96d33f076f090445835927d14a`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 46.6 MB (46592623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e6065449687e6e72bfb2b668e732b0b037d407fef4c6382e9856be40cf87e2`  
		Last Modified: Wed, 03 Jul 2024 01:52:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713aeba068a26251712578b4b15cd756f00790b76a22fe81792ab77f7eed004`  
		Last Modified: Wed, 03 Jul 2024 01:52:52 GMT  
		Size: 66.1 MB (66059310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4209b7ddaec0de809f531af4fc9c7389344dc8aa4eeb66b1c9e84c4f69d967`  
		Last Modified: Wed, 03 Jul 2024 01:52:51 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fce3cc605f56babb7e8b593c1140ee4a9e7950e7c5d266c216779b929b75a495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a646c47944a46710b7de183b62400d9bcab2f32022da0154debccbddb6b4a`

```dockerfile
```

-	Layers:
	-	`sha256:b8dde974271a2d566789a3c56c107f56d89c2f8b1d15991f27ecf853afdaef2c`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfddd4b0e1552d6246e226a16342782ebd3d7802495aa204a581e7b395caeaff`  
		Last Modified: Wed, 03 Jul 2024 01:52:49 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json
