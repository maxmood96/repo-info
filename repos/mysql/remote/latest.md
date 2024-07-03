## `mysql:latest`

```console
$ docker pull mysql@sha256:b41316975c64a7394c4f385566180d5743c9818583473b18bd6d74c41fa00cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

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

### `mysql:latest` - unknown; unknown

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

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:81e9d95d528511718b81cb9c548e1b922976bf359ed1083782bdbbbccf9ad85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165935645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26af66f0ce61786c7c80a4c3df3fc82449ba62eb649d2a456841697910e1e988`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeaac00f5df03f6f38bf7ecc4769b9a23e55056025a5851c1a4d5c4686a8b7d`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93611301cba5889c772d61260e8efc0c7c1c37a70e8e7db9efc2b2cf67010e53`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687d48bd5eed486f834f2aeeb98c3b31c69632e804094345d8fce02a284c911`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 6.3 MB (6314755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbb8564b525ee1fc261327bbc1a7f748c6f0cfb4c5b57fab5ecab6c2221b850`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1bd0a565d7cf1e2dc7481c126af4bc99d8452795d57895c45de63bf2fe9f48`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d3d3a6688431c46150da632ff0efc970557606cbb0a203fda8d9d19a20990`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 46.1 MB (46085104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ed4303a4e50950db106c0879157df3c728f33abce028195ffb1b6043fb7315`  
		Last Modified: Fri, 21 Jun 2024 20:53:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9690ceac92fb0094b530371d299c5daab1c86ef2eb84a309bb82c1c503e72c0`  
		Last Modified: Fri, 21 Jun 2024 20:53:15 GMT  
		Size: 65.0 MB (64960102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126b0c16732837c2e605f427369b409489aee417adb922a9b505fc1e2f6d7367`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:96c74d9c944ec216dd0905796e8266e5eda94c473ef92203cac63cf9ac813690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c494850bc9fd62051a3865528b786eb10a05e07a7c67a5130389dbffd49a4d5`

```dockerfile
```

-	Layers:
	-	`sha256:3de42c8f2b5abf1f1286cb643a75df2bad4f4cd8d9b1ec11f1f6577283cc3c68`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 13.6 MB (13556214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4242312b762224f545c08985e96af2caa198878729e7929714cc0e98c88f2c`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json
