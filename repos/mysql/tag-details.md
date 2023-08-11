<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5-oracle`](#mysql5-oracle)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7-oracle`](#mysql57-oracle)
-	[`mysql:5.7.43`](#mysql5743)
-	[`mysql:5.7.43-oracle`](#mysql5743-oracle)
-	[`mysql:8`](#mysql8)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0.34`](#mysql8034)
-	[`mysql:8.0.34-debian`](#mysql8034-debian)
-	[`mysql:8.0.34-oracle`](#mysql8034-oracle)
-	[`mysql:8.1`](#mysql81)
-	[`mysql:8.1-oracle`](#mysql81-oracle)
-	[`mysql:8.1.0`](#mysql810)
-	[`mysql:8.1.0-oracle`](#mysql810-oracle)
-	[`mysql:innovation`](#mysqlinnovation)
-	[`mysql:innovation-oracle`](#mysqlinnovation-oracle)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:oracle`](#mysqloracle)

## `mysql:5`

```console
$ docker pull mysql@sha256:2c23f254c6b9444ecda9ba36051a9800e8934a2f5828ecc8730531db8142af83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:aaa1374f1e6c24d73e9dfa8f2cdae81c8054e6d1d80c32da883a9050258b6e83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170241704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92034fe9a41f4344b97f3fc88a8796248e2cfa9b934be58379f3dbc150d07d9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Jun 2023 07:21:40 GMT
ADD file:733a37449d62d6e9f530185b9244e06cd8ff0ee896632576ae644437d0a1f852 in / 
# Wed, 14 Jun 2023 07:21:40 GMT
CMD ["/bin/bash"]
# Wed, 14 Jun 2023 09:53:50 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Jun 2023 09:53:50 GMT
ENV GOSU_VERSION=1.16
# Wed, 14 Jun 2023 09:53:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jun 2023 09:54:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 14 Jun 2023 09:54:12 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Jun 2023 09:54:12 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 03 Aug 2023 01:42:12 GMT
ENV MYSQL_VERSION=5.7.43-1.el7
# Thu, 03 Aug 2023 01:42:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 03 Aug 2023 01:42:37 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 03 Aug 2023 01:42:38 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 03 Aug 2023 01:42:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el7
# Thu, 03 Aug 2023 01:43:30 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 03 Aug 2023 01:43:31 GMT
VOLUME [/var/lib/mysql]
# Thu, 03 Aug 2023 01:43:31 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 03 Aug 2023 01:43:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 03 Aug 2023 01:43:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 01:43:32 GMT
EXPOSE 3306 33060
# Thu, 03 Aug 2023 01:43:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:70e9ff4420fbc58483e68c13199a06c24b14013b2548998a7e367f59ca5157bc`  
		Last Modified: Wed, 14 Jun 2023 07:22:30 GMT  
		Size: 50.5 MB (50484765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca4383b183f283dc0ac1a0351f5cb31f75dbd244bee8dc0988af4a50f2c59df`  
		Last Modified: Wed, 14 Jun 2023 09:55:49 GMT  
		Size: 872.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e282e7651b1612ff17f6246e0847dad6996add940329721a4756a1879f15a23`  
		Last Modified: Wed, 14 Jun 2023 09:55:49 GMT  
		Size: 983.7 KB (983711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa0e0ca7078cd2e1abcaa6847bc545576fd23586b4ae3ccc90b31637f27b1f`  
		Last Modified: Wed, 14 Jun 2023 09:55:48 GMT  
		Size: 4.6 MB (4601387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb790cf638212f7a95cd187ed8515ff749c06d616bab23ee7ff4f87969533c7`  
		Last Modified: Wed, 14 Jun 2023 09:55:47 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b277ff292942b9e5a1ca6d9d1d5ead0955f0001a5f8c57b982dffa7bc534c9`  
		Last Modified: Thu, 03 Aug 2023 01:44:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692fe44694296b1cf981626e30c3f3338ed299a41f60367e551c04a61e2c4f40`  
		Last Modified: Thu, 03 Aug 2023 01:44:34 GMT  
		Size: 25.5 MB (25544697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d447d97bbd2395a81a7a5dc435182487474c27a13a32ad65c26abeb698974a`  
		Last Modified: Thu, 03 Aug 2023 01:44:30 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ee594517ba13be21ee4a77972e01a16195f9115eb13e08670ec588f7511869`  
		Last Modified: Thu, 03 Aug 2023 01:44:43 GMT  
		Size: 88.6 MB (88617448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ae52de4d77b43e822cf73c854742ce7ce00f5052dda7fc1328104f5fb47197`  
		Last Modified: Thu, 03 Aug 2023 01:44:30 GMT  
		Size: 5.4 KB (5395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cc05a182b55da231eb06bb7c485714ab9e34087e7211635d4a702e1776ec57`  
		Last Modified: Thu, 03 Aug 2023 01:44:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:2c23f254c6b9444ecda9ba36051a9800e8934a2f5828ecc8730531db8142af83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:aaa1374f1e6c24d73e9dfa8f2cdae81c8054e6d1d80c32da883a9050258b6e83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170241704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92034fe9a41f4344b97f3fc88a8796248e2cfa9b934be58379f3dbc150d07d9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Jun 2023 07:21:40 GMT
ADD file:733a37449d62d6e9f530185b9244e06cd8ff0ee896632576ae644437d0a1f852 in / 
# Wed, 14 Jun 2023 07:21:40 GMT
CMD ["/bin/bash"]
# Wed, 14 Jun 2023 09:53:50 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Jun 2023 09:53:50 GMT
ENV GOSU_VERSION=1.16
# Wed, 14 Jun 2023 09:53:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jun 2023 09:54:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 14 Jun 2023 09:54:12 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Jun 2023 09:54:12 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 03 Aug 2023 01:42:12 GMT
ENV MYSQL_VERSION=5.7.43-1.el7
# Thu, 03 Aug 2023 01:42:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 03 Aug 2023 01:42:37 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 03 Aug 2023 01:42:38 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 03 Aug 2023 01:42:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el7
# Thu, 03 Aug 2023 01:43:30 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 03 Aug 2023 01:43:31 GMT
VOLUME [/var/lib/mysql]
# Thu, 03 Aug 2023 01:43:31 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 03 Aug 2023 01:43:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 03 Aug 2023 01:43:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 01:43:32 GMT
EXPOSE 3306 33060
# Thu, 03 Aug 2023 01:43:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:70e9ff4420fbc58483e68c13199a06c24b14013b2548998a7e367f59ca5157bc`  
		Last Modified: Wed, 14 Jun 2023 07:22:30 GMT  
		Size: 50.5 MB (50484765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca4383b183f283dc0ac1a0351f5cb31f75dbd244bee8dc0988af4a50f2c59df`  
		Last Modified: Wed, 14 Jun 2023 09:55:49 GMT  
		Size: 872.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e282e7651b1612ff17f6246e0847dad6996add940329721a4756a1879f15a23`  
		Last Modified: Wed, 14 Jun 2023 09:55:49 GMT  
		Size: 983.7 KB (983711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa0e0ca7078cd2e1abcaa6847bc545576fd23586b4ae3ccc90b31637f27b1f`  
		Last Modified: Wed, 14 Jun 2023 09:55:48 GMT  
		Size: 4.6 MB (4601387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb790cf638212f7a95cd187ed8515ff749c06d616bab23ee7ff4f87969533c7`  
		Last Modified: Wed, 14 Jun 2023 09:55:47 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b277ff292942b9e5a1ca6d9d1d5ead0955f0001a5f8c57b982dffa7bc534c9`  
		Last Modified: Thu, 03 Aug 2023 01:44:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692fe44694296b1cf981626e30c3f3338ed299a41f60367e551c04a61e2c4f40`  
		Last Modified: Thu, 03 Aug 2023 01:44:34 GMT  
		Size: 25.5 MB (25544697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d447d97bbd2395a81a7a5dc435182487474c27a13a32ad65c26abeb698974a`  
		Last Modified: Thu, 03 Aug 2023 01:44:30 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ee594517ba13be21ee4a77972e01a16195f9115eb13e08670ec588f7511869`  
		Last Modified: Thu, 03 Aug 2023 01:44:43 GMT  
		Size: 88.6 MB (88617448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ae52de4d77b43e822cf73c854742ce7ce00f5052dda7fc1328104f5fb47197`  
		Last Modified: Thu, 03 Aug 2023 01:44:30 GMT  
		Size: 5.4 KB (5395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cc05a182b55da231eb06bb7c485714ab9e34087e7211635d4a702e1776ec57`  
		Last Modified: Thu, 03 Aug 2023 01:44:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:2c23f254c6b9444ecda9ba36051a9800e8934a2f5828ecc8730531db8142af83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:aaa1374f1e6c24d73e9dfa8f2cdae81c8054e6d1d80c32da883a9050258b6e83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170241704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92034fe9a41f4344b97f3fc88a8796248e2cfa9b934be58379f3dbc150d07d9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Jun 2023 07:21:40 GMT
ADD file:733a37449d62d6e9f530185b9244e06cd8ff0ee896632576ae644437d0a1f852 in / 
# Wed, 14 Jun 2023 07:21:40 GMT
CMD ["/bin/bash"]
# Wed, 14 Jun 2023 09:53:50 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Jun 2023 09:53:50 GMT
ENV GOSU_VERSION=1.16
# Wed, 14 Jun 2023 09:53:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jun 2023 09:54:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 14 Jun 2023 09:54:12 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Jun 2023 09:54:12 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 03 Aug 2023 01:42:12 GMT
ENV MYSQL_VERSION=5.7.43-1.el7
# Thu, 03 Aug 2023 01:42:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 03 Aug 2023 01:42:37 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 03 Aug 2023 01:42:38 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 03 Aug 2023 01:42:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el7
# Thu, 03 Aug 2023 01:43:30 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 03 Aug 2023 01:43:31 GMT
VOLUME [/var/lib/mysql]
# Thu, 03 Aug 2023 01:43:31 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 03 Aug 2023 01:43:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 03 Aug 2023 01:43:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 01:43:32 GMT
EXPOSE 3306 33060
# Thu, 03 Aug 2023 01:43:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:70e9ff4420fbc58483e68c13199a06c24b14013b2548998a7e367f59ca5157bc`  
		Last Modified: Wed, 14 Jun 2023 07:22:30 GMT  
		Size: 50.5 MB (50484765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca4383b183f283dc0ac1a0351f5cb31f75dbd244bee8dc0988af4a50f2c59df`  
		Last Modified: Wed, 14 Jun 2023 09:55:49 GMT  
		Size: 872.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e282e7651b1612ff17f6246e0847dad6996add940329721a4756a1879f15a23`  
		Last Modified: Wed, 14 Jun 2023 09:55:49 GMT  
		Size: 983.7 KB (983711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa0e0ca7078cd2e1abcaa6847bc545576fd23586b4ae3ccc90b31637f27b1f`  
		Last Modified: Wed, 14 Jun 2023 09:55:48 GMT  
		Size: 4.6 MB (4601387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb790cf638212f7a95cd187ed8515ff749c06d616bab23ee7ff4f87969533c7`  
		Last Modified: Wed, 14 Jun 2023 09:55:47 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b277ff292942b9e5a1ca6d9d1d5ead0955f0001a5f8c57b982dffa7bc534c9`  
		Last Modified: Thu, 03 Aug 2023 01:44:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692fe44694296b1cf981626e30c3f3338ed299a41f60367e551c04a61e2c4f40`  
		Last Modified: Thu, 03 Aug 2023 01:44:34 GMT  
		Size: 25.5 MB (25544697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d447d97bbd2395a81a7a5dc435182487474c27a13a32ad65c26abeb698974a`  
		Last Modified: Thu, 03 Aug 2023 01:44:30 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ee594517ba13be21ee4a77972e01a16195f9115eb13e08670ec588f7511869`  
		Last Modified: Thu, 03 Aug 2023 01:44:43 GMT  
		Size: 88.6 MB (88617448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ae52de4d77b43e822cf73c854742ce7ce00f5052dda7fc1328104f5fb47197`  
		Last Modified: Thu, 03 Aug 2023 01:44:30 GMT  
		Size: 5.4 KB (5395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cc05a182b55da231eb06bb7c485714ab9e34087e7211635d4a702e1776ec57`  
		Last Modified: Thu, 03 Aug 2023 01:44:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:2c23f254c6b9444ecda9ba36051a9800e8934a2f5828ecc8730531db8142af83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:aaa1374f1e6c24d73e9dfa8f2cdae81c8054e6d1d80c32da883a9050258b6e83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170241704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92034fe9a41f4344b97f3fc88a8796248e2cfa9b934be58379f3dbc150d07d9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Jun 2023 07:21:40 GMT
ADD file:733a37449d62d6e9f530185b9244e06cd8ff0ee896632576ae644437d0a1f852 in / 
# Wed, 14 Jun 2023 07:21:40 GMT
CMD ["/bin/bash"]
# Wed, 14 Jun 2023 09:53:50 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Jun 2023 09:53:50 GMT
ENV GOSU_VERSION=1.16
# Wed, 14 Jun 2023 09:53:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jun 2023 09:54:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 14 Jun 2023 09:54:12 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Jun 2023 09:54:12 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 03 Aug 2023 01:42:12 GMT
ENV MYSQL_VERSION=5.7.43-1.el7
# Thu, 03 Aug 2023 01:42:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 03 Aug 2023 01:42:37 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 03 Aug 2023 01:42:38 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 03 Aug 2023 01:42:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el7
# Thu, 03 Aug 2023 01:43:30 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 03 Aug 2023 01:43:31 GMT
VOLUME [/var/lib/mysql]
# Thu, 03 Aug 2023 01:43:31 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 03 Aug 2023 01:43:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 03 Aug 2023 01:43:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 01:43:32 GMT
EXPOSE 3306 33060
# Thu, 03 Aug 2023 01:43:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:70e9ff4420fbc58483e68c13199a06c24b14013b2548998a7e367f59ca5157bc`  
		Last Modified: Wed, 14 Jun 2023 07:22:30 GMT  
		Size: 50.5 MB (50484765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca4383b183f283dc0ac1a0351f5cb31f75dbd244bee8dc0988af4a50f2c59df`  
		Last Modified: Wed, 14 Jun 2023 09:55:49 GMT  
		Size: 872.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e282e7651b1612ff17f6246e0847dad6996add940329721a4756a1879f15a23`  
		Last Modified: Wed, 14 Jun 2023 09:55:49 GMT  
		Size: 983.7 KB (983711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa0e0ca7078cd2e1abcaa6847bc545576fd23586b4ae3ccc90b31637f27b1f`  
		Last Modified: Wed, 14 Jun 2023 09:55:48 GMT  
		Size: 4.6 MB (4601387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb790cf638212f7a95cd187ed8515ff749c06d616bab23ee7ff4f87969533c7`  
		Last Modified: Wed, 14 Jun 2023 09:55:47 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b277ff292942b9e5a1ca6d9d1d5ead0955f0001a5f8c57b982dffa7bc534c9`  
		Last Modified: Thu, 03 Aug 2023 01:44:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692fe44694296b1cf981626e30c3f3338ed299a41f60367e551c04a61e2c4f40`  
		Last Modified: Thu, 03 Aug 2023 01:44:34 GMT  
		Size: 25.5 MB (25544697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d447d97bbd2395a81a7a5dc435182487474c27a13a32ad65c26abeb698974a`  
		Last Modified: Thu, 03 Aug 2023 01:44:30 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ee594517ba13be21ee4a77972e01a16195f9115eb13e08670ec588f7511869`  
		Last Modified: Thu, 03 Aug 2023 01:44:43 GMT  
		Size: 88.6 MB (88617448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ae52de4d77b43e822cf73c854742ce7ce00f5052dda7fc1328104f5fb47197`  
		Last Modified: Thu, 03 Aug 2023 01:44:30 GMT  
		Size: 5.4 KB (5395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cc05a182b55da231eb06bb7c485714ab9e34087e7211635d4a702e1776ec57`  
		Last Modified: Thu, 03 Aug 2023 01:44:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.43`

```console
$ docker pull mysql@sha256:2c23f254c6b9444ecda9ba36051a9800e8934a2f5828ecc8730531db8142af83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.43` - linux; amd64

```console
$ docker pull mysql@sha256:aaa1374f1e6c24d73e9dfa8f2cdae81c8054e6d1d80c32da883a9050258b6e83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170241704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92034fe9a41f4344b97f3fc88a8796248e2cfa9b934be58379f3dbc150d07d9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Jun 2023 07:21:40 GMT
ADD file:733a37449d62d6e9f530185b9244e06cd8ff0ee896632576ae644437d0a1f852 in / 
# Wed, 14 Jun 2023 07:21:40 GMT
CMD ["/bin/bash"]
# Wed, 14 Jun 2023 09:53:50 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Jun 2023 09:53:50 GMT
ENV GOSU_VERSION=1.16
# Wed, 14 Jun 2023 09:53:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jun 2023 09:54:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 14 Jun 2023 09:54:12 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Jun 2023 09:54:12 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 03 Aug 2023 01:42:12 GMT
ENV MYSQL_VERSION=5.7.43-1.el7
# Thu, 03 Aug 2023 01:42:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 03 Aug 2023 01:42:37 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 03 Aug 2023 01:42:38 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 03 Aug 2023 01:42:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el7
# Thu, 03 Aug 2023 01:43:30 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 03 Aug 2023 01:43:31 GMT
VOLUME [/var/lib/mysql]
# Thu, 03 Aug 2023 01:43:31 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 03 Aug 2023 01:43:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 03 Aug 2023 01:43:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 01:43:32 GMT
EXPOSE 3306 33060
# Thu, 03 Aug 2023 01:43:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:70e9ff4420fbc58483e68c13199a06c24b14013b2548998a7e367f59ca5157bc`  
		Last Modified: Wed, 14 Jun 2023 07:22:30 GMT  
		Size: 50.5 MB (50484765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca4383b183f283dc0ac1a0351f5cb31f75dbd244bee8dc0988af4a50f2c59df`  
		Last Modified: Wed, 14 Jun 2023 09:55:49 GMT  
		Size: 872.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e282e7651b1612ff17f6246e0847dad6996add940329721a4756a1879f15a23`  
		Last Modified: Wed, 14 Jun 2023 09:55:49 GMT  
		Size: 983.7 KB (983711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa0e0ca7078cd2e1abcaa6847bc545576fd23586b4ae3ccc90b31637f27b1f`  
		Last Modified: Wed, 14 Jun 2023 09:55:48 GMT  
		Size: 4.6 MB (4601387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb790cf638212f7a95cd187ed8515ff749c06d616bab23ee7ff4f87969533c7`  
		Last Modified: Wed, 14 Jun 2023 09:55:47 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b277ff292942b9e5a1ca6d9d1d5ead0955f0001a5f8c57b982dffa7bc534c9`  
		Last Modified: Thu, 03 Aug 2023 01:44:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692fe44694296b1cf981626e30c3f3338ed299a41f60367e551c04a61e2c4f40`  
		Last Modified: Thu, 03 Aug 2023 01:44:34 GMT  
		Size: 25.5 MB (25544697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d447d97bbd2395a81a7a5dc435182487474c27a13a32ad65c26abeb698974a`  
		Last Modified: Thu, 03 Aug 2023 01:44:30 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ee594517ba13be21ee4a77972e01a16195f9115eb13e08670ec588f7511869`  
		Last Modified: Thu, 03 Aug 2023 01:44:43 GMT  
		Size: 88.6 MB (88617448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ae52de4d77b43e822cf73c854742ce7ce00f5052dda7fc1328104f5fb47197`  
		Last Modified: Thu, 03 Aug 2023 01:44:30 GMT  
		Size: 5.4 KB (5395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cc05a182b55da231eb06bb7c485714ab9e34087e7211635d4a702e1776ec57`  
		Last Modified: Thu, 03 Aug 2023 01:44:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.43-oracle`

```console
$ docker pull mysql@sha256:2c23f254c6b9444ecda9ba36051a9800e8934a2f5828ecc8730531db8142af83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.43-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:aaa1374f1e6c24d73e9dfa8f2cdae81c8054e6d1d80c32da883a9050258b6e83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170241704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92034fe9a41f4344b97f3fc88a8796248e2cfa9b934be58379f3dbc150d07d9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Jun 2023 07:21:40 GMT
ADD file:733a37449d62d6e9f530185b9244e06cd8ff0ee896632576ae644437d0a1f852 in / 
# Wed, 14 Jun 2023 07:21:40 GMT
CMD ["/bin/bash"]
# Wed, 14 Jun 2023 09:53:50 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 14 Jun 2023 09:53:50 GMT
ENV GOSU_VERSION=1.16
# Wed, 14 Jun 2023 09:53:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jun 2023 09:54:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 14 Jun 2023 09:54:12 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 14 Jun 2023 09:54:12 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 03 Aug 2023 01:42:12 GMT
ENV MYSQL_VERSION=5.7.43-1.el7
# Thu, 03 Aug 2023 01:42:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 03 Aug 2023 01:42:37 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 03 Aug 2023 01:42:38 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 03 Aug 2023 01:42:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el7
# Thu, 03 Aug 2023 01:43:30 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 03 Aug 2023 01:43:31 GMT
VOLUME [/var/lib/mysql]
# Thu, 03 Aug 2023 01:43:31 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 03 Aug 2023 01:43:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 03 Aug 2023 01:43:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 01:43:32 GMT
EXPOSE 3306 33060
# Thu, 03 Aug 2023 01:43:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:70e9ff4420fbc58483e68c13199a06c24b14013b2548998a7e367f59ca5157bc`  
		Last Modified: Wed, 14 Jun 2023 07:22:30 GMT  
		Size: 50.5 MB (50484765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca4383b183f283dc0ac1a0351f5cb31f75dbd244bee8dc0988af4a50f2c59df`  
		Last Modified: Wed, 14 Jun 2023 09:55:49 GMT  
		Size: 872.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e282e7651b1612ff17f6246e0847dad6996add940329721a4756a1879f15a23`  
		Last Modified: Wed, 14 Jun 2023 09:55:49 GMT  
		Size: 983.7 KB (983711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa0e0ca7078cd2e1abcaa6847bc545576fd23586b4ae3ccc90b31637f27b1f`  
		Last Modified: Wed, 14 Jun 2023 09:55:48 GMT  
		Size: 4.6 MB (4601387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb790cf638212f7a95cd187ed8515ff749c06d616bab23ee7ff4f87969533c7`  
		Last Modified: Wed, 14 Jun 2023 09:55:47 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b277ff292942b9e5a1ca6d9d1d5ead0955f0001a5f8c57b982dffa7bc534c9`  
		Last Modified: Thu, 03 Aug 2023 01:44:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692fe44694296b1cf981626e30c3f3338ed299a41f60367e551c04a61e2c4f40`  
		Last Modified: Thu, 03 Aug 2023 01:44:34 GMT  
		Size: 25.5 MB (25544697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d447d97bbd2395a81a7a5dc435182487474c27a13a32ad65c26abeb698974a`  
		Last Modified: Thu, 03 Aug 2023 01:44:30 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ee594517ba13be21ee4a77972e01a16195f9115eb13e08670ec588f7511869`  
		Last Modified: Thu, 03 Aug 2023 01:44:43 GMT  
		Size: 88.6 MB (88617448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ae52de4d77b43e822cf73c854742ce7ce00f5052dda7fc1328104f5fb47197`  
		Last Modified: Thu, 03 Aug 2023 01:44:30 GMT  
		Size: 5.4 KB (5395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cc05a182b55da231eb06bb7c485714ab9e34087e7211635d4a702e1776ec57`  
		Last Modified: Thu, 03 Aug 2023 01:44:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:c0455ac041844b5e65cd08571387fa5b50ab2a6179557fd938298cab13acf0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8` - linux; amd64

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

### `mysql:8` - linux; arm64 variant v8

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

## `mysql:8.0`

```console
$ docker pull mysql@sha256:f0e71f077bb27fe17b1b9551f75d1b35ad4dfe3a33c82412acf19684790f3a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:53ca64a889514c294b85d003de4de35098734a025c776d659fc75ae23a63f5c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166483078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5761fe35fa5313fe4b83b3f2c4100c010db402f4699fefa1e43de733cbd9b6d7`
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
# Fri, 11 Aug 2023 01:39:09 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 11 Aug 2023 01:39:09 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Fri, 11 Aug 2023 01:39:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 11 Aug 2023 01:39:42 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 11 Aug 2023 01:39:43 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 11 Aug 2023 01:39:43 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Fri, 11 Aug 2023 01:40:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 11 Aug 2023 01:40:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Aug 2023 01:40:23 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 11 Aug 2023 01:40:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Aug 2023 01:40:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:40:23 GMT
EXPOSE 3306 33060
# Fri, 11 Aug 2023 01:40:23 GMT
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
	-	`sha256:5110d0b8df84e9ce4f488c02930728c1c50d17bc01e2ab8d9a96492c0633f6c5`  
		Last Modified: Fri, 11 Aug 2023 01:41:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71def905d921b96a1cf06d7ccaace6b040bccaceae7a1b0dec272ae8ea5b7524`  
		Last Modified: Fri, 11 Aug 2023 01:41:35 GMT  
		Size: 58.5 MB (58474828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29c4f8eb3c1bb65109dfb397434114b2c60c7a2b003b8d82dbadbb32e96883a`  
		Last Modified: Fri, 11 Aug 2023 01:41:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769af171cdaaaa8f66f2adc619af9a9eca5ebb074f45195c98cd0d5da410e312`  
		Last Modified: Fri, 11 Aug 2023 01:41:37 GMT  
		Size: 57.5 MB (57502195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0ba6abbff7269578ee63f7361587ef66da064844b37d7dca38036eb885516`  
		Last Modified: Fri, 11 Aug 2023 01:41:28 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7e1ae1140329a0da05dff65373a93e055b90d1fa85a0a4da2cb2e80fa6bd64`  
		Last Modified: Fri, 11 Aug 2023 01:41:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:10ef2cfd87b5e30090513e753d2987b16b74912db9bc69c7dadc767b0f5c9a55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170094742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0560a40914be93510aa0f702d8c7146cbfc802f5c2f431069ea5959351a5bb`
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
# Fri, 11 Aug 2023 01:08:22 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 11 Aug 2023 01:08:23 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Fri, 11 Aug 2023 01:08:23 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 11 Aug 2023 01:08:52 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 11 Aug 2023 01:08:54 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 11 Aug 2023 01:08:54 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Fri, 11 Aug 2023 01:09:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 11 Aug 2023 01:09:29 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Aug 2023 01:09:29 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 11 Aug 2023 01:09:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Aug 2023 01:09:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:09:30 GMT
EXPOSE 3306 33060
# Fri, 11 Aug 2023 01:09:30 GMT
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
	-	`sha256:0b787b806e38de03b2d72e96cfe25a868fb168c573dc0063c8ba51e26439cc31`  
		Last Modified: Fri, 11 Aug 2023 01:10:23 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819b762ef4103ec6a4cf4d3a615f42765f4e015ded181f89ed42f685f91b093e`  
		Last Modified: Fri, 11 Aug 2023 01:10:27 GMT  
		Size: 57.5 MB (57466029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff204301a50a514f15fb25d6c8e5743791c27f9d0c677aff1192f9ce7da6ae2`  
		Last Modified: Fri, 11 Aug 2023 01:10:21 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fa96651db14f007e86d3b4645b4b556e45b468438a7cfd2396798ae8990fa8`  
		Last Modified: Fri, 11 Aug 2023 01:10:29 GMT  
		Size: 63.8 MB (63783276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9cc97cc6171b860cce489a4a286ef4dc2137d6224f44053d94e616215882240`  
		Last Modified: Fri, 11 Aug 2023 01:10:21 GMT  
		Size: 5.4 KB (5395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1675ad04c06d86eea95ff56f9a0d96e8b2d64c9d2dc4a1c7e70863c4b7fddd15`  
		Last Modified: Fri, 11 Aug 2023 01:10:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:49f4fcb0087318aa1c222c7e8ceacbb541cdc457c6307d45e6ee4313f4902e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:26db38c917a651edd01fc69bb56b8e068397a1ca4dfef9739cecc61f3111e6b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179509315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992367f7e447afa8958f0b52f60a32bf01362731ac144922e319c26d5bade895`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 04:00:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 28 Jul 2023 04:00:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 04:00:26 GMT
ENV GOSU_VERSION=1.16
# Fri, 28 Jul 2023 04:00:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 28 Jul 2023 04:00:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 28 Jul 2023 04:00:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 04:00:41 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 28 Jul 2023 04:00:41 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 28 Jul 2023 04:00:41 GMT
ENV MYSQL_VERSION=8.0.34-1debian11
# Fri, 28 Jul 2023 04:00:42 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 28 Jul 2023 04:00:56 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 28 Jul 2023 04:00:57 GMT
VOLUME [/var/lib/mysql]
# Fri, 28 Jul 2023 04:00:57 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 28 Jul 2023 04:00:57 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 28 Jul 2023 04:00:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 04:00:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 04:00:58 GMT
EXPOSE 3306 33060
# Fri, 28 Jul 2023 04:00:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b034716887fd3351d90a2dadd53aa4984cd39f8397149d2fde665822cbdfb285`  
		Last Modified: Fri, 28 Jul 2023 04:02:17 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882448c7d618dde8cedcebbf5843a1abdc3f8840035073f44ac0be1c75a88222`  
		Last Modified: Fri, 28 Jul 2023 04:02:17 GMT  
		Size: 4.4 MB (4415051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14ac4640b87d832c2419b4c3968a4718ab31ef1cec549b8415be42ebb792611`  
		Last Modified: Fri, 28 Jul 2023 04:02:15 GMT  
		Size: 1.5 MB (1471510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2978613e401218d6fd28693e6d47c7110dd5d4bd2f750ee1d37fc4f8428fd9`  
		Last Modified: Fri, 28 Jul 2023 04:02:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33d24cb8c756b450de2635eb9fba6c9647da56ab1945e6c2b4e3926725ac3de`  
		Last Modified: Fri, 28 Jul 2023 04:02:17 GMT  
		Size: 12.7 MB (12662071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fa14fc88fc63d64bb0d429a08bdaaae8f80694ad373b7c85e566d535fc88e5`  
		Last Modified: Fri, 28 Jul 2023 04:02:14 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42deb22ec16d8d602e97596083fd18c35167815a0af24879dfd937d052bf72be`  
		Last Modified: Fri, 28 Jul 2023 04:02:13 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d31d600a65d21a8dcd2963f131d5a412a1b257f8b7ede1896a939929cc24e6`  
		Last Modified: Fri, 28 Jul 2023 04:02:30 GMT  
		Size: 129.5 MB (129532040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b9f5aba00d7eab19f55c9f54637f274c1275e6a8f33508b24dc332c4334e07`  
		Last Modified: Fri, 28 Jul 2023 04:02:13 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98222a66de151bb3ad1b199d0398af90a4552e2515f3bd52663e7df2c56b72a7`  
		Last Modified: Fri, 28 Jul 2023 04:02:12 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff8f0c3c67bc36e46203bc2fb68ed8023121c5f4b607ddd8d8ff48c01384452`  
		Last Modified: Fri, 28 Jul 2023 04:02:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:f0e71f077bb27fe17b1b9551f75d1b35ad4dfe3a33c82412acf19684790f3a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:53ca64a889514c294b85d003de4de35098734a025c776d659fc75ae23a63f5c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166483078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5761fe35fa5313fe4b83b3f2c4100c010db402f4699fefa1e43de733cbd9b6d7`
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
# Fri, 11 Aug 2023 01:39:09 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 11 Aug 2023 01:39:09 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Fri, 11 Aug 2023 01:39:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 11 Aug 2023 01:39:42 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 11 Aug 2023 01:39:43 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 11 Aug 2023 01:39:43 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Fri, 11 Aug 2023 01:40:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 11 Aug 2023 01:40:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Aug 2023 01:40:23 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 11 Aug 2023 01:40:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Aug 2023 01:40:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:40:23 GMT
EXPOSE 3306 33060
# Fri, 11 Aug 2023 01:40:23 GMT
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
	-	`sha256:5110d0b8df84e9ce4f488c02930728c1c50d17bc01e2ab8d9a96492c0633f6c5`  
		Last Modified: Fri, 11 Aug 2023 01:41:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71def905d921b96a1cf06d7ccaace6b040bccaceae7a1b0dec272ae8ea5b7524`  
		Last Modified: Fri, 11 Aug 2023 01:41:35 GMT  
		Size: 58.5 MB (58474828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29c4f8eb3c1bb65109dfb397434114b2c60c7a2b003b8d82dbadbb32e96883a`  
		Last Modified: Fri, 11 Aug 2023 01:41:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769af171cdaaaa8f66f2adc619af9a9eca5ebb074f45195c98cd0d5da410e312`  
		Last Modified: Fri, 11 Aug 2023 01:41:37 GMT  
		Size: 57.5 MB (57502195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0ba6abbff7269578ee63f7361587ef66da064844b37d7dca38036eb885516`  
		Last Modified: Fri, 11 Aug 2023 01:41:28 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7e1ae1140329a0da05dff65373a93e055b90d1fa85a0a4da2cb2e80fa6bd64`  
		Last Modified: Fri, 11 Aug 2023 01:41:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:10ef2cfd87b5e30090513e753d2987b16b74912db9bc69c7dadc767b0f5c9a55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170094742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0560a40914be93510aa0f702d8c7146cbfc802f5c2f431069ea5959351a5bb`
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
# Fri, 11 Aug 2023 01:08:22 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 11 Aug 2023 01:08:23 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Fri, 11 Aug 2023 01:08:23 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 11 Aug 2023 01:08:52 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 11 Aug 2023 01:08:54 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 11 Aug 2023 01:08:54 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Fri, 11 Aug 2023 01:09:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 11 Aug 2023 01:09:29 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Aug 2023 01:09:29 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 11 Aug 2023 01:09:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Aug 2023 01:09:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:09:30 GMT
EXPOSE 3306 33060
# Fri, 11 Aug 2023 01:09:30 GMT
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
	-	`sha256:0b787b806e38de03b2d72e96cfe25a868fb168c573dc0063c8ba51e26439cc31`  
		Last Modified: Fri, 11 Aug 2023 01:10:23 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819b762ef4103ec6a4cf4d3a615f42765f4e015ded181f89ed42f685f91b093e`  
		Last Modified: Fri, 11 Aug 2023 01:10:27 GMT  
		Size: 57.5 MB (57466029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff204301a50a514f15fb25d6c8e5743791c27f9d0c677aff1192f9ce7da6ae2`  
		Last Modified: Fri, 11 Aug 2023 01:10:21 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fa96651db14f007e86d3b4645b4b556e45b468438a7cfd2396798ae8990fa8`  
		Last Modified: Fri, 11 Aug 2023 01:10:29 GMT  
		Size: 63.8 MB (63783276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9cc97cc6171b860cce489a4a286ef4dc2137d6224f44053d94e616215882240`  
		Last Modified: Fri, 11 Aug 2023 01:10:21 GMT  
		Size: 5.4 KB (5395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1675ad04c06d86eea95ff56f9a0d96e8b2d64c9d2dc4a1c7e70863c4b7fddd15`  
		Last Modified: Fri, 11 Aug 2023 01:10:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.34`

```console
$ docker pull mysql@sha256:f0e71f077bb27fe17b1b9551f75d1b35ad4dfe3a33c82412acf19684790f3a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.34` - linux; amd64

```console
$ docker pull mysql@sha256:53ca64a889514c294b85d003de4de35098734a025c776d659fc75ae23a63f5c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166483078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5761fe35fa5313fe4b83b3f2c4100c010db402f4699fefa1e43de733cbd9b6d7`
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
# Fri, 11 Aug 2023 01:39:09 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 11 Aug 2023 01:39:09 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Fri, 11 Aug 2023 01:39:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 11 Aug 2023 01:39:42 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 11 Aug 2023 01:39:43 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 11 Aug 2023 01:39:43 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Fri, 11 Aug 2023 01:40:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 11 Aug 2023 01:40:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Aug 2023 01:40:23 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 11 Aug 2023 01:40:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Aug 2023 01:40:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:40:23 GMT
EXPOSE 3306 33060
# Fri, 11 Aug 2023 01:40:23 GMT
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
	-	`sha256:5110d0b8df84e9ce4f488c02930728c1c50d17bc01e2ab8d9a96492c0633f6c5`  
		Last Modified: Fri, 11 Aug 2023 01:41:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71def905d921b96a1cf06d7ccaace6b040bccaceae7a1b0dec272ae8ea5b7524`  
		Last Modified: Fri, 11 Aug 2023 01:41:35 GMT  
		Size: 58.5 MB (58474828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29c4f8eb3c1bb65109dfb397434114b2c60c7a2b003b8d82dbadbb32e96883a`  
		Last Modified: Fri, 11 Aug 2023 01:41:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769af171cdaaaa8f66f2adc619af9a9eca5ebb074f45195c98cd0d5da410e312`  
		Last Modified: Fri, 11 Aug 2023 01:41:37 GMT  
		Size: 57.5 MB (57502195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0ba6abbff7269578ee63f7361587ef66da064844b37d7dca38036eb885516`  
		Last Modified: Fri, 11 Aug 2023 01:41:28 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7e1ae1140329a0da05dff65373a93e055b90d1fa85a0a4da2cb2e80fa6bd64`  
		Last Modified: Fri, 11 Aug 2023 01:41:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.34` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:10ef2cfd87b5e30090513e753d2987b16b74912db9bc69c7dadc767b0f5c9a55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170094742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0560a40914be93510aa0f702d8c7146cbfc802f5c2f431069ea5959351a5bb`
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
# Fri, 11 Aug 2023 01:08:22 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 11 Aug 2023 01:08:23 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Fri, 11 Aug 2023 01:08:23 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 11 Aug 2023 01:08:52 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 11 Aug 2023 01:08:54 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 11 Aug 2023 01:08:54 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Fri, 11 Aug 2023 01:09:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 11 Aug 2023 01:09:29 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Aug 2023 01:09:29 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 11 Aug 2023 01:09:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Aug 2023 01:09:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:09:30 GMT
EXPOSE 3306 33060
# Fri, 11 Aug 2023 01:09:30 GMT
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
	-	`sha256:0b787b806e38de03b2d72e96cfe25a868fb168c573dc0063c8ba51e26439cc31`  
		Last Modified: Fri, 11 Aug 2023 01:10:23 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819b762ef4103ec6a4cf4d3a615f42765f4e015ded181f89ed42f685f91b093e`  
		Last Modified: Fri, 11 Aug 2023 01:10:27 GMT  
		Size: 57.5 MB (57466029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff204301a50a514f15fb25d6c8e5743791c27f9d0c677aff1192f9ce7da6ae2`  
		Last Modified: Fri, 11 Aug 2023 01:10:21 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fa96651db14f007e86d3b4645b4b556e45b468438a7cfd2396798ae8990fa8`  
		Last Modified: Fri, 11 Aug 2023 01:10:29 GMT  
		Size: 63.8 MB (63783276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9cc97cc6171b860cce489a4a286ef4dc2137d6224f44053d94e616215882240`  
		Last Modified: Fri, 11 Aug 2023 01:10:21 GMT  
		Size: 5.4 KB (5395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1675ad04c06d86eea95ff56f9a0d96e8b2d64c9d2dc4a1c7e70863c4b7fddd15`  
		Last Modified: Fri, 11 Aug 2023 01:10:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.34-debian`

```console
$ docker pull mysql@sha256:49f4fcb0087318aa1c222c7e8ceacbb541cdc457c6307d45e6ee4313f4902e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.34-debian` - linux; amd64

```console
$ docker pull mysql@sha256:26db38c917a651edd01fc69bb56b8e068397a1ca4dfef9739cecc61f3111e6b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179509315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992367f7e447afa8958f0b52f60a32bf01362731ac144922e319c26d5bade895`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 04:00:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 28 Jul 2023 04:00:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 04:00:26 GMT
ENV GOSU_VERSION=1.16
# Fri, 28 Jul 2023 04:00:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 28 Jul 2023 04:00:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 28 Jul 2023 04:00:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 04:00:41 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 28 Jul 2023 04:00:41 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 28 Jul 2023 04:00:41 GMT
ENV MYSQL_VERSION=8.0.34-1debian11
# Fri, 28 Jul 2023 04:00:42 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 28 Jul 2023 04:00:56 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 28 Jul 2023 04:00:57 GMT
VOLUME [/var/lib/mysql]
# Fri, 28 Jul 2023 04:00:57 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 28 Jul 2023 04:00:57 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 28 Jul 2023 04:00:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 28 Jul 2023 04:00:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 04:00:58 GMT
EXPOSE 3306 33060
# Fri, 28 Jul 2023 04:00:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b034716887fd3351d90a2dadd53aa4984cd39f8397149d2fde665822cbdfb285`  
		Last Modified: Fri, 28 Jul 2023 04:02:17 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882448c7d618dde8cedcebbf5843a1abdc3f8840035073f44ac0be1c75a88222`  
		Last Modified: Fri, 28 Jul 2023 04:02:17 GMT  
		Size: 4.4 MB (4415051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14ac4640b87d832c2419b4c3968a4718ab31ef1cec549b8415be42ebb792611`  
		Last Modified: Fri, 28 Jul 2023 04:02:15 GMT  
		Size: 1.5 MB (1471510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2978613e401218d6fd28693e6d47c7110dd5d4bd2f750ee1d37fc4f8428fd9`  
		Last Modified: Fri, 28 Jul 2023 04:02:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33d24cb8c756b450de2635eb9fba6c9647da56ab1945e6c2b4e3926725ac3de`  
		Last Modified: Fri, 28 Jul 2023 04:02:17 GMT  
		Size: 12.7 MB (12662071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fa14fc88fc63d64bb0d429a08bdaaae8f80694ad373b7c85e566d535fc88e5`  
		Last Modified: Fri, 28 Jul 2023 04:02:14 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42deb22ec16d8d602e97596083fd18c35167815a0af24879dfd937d052bf72be`  
		Last Modified: Fri, 28 Jul 2023 04:02:13 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d31d600a65d21a8dcd2963f131d5a412a1b257f8b7ede1896a939929cc24e6`  
		Last Modified: Fri, 28 Jul 2023 04:02:30 GMT  
		Size: 129.5 MB (129532040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b9f5aba00d7eab19f55c9f54637f274c1275e6a8f33508b24dc332c4334e07`  
		Last Modified: Fri, 28 Jul 2023 04:02:13 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98222a66de151bb3ad1b199d0398af90a4552e2515f3bd52663e7df2c56b72a7`  
		Last Modified: Fri, 28 Jul 2023 04:02:12 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff8f0c3c67bc36e46203bc2fb68ed8023121c5f4b607ddd8d8ff48c01384452`  
		Last Modified: Fri, 28 Jul 2023 04:02:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.34-oracle`

```console
$ docker pull mysql@sha256:f0e71f077bb27fe17b1b9551f75d1b35ad4dfe3a33c82412acf19684790f3a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.34-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:53ca64a889514c294b85d003de4de35098734a025c776d659fc75ae23a63f5c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166483078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5761fe35fa5313fe4b83b3f2c4100c010db402f4699fefa1e43de733cbd9b6d7`
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
# Fri, 11 Aug 2023 01:39:09 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 11 Aug 2023 01:39:09 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Fri, 11 Aug 2023 01:39:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 11 Aug 2023 01:39:42 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 11 Aug 2023 01:39:43 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 11 Aug 2023 01:39:43 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Fri, 11 Aug 2023 01:40:21 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 11 Aug 2023 01:40:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Aug 2023 01:40:23 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 11 Aug 2023 01:40:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Aug 2023 01:40:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:40:23 GMT
EXPOSE 3306 33060
# Fri, 11 Aug 2023 01:40:23 GMT
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
	-	`sha256:5110d0b8df84e9ce4f488c02930728c1c50d17bc01e2ab8d9a96492c0633f6c5`  
		Last Modified: Fri, 11 Aug 2023 01:41:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71def905d921b96a1cf06d7ccaace6b040bccaceae7a1b0dec272ae8ea5b7524`  
		Last Modified: Fri, 11 Aug 2023 01:41:35 GMT  
		Size: 58.5 MB (58474828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29c4f8eb3c1bb65109dfb397434114b2c60c7a2b003b8d82dbadbb32e96883a`  
		Last Modified: Fri, 11 Aug 2023 01:41:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769af171cdaaaa8f66f2adc619af9a9eca5ebb074f45195c98cd0d5da410e312`  
		Last Modified: Fri, 11 Aug 2023 01:41:37 GMT  
		Size: 57.5 MB (57502195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0ba6abbff7269578ee63f7361587ef66da064844b37d7dca38036eb885516`  
		Last Modified: Fri, 11 Aug 2023 01:41:28 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7e1ae1140329a0da05dff65373a93e055b90d1fa85a0a4da2cb2e80fa6bd64`  
		Last Modified: Fri, 11 Aug 2023 01:41:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.34-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:10ef2cfd87b5e30090513e753d2987b16b74912db9bc69c7dadc767b0f5c9a55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170094742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0560a40914be93510aa0f702d8c7146cbfc802f5c2f431069ea5959351a5bb`
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
# Fri, 11 Aug 2023 01:08:22 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 11 Aug 2023 01:08:23 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Fri, 11 Aug 2023 01:08:23 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 11 Aug 2023 01:08:52 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 11 Aug 2023 01:08:54 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 11 Aug 2023 01:08:54 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Fri, 11 Aug 2023 01:09:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 11 Aug 2023 01:09:29 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Aug 2023 01:09:29 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 11 Aug 2023 01:09:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Aug 2023 01:09:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:09:30 GMT
EXPOSE 3306 33060
# Fri, 11 Aug 2023 01:09:30 GMT
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
	-	`sha256:0b787b806e38de03b2d72e96cfe25a868fb168c573dc0063c8ba51e26439cc31`  
		Last Modified: Fri, 11 Aug 2023 01:10:23 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819b762ef4103ec6a4cf4d3a615f42765f4e015ded181f89ed42f685f91b093e`  
		Last Modified: Fri, 11 Aug 2023 01:10:27 GMT  
		Size: 57.5 MB (57466029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff204301a50a514f15fb25d6c8e5743791c27f9d0c677aff1192f9ce7da6ae2`  
		Last Modified: Fri, 11 Aug 2023 01:10:21 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fa96651db14f007e86d3b4645b4b556e45b468438a7cfd2396798ae8990fa8`  
		Last Modified: Fri, 11 Aug 2023 01:10:29 GMT  
		Size: 63.8 MB (63783276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9cc97cc6171b860cce489a4a286ef4dc2137d6224f44053d94e616215882240`  
		Last Modified: Fri, 11 Aug 2023 01:10:21 GMT  
		Size: 5.4 KB (5395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1675ad04c06d86eea95ff56f9a0d96e8b2d64c9d2dc4a1c7e70863c4b7fddd15`  
		Last Modified: Fri, 11 Aug 2023 01:10:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.1`

```console
$ docker pull mysql@sha256:c0455ac041844b5e65cd08571387fa5b50ab2a6179557fd938298cab13acf0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.1` - linux; amd64

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

### `mysql:8.1` - linux; arm64 variant v8

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

## `mysql:8.1-oracle`

```console
$ docker pull mysql@sha256:c0455ac041844b5e65cd08571387fa5b50ab2a6179557fd938298cab13acf0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.1-oracle` - linux; amd64

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

### `mysql:8.1-oracle` - linux; arm64 variant v8

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

## `mysql:8.1.0`

```console
$ docker pull mysql@sha256:c0455ac041844b5e65cd08571387fa5b50ab2a6179557fd938298cab13acf0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.1.0` - linux; amd64

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

### `mysql:8.1.0` - linux; arm64 variant v8

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

## `mysql:8.1.0-oracle`

```console
$ docker pull mysql@sha256:c0455ac041844b5e65cd08571387fa5b50ab2a6179557fd938298cab13acf0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.1.0-oracle` - linux; amd64

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

### `mysql:8.1.0-oracle` - linux; arm64 variant v8

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

## `mysql:innovation`

```console
$ docker pull mysql@sha256:c0455ac041844b5e65cd08571387fa5b50ab2a6179557fd938298cab13acf0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:innovation` - linux; amd64

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

### `mysql:innovation` - linux; arm64 variant v8

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

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:c0455ac041844b5e65cd08571387fa5b50ab2a6179557fd938298cab13acf0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:innovation-oracle` - linux; amd64

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

### `mysql:innovation-oracle` - linux; arm64 variant v8

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

## `mysql:latest`

```console
$ docker pull mysql@sha256:c0455ac041844b5e65cd08571387fa5b50ab2a6179557fd938298cab13acf0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:latest` - linux; amd64

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

### `mysql:latest` - linux; arm64 variant v8

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

## `mysql:oracle`

```console
$ docker pull mysql@sha256:c0455ac041844b5e65cd08571387fa5b50ab2a6179557fd938298cab13acf0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

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

### `mysql:oracle` - linux; arm64 variant v8

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
