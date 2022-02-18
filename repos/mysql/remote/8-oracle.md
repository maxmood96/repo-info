## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:9512f029374784fc2877864394644ce0f4138070235ceb9feed17ebba9c4f2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a1fc8cc7d62da0e5e35e098c8f99e12d6dfe253249c1a8e7392644e5ec9fbf2d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131247835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666b7bdb9b1e4dd70402bf89b44145af4ee43e8a1f8b6823a7348df3d4b5347f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Feb 2022 18:20:31 GMT
ADD file:636d5d8575ec6ddd380a3bbf41530219d37249378b4abd151d94842377cc55d9 in / 
# Fri, 11 Feb 2022 18:20:32 GMT
CMD ["/bin/bash"]
# Fri, 18 Feb 2022 01:20:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 18 Feb 2022 01:20:09 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Feb 2022 01:20:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Feb 2022 01:20:58 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:21:18 GMT
RUN set -eux; microdnf install -y findutils; microdnf clean all
# Fri, 18 Feb 2022 01:21:18 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Feb 2022 01:21:19 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 18 Feb 2022 01:21:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 18 Feb 2022 01:21:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 18 Feb 2022 01:21:59 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 18 Feb 2022 01:21:59 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 18 Feb 2022 01:22:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 18 Feb 2022 01:22:54 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:22:54 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:22:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:22:55 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:22:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:010357f4c091049bd23724817a1881f575ff94d35f4c621b4f87b2876049650b`  
		Last Modified: Fri, 11 Feb 2022 18:21:24 GMT  
		Size: 42.1 MB (42105112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efa408bcdb6fa7a3da670da56c2117a4fc7969a39ab0e37db4bb4e52b1d38ba`  
		Last Modified: Fri, 18 Feb 2022 01:25:39 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290fe0478d05d79d3ad6a2676a72d0ba98072c8e9fad91f0ff027c0db9e7d5e8`  
		Last Modified: Fri, 18 Feb 2022 01:25:38 GMT  
		Size: 928.8 KB (928833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e475a5588ead2e9a8ae74a3294b26b4b5e795e112c6d54779b307f634296a245`  
		Last Modified: Fri, 18 Feb 2022 01:25:37 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367255e5d85a8f2afeeba49f8c0d98c53ce2e201fb284a84ff4984b30c8eeef9`  
		Last Modified: Fri, 18 Feb 2022 01:25:38 GMT  
		Size: 2.8 MB (2771655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0145e7f2d239af74be7d51a6fff3109e8b1616bf8c5b0513becf1aca4b95c7`  
		Last Modified: Fri, 18 Feb 2022 01:25:35 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2c7c0af6e385712bfc837437da2f4005768173e65e7309f05177e737bc58a2`  
		Last Modified: Fri, 18 Feb 2022 01:25:44 GMT  
		Size: 47.2 MB (47214228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e8104a253cabe5deab9f62b2230e88688a12a40259b99e381146ff74be5590`  
		Last Modified: Fri, 18 Feb 2022 01:25:35 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12a051e07b4ace9aad8389609189650858c935b6ad3a35337ca9d33e5e1066c`  
		Last Modified: Fri, 18 Feb 2022 01:25:43 GMT  
		Size: 38.2 MB (38218699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008ae851b8156d7791e78f5dc696d017706f11c2618cb0f7de591fbb6b9a39ea`  
		Last Modified: Fri, 18 Feb 2022 01:25:35 GMT  
		Size: 4.9 KB (4947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:864c06f43933df5c68695ab9d5325c32e0dfd4b20f8625438f973a767d17db6e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139600775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b4461a4e5e28ca90ef33a5c9237a9c139e69387c3eba6a76b3edabe62bd30a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Feb 2022 18:58:36 GMT
ADD file:8d5a0dcc45ab23c7b507e80b63e5752d94837f490600ce95fb8ba8ed2f7baa2d in / 
# Fri, 11 Feb 2022 18:58:37 GMT
CMD ["/bin/bash"]
# Fri, 18 Feb 2022 01:40:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 18 Feb 2022 01:40:09 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Feb 2022 01:40:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Feb 2022 01:40:47 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:41:07 GMT
RUN set -eux; microdnf install -y findutils; microdnf clean all
# Fri, 18 Feb 2022 01:41:08 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Feb 2022 01:41:09 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 18 Feb 2022 01:41:10 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 18 Feb 2022 01:41:36 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 18 Feb 2022 01:41:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 18 Feb 2022 01:41:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 18 Feb 2022 01:42:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 18 Feb 2022 01:42:16 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:42:18 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:42:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:42:19 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:42:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ffdd659a9f05cadeed9c2d5cead839f585163662ca7f847a41fd64bb4e503f0c`  
		Last Modified: Fri, 11 Feb 2022 18:59:38 GMT  
		Size: 42.0 MB (42018804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0160f0527322be235d3dfdb8e677d5ef11bf2da725fc7a4c77f93c96d3d43c`  
		Last Modified: Fri, 18 Feb 2022 01:42:53 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4f9628b4dd4430ea84a7c1a9fc0c2c79a4528061ce123f84f5c31588ebe3aa`  
		Last Modified: Fri, 18 Feb 2022 01:42:51 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b56dfbe8243073b27947bcb79383dcfd2acb24b72d75636e8197132be58fddb`  
		Last Modified: Fri, 18 Feb 2022 01:42:50 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08686ba04fe0e471d22561e7166ad976131e78cc3efba4e9dc64196c094a68cc`  
		Last Modified: Fri, 18 Feb 2022 01:42:51 GMT  
		Size: 2.9 MB (2910502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8daf67bf57567ac1ecfb9c2a8be8156e2a44abc47d4c5f09088fbf581c801c`  
		Last Modified: Fri, 18 Feb 2022 01:42:48 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7337a7ba43b6ce840a216f8ef02776bd500ebb1a55f7b9d48961f5541a6b2c`  
		Last Modified: Fri, 18 Feb 2022 01:42:56 GMT  
		Size: 53.4 MB (53366552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9fa2ec7808380af503327d2db5e2d091441cab236a9ca9cadbed7e4e92be4e9`  
		Last Modified: Fri, 18 Feb 2022 01:42:48 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae724a1d53b4c7ba14b808a7e402e4c9915fb48156274293faa94e066c2f219d`  
		Last Modified: Fri, 18 Feb 2022 01:42:55 GMT  
		Size: 40.4 MB (40438539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f25446c7b13142d0f4941a972a79e61fd69c9f7543bcaed629cdc5a09f57e0`  
		Last Modified: Fri, 18 Feb 2022 01:42:48 GMT  
		Size: 4.9 KB (4948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
