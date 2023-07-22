## `mysql:latest`

```console
$ docker pull mysql@sha256:ea68e51ffe9b96fef6076f1218af11301aeaf13c6201e0ec9aaef5791d5ddc5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:eb11df7b201aa831c1f1a0c4a07a630b40fcbfacdb7eb6fda8c41277c00c7849
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165693739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6360852d65467a8252391f24826648079893ea03e52d4d8ee5f07fcdeb6d25e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:32 GMT
ADD file:6d43f7bf7c8d8c056e6fcc566ccfa2c1e42be1ef095f94d6780d0ca7d9a02e6e in / 
# Sat, 22 Jul 2023 01:20:32 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:37:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 22 Jul 2023 01:37:28 GMT
ENV GOSU_VERSION=1.16
# Sat, 22 Jul 2023 01:37:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 22 Jul 2023 01:37:58 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 22 Jul 2023 01:37:59 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 22 Jul 2023 01:37:59 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 22 Jul 2023 01:37:59 GMT
ENV MYSQL_VERSION=8.0.33-1.el8
# Sat, 22 Jul 2023 01:38:00 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 22 Jul 2023 01:38:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 22 Jul 2023 01:38:34 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 22 Jul 2023 01:38:34 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1.el8
# Sat, 22 Jul 2023 01:39:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 22 Jul 2023 01:39:13 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Jul 2023 01:39:13 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 22 Jul 2023 01:39:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 22 Jul 2023 01:39:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Jul 2023 01:39:14 GMT
EXPOSE 3306 33060
# Sat, 22 Jul 2023 01:39:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:49bb46380f8cb3491e82d000b27a6eb26b2490291da814ce3363bbf2c8baeb1a`  
		Last Modified: Sat, 22 Jul 2023 01:21:47 GMT  
		Size: 44.9 MB (44915006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab3066bbf8fc576b01df1b0391e5a72a7ff72b1c0c5d09a7bab3db2a51d4744`  
		Last Modified: Sat, 22 Jul 2023 01:39:42 GMT  
		Size: 884.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6eef8c26cf9c633276ffd191110525157aa8811962fce9164a8a79814d497bd`  
		Last Modified: Sat, 22 Jul 2023 01:39:42 GMT  
		Size: 982.8 KB (982822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e908b1dcba2267120afc44b8f24aba3cdf060da1257257196b07f34edd7e959`  
		Last Modified: Sat, 22 Jul 2023 01:39:41 GMT  
		Size: 4.6 MB (4611560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480c3912a2fde8647ba9e97d569e907841498684daa29bd86ba58710923b927d`  
		Last Modified: Sat, 22 Jul 2023 01:39:40 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a648ecb3cf74a58ea563b9fa617f389d20ad307b98d1ee31bb38b529e28241`  
		Last Modified: Sat, 22 Jul 2023 01:39:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6313eed007807d8f70c46daf7c87a6036ad41b272af6ac25aca76e6be2621141`  
		Last Modified: Sat, 22 Jul 2023 01:39:47 GMT  
		Size: 58.6 MB (58604533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668fe2d98404a0684b0c56382e44806d0912dcd0f77c2ee15e03f0d9cd3928d3`  
		Last Modified: Sat, 22 Jul 2023 01:39:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f8a843b813f7f36546e958354a3dec9f327201b4ffb6b7fb3a71dab1afccb8`  
		Last Modified: Sat, 22 Jul 2023 01:39:48 GMT  
		Size: 56.6 MB (56570142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80ab9fc8db51e668986ee4482e07cd85e73e42da14604d05e136a8a35cb20cc`  
		Last Modified: Sat, 22 Jul 2023 01:39:38 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8b6b073273cad4dc094f46f9568f1f9d73a346616fb15ad53901c9a5e678c2`  
		Last Modified: Sat, 22 Jul 2023 01:39:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:62edf9f348c5dcf178e6b600b22318bad18fde151d4766126e5e7b68e16547c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169426885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e6f938c13843277ec4fe0b165319ad8fad9d5638dfc42245e56638314cbae8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 22 Jul 2023 01:03:33 GMT
ADD file:49b1f7f2b2558f78918f26b488622ad08fa607583d0a45f4f116773e2c13cf96 in / 
# Sat, 22 Jul 2023 01:03:34 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:20:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 22 Jul 2023 01:20:07 GMT
ENV GOSU_VERSION=1.16
# Sat, 22 Jul 2023 01:20:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 22 Jul 2023 01:20:36 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 22 Jul 2023 01:20:37 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 22 Jul 2023 01:20:37 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 22 Jul 2023 01:20:37 GMT
ENV MYSQL_VERSION=8.0.33-1.el8
# Sat, 22 Jul 2023 01:20:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 22 Jul 2023 01:21:07 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 22 Jul 2023 01:21:08 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 22 Jul 2023 01:21:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1.el8
# Sat, 22 Jul 2023 01:21:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 22 Jul 2023 01:21:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 22 Jul 2023 01:21:49 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 22 Jul 2023 01:21:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 22 Jul 2023 01:21:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Jul 2023 01:21:50 GMT
EXPOSE 3306 33060
# Sat, 22 Jul 2023 01:21:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1817bc1e6309503caf2242a5c83a4a6e9ebfdfb378d39bc92607690883a98c66`  
		Last Modified: Sat, 22 Jul 2023 01:04:31 GMT  
		Size: 43.6 MB (43623755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740bd54462bcaa8cf5795022cb1daf5bf3b565d088fa1589e0e310225f2420d2`  
		Last Modified: Sat, 22 Jul 2023 01:22:13 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e5ed4e69b309907018566aa973118702a7ad4f73cb732e4fb36fea862eaa26`  
		Last Modified: Sat, 22 Jul 2023 01:22:13 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdf88d7bbb7fa583fd2dfb4b80fa9ae42f0e8f228e3c15bdcf873dfadcaa445`  
		Last Modified: Sat, 22 Jul 2023 01:22:12 GMT  
		Size: 4.3 MB (4294535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a5f85609500a34b3d4c06362e79700456581cfaf64335c617b36a10635033b`  
		Last Modified: Sat, 22 Jul 2023 01:22:11 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b5db4d9b98684ded0da9ecd2569a4882619860e87910d7982064b73a73035c`  
		Last Modified: Sat, 22 Jul 2023 01:22:11 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22418c1834882fc37b934c33040fa267cce75b3437ac6e6c1030ca392d8cddd`  
		Last Modified: Sat, 22 Jul 2023 01:22:15 GMT  
		Size: 57.7 MB (57696245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5876e40ed21700302c8cd3ac3ff37a1e71cf871485a5e5ef7241a5dd6239e5`  
		Last Modified: Sat, 22 Jul 2023 01:22:09 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7221ad5e06ec7f9649161e73793ec55eb8008ffba87b4509e6bf687ea30798eb`  
		Last Modified: Sat, 22 Jul 2023 01:22:17 GMT  
		Size: 62.9 MB (62889678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778fd411739775dd92f0708d1251fec5705a9cb9f503fd143c817c3f43feaf7a`  
		Last Modified: Sat, 22 Jul 2023 01:22:09 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff6298de70dec567edc9b0dc265b794a8ad26b9fd1e77038f50c6d34e2af4a4`  
		Last Modified: Sat, 22 Jul 2023 01:22:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
