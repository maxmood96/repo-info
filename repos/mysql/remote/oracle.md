## `mysql:oracle`

```console
$ docker pull mysql@sha256:9de9d54fecee6253130e65154b930978b1fcc336bcc86dfd06e89b72a2588ebe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f9097d95a4ba5451fff79f4110ea6d750ac17ca08840f1190a73320b84ca4c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183363460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f343283ab56d883ec8ea17641b5d61d0252cc6c97dad3849cf3681dd1e2f37d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:c53be7373aad45b6ab1d0accc144396269617e0efcd2892e9521c25fe73fd71e in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd37f6d992035c9959b83f8f96b15cac9d66542a608f378e6e97c17830b72d80`  
		Last Modified: Tue, 16 Apr 2024 19:55:43 GMT  
		Size: 51.3 MB (51320403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e733cb05765178b34cf17a4926b891f9b2613926275bb1fdd22854ce43a0d566`  
		Last Modified: Tue, 16 Apr 2024 20:50:50 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2fd35011dc60f3d2c366ff4238f17bc60551ef02d666c4b9e0c242a0110abb`  
		Last Modified: Tue, 16 Apr 2024 20:50:50 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5233d0f6ee34ea3a107eda8bc623887e3d478e179c9df9f2cc063a66347b51d`  
		Last Modified: Tue, 16 Apr 2024 20:50:50 GMT  
		Size: 4.6 MB (4599719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf11fd8658d3b9f083d0c09bbd2ab276319761e9f02c60bf107a3129a660f170`  
		Last Modified: Tue, 16 Apr 2024 20:50:50 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85344d57c3cb3d776d39392adfac3b66fb93447923d10761ec5c7221a70f71e8`  
		Last Modified: Tue, 16 Apr 2024 20:50:51 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eebca71f40d7370cc0bf2248ee15952632e5707014828ef1fbb2b9d59b36254`  
		Last Modified: Tue, 16 Apr 2024 20:50:52 GMT  
		Size: 63.1 MB (63080394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e468a1ddacbcd8250ed7a53040e50b12b12c1f481d9189554dbfc8171346be`  
		Last Modified: Tue, 16 Apr 2024 20:50:51 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b2b8d35c755381751828e7dd4d348d2a1900f32a0124220f78d4d15cd1cd5d`  
		Last Modified: Tue, 16 Apr 2024 20:50:52 GMT  
		Size: 63.4 MB (63370611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ba1b7684b4f2842be26f4f6e5f8e3d38238a5178910f101901c691b3c42626`  
		Last Modified: Tue, 16 Apr 2024 20:50:51 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3f5d4c1f99770d59111800952284c1a80e8e6fc828e26b25f116f66d99844735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14286655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:186c02e5b6f3d708cfe1efbe49d3c068cd9dfb9dd74f6760730212223996e19c`

```dockerfile
```

-	Layers:
	-	`sha256:4e8b7f1241451186661b95027593572bdca3ef77eebca723e1aa617a8b8af302`  
		Last Modified: Tue, 16 Apr 2024 20:50:50 GMT  
		Size: 14.3 MB (14251402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d45cae7db54bea401477859de885e554b1f8018c57b7a0d8dbc904780dfca8`  
		Last Modified: Tue, 16 Apr 2024 20:50:50 GMT  
		Size: 35.3 KB (35253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3c8a4cbedece61d65a71af97c3faff88b6fdd7aeb9440b425e8e9fa57a69626a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181380839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e24fab8e6af5839ad220ee529c92c5928d1924ff29dad29a15f6780a5c6665e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 26 Mar 2024 03:50:44 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Tue, 26 Mar 2024 03:50:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Mar 2024 03:50:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 03:50:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 03:50:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 26 Mar 2024 03:50:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd4f8e415ca18dc0ceb9fb0cc7ce91b49cb4a4df85151ed7f3ac2a61ddb2012`  
		Last Modified: Tue, 16 Apr 2024 20:07:50 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e01a6ece3afbc5e9bbbcf1d8150dc3de9ac2b3ab6d578ac17d120a0a62f6c75`  
		Last Modified: Tue, 16 Apr 2024 20:07:50 GMT  
		Size: 913.4 KB (913449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfdeffd91404630ce8145820b88429909e3310d33ddac4cf26ae972b210360b`  
		Last Modified: Tue, 16 Apr 2024 20:07:51 GMT  
		Size: 4.3 MB (4302586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fed55ee93c9e222231cb00f47e3c950d52db4ab075c39b00af2e9667efc387`  
		Last Modified: Tue, 16 Apr 2024 20:07:51 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83404f4e484731eac2bcaaff89ecb8f248d8c50e91327fe8ba01306ccedfa082`  
		Last Modified: Tue, 16 Apr 2024 20:07:51 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad53405df78905dbe9a8138ff4af0ec0884f51399560aa7d4dbf2f86957d021`  
		Last Modified: Tue, 16 Apr 2024 20:07:54 GMT  
		Size: 62.0 MB (62047645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c5f6f4cc6ea294d63df235115dc2e0f05975c7a64c4797f7564d27fed87216`  
		Last Modified: Tue, 16 Apr 2024 20:07:52 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04d803ff9c763a1e4ae3130e44f9cf7c017a6fdab5fb5b4177e3c126aa4b822`  
		Last Modified: Tue, 16 Apr 2024 20:07:54 GMT  
		Size: 64.0 MB (64025553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06a309d43da9db3985213c267cbf2a793473570363421fe8307e668cfac4c2a`  
		Last Modified: Tue, 16 Apr 2024 20:07:52 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a0f3689f8c039124c43ae02cc65a61678060a14676cb8bd9cf469c8d7cab44bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14284968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa1b87b47cb8518cc19f4da37c13a97c12d1d3443ccf8ec1e4c08d39b5b9052`

```dockerfile
```

-	Layers:
	-	`sha256:a61aef2dca857c98747bc19da218316c85b9bee6eaa1d8d7822a948fc03c1636`  
		Last Modified: Tue, 16 Apr 2024 20:07:51 GMT  
		Size: 14.2 MB (14249682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2cce9e6b95bd139abe6dbee0a649ce8182887f94f0707616e97e83523676ce1`  
		Last Modified: Tue, 16 Apr 2024 20:07:50 GMT  
		Size: 35.3 KB (35286 bytes)  
		MIME: application/vnd.in-toto+json
