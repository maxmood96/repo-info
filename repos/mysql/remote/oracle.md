## `mysql:oracle`

```console
$ docker pull mysql@sha256:808d02026b5b3edf185e9201db89abdf701fcce11f980ce810adf49c7c7342b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

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

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b156b996b09d1509a78a84dd5a71cf673b5ff60c3ae22c27194e62ac2a7d1266
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139997480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b3b1d5bc990340c2df8472a7a78af238dfb761ace123d9b13ccd4d3dfc4332`
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
# Wed, 23 Feb 2022 21:40:19 GMT
RUN set -eux; 	microdnf install -y 		gzip 		xz 		findutils 	; 	microdnf clean all
# Wed, 23 Feb 2022 21:41:00 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 23 Feb 2022 21:41:01 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 23 Feb 2022 21:41:02 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Wed, 23 Feb 2022 21:41:03 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 23 Feb 2022 21:41:25 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 23 Feb 2022 21:41:26 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 23 Feb 2022 21:41:26 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Wed, 23 Feb 2022 21:41:54 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 23 Feb 2022 21:41:54 GMT
VOLUME [/var/lib/mysql]
# Wed, 23 Feb 2022 21:41:56 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Wed, 23 Feb 2022 21:41:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Feb 2022 21:41:57 GMT
EXPOSE 3306 33060
# Wed, 23 Feb 2022 21:41:58 GMT
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
	-	`sha256:af70585b7a192f4e200798deae1a8cba89afbc03b7097032112e5bc4571f2660`  
		Last Modified: Wed, 23 Feb 2022 21:42:28 GMT  
		Size: 3.3 MB (3258221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a63cf661d5c4d9057b557f1268efa4cf1770596543728a33c76e31c3c38bf7`  
		Last Modified: Wed, 23 Feb 2022 21:42:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20f69348b09e5a78b36c179334aed779d534c322ee73c63149283f619fdf480`  
		Last Modified: Wed, 23 Feb 2022 21:42:25 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165d6f7910557f5385a0a152ca459c4a3a513a0be5091c54bea6c889e1093911`  
		Last Modified: Wed, 23 Feb 2022 21:42:33 GMT  
		Size: 53.4 MB (53382212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496a314c288f953196b7101c88f8b67bf0ae5a07cbc362202f3ec30fddc9ac2f`  
		Last Modified: Wed, 23 Feb 2022 21:42:25 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef4c71a5c7ada2f9db19897deb642356f81aa03dbf6811019ae506d089cad2e`  
		Last Modified: Wed, 23 Feb 2022 21:42:32 GMT  
		Size: 40.5 MB (40471863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb56c1084a5c94c7e6a9ee9e65bb8cbbe3fccf7193667900469ff5fa3756bc77`  
		Last Modified: Wed, 23 Feb 2022 21:42:25 GMT  
		Size: 5.0 KB (4956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
