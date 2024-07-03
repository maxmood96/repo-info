## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:0a4acc6d272909a42df161d30b95ef1880f0fa07e9119e76de43f4563459ec3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

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

### `mysql:lts-oraclelinux9` - unknown; unknown

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
