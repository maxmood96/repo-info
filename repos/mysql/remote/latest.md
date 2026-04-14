## `mysql:latest`

```console
$ docker pull mysql@sha256:9b69d1776846f437243ef5b6599e31ef11b317b60babbf37de21dfb38932dbc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:293568b65abf19458159043d9732c0c2709cae23b667ce2b4c2287efa20b9548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266346024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf70b94193eaf72587af450da5894cea4618b1bb06e43e57f18aa62e67b7f9db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:44 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:13 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:55 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:55 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0ec069c9cd5ac9103c7a520cb11dfe73b1a9b1fe2ee81ebdb76b0fc5ff18e`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061cabbd0c34362de1bb33fd5274a664d977130f11aedf981bb5570aa5fd8aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fccd87f358c51ab5ccb27c97e2098347ca6840005fd33a099743e46854f405e`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 6.2 MB (6170043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d0deb4205f9d0665254f6e7f6db1d757b88707dd6a0597b8c3c56c9223eb80`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9786ad645331e605504b837a79176f4d89527bcc0266c46d9c4505d73ba60e`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57121fed762a6791347072d85d00dbd9067b0518e6a680ad4c09833a86bbc5a`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 51.4 MB (51443668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fc379bdf14e754e97b2185967ed519087ecbad1f3d17142a95b0a93feb826`  
		Last Modified: Tue, 14 Apr 2026 19:13:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524e9fe686ebd0ee9dfe9093ab1d621766327a6d1828df1a7f997ce715909d41`  
		Last Modified: Tue, 14 Apr 2026 19:13:36 GMT  
		Size: 160.6 MB (160628862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119fb62783d0039b2aef6a2d75bbfba8b7b65deb2d74c1761eeb2c5f038f5e53`  
		Last Modified: Tue, 14 Apr 2026 19:13:33 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:b2f49e1ea698f5050ed985b1266c08462f8a6bbd269d82ad357b5f25026145e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aec375a00ab4b9553e0ff69f64aa1814d5673599a6134d6ee810e6f70a088a7`

```dockerfile
```

-	Layers:
	-	`sha256:c60ece342068acf24c11e9ee69ef698ff4724fb692792d27336e3093a51e0d74`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 16.3 MB (16297452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6478c2ec550fdd422e388d003f731bfa39369d9db8c581b9830c4ab57f39d9`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9bc1439fef05e41bc4d35a2a2436d5859aca015f8526ee2df2fa22c2f6b45040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261443434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771f172911b8c47eea2b6ea07560f9ea5b0e483fc1cfaf54b43faa907684f49d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 14 Apr 2026 19:11:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 14 Apr 2026 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 14 Apr 2026 19:11:38 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:11:38 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 14 Apr 2026 19:12:09 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Tue, 14 Apr 2026 19:12:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Apr 2026 19:12:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:12:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 19:12:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896781c011d25cf234ffd0c0fa374676f62a98951123bfb46266e17d46a663d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa84208659020d752d622fa9e3e2665087a0d7029328bb1aff2226ad4c858d`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db918e56439b6879b1a0cfaa740fdb0eb5b343faed3f2aea9621120788c49f3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 5.8 MB (5791943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c9f27d8226aa6b92eb507a7eb160a1bbf5545a98475f6a151345ffc9eda11`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b3e259c5b537f7297025424f4c3f22a30b4c41aaeea68718a9aee78049d4f`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b800cbfe6348e0c79d77e51ec6ed765cd31da53322ce7963a943e07a55890aa`  
		Last Modified: Tue, 14 Apr 2026 19:13:31 GMT  
		Size: 50.1 MB (50080340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46218bad4f2276becb57b16930f7b9ea148e88f56e808cc4a0b9659ff36333a5`  
		Last Modified: Tue, 14 Apr 2026 19:13:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a2471671bf753ea9c5214e96f1ff53e042a5aeb38150550770baf31042c213`  
		Last Modified: Tue, 14 Apr 2026 19:13:34 GMT  
		Size: 158.9 MB (158924452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955ea24d972da7b792a20becf72704b2ae682f80fd60a21a488fd7c06ca45356`  
		Last Modified: Tue, 14 Apr 2026 19:13:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:b7740a991aaba6af976e228ffad85cecc00c14648e85081ac531fd6aeafeae0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a1faa7e3018914e322777c8834d39c6c8e0cb4ac3070f23e843763ee134ef2`

```dockerfile
```

-	Layers:
	-	`sha256:8c5cf86452c2871a87aa05e4755ba12fa213609fece345b61a01fa01e8b991f6`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 16.3 MB (16295908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43fd1cb70c5c79f4b4868c05a41cd62da724c6d55a93c65b7da1e9fe4d349dd3`  
		Last Modified: Tue, 14 Apr 2026 19:13:28 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json
