## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:c0455ac041844b5e65cd08571387fa5b50ab2a6179557fd938298cab13acf0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:eb00f19a38312b85bfb7195eead2d07d35279f2a6a61b3dc994094dcefa57986
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166745819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99afc808f15be15cd1d9890394123034a79d1f3204d5b417d8558990cdf30167`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:36 GMT
ADD file:196115c6281a0a56854066be2766eb0dc9da452f60a060b90bbe681e6b8ffc11 in / 
# Fri, 11 Aug 2023 01:20:36 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:37:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 11 Aug 2023 01:37:15 GMT
ENV GOSU_VERSION=1.16
# Fri, 11 Aug 2023 01:37:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Aug 2023 01:37:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 11 Aug 2023 01:37:47 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 11 Aug 2023 01:37:47 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 11 Aug 2023 01:37:47 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Fri, 11 Aug 2023 01:37:47 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 11 Aug 2023 01:38:20 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 11 Aug 2023 01:38:21 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 11 Aug 2023 01:38:21 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Fri, 11 Aug 2023 01:38:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 11 Aug 2023 01:39:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Aug 2023 01:39:00 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 11 Aug 2023 01:39:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:39:00 GMT
EXPOSE 3306 33060
# Fri, 11 Aug 2023 01:39:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b193354265ba898bb7548038f52378b3dbb6aac5afbaca49bb83ccfe51dfadeb`  
		Last Modified: Fri, 11 Aug 2023 01:21:58 GMT  
		Size: 44.9 MB (44910081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a15c0bb3582b6a26d2c2e3705d5ee1606426cecd044ef8723a35cfa87be620`  
		Last Modified: Fri, 11 Aug 2023 01:40:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02da291ad1e4b296bbd625851ff7cea3c2d034fe2e0b228ca9ae2bea95cda090`  
		Last Modified: Fri, 11 Aug 2023 01:40:52 GMT  
		Size: 982.8 KB (982824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a89a1d664eece0e3ff93bd9fe2e4adc040111786f1b96cfab84f4ad6fd798ae`  
		Last Modified: Fri, 11 Aug 2023 01:40:52 GMT  
		Size: 4.6 MB (4603476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24ae651305152f1387de87ffe3e801ca863c5fec0a0ef7a35d7945a204334b8`  
		Last Modified: Fri, 11 Aug 2023 01:40:51 GMT  
		Size: 2.6 KB (2626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8542424719324ba97b9bc1ace2668a34b438ee0ea82ec531082df5b8aeaf7cd`  
		Last Modified: Fri, 11 Aug 2023 01:40:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a240a3b3d511a34ad163b9f74a40587ceaf70756a0d519a95ed9ec7ef7b3592`  
		Last Modified: Fri, 11 Aug 2023 01:40:57 GMT  
		Size: 58.7 MB (58745951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf57120f71f88f945a273051e6a47703def8f74059b4167b502082ab7ba2ae3`  
		Last Modified: Fri, 11 Aug 2023 01:40:49 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64090e82a0b0bc4e5a3f2f7b31006d5f6d5727d8a9f9a6149c6002255221d99`  
		Last Modified: Fri, 11 Aug 2023 01:40:59 GMT  
		Size: 57.5 MB (57493931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7c7515d542a06b5859d349120753049c822f96f0e5d6425521665dbfebb1bd`  
		Last Modified: Fri, 11 Aug 2023 01:40:49 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:879dc7f99787cec167fd641de9a9956161aaf078d52a7df791108e15b27545d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170320342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfb0ec4d54ad6c6f51e03ce444f792731ac97d79c4575ee74e291b01b6a4bed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 00:40:33 GMT
ADD file:24663feb951dcfae36948e6cbc8697e8bef563d86c15af3daa54a1b830965593 in / 
# Fri, 11 Aug 2023 00:40:34 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:06:30 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 11 Aug 2023 01:06:30 GMT
ENV GOSU_VERSION=1.16
# Fri, 11 Aug 2023 01:06:34 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Aug 2023 01:07:05 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 11 Aug 2023 01:07:06 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 11 Aug 2023 01:07:06 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 11 Aug 2023 01:07:06 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Fri, 11 Aug 2023 01:07:07 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 11 Aug 2023 01:07:39 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 11 Aug 2023 01:07:40 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 11 Aug 2023 01:07:40 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Fri, 11 Aug 2023 01:08:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 11 Aug 2023 01:08:17 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Aug 2023 01:08:17 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 11 Aug 2023 01:08:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:08:17 GMT
EXPOSE 3306 33060
# Fri, 11 Aug 2023 01:08:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd2ec1b01835c3bcf117123886f982435cd8e445790b761779f35779d61faad3`  
		Last Modified: Fri, 11 Aug 2023 00:41:41 GMT  
		Size: 43.6 MB (43625591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2e560d878c2ef4b4d488384e62b7c7105026d91c2e5c78c2adac0bf0131703`  
		Last Modified: Fri, 11 Aug 2023 01:09:47 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8397fbbbc3b5f8cc70741af545a812c0e614ac4ab73d6f2f1f3a85c04ee8516`  
		Last Modified: Fri, 11 Aug 2023 01:09:46 GMT  
		Size: 913.0 KB (913005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff4258297ab21bd32c7e36e0ab6efa98f0750e969045032c41fa33d1a31273c`  
		Last Modified: Fri, 11 Aug 2023 01:09:46 GMT  
		Size: 4.3 MB (4297157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137be606bff345262f5d1a644dde8817fa10fb44346f2e3b8f0027c32c1eeb5a`  
		Last Modified: Fri, 11 Aug 2023 01:09:45 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef6a538fcba799d2016b52a70592ab5234c1c73909911d60b4d612a7e17a9c8`  
		Last Modified: Fri, 11 Aug 2023 01:09:43 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5431fa8c17daf35f38c4fb7e169992ad9c2efb975ebba197767a0e30b479fd3`  
		Last Modified: Fri, 11 Aug 2023 01:09:49 GMT  
		Size: 57.7 MB (57697307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23af94ba633876db53bee4caafbfcbe55a6abb288a8a8924d385fe0eaebdc623`  
		Last Modified: Fri, 11 Aug 2023 01:09:43 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a8250fff2832401391e97d31049ae77dd3e0b2959e4496d8e3c2d624812f7f`  
		Last Modified: Fri, 11 Aug 2023 01:09:53 GMT  
		Size: 63.8 MB (63777712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7e1aea563bf97d862d4b65f1c1be513c0c6f7a8f2d2b10e8fa2a69ce0e0aee`  
		Last Modified: Fri, 11 Aug 2023 01:09:43 GMT  
		Size: 5.4 KB (5395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
