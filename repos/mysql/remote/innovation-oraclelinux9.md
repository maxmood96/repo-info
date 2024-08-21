## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:9ceea965bd96a49b4299b8515fd92c3dc8ab26f34563795a350aae422985ea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:9dc25923527a49b8de140a9e208faf7f00c0b21514b23e6569d53c63d1d50b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170262241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a6bffb6c998c5ffd6c88481981e0a037741d44907152ea2e94d5722613234c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb864cc9a3bd2dde9a981b5f4729a03a9b8370a8fb02c837d6fe16211174886`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b934a1f907becd6f478b6bc6b703dfb83629fe0a171fa9a696004cf47717f0e`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 6.7 MB (6711430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acadb43dd051779979829023f65806eaad0443bce2e9bf60e05f70cf18b54df`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe22960d72c3cc4519cfbc8a6997603938f683c28ec2dc7dda8bc4ae8bc463`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9856e7a4274447dfe0a40b441f65c03a184244f3daecf22e103bbb1e93f9515f`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 47.7 MB (47690153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb79212beaf4ce96310fe9ec8b94df644a8d922d19745ac32f1d991e64843d9`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885acf912a94f1a04dd5426568bebfc394244d1a0c345f1ba82fb5ebb60a7626`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 65.9 MB (65873358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbb350c706285b27404c845f80963694d9d4db32a2dc410c9ac16832ac1ebff`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2dd20e303aa6a9a70c80cdce337e1ffb12c07d4b57cba48a59b30afe6ff71741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddddafdde7a83093655088189b9a6b815cee46b6f41a75c9b442088f77a42411`

```dockerfile
```

-	Layers:
	-	`sha256:449f7555a5f84e6d81dc011f386235b924403ee1f1e865c9af1e1d8ecd5f0aaa`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 13.8 MB (13820563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f9481aa981cc50282578a3e844269f38ef02c302baa33e19427575ae5b71cb`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:29a6f361e800231d32d4624395e9e98c2d346cbfe9f37864016b53bc33decab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167528878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affb2bfc837e9a7361c9df387b89eb37a0b769001f8cb1bd0fa9abb71fdd56ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394d9fd8cd54292151d463f653c6f42ca47ea2f0cafede81b3cbbf703a5dd97`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c130709c94e50dc69e7c8d7d78923fa17c7cfafd7410ed52f5539e8de93e2ad5`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 46.6 MB (46581568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef2860059f2b1ed77483e2f97114a2fa3dc8f2d333bdd948c592ae3420bf5b`  
		Last Modified: Wed, 21 Aug 2024 01:07:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c4e968e873574a849dad79bdc20ac439e4e26903e1af8633c450465296dd4b`  
		Last Modified: Wed, 21 Aug 2024 01:07:59 GMT  
		Size: 66.1 MB (66055908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02ede93afa6fa1da188907383ac3f5c19a6797df4936fcbbbba2faf252aef0`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7074c3c778d62cef28870c6018d559c21a24905a8b6cb0d64a4f9878f5d28bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac3c71581b77db2e81ea1b222338aadc792276af410f008a372497486bc441a`

```dockerfile
```

-	Layers:
	-	`sha256:ca417120b66da7fd75b026dc826e4d9a45e4451a683215d63b7ded456c607b6f`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 13.8 MB (13815749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c89fdeab249fdc26db3da969e9fd14e616c0001790dab5b0d07ef47b6ef491`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json
