## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:28540698ce89bd72f985044de942d65bd99c6fadb2db105327db57f3f70564f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:dd42a451fe2a7ac18f9fbc9478c30596372cd27c2222c4cb50620338d03ee26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274726167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d568f67edbcf69c54ea79487427c32545904967c48506583f4766e787e766732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:21 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:22 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:56:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ebb6c280f32a1dfc2cb5f613ff06fc9655058e47ce2bad6c0d13d2da035f79`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908b1bc00359c9aae93c3b9c769ee2ee12f1b1a21696f48ffe53d644567e76a`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db16934d0d6e819d06f6b2cbf38d291093a463681e6e85ac330429acaf5e7fa8`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 6.2 MB (6171583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e867246b3f6037ef3b66680fd529522051f7f583f973e7dbceeb5bb5b0f0a155`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535942d9d4859ea36596b22311a813c21c7defcca5ac911e0770608e56a27a7d`  
		Last Modified: Mon, 01 Dec 2025 23:57:38 GMT  
		Size: 51.3 MB (51336861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe13791f0771c7f09a6c5f55fb1282480fc41d18fd6bb85177a6416551006a53`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11039659ba62b150c643aebc494fa3bfabdd8e5c4175cdc105c81a747e8832d3`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 169.1 MB (169112510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8d13e504cb59db0790adc6737e2aeac761be9fd5f46a12dff48f4391d7b87`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f435df576ad8d14dc479a4c624c7f4e762d5d41a6a073bba3455392c2584161d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e17b047ec75afcce73a20b56745d08ded16b02b57cc4d1d80ceffd42adbead`

```dockerfile
```

-	Layers:
	-	`sha256:281726107253b80d8c24afec196d3fb967bbba51ce136132bcb07873bd92c2ce`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 17.8 MB (17815020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd72744b88618cff278d4719e7eda816d1ec29e04d9f0cc4e8c3084c39933fe`  
		Last Modified: Tue, 02 Dec 2025 01:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26805bc8977e93152ad61f620b70b87aaf6713d36e42f08ad6eb322359849465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269789897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6dc43ebcc2dfbf41bc4e606bf57af93eef0de4dce44b411f30ec577a5683d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:01:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bbd8b344977d2131957f2f00f275441274e31715dc1d1473c20b8ec67524eb`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199e342212b84b8ef4f240bec84f21a4215246de8d514308f3c95990e19e8f0`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585198749088ef70e67058ff70bd094344444fbfe9211714dc78aa4e98313953`  
		Last Modified: Tue, 02 Dec 2025 00:02:31 GMT  
		Size: 5.8 MB (5796160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afd93cb2f54f5ba58e374886859e031cc72622d3ecec202e10a297dac8a4873`  
		Last Modified: Tue, 02 Dec 2025 00:02:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944b0228f20de1366fc847ac7dd86e376ac7b58b1cf99acba420bf9f7b2c7143`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e6790a7fa3a430d20c6ad9edc7708cefba9e84f5f0a5a90a92f099da964d75`  
		Last Modified: Tue, 02 Dec 2025 00:02:37 GMT  
		Size: 50.0 MB (49959028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b134e4118a9ed82dc6a87867d0f859409fdcccbd7301cb1ef2aa6af3e4297b`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0554060e6af42f8c244b9c96788834fdbaa79f06e9864d21397ef25be14e822`  
		Last Modified: Tue, 02 Dec 2025 00:09:41 GMT  
		Size: 167.4 MB (167390718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63aaf551940125ab8fb1726f3d86414721b584566486906cbfe481da077c0c8`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:402f11d78a6bc3f10146c41aa1fd9fd2348b303f4abeb191dec58783a8fe245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa3c8bf5ce62b96b1b24554d4fe819b77d4ab7c488bae2bbbc7ec2ed82f22a1`

```dockerfile
```

-	Layers:
	-	`sha256:5ed8c2c4a68789e5f36c3d3a8dfa2562bb661d11ba9cf1951e3c5a3a7c0208ff`  
		Last Modified: Tue, 02 Dec 2025 01:03:31 GMT  
		Size: 17.8 MB (17810163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5251c790224237a824a0a3199cb8907eed13a99a203660bfe0e5cfcb9a1663a3`  
		Last Modified: Tue, 02 Dec 2025 01:03:32 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json
