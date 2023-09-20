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
$ docker pull mysql@sha256:85ab57eb4a48ada2a341dcf7d96733ce2f370fffb8e8e216991b106e50fa6434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:ecf2a95e14266b1d3fb72968b84ba2f32f1a0e9288d4ed2dc72f2012d3bb8587
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da80fe49fcfad1ac311a2e34c42730c943706c2008083f5e4feeb6d77cdbc1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:40:54 GMT
ADD file:1632d5b9918ff63c9e38191b65ad8e6f1e0eb5c2ef274cce4f50534bba2f7493 in / 
# Sat, 16 Sep 2023 02:40:55 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:13:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:13:04 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:13:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:13:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:13:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:13:36 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 16 Sep 2023 03:13:36 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Sat, 16 Sep 2023 03:13:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:14:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:14:54 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:14:55 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:14:55 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:14:55 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:14:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bc377bce3181aab0e51009b13b6a6890e49c64e7bf6ab7fa12dce86a95c88bd4`  
		Last Modified: Sat, 16 Sep 2023 02:42:29 GMT  
		Size: 44.9 MB (44911063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bab949ab517e3be7ce2e1a260efa70a0b8d086b9a8eb94421e263202aebec7`  
		Last Modified: Sat, 16 Sep 2023 03:17:00 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73682200afb7af28b17b7f0b43ab59e0f6dee7de613a75eea5cbb9bd6051f034`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c32d486523845672c2afde18b2048f166858bed8cbd70df044ee6c2403cacd`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 4.6 MB (4606599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54341582c90c5e4c851a5a19299024e784fc074bc89a250e5bb0c54a1e29dbf8`  
		Last Modified: Sat, 16 Sep 2023 03:16:57 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7490cd8f4d9b6814db10f8ac442f731ec4d04f9ec8a8fd3d1c995c2638700a56`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de967683cb3b284286c63a20fe7a0271ec7439c3ee46d39fc4746908a530fa65`  
		Last Modified: Sat, 16 Sep 2023 03:17:04 GMT  
		Size: 58.8 MB (58762808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39564f901a1edbe29de6869cc926733691e90c7fdee348fba590947754e91baa`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95e6efa291a87c772fa329e54fb4d0a8bba432ee01512fd7cf2b8732607eca3`  
		Last Modified: Sat, 16 Sep 2023 03:17:06 GMT  
		Size: 57.5 MB (57507195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8366d05afd7cc6b88fe7ccabf752a1ba4cfb5e73b6f228ef23190553e16438e5`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85e2dc34bdafb7a98b44902ac50c752adb70fd3589d0341955d65fa15faf61f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170318488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcbfd21648790d5c427728c74b254dd99eefd04cb0f3307199eb133de21cffc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:21:42 GMT
ADD file:c1b7bfaf11bf64b9c1b24345749a98cbd3f593162ea942e12b15c6f2110c1e94 in / 
# Sat, 16 Sep 2023 02:21:43 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:05:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:05:11 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:05:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:05:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:05:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:05:44 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 16 Sep 2023 03:05:44 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Sat, 16 Sep 2023 03:05:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:06:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:06:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:06:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:06:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:06:57 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:06:58 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:06:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:06:58 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:06:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d095360c6402749d9f7a3d7b7cdd417f27e41419f8027f4704ab00d0dd8ae7ee`  
		Last Modified: Sat, 16 Sep 2023 02:22:42 GMT  
		Size: 43.6 MB (43630964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0858301c0b29f5044b8124bf239eb818ea26beb8a761063839d8d22edcd1388`  
		Last Modified: Sat, 16 Sep 2023 03:08:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f442c155184089167742040807da8601460238f51bbfd6744e0c7a27f8f4bf2d`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 913.0 KB (912997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d70ba84e123b2ee603b84a3c4c0b9b247094ea07bb514eda5e8fc996d2bc89`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 4.3 MB (4302778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344316b4b482ae2b698900c186f8d5e55ff4060775edd5acac581058b02af8db`  
		Last Modified: Sat, 16 Sep 2023 03:08:38 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646e59d2b5913ed94c45bb54967c95965ac1c552213bf3fdc044926933196025`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d710d330bbe275dc6d4ab63a0fc43d0937e3d00522e6488a52e882e0be0eca4`  
		Last Modified: Sat, 16 Sep 2023 03:08:42 GMT  
		Size: 57.7 MB (57695529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fa9584c724548ebf9aeac0d3b92cc7b80ae8487599959613f87a44707ed765`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c19adc05d53aee28a6f99e5a4ae5a62539a856353547c8cb25b839e724ef94`  
		Last Modified: Sat, 16 Sep 2023 03:08:44 GMT  
		Size: 63.8 MB (63766659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6b1dad8c4a79d306583a0d88379d0f3cff5dd07bad3d1a97520365a26e6e8f`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:85ab57eb4a48ada2a341dcf7d96733ce2f370fffb8e8e216991b106e50fa6434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:ecf2a95e14266b1d3fb72968b84ba2f32f1a0e9288d4ed2dc72f2012d3bb8587
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da80fe49fcfad1ac311a2e34c42730c943706c2008083f5e4feeb6d77cdbc1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:40:54 GMT
ADD file:1632d5b9918ff63c9e38191b65ad8e6f1e0eb5c2ef274cce4f50534bba2f7493 in / 
# Sat, 16 Sep 2023 02:40:55 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:13:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:13:04 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:13:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:13:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:13:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:13:36 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 16 Sep 2023 03:13:36 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Sat, 16 Sep 2023 03:13:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:14:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:14:54 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:14:55 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:14:55 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:14:55 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:14:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bc377bce3181aab0e51009b13b6a6890e49c64e7bf6ab7fa12dce86a95c88bd4`  
		Last Modified: Sat, 16 Sep 2023 02:42:29 GMT  
		Size: 44.9 MB (44911063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bab949ab517e3be7ce2e1a260efa70a0b8d086b9a8eb94421e263202aebec7`  
		Last Modified: Sat, 16 Sep 2023 03:17:00 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73682200afb7af28b17b7f0b43ab59e0f6dee7de613a75eea5cbb9bd6051f034`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c32d486523845672c2afde18b2048f166858bed8cbd70df044ee6c2403cacd`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 4.6 MB (4606599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54341582c90c5e4c851a5a19299024e784fc074bc89a250e5bb0c54a1e29dbf8`  
		Last Modified: Sat, 16 Sep 2023 03:16:57 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7490cd8f4d9b6814db10f8ac442f731ec4d04f9ec8a8fd3d1c995c2638700a56`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de967683cb3b284286c63a20fe7a0271ec7439c3ee46d39fc4746908a530fa65`  
		Last Modified: Sat, 16 Sep 2023 03:17:04 GMT  
		Size: 58.8 MB (58762808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39564f901a1edbe29de6869cc926733691e90c7fdee348fba590947754e91baa`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95e6efa291a87c772fa329e54fb4d0a8bba432ee01512fd7cf2b8732607eca3`  
		Last Modified: Sat, 16 Sep 2023 03:17:06 GMT  
		Size: 57.5 MB (57507195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8366d05afd7cc6b88fe7ccabf752a1ba4cfb5e73b6f228ef23190553e16438e5`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85e2dc34bdafb7a98b44902ac50c752adb70fd3589d0341955d65fa15faf61f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170318488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcbfd21648790d5c427728c74b254dd99eefd04cb0f3307199eb133de21cffc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:21:42 GMT
ADD file:c1b7bfaf11bf64b9c1b24345749a98cbd3f593162ea942e12b15c6f2110c1e94 in / 
# Sat, 16 Sep 2023 02:21:43 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:05:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:05:11 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:05:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:05:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:05:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:05:44 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 16 Sep 2023 03:05:44 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Sat, 16 Sep 2023 03:05:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:06:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:06:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:06:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:06:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:06:57 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:06:58 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:06:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:06:58 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:06:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d095360c6402749d9f7a3d7b7cdd417f27e41419f8027f4704ab00d0dd8ae7ee`  
		Last Modified: Sat, 16 Sep 2023 02:22:42 GMT  
		Size: 43.6 MB (43630964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0858301c0b29f5044b8124bf239eb818ea26beb8a761063839d8d22edcd1388`  
		Last Modified: Sat, 16 Sep 2023 03:08:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f442c155184089167742040807da8601460238f51bbfd6744e0c7a27f8f4bf2d`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 913.0 KB (912997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d70ba84e123b2ee603b84a3c4c0b9b247094ea07bb514eda5e8fc996d2bc89`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 4.3 MB (4302778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344316b4b482ae2b698900c186f8d5e55ff4060775edd5acac581058b02af8db`  
		Last Modified: Sat, 16 Sep 2023 03:08:38 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646e59d2b5913ed94c45bb54967c95965ac1c552213bf3fdc044926933196025`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d710d330bbe275dc6d4ab63a0fc43d0937e3d00522e6488a52e882e0be0eca4`  
		Last Modified: Sat, 16 Sep 2023 03:08:42 GMT  
		Size: 57.7 MB (57695529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fa9584c724548ebf9aeac0d3b92cc7b80ae8487599959613f87a44707ed765`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c19adc05d53aee28a6f99e5a4ae5a62539a856353547c8cb25b839e724ef94`  
		Last Modified: Sat, 16 Sep 2023 03:08:44 GMT  
		Size: 63.8 MB (63766659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6b1dad8c4a79d306583a0d88379d0f3cff5dd07bad3d1a97520365a26e6e8f`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:09cf783c365fcd00ecda11e10239775373c8040562aaf59f74d28ab17488af12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:e6fbd1b655b53b67508a21b446d554c8b36600449673ef9ee09193f63372ab8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166492942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca55c632ed6d006d4b672c08bf342d0baf8a8c6721a159607ef69c4cacc3a95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:40:54 GMT
ADD file:1632d5b9918ff63c9e38191b65ad8e6f1e0eb5c2ef274cce4f50534bba2f7493 in / 
# Sat, 16 Sep 2023 02:40:55 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:13:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:13:04 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:13:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:13:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:13:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 16 Sep 2023 03:15:12 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:15:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:15:48 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:15:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:15:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:16:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:16:31 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:16:31 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:16:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 16 Sep 2023 03:16:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:16:31 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:16:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bc377bce3181aab0e51009b13b6a6890e49c64e7bf6ab7fa12dce86a95c88bd4`  
		Last Modified: Sat, 16 Sep 2023 02:42:29 GMT  
		Size: 44.9 MB (44911063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bab949ab517e3be7ce2e1a260efa70a0b8d086b9a8eb94421e263202aebec7`  
		Last Modified: Sat, 16 Sep 2023 03:17:00 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73682200afb7af28b17b7f0b43ab59e0f6dee7de613a75eea5cbb9bd6051f034`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c32d486523845672c2afde18b2048f166858bed8cbd70df044ee6c2403cacd`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 4.6 MB (4606599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54341582c90c5e4c851a5a19299024e784fc074bc89a250e5bb0c54a1e29dbf8`  
		Last Modified: Sat, 16 Sep 2023 03:16:57 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12f032a8b52f337ef476dffbdc5929c946638d80ce5a6532206c83b962365d8`  
		Last Modified: Sat, 16 Sep 2023 03:17:38 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ec0aa1a86a21f28a71a1802009e52c58b5c88792d6ad73040d1c875e186299`  
		Last Modified: Sat, 16 Sep 2023 03:17:45 GMT  
		Size: 58.5 MB (58489547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11420f2dc474034879262492e5175ebeeb3da67bc0d5f4df3c8dd35518a7857e`  
		Last Modified: Sat, 16 Sep 2023 03:17:36 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed2bfaed4c56b2952ce7951559a1e8a504b928563596527ce595ef4d429208b`  
		Last Modified: Sat, 16 Sep 2023 03:17:48 GMT  
		Size: 57.5 MB (57493239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976e93fe68868d92851150fcf5368c07d6ca40e97e7e32d33d83d6ba0891326e`  
		Last Modified: Sat, 16 Sep 2023 03:17:37 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a4f8e9a685c98036922c1faebdce6fb5780f2f150e12e39a34cf0aa7e8a70c`  
		Last Modified: Sat, 16 Sep 2023 03:17:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7d1ee88e020553ff9cd56436f66ba752735ee131b77b43acab7a0250a4e7b720
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170084867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5fb818356dab5d361ec766077ce90f95215cfe87443700c698d5be8c5532ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:21:42 GMT
ADD file:c1b7bfaf11bf64b9c1b24345749a98cbd3f593162ea942e12b15c6f2110c1e94 in / 
# Sat, 16 Sep 2023 02:21:43 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:05:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:05:11 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:05:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:05:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:05:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:07:04 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 16 Sep 2023 03:07:04 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:07:04 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:07:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:07:39 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:07:39 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:08:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:08:15 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:08:15 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:08:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 16 Sep 2023 03:08:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:08:16 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:08:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d095360c6402749d9f7a3d7b7cdd417f27e41419f8027f4704ab00d0dd8ae7ee`  
		Last Modified: Sat, 16 Sep 2023 02:22:42 GMT  
		Size: 43.6 MB (43630964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0858301c0b29f5044b8124bf239eb818ea26beb8a761063839d8d22edcd1388`  
		Last Modified: Sat, 16 Sep 2023 03:08:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f442c155184089167742040807da8601460238f51bbfd6744e0c7a27f8f4bf2d`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 913.0 KB (912997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d70ba84e123b2ee603b84a3c4c0b9b247094ea07bb514eda5e8fc996d2bc89`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 4.3 MB (4302778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344316b4b482ae2b698900c186f8d5e55ff4060775edd5acac581058b02af8db`  
		Last Modified: Sat, 16 Sep 2023 03:08:38 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c08d57290eee845b9d8f78494f2841f187dec36a3610a2bc3621cbf47d88c82`  
		Last Modified: Sat, 16 Sep 2023 03:09:15 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f14c56729a234a2432b082ecc9bcf401aeb30cbdb5ebcd59a816dd71e4785bf`  
		Last Modified: Sat, 16 Sep 2023 03:09:19 GMT  
		Size: 57.5 MB (57457887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcd6640a567221afe4161fbd2b66fa3ac356a89df93d85a183c3049a2248b1c`  
		Last Modified: Sat, 16 Sep 2023 03:09:13 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1a54628d1a9fdf7c21dfd782172a0e784d0d2216428be72be3d97e35ab5a0c`  
		Last Modified: Sat, 16 Sep 2023 03:09:22 GMT  
		Size: 63.8 MB (63770566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec8cd7bbeeca01949e32c0e5047615827b95aabd1c7af25b883b4ef89f62b0d`  
		Last Modified: Sat, 16 Sep 2023 03:09:13 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65248fde3259ad79f7b2e9f0ff6c097536b20f87a3bb3c77091cb72bb039ed0`  
		Last Modified: Sat, 16 Sep 2023 03:09:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:e7d98ddd803bf80e718f3b2768652e9f17ef77e08a8a92bacbdaed55cec76b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:884b0e4378ef3b08e5e1082013432f858693019531f0758a986fe2549b7f070b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179509674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a61236e6f26d59684058f19b34a99259ad98bf52f33c87a51703942f9f4db8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:03:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Sep 2023 17:03:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:03:33 GMT
ENV GOSU_VERSION=1.16
# Wed, 20 Sep 2023 17:03:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Sep 2023 17:03:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Sep 2023 17:03:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:03:47 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Sep 2023 17:03:47 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 20 Sep 2023 17:03:47 GMT
ENV MYSQL_VERSION=8.0.34-1debian11
# Wed, 20 Sep 2023 17:03:48 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 20 Sep 2023 17:04:04 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 20 Sep 2023 17:04:04 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 Sep 2023 17:04:05 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 20 Sep 2023 17:04:05 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 20 Sep 2023 17:04:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 20 Sep 2023 17:04:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Sep 2023 17:04:05 GMT
EXPOSE 3306 33060
# Wed, 20 Sep 2023 17:04:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71e81bf2a3ccfbe1d110130d0e6798676acbcff61ca00230993ab464816f45e`  
		Last Modified: Wed, 20 Sep 2023 17:04:43 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3a5aabf422150647676ae3c4ccfdd6076e59f53c8700af07ab495e3ad319e0`  
		Last Modified: Wed, 20 Sep 2023 17:04:43 GMT  
		Size: 4.4 MB (4415030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710c034e9a2853c1757423d59bbdc5fac1167632c6ecbb884d3a0168d3d9bc54`  
		Last Modified: Wed, 20 Sep 2023 17:04:41 GMT  
		Size: 1.5 MB (1471540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e40f425faecd604a5ac51751b7f35190fc29bc7bd163935131c653f24d78eb`  
		Last Modified: Wed, 20 Sep 2023 17:04:41 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203652ae7f2e171ed82c74452b1f9b4080aefbfa74dc376ba0e39a4155a5cd1a`  
		Last Modified: Wed, 20 Sep 2023 17:04:43 GMT  
		Size: 12.7 MB (12662088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a91bbbc87b1637df195b9135721c1f07d3b2769aa8d97f813abc0935a4f82b`  
		Last Modified: Wed, 20 Sep 2023 17:04:40 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a66da1a56a90141be01430878b73a3b712f17ff5e87ac3754a4213a8595d16f`  
		Last Modified: Wed, 20 Sep 2023 17:04:38 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3846679b4e81080a751a7a3d196e20d1a10ff9313fdc3be32475a002f7d833a7`  
		Last Modified: Wed, 20 Sep 2023 17:04:57 GMT  
		Size: 129.5 MB (129532271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f92d3b4efe327863fc8db2a37765c5e891ce0d439ead27eb496b4bbdfec16d`  
		Last Modified: Wed, 20 Sep 2023 17:04:38 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c7399a8a3022163762490d18c80ebc57b16c9e49080c240adf626c234e57ec`  
		Last Modified: Wed, 20 Sep 2023 17:04:39 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e5bac08517e9f1ecea03e0ebfb8e43766738d82b21256378eee9d1cabcefc5`  
		Last Modified: Wed, 20 Sep 2023 17:04:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:09cf783c365fcd00ecda11e10239775373c8040562aaf59f74d28ab17488af12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e6fbd1b655b53b67508a21b446d554c8b36600449673ef9ee09193f63372ab8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166492942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca55c632ed6d006d4b672c08bf342d0baf8a8c6721a159607ef69c4cacc3a95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:40:54 GMT
ADD file:1632d5b9918ff63c9e38191b65ad8e6f1e0eb5c2ef274cce4f50534bba2f7493 in / 
# Sat, 16 Sep 2023 02:40:55 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:13:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:13:04 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:13:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:13:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:13:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 16 Sep 2023 03:15:12 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:15:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:15:48 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:15:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:15:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:16:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:16:31 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:16:31 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:16:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 16 Sep 2023 03:16:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:16:31 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:16:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bc377bce3181aab0e51009b13b6a6890e49c64e7bf6ab7fa12dce86a95c88bd4`  
		Last Modified: Sat, 16 Sep 2023 02:42:29 GMT  
		Size: 44.9 MB (44911063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bab949ab517e3be7ce2e1a260efa70a0b8d086b9a8eb94421e263202aebec7`  
		Last Modified: Sat, 16 Sep 2023 03:17:00 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73682200afb7af28b17b7f0b43ab59e0f6dee7de613a75eea5cbb9bd6051f034`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c32d486523845672c2afde18b2048f166858bed8cbd70df044ee6c2403cacd`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 4.6 MB (4606599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54341582c90c5e4c851a5a19299024e784fc074bc89a250e5bb0c54a1e29dbf8`  
		Last Modified: Sat, 16 Sep 2023 03:16:57 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12f032a8b52f337ef476dffbdc5929c946638d80ce5a6532206c83b962365d8`  
		Last Modified: Sat, 16 Sep 2023 03:17:38 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ec0aa1a86a21f28a71a1802009e52c58b5c88792d6ad73040d1c875e186299`  
		Last Modified: Sat, 16 Sep 2023 03:17:45 GMT  
		Size: 58.5 MB (58489547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11420f2dc474034879262492e5175ebeeb3da67bc0d5f4df3c8dd35518a7857e`  
		Last Modified: Sat, 16 Sep 2023 03:17:36 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed2bfaed4c56b2952ce7951559a1e8a504b928563596527ce595ef4d429208b`  
		Last Modified: Sat, 16 Sep 2023 03:17:48 GMT  
		Size: 57.5 MB (57493239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976e93fe68868d92851150fcf5368c07d6ca40e97e7e32d33d83d6ba0891326e`  
		Last Modified: Sat, 16 Sep 2023 03:17:37 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a4f8e9a685c98036922c1faebdce6fb5780f2f150e12e39a34cf0aa7e8a70c`  
		Last Modified: Sat, 16 Sep 2023 03:17:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7d1ee88e020553ff9cd56436f66ba752735ee131b77b43acab7a0250a4e7b720
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170084867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5fb818356dab5d361ec766077ce90f95215cfe87443700c698d5be8c5532ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:21:42 GMT
ADD file:c1b7bfaf11bf64b9c1b24345749a98cbd3f593162ea942e12b15c6f2110c1e94 in / 
# Sat, 16 Sep 2023 02:21:43 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:05:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:05:11 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:05:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:05:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:05:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:07:04 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 16 Sep 2023 03:07:04 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:07:04 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:07:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:07:39 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:07:39 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:08:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:08:15 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:08:15 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:08:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 16 Sep 2023 03:08:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:08:16 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:08:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d095360c6402749d9f7a3d7b7cdd417f27e41419f8027f4704ab00d0dd8ae7ee`  
		Last Modified: Sat, 16 Sep 2023 02:22:42 GMT  
		Size: 43.6 MB (43630964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0858301c0b29f5044b8124bf239eb818ea26beb8a761063839d8d22edcd1388`  
		Last Modified: Sat, 16 Sep 2023 03:08:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f442c155184089167742040807da8601460238f51bbfd6744e0c7a27f8f4bf2d`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 913.0 KB (912997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d70ba84e123b2ee603b84a3c4c0b9b247094ea07bb514eda5e8fc996d2bc89`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 4.3 MB (4302778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344316b4b482ae2b698900c186f8d5e55ff4060775edd5acac581058b02af8db`  
		Last Modified: Sat, 16 Sep 2023 03:08:38 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c08d57290eee845b9d8f78494f2841f187dec36a3610a2bc3621cbf47d88c82`  
		Last Modified: Sat, 16 Sep 2023 03:09:15 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f14c56729a234a2432b082ecc9bcf401aeb30cbdb5ebcd59a816dd71e4785bf`  
		Last Modified: Sat, 16 Sep 2023 03:09:19 GMT  
		Size: 57.5 MB (57457887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcd6640a567221afe4161fbd2b66fa3ac356a89df93d85a183c3049a2248b1c`  
		Last Modified: Sat, 16 Sep 2023 03:09:13 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1a54628d1a9fdf7c21dfd782172a0e784d0d2216428be72be3d97e35ab5a0c`  
		Last Modified: Sat, 16 Sep 2023 03:09:22 GMT  
		Size: 63.8 MB (63770566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec8cd7bbeeca01949e32c0e5047615827b95aabd1c7af25b883b4ef89f62b0d`  
		Last Modified: Sat, 16 Sep 2023 03:09:13 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65248fde3259ad79f7b2e9f0ff6c097536b20f87a3bb3c77091cb72bb039ed0`  
		Last Modified: Sat, 16 Sep 2023 03:09:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.34`

```console
$ docker pull mysql@sha256:09cf783c365fcd00ecda11e10239775373c8040562aaf59f74d28ab17488af12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.34` - linux; amd64

```console
$ docker pull mysql@sha256:e6fbd1b655b53b67508a21b446d554c8b36600449673ef9ee09193f63372ab8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166492942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca55c632ed6d006d4b672c08bf342d0baf8a8c6721a159607ef69c4cacc3a95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:40:54 GMT
ADD file:1632d5b9918ff63c9e38191b65ad8e6f1e0eb5c2ef274cce4f50534bba2f7493 in / 
# Sat, 16 Sep 2023 02:40:55 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:13:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:13:04 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:13:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:13:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:13:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 16 Sep 2023 03:15:12 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:15:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:15:48 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:15:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:15:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:16:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:16:31 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:16:31 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:16:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 16 Sep 2023 03:16:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:16:31 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:16:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bc377bce3181aab0e51009b13b6a6890e49c64e7bf6ab7fa12dce86a95c88bd4`  
		Last Modified: Sat, 16 Sep 2023 02:42:29 GMT  
		Size: 44.9 MB (44911063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bab949ab517e3be7ce2e1a260efa70a0b8d086b9a8eb94421e263202aebec7`  
		Last Modified: Sat, 16 Sep 2023 03:17:00 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73682200afb7af28b17b7f0b43ab59e0f6dee7de613a75eea5cbb9bd6051f034`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c32d486523845672c2afde18b2048f166858bed8cbd70df044ee6c2403cacd`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 4.6 MB (4606599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54341582c90c5e4c851a5a19299024e784fc074bc89a250e5bb0c54a1e29dbf8`  
		Last Modified: Sat, 16 Sep 2023 03:16:57 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12f032a8b52f337ef476dffbdc5929c946638d80ce5a6532206c83b962365d8`  
		Last Modified: Sat, 16 Sep 2023 03:17:38 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ec0aa1a86a21f28a71a1802009e52c58b5c88792d6ad73040d1c875e186299`  
		Last Modified: Sat, 16 Sep 2023 03:17:45 GMT  
		Size: 58.5 MB (58489547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11420f2dc474034879262492e5175ebeeb3da67bc0d5f4df3c8dd35518a7857e`  
		Last Modified: Sat, 16 Sep 2023 03:17:36 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed2bfaed4c56b2952ce7951559a1e8a504b928563596527ce595ef4d429208b`  
		Last Modified: Sat, 16 Sep 2023 03:17:48 GMT  
		Size: 57.5 MB (57493239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976e93fe68868d92851150fcf5368c07d6ca40e97e7e32d33d83d6ba0891326e`  
		Last Modified: Sat, 16 Sep 2023 03:17:37 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a4f8e9a685c98036922c1faebdce6fb5780f2f150e12e39a34cf0aa7e8a70c`  
		Last Modified: Sat, 16 Sep 2023 03:17:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.34` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7d1ee88e020553ff9cd56436f66ba752735ee131b77b43acab7a0250a4e7b720
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170084867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5fb818356dab5d361ec766077ce90f95215cfe87443700c698d5be8c5532ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:21:42 GMT
ADD file:c1b7bfaf11bf64b9c1b24345749a98cbd3f593162ea942e12b15c6f2110c1e94 in / 
# Sat, 16 Sep 2023 02:21:43 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:05:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:05:11 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:05:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:05:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:05:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:07:04 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 16 Sep 2023 03:07:04 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:07:04 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:07:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:07:39 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:07:39 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:08:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:08:15 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:08:15 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:08:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 16 Sep 2023 03:08:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:08:16 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:08:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d095360c6402749d9f7a3d7b7cdd417f27e41419f8027f4704ab00d0dd8ae7ee`  
		Last Modified: Sat, 16 Sep 2023 02:22:42 GMT  
		Size: 43.6 MB (43630964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0858301c0b29f5044b8124bf239eb818ea26beb8a761063839d8d22edcd1388`  
		Last Modified: Sat, 16 Sep 2023 03:08:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f442c155184089167742040807da8601460238f51bbfd6744e0c7a27f8f4bf2d`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 913.0 KB (912997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d70ba84e123b2ee603b84a3c4c0b9b247094ea07bb514eda5e8fc996d2bc89`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 4.3 MB (4302778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344316b4b482ae2b698900c186f8d5e55ff4060775edd5acac581058b02af8db`  
		Last Modified: Sat, 16 Sep 2023 03:08:38 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c08d57290eee845b9d8f78494f2841f187dec36a3610a2bc3621cbf47d88c82`  
		Last Modified: Sat, 16 Sep 2023 03:09:15 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f14c56729a234a2432b082ecc9bcf401aeb30cbdb5ebcd59a816dd71e4785bf`  
		Last Modified: Sat, 16 Sep 2023 03:09:19 GMT  
		Size: 57.5 MB (57457887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcd6640a567221afe4161fbd2b66fa3ac356a89df93d85a183c3049a2248b1c`  
		Last Modified: Sat, 16 Sep 2023 03:09:13 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1a54628d1a9fdf7c21dfd782172a0e784d0d2216428be72be3d97e35ab5a0c`  
		Last Modified: Sat, 16 Sep 2023 03:09:22 GMT  
		Size: 63.8 MB (63770566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec8cd7bbeeca01949e32c0e5047615827b95aabd1c7af25b883b4ef89f62b0d`  
		Last Modified: Sat, 16 Sep 2023 03:09:13 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65248fde3259ad79f7b2e9f0ff6c097536b20f87a3bb3c77091cb72bb039ed0`  
		Last Modified: Sat, 16 Sep 2023 03:09:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.34-debian`

```console
$ docker pull mysql@sha256:e7d98ddd803bf80e718f3b2768652e9f17ef77e08a8a92bacbdaed55cec76b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.34-debian` - linux; amd64

```console
$ docker pull mysql@sha256:884b0e4378ef3b08e5e1082013432f858693019531f0758a986fe2549b7f070b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179509674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a61236e6f26d59684058f19b34a99259ad98bf52f33c87a51703942f9f4db8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:03:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Sep 2023 17:03:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:03:33 GMT
ENV GOSU_VERSION=1.16
# Wed, 20 Sep 2023 17:03:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Sep 2023 17:03:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Sep 2023 17:03:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:03:47 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Sep 2023 17:03:47 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 20 Sep 2023 17:03:47 GMT
ENV MYSQL_VERSION=8.0.34-1debian11
# Wed, 20 Sep 2023 17:03:48 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 20 Sep 2023 17:04:04 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 20 Sep 2023 17:04:04 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 Sep 2023 17:04:05 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 20 Sep 2023 17:04:05 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 20 Sep 2023 17:04:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 20 Sep 2023 17:04:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Sep 2023 17:04:05 GMT
EXPOSE 3306 33060
# Wed, 20 Sep 2023 17:04:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71e81bf2a3ccfbe1d110130d0e6798676acbcff61ca00230993ab464816f45e`  
		Last Modified: Wed, 20 Sep 2023 17:04:43 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3a5aabf422150647676ae3c4ccfdd6076e59f53c8700af07ab495e3ad319e0`  
		Last Modified: Wed, 20 Sep 2023 17:04:43 GMT  
		Size: 4.4 MB (4415030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710c034e9a2853c1757423d59bbdc5fac1167632c6ecbb884d3a0168d3d9bc54`  
		Last Modified: Wed, 20 Sep 2023 17:04:41 GMT  
		Size: 1.5 MB (1471540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e40f425faecd604a5ac51751b7f35190fc29bc7bd163935131c653f24d78eb`  
		Last Modified: Wed, 20 Sep 2023 17:04:41 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203652ae7f2e171ed82c74452b1f9b4080aefbfa74dc376ba0e39a4155a5cd1a`  
		Last Modified: Wed, 20 Sep 2023 17:04:43 GMT  
		Size: 12.7 MB (12662088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a91bbbc87b1637df195b9135721c1f07d3b2769aa8d97f813abc0935a4f82b`  
		Last Modified: Wed, 20 Sep 2023 17:04:40 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a66da1a56a90141be01430878b73a3b712f17ff5e87ac3754a4213a8595d16f`  
		Last Modified: Wed, 20 Sep 2023 17:04:38 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3846679b4e81080a751a7a3d196e20d1a10ff9313fdc3be32475a002f7d833a7`  
		Last Modified: Wed, 20 Sep 2023 17:04:57 GMT  
		Size: 129.5 MB (129532271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f92d3b4efe327863fc8db2a37765c5e891ce0d439ead27eb496b4bbdfec16d`  
		Last Modified: Wed, 20 Sep 2023 17:04:38 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c7399a8a3022163762490d18c80ebc57b16c9e49080c240adf626c234e57ec`  
		Last Modified: Wed, 20 Sep 2023 17:04:39 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e5bac08517e9f1ecea03e0ebfb8e43766738d82b21256378eee9d1cabcefc5`  
		Last Modified: Wed, 20 Sep 2023 17:04:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.34-oracle`

```console
$ docker pull mysql@sha256:09cf783c365fcd00ecda11e10239775373c8040562aaf59f74d28ab17488af12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.34-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e6fbd1b655b53b67508a21b446d554c8b36600449673ef9ee09193f63372ab8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166492942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca55c632ed6d006d4b672c08bf342d0baf8a8c6721a159607ef69c4cacc3a95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:40:54 GMT
ADD file:1632d5b9918ff63c9e38191b65ad8e6f1e0eb5c2ef274cce4f50534bba2f7493 in / 
# Sat, 16 Sep 2023 02:40:55 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:13:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:13:04 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:13:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:13:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:13:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 16 Sep 2023 03:15:12 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:15:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:15:48 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:15:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:15:49 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:16:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:16:31 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:16:31 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:16:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 16 Sep 2023 03:16:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:16:31 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:16:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bc377bce3181aab0e51009b13b6a6890e49c64e7bf6ab7fa12dce86a95c88bd4`  
		Last Modified: Sat, 16 Sep 2023 02:42:29 GMT  
		Size: 44.9 MB (44911063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bab949ab517e3be7ce2e1a260efa70a0b8d086b9a8eb94421e263202aebec7`  
		Last Modified: Sat, 16 Sep 2023 03:17:00 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73682200afb7af28b17b7f0b43ab59e0f6dee7de613a75eea5cbb9bd6051f034`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c32d486523845672c2afde18b2048f166858bed8cbd70df044ee6c2403cacd`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 4.6 MB (4606599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54341582c90c5e4c851a5a19299024e784fc074bc89a250e5bb0c54a1e29dbf8`  
		Last Modified: Sat, 16 Sep 2023 03:16:57 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12f032a8b52f337ef476dffbdc5929c946638d80ce5a6532206c83b962365d8`  
		Last Modified: Sat, 16 Sep 2023 03:17:38 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ec0aa1a86a21f28a71a1802009e52c58b5c88792d6ad73040d1c875e186299`  
		Last Modified: Sat, 16 Sep 2023 03:17:45 GMT  
		Size: 58.5 MB (58489547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11420f2dc474034879262492e5175ebeeb3da67bc0d5f4df3c8dd35518a7857e`  
		Last Modified: Sat, 16 Sep 2023 03:17:36 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed2bfaed4c56b2952ce7951559a1e8a504b928563596527ce595ef4d429208b`  
		Last Modified: Sat, 16 Sep 2023 03:17:48 GMT  
		Size: 57.5 MB (57493239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976e93fe68868d92851150fcf5368c07d6ca40e97e7e32d33d83d6ba0891326e`  
		Last Modified: Sat, 16 Sep 2023 03:17:37 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a4f8e9a685c98036922c1faebdce6fb5780f2f150e12e39a34cf0aa7e8a70c`  
		Last Modified: Sat, 16 Sep 2023 03:17:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.34-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7d1ee88e020553ff9cd56436f66ba752735ee131b77b43acab7a0250a4e7b720
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170084867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5fb818356dab5d361ec766077ce90f95215cfe87443700c698d5be8c5532ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:21:42 GMT
ADD file:c1b7bfaf11bf64b9c1b24345749a98cbd3f593162ea942e12b15c6f2110c1e94 in / 
# Sat, 16 Sep 2023 02:21:43 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:05:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:05:11 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:05:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:05:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:05:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:07:04 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 16 Sep 2023 03:07:04 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:07:04 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:07:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:07:39 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:07:39 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:08:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:08:15 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:08:15 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:08:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 16 Sep 2023 03:08:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:08:16 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:08:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d095360c6402749d9f7a3d7b7cdd417f27e41419f8027f4704ab00d0dd8ae7ee`  
		Last Modified: Sat, 16 Sep 2023 02:22:42 GMT  
		Size: 43.6 MB (43630964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0858301c0b29f5044b8124bf239eb818ea26beb8a761063839d8d22edcd1388`  
		Last Modified: Sat, 16 Sep 2023 03:08:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f442c155184089167742040807da8601460238f51bbfd6744e0c7a27f8f4bf2d`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 913.0 KB (912997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d70ba84e123b2ee603b84a3c4c0b9b247094ea07bb514eda5e8fc996d2bc89`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 4.3 MB (4302778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344316b4b482ae2b698900c186f8d5e55ff4060775edd5acac581058b02af8db`  
		Last Modified: Sat, 16 Sep 2023 03:08:38 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c08d57290eee845b9d8f78494f2841f187dec36a3610a2bc3621cbf47d88c82`  
		Last Modified: Sat, 16 Sep 2023 03:09:15 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f14c56729a234a2432b082ecc9bcf401aeb30cbdb5ebcd59a816dd71e4785bf`  
		Last Modified: Sat, 16 Sep 2023 03:09:19 GMT  
		Size: 57.5 MB (57457887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcd6640a567221afe4161fbd2b66fa3ac356a89df93d85a183c3049a2248b1c`  
		Last Modified: Sat, 16 Sep 2023 03:09:13 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1a54628d1a9fdf7c21dfd782172a0e784d0d2216428be72be3d97e35ab5a0c`  
		Last Modified: Sat, 16 Sep 2023 03:09:22 GMT  
		Size: 63.8 MB (63770566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec8cd7bbeeca01949e32c0e5047615827b95aabd1c7af25b883b4ef89f62b0d`  
		Last Modified: Sat, 16 Sep 2023 03:09:13 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65248fde3259ad79f7b2e9f0ff6c097536b20f87a3bb3c77091cb72bb039ed0`  
		Last Modified: Sat, 16 Sep 2023 03:09:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.1`

```console
$ docker pull mysql@sha256:85ab57eb4a48ada2a341dcf7d96733ce2f370fffb8e8e216991b106e50fa6434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.1` - linux; amd64

```console
$ docker pull mysql@sha256:ecf2a95e14266b1d3fb72968b84ba2f32f1a0e9288d4ed2dc72f2012d3bb8587
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da80fe49fcfad1ac311a2e34c42730c943706c2008083f5e4feeb6d77cdbc1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:40:54 GMT
ADD file:1632d5b9918ff63c9e38191b65ad8e6f1e0eb5c2ef274cce4f50534bba2f7493 in / 
# Sat, 16 Sep 2023 02:40:55 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:13:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:13:04 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:13:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:13:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:13:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:13:36 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 16 Sep 2023 03:13:36 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Sat, 16 Sep 2023 03:13:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:14:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:14:54 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:14:55 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:14:55 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:14:55 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:14:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bc377bce3181aab0e51009b13b6a6890e49c64e7bf6ab7fa12dce86a95c88bd4`  
		Last Modified: Sat, 16 Sep 2023 02:42:29 GMT  
		Size: 44.9 MB (44911063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bab949ab517e3be7ce2e1a260efa70a0b8d086b9a8eb94421e263202aebec7`  
		Last Modified: Sat, 16 Sep 2023 03:17:00 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73682200afb7af28b17b7f0b43ab59e0f6dee7de613a75eea5cbb9bd6051f034`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c32d486523845672c2afde18b2048f166858bed8cbd70df044ee6c2403cacd`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 4.6 MB (4606599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54341582c90c5e4c851a5a19299024e784fc074bc89a250e5bb0c54a1e29dbf8`  
		Last Modified: Sat, 16 Sep 2023 03:16:57 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7490cd8f4d9b6814db10f8ac442f731ec4d04f9ec8a8fd3d1c995c2638700a56`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de967683cb3b284286c63a20fe7a0271ec7439c3ee46d39fc4746908a530fa65`  
		Last Modified: Sat, 16 Sep 2023 03:17:04 GMT  
		Size: 58.8 MB (58762808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39564f901a1edbe29de6869cc926733691e90c7fdee348fba590947754e91baa`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95e6efa291a87c772fa329e54fb4d0a8bba432ee01512fd7cf2b8732607eca3`  
		Last Modified: Sat, 16 Sep 2023 03:17:06 GMT  
		Size: 57.5 MB (57507195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8366d05afd7cc6b88fe7ccabf752a1ba4cfb5e73b6f228ef23190553e16438e5`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.1` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85e2dc34bdafb7a98b44902ac50c752adb70fd3589d0341955d65fa15faf61f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170318488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcbfd21648790d5c427728c74b254dd99eefd04cb0f3307199eb133de21cffc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:21:42 GMT
ADD file:c1b7bfaf11bf64b9c1b24345749a98cbd3f593162ea942e12b15c6f2110c1e94 in / 
# Sat, 16 Sep 2023 02:21:43 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:05:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:05:11 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:05:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:05:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:05:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:05:44 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 16 Sep 2023 03:05:44 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Sat, 16 Sep 2023 03:05:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:06:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:06:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:06:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:06:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:06:57 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:06:58 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:06:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:06:58 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:06:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d095360c6402749d9f7a3d7b7cdd417f27e41419f8027f4704ab00d0dd8ae7ee`  
		Last Modified: Sat, 16 Sep 2023 02:22:42 GMT  
		Size: 43.6 MB (43630964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0858301c0b29f5044b8124bf239eb818ea26beb8a761063839d8d22edcd1388`  
		Last Modified: Sat, 16 Sep 2023 03:08:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f442c155184089167742040807da8601460238f51bbfd6744e0c7a27f8f4bf2d`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 913.0 KB (912997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d70ba84e123b2ee603b84a3c4c0b9b247094ea07bb514eda5e8fc996d2bc89`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 4.3 MB (4302778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344316b4b482ae2b698900c186f8d5e55ff4060775edd5acac581058b02af8db`  
		Last Modified: Sat, 16 Sep 2023 03:08:38 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646e59d2b5913ed94c45bb54967c95965ac1c552213bf3fdc044926933196025`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d710d330bbe275dc6d4ab63a0fc43d0937e3d00522e6488a52e882e0be0eca4`  
		Last Modified: Sat, 16 Sep 2023 03:08:42 GMT  
		Size: 57.7 MB (57695529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fa9584c724548ebf9aeac0d3b92cc7b80ae8487599959613f87a44707ed765`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c19adc05d53aee28a6f99e5a4ae5a62539a856353547c8cb25b839e724ef94`  
		Last Modified: Sat, 16 Sep 2023 03:08:44 GMT  
		Size: 63.8 MB (63766659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6b1dad8c4a79d306583a0d88379d0f3cff5dd07bad3d1a97520365a26e6e8f`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.1-oracle`

```console
$ docker pull mysql@sha256:85ab57eb4a48ada2a341dcf7d96733ce2f370fffb8e8e216991b106e50fa6434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.1-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:ecf2a95e14266b1d3fb72968b84ba2f32f1a0e9288d4ed2dc72f2012d3bb8587
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da80fe49fcfad1ac311a2e34c42730c943706c2008083f5e4feeb6d77cdbc1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:40:54 GMT
ADD file:1632d5b9918ff63c9e38191b65ad8e6f1e0eb5c2ef274cce4f50534bba2f7493 in / 
# Sat, 16 Sep 2023 02:40:55 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:13:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:13:04 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:13:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:13:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:13:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:13:36 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 16 Sep 2023 03:13:36 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Sat, 16 Sep 2023 03:13:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:14:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:14:54 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:14:55 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:14:55 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:14:55 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:14:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bc377bce3181aab0e51009b13b6a6890e49c64e7bf6ab7fa12dce86a95c88bd4`  
		Last Modified: Sat, 16 Sep 2023 02:42:29 GMT  
		Size: 44.9 MB (44911063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bab949ab517e3be7ce2e1a260efa70a0b8d086b9a8eb94421e263202aebec7`  
		Last Modified: Sat, 16 Sep 2023 03:17:00 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73682200afb7af28b17b7f0b43ab59e0f6dee7de613a75eea5cbb9bd6051f034`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c32d486523845672c2afde18b2048f166858bed8cbd70df044ee6c2403cacd`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 4.6 MB (4606599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54341582c90c5e4c851a5a19299024e784fc074bc89a250e5bb0c54a1e29dbf8`  
		Last Modified: Sat, 16 Sep 2023 03:16:57 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7490cd8f4d9b6814db10f8ac442f731ec4d04f9ec8a8fd3d1c995c2638700a56`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de967683cb3b284286c63a20fe7a0271ec7439c3ee46d39fc4746908a530fa65`  
		Last Modified: Sat, 16 Sep 2023 03:17:04 GMT  
		Size: 58.8 MB (58762808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39564f901a1edbe29de6869cc926733691e90c7fdee348fba590947754e91baa`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95e6efa291a87c772fa329e54fb4d0a8bba432ee01512fd7cf2b8732607eca3`  
		Last Modified: Sat, 16 Sep 2023 03:17:06 GMT  
		Size: 57.5 MB (57507195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8366d05afd7cc6b88fe7ccabf752a1ba4cfb5e73b6f228ef23190553e16438e5`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.1-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85e2dc34bdafb7a98b44902ac50c752adb70fd3589d0341955d65fa15faf61f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170318488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcbfd21648790d5c427728c74b254dd99eefd04cb0f3307199eb133de21cffc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:21:42 GMT
ADD file:c1b7bfaf11bf64b9c1b24345749a98cbd3f593162ea942e12b15c6f2110c1e94 in / 
# Sat, 16 Sep 2023 02:21:43 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:05:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:05:11 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:05:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:05:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:05:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:05:44 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 16 Sep 2023 03:05:44 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Sat, 16 Sep 2023 03:05:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:06:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:06:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:06:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:06:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:06:57 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:06:58 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:06:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:06:58 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:06:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d095360c6402749d9f7a3d7b7cdd417f27e41419f8027f4704ab00d0dd8ae7ee`  
		Last Modified: Sat, 16 Sep 2023 02:22:42 GMT  
		Size: 43.6 MB (43630964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0858301c0b29f5044b8124bf239eb818ea26beb8a761063839d8d22edcd1388`  
		Last Modified: Sat, 16 Sep 2023 03:08:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f442c155184089167742040807da8601460238f51bbfd6744e0c7a27f8f4bf2d`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 913.0 KB (912997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d70ba84e123b2ee603b84a3c4c0b9b247094ea07bb514eda5e8fc996d2bc89`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 4.3 MB (4302778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344316b4b482ae2b698900c186f8d5e55ff4060775edd5acac581058b02af8db`  
		Last Modified: Sat, 16 Sep 2023 03:08:38 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646e59d2b5913ed94c45bb54967c95965ac1c552213bf3fdc044926933196025`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d710d330bbe275dc6d4ab63a0fc43d0937e3d00522e6488a52e882e0be0eca4`  
		Last Modified: Sat, 16 Sep 2023 03:08:42 GMT  
		Size: 57.7 MB (57695529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fa9584c724548ebf9aeac0d3b92cc7b80ae8487599959613f87a44707ed765`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c19adc05d53aee28a6f99e5a4ae5a62539a856353547c8cb25b839e724ef94`  
		Last Modified: Sat, 16 Sep 2023 03:08:44 GMT  
		Size: 63.8 MB (63766659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6b1dad8c4a79d306583a0d88379d0f3cff5dd07bad3d1a97520365a26e6e8f`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.1.0`

```console
$ docker pull mysql@sha256:85ab57eb4a48ada2a341dcf7d96733ce2f370fffb8e8e216991b106e50fa6434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.1.0` - linux; amd64

```console
$ docker pull mysql@sha256:ecf2a95e14266b1d3fb72968b84ba2f32f1a0e9288d4ed2dc72f2012d3bb8587
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da80fe49fcfad1ac311a2e34c42730c943706c2008083f5e4feeb6d77cdbc1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:40:54 GMT
ADD file:1632d5b9918ff63c9e38191b65ad8e6f1e0eb5c2ef274cce4f50534bba2f7493 in / 
# Sat, 16 Sep 2023 02:40:55 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:13:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:13:04 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:13:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:13:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:13:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:13:36 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 16 Sep 2023 03:13:36 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Sat, 16 Sep 2023 03:13:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:14:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:14:54 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:14:55 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:14:55 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:14:55 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:14:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bc377bce3181aab0e51009b13b6a6890e49c64e7bf6ab7fa12dce86a95c88bd4`  
		Last Modified: Sat, 16 Sep 2023 02:42:29 GMT  
		Size: 44.9 MB (44911063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bab949ab517e3be7ce2e1a260efa70a0b8d086b9a8eb94421e263202aebec7`  
		Last Modified: Sat, 16 Sep 2023 03:17:00 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73682200afb7af28b17b7f0b43ab59e0f6dee7de613a75eea5cbb9bd6051f034`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c32d486523845672c2afde18b2048f166858bed8cbd70df044ee6c2403cacd`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 4.6 MB (4606599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54341582c90c5e4c851a5a19299024e784fc074bc89a250e5bb0c54a1e29dbf8`  
		Last Modified: Sat, 16 Sep 2023 03:16:57 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7490cd8f4d9b6814db10f8ac442f731ec4d04f9ec8a8fd3d1c995c2638700a56`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de967683cb3b284286c63a20fe7a0271ec7439c3ee46d39fc4746908a530fa65`  
		Last Modified: Sat, 16 Sep 2023 03:17:04 GMT  
		Size: 58.8 MB (58762808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39564f901a1edbe29de6869cc926733691e90c7fdee348fba590947754e91baa`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95e6efa291a87c772fa329e54fb4d0a8bba432ee01512fd7cf2b8732607eca3`  
		Last Modified: Sat, 16 Sep 2023 03:17:06 GMT  
		Size: 57.5 MB (57507195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8366d05afd7cc6b88fe7ccabf752a1ba4cfb5e73b6f228ef23190553e16438e5`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.1.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85e2dc34bdafb7a98b44902ac50c752adb70fd3589d0341955d65fa15faf61f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170318488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcbfd21648790d5c427728c74b254dd99eefd04cb0f3307199eb133de21cffc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:21:42 GMT
ADD file:c1b7bfaf11bf64b9c1b24345749a98cbd3f593162ea942e12b15c6f2110c1e94 in / 
# Sat, 16 Sep 2023 02:21:43 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:05:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:05:11 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:05:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:05:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:05:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:05:44 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 16 Sep 2023 03:05:44 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Sat, 16 Sep 2023 03:05:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:06:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:06:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:06:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:06:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:06:57 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:06:58 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:06:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:06:58 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:06:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d095360c6402749d9f7a3d7b7cdd417f27e41419f8027f4704ab00d0dd8ae7ee`  
		Last Modified: Sat, 16 Sep 2023 02:22:42 GMT  
		Size: 43.6 MB (43630964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0858301c0b29f5044b8124bf239eb818ea26beb8a761063839d8d22edcd1388`  
		Last Modified: Sat, 16 Sep 2023 03:08:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f442c155184089167742040807da8601460238f51bbfd6744e0c7a27f8f4bf2d`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 913.0 KB (912997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d70ba84e123b2ee603b84a3c4c0b9b247094ea07bb514eda5e8fc996d2bc89`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 4.3 MB (4302778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344316b4b482ae2b698900c186f8d5e55ff4060775edd5acac581058b02af8db`  
		Last Modified: Sat, 16 Sep 2023 03:08:38 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646e59d2b5913ed94c45bb54967c95965ac1c552213bf3fdc044926933196025`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d710d330bbe275dc6d4ab63a0fc43d0937e3d00522e6488a52e882e0be0eca4`  
		Last Modified: Sat, 16 Sep 2023 03:08:42 GMT  
		Size: 57.7 MB (57695529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fa9584c724548ebf9aeac0d3b92cc7b80ae8487599959613f87a44707ed765`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c19adc05d53aee28a6f99e5a4ae5a62539a856353547c8cb25b839e724ef94`  
		Last Modified: Sat, 16 Sep 2023 03:08:44 GMT  
		Size: 63.8 MB (63766659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6b1dad8c4a79d306583a0d88379d0f3cff5dd07bad3d1a97520365a26e6e8f`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.1.0-oracle`

```console
$ docker pull mysql@sha256:85ab57eb4a48ada2a341dcf7d96733ce2f370fffb8e8e216991b106e50fa6434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.1.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:ecf2a95e14266b1d3fb72968b84ba2f32f1a0e9288d4ed2dc72f2012d3bb8587
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da80fe49fcfad1ac311a2e34c42730c943706c2008083f5e4feeb6d77cdbc1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:40:54 GMT
ADD file:1632d5b9918ff63c9e38191b65ad8e6f1e0eb5c2ef274cce4f50534bba2f7493 in / 
# Sat, 16 Sep 2023 02:40:55 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:13:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:13:04 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:13:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:13:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:13:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:13:36 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 16 Sep 2023 03:13:36 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Sat, 16 Sep 2023 03:13:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:14:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:14:54 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:14:55 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:14:55 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:14:55 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:14:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bc377bce3181aab0e51009b13b6a6890e49c64e7bf6ab7fa12dce86a95c88bd4`  
		Last Modified: Sat, 16 Sep 2023 02:42:29 GMT  
		Size: 44.9 MB (44911063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bab949ab517e3be7ce2e1a260efa70a0b8d086b9a8eb94421e263202aebec7`  
		Last Modified: Sat, 16 Sep 2023 03:17:00 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73682200afb7af28b17b7f0b43ab59e0f6dee7de613a75eea5cbb9bd6051f034`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c32d486523845672c2afde18b2048f166858bed8cbd70df044ee6c2403cacd`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 4.6 MB (4606599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54341582c90c5e4c851a5a19299024e784fc074bc89a250e5bb0c54a1e29dbf8`  
		Last Modified: Sat, 16 Sep 2023 03:16:57 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7490cd8f4d9b6814db10f8ac442f731ec4d04f9ec8a8fd3d1c995c2638700a56`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de967683cb3b284286c63a20fe7a0271ec7439c3ee46d39fc4746908a530fa65`  
		Last Modified: Sat, 16 Sep 2023 03:17:04 GMT  
		Size: 58.8 MB (58762808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39564f901a1edbe29de6869cc926733691e90c7fdee348fba590947754e91baa`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95e6efa291a87c772fa329e54fb4d0a8bba432ee01512fd7cf2b8732607eca3`  
		Last Modified: Sat, 16 Sep 2023 03:17:06 GMT  
		Size: 57.5 MB (57507195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8366d05afd7cc6b88fe7ccabf752a1ba4cfb5e73b6f228ef23190553e16438e5`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.1.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85e2dc34bdafb7a98b44902ac50c752adb70fd3589d0341955d65fa15faf61f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170318488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcbfd21648790d5c427728c74b254dd99eefd04cb0f3307199eb133de21cffc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:21:42 GMT
ADD file:c1b7bfaf11bf64b9c1b24345749a98cbd3f593162ea942e12b15c6f2110c1e94 in / 
# Sat, 16 Sep 2023 02:21:43 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:05:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:05:11 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:05:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:05:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:05:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:05:44 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 16 Sep 2023 03:05:44 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Sat, 16 Sep 2023 03:05:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:06:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:06:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:06:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:06:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:06:57 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:06:58 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:06:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:06:58 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:06:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d095360c6402749d9f7a3d7b7cdd417f27e41419f8027f4704ab00d0dd8ae7ee`  
		Last Modified: Sat, 16 Sep 2023 02:22:42 GMT  
		Size: 43.6 MB (43630964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0858301c0b29f5044b8124bf239eb818ea26beb8a761063839d8d22edcd1388`  
		Last Modified: Sat, 16 Sep 2023 03:08:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f442c155184089167742040807da8601460238f51bbfd6744e0c7a27f8f4bf2d`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 913.0 KB (912997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d70ba84e123b2ee603b84a3c4c0b9b247094ea07bb514eda5e8fc996d2bc89`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 4.3 MB (4302778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344316b4b482ae2b698900c186f8d5e55ff4060775edd5acac581058b02af8db`  
		Last Modified: Sat, 16 Sep 2023 03:08:38 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646e59d2b5913ed94c45bb54967c95965ac1c552213bf3fdc044926933196025`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d710d330bbe275dc6d4ab63a0fc43d0937e3d00522e6488a52e882e0be0eca4`  
		Last Modified: Sat, 16 Sep 2023 03:08:42 GMT  
		Size: 57.7 MB (57695529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fa9584c724548ebf9aeac0d3b92cc7b80ae8487599959613f87a44707ed765`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c19adc05d53aee28a6f99e5a4ae5a62539a856353547c8cb25b839e724ef94`  
		Last Modified: Sat, 16 Sep 2023 03:08:44 GMT  
		Size: 63.8 MB (63766659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6b1dad8c4a79d306583a0d88379d0f3cff5dd07bad3d1a97520365a26e6e8f`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:innovation`

```console
$ docker pull mysql@sha256:85ab57eb4a48ada2a341dcf7d96733ce2f370fffb8e8e216991b106e50fa6434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:ecf2a95e14266b1d3fb72968b84ba2f32f1a0e9288d4ed2dc72f2012d3bb8587
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da80fe49fcfad1ac311a2e34c42730c943706c2008083f5e4feeb6d77cdbc1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:40:54 GMT
ADD file:1632d5b9918ff63c9e38191b65ad8e6f1e0eb5c2ef274cce4f50534bba2f7493 in / 
# Sat, 16 Sep 2023 02:40:55 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:13:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:13:04 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:13:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:13:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:13:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:13:36 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 16 Sep 2023 03:13:36 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Sat, 16 Sep 2023 03:13:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:14:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:14:54 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:14:55 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:14:55 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:14:55 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:14:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bc377bce3181aab0e51009b13b6a6890e49c64e7bf6ab7fa12dce86a95c88bd4`  
		Last Modified: Sat, 16 Sep 2023 02:42:29 GMT  
		Size: 44.9 MB (44911063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bab949ab517e3be7ce2e1a260efa70a0b8d086b9a8eb94421e263202aebec7`  
		Last Modified: Sat, 16 Sep 2023 03:17:00 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73682200afb7af28b17b7f0b43ab59e0f6dee7de613a75eea5cbb9bd6051f034`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c32d486523845672c2afde18b2048f166858bed8cbd70df044ee6c2403cacd`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 4.6 MB (4606599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54341582c90c5e4c851a5a19299024e784fc074bc89a250e5bb0c54a1e29dbf8`  
		Last Modified: Sat, 16 Sep 2023 03:16:57 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7490cd8f4d9b6814db10f8ac442f731ec4d04f9ec8a8fd3d1c995c2638700a56`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de967683cb3b284286c63a20fe7a0271ec7439c3ee46d39fc4746908a530fa65`  
		Last Modified: Sat, 16 Sep 2023 03:17:04 GMT  
		Size: 58.8 MB (58762808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39564f901a1edbe29de6869cc926733691e90c7fdee348fba590947754e91baa`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95e6efa291a87c772fa329e54fb4d0a8bba432ee01512fd7cf2b8732607eca3`  
		Last Modified: Sat, 16 Sep 2023 03:17:06 GMT  
		Size: 57.5 MB (57507195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8366d05afd7cc6b88fe7ccabf752a1ba4cfb5e73b6f228ef23190553e16438e5`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85e2dc34bdafb7a98b44902ac50c752adb70fd3589d0341955d65fa15faf61f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170318488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcbfd21648790d5c427728c74b254dd99eefd04cb0f3307199eb133de21cffc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:21:42 GMT
ADD file:c1b7bfaf11bf64b9c1b24345749a98cbd3f593162ea942e12b15c6f2110c1e94 in / 
# Sat, 16 Sep 2023 02:21:43 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:05:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:05:11 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:05:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:05:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:05:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:05:44 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 16 Sep 2023 03:05:44 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Sat, 16 Sep 2023 03:05:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:06:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:06:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:06:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:06:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:06:57 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:06:58 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:06:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:06:58 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:06:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d095360c6402749d9f7a3d7b7cdd417f27e41419f8027f4704ab00d0dd8ae7ee`  
		Last Modified: Sat, 16 Sep 2023 02:22:42 GMT  
		Size: 43.6 MB (43630964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0858301c0b29f5044b8124bf239eb818ea26beb8a761063839d8d22edcd1388`  
		Last Modified: Sat, 16 Sep 2023 03:08:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f442c155184089167742040807da8601460238f51bbfd6744e0c7a27f8f4bf2d`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 913.0 KB (912997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d70ba84e123b2ee603b84a3c4c0b9b247094ea07bb514eda5e8fc996d2bc89`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 4.3 MB (4302778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344316b4b482ae2b698900c186f8d5e55ff4060775edd5acac581058b02af8db`  
		Last Modified: Sat, 16 Sep 2023 03:08:38 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646e59d2b5913ed94c45bb54967c95965ac1c552213bf3fdc044926933196025`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d710d330bbe275dc6d4ab63a0fc43d0937e3d00522e6488a52e882e0be0eca4`  
		Last Modified: Sat, 16 Sep 2023 03:08:42 GMT  
		Size: 57.7 MB (57695529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fa9584c724548ebf9aeac0d3b92cc7b80ae8487599959613f87a44707ed765`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c19adc05d53aee28a6f99e5a4ae5a62539a856353547c8cb25b839e724ef94`  
		Last Modified: Sat, 16 Sep 2023 03:08:44 GMT  
		Size: 63.8 MB (63766659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6b1dad8c4a79d306583a0d88379d0f3cff5dd07bad3d1a97520365a26e6e8f`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:85ab57eb4a48ada2a341dcf7d96733ce2f370fffb8e8e216991b106e50fa6434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:ecf2a95e14266b1d3fb72968b84ba2f32f1a0e9288d4ed2dc72f2012d3bb8587
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da80fe49fcfad1ac311a2e34c42730c943706c2008083f5e4feeb6d77cdbc1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:40:54 GMT
ADD file:1632d5b9918ff63c9e38191b65ad8e6f1e0eb5c2ef274cce4f50534bba2f7493 in / 
# Sat, 16 Sep 2023 02:40:55 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:13:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:13:04 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:13:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:13:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:13:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:13:36 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 16 Sep 2023 03:13:36 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Sat, 16 Sep 2023 03:13:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:14:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:14:54 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:14:55 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:14:55 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:14:55 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:14:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bc377bce3181aab0e51009b13b6a6890e49c64e7bf6ab7fa12dce86a95c88bd4`  
		Last Modified: Sat, 16 Sep 2023 02:42:29 GMT  
		Size: 44.9 MB (44911063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bab949ab517e3be7ce2e1a260efa70a0b8d086b9a8eb94421e263202aebec7`  
		Last Modified: Sat, 16 Sep 2023 03:17:00 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73682200afb7af28b17b7f0b43ab59e0f6dee7de613a75eea5cbb9bd6051f034`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c32d486523845672c2afde18b2048f166858bed8cbd70df044ee6c2403cacd`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 4.6 MB (4606599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54341582c90c5e4c851a5a19299024e784fc074bc89a250e5bb0c54a1e29dbf8`  
		Last Modified: Sat, 16 Sep 2023 03:16:57 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7490cd8f4d9b6814db10f8ac442f731ec4d04f9ec8a8fd3d1c995c2638700a56`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de967683cb3b284286c63a20fe7a0271ec7439c3ee46d39fc4746908a530fa65`  
		Last Modified: Sat, 16 Sep 2023 03:17:04 GMT  
		Size: 58.8 MB (58762808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39564f901a1edbe29de6869cc926733691e90c7fdee348fba590947754e91baa`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95e6efa291a87c772fa329e54fb4d0a8bba432ee01512fd7cf2b8732607eca3`  
		Last Modified: Sat, 16 Sep 2023 03:17:06 GMT  
		Size: 57.5 MB (57507195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8366d05afd7cc6b88fe7ccabf752a1ba4cfb5e73b6f228ef23190553e16438e5`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85e2dc34bdafb7a98b44902ac50c752adb70fd3589d0341955d65fa15faf61f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170318488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcbfd21648790d5c427728c74b254dd99eefd04cb0f3307199eb133de21cffc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:21:42 GMT
ADD file:c1b7bfaf11bf64b9c1b24345749a98cbd3f593162ea942e12b15c6f2110c1e94 in / 
# Sat, 16 Sep 2023 02:21:43 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:05:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:05:11 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:05:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:05:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:05:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:05:44 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 16 Sep 2023 03:05:44 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Sat, 16 Sep 2023 03:05:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:06:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:06:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:06:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:06:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:06:57 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:06:58 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:06:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:06:58 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:06:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d095360c6402749d9f7a3d7b7cdd417f27e41419f8027f4704ab00d0dd8ae7ee`  
		Last Modified: Sat, 16 Sep 2023 02:22:42 GMT  
		Size: 43.6 MB (43630964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0858301c0b29f5044b8124bf239eb818ea26beb8a761063839d8d22edcd1388`  
		Last Modified: Sat, 16 Sep 2023 03:08:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f442c155184089167742040807da8601460238f51bbfd6744e0c7a27f8f4bf2d`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 913.0 KB (912997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d70ba84e123b2ee603b84a3c4c0b9b247094ea07bb514eda5e8fc996d2bc89`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 4.3 MB (4302778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344316b4b482ae2b698900c186f8d5e55ff4060775edd5acac581058b02af8db`  
		Last Modified: Sat, 16 Sep 2023 03:08:38 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646e59d2b5913ed94c45bb54967c95965ac1c552213bf3fdc044926933196025`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d710d330bbe275dc6d4ab63a0fc43d0937e3d00522e6488a52e882e0be0eca4`  
		Last Modified: Sat, 16 Sep 2023 03:08:42 GMT  
		Size: 57.7 MB (57695529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fa9584c724548ebf9aeac0d3b92cc7b80ae8487599959613f87a44707ed765`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c19adc05d53aee28a6f99e5a4ae5a62539a856353547c8cb25b839e724ef94`  
		Last Modified: Sat, 16 Sep 2023 03:08:44 GMT  
		Size: 63.8 MB (63766659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6b1dad8c4a79d306583a0d88379d0f3cff5dd07bad3d1a97520365a26e6e8f`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:85ab57eb4a48ada2a341dcf7d96733ce2f370fffb8e8e216991b106e50fa6434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:ecf2a95e14266b1d3fb72968b84ba2f32f1a0e9288d4ed2dc72f2012d3bb8587
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da80fe49fcfad1ac311a2e34c42730c943706c2008083f5e4feeb6d77cdbc1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:40:54 GMT
ADD file:1632d5b9918ff63c9e38191b65ad8e6f1e0eb5c2ef274cce4f50534bba2f7493 in / 
# Sat, 16 Sep 2023 02:40:55 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:13:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:13:04 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:13:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:13:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:13:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:13:36 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 16 Sep 2023 03:13:36 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Sat, 16 Sep 2023 03:13:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:14:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:14:54 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:14:55 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:14:55 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:14:55 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:14:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bc377bce3181aab0e51009b13b6a6890e49c64e7bf6ab7fa12dce86a95c88bd4`  
		Last Modified: Sat, 16 Sep 2023 02:42:29 GMT  
		Size: 44.9 MB (44911063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bab949ab517e3be7ce2e1a260efa70a0b8d086b9a8eb94421e263202aebec7`  
		Last Modified: Sat, 16 Sep 2023 03:17:00 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73682200afb7af28b17b7f0b43ab59e0f6dee7de613a75eea5cbb9bd6051f034`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c32d486523845672c2afde18b2048f166858bed8cbd70df044ee6c2403cacd`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 4.6 MB (4606599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54341582c90c5e4c851a5a19299024e784fc074bc89a250e5bb0c54a1e29dbf8`  
		Last Modified: Sat, 16 Sep 2023 03:16:57 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7490cd8f4d9b6814db10f8ac442f731ec4d04f9ec8a8fd3d1c995c2638700a56`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de967683cb3b284286c63a20fe7a0271ec7439c3ee46d39fc4746908a530fa65`  
		Last Modified: Sat, 16 Sep 2023 03:17:04 GMT  
		Size: 58.8 MB (58762808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39564f901a1edbe29de6869cc926733691e90c7fdee348fba590947754e91baa`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95e6efa291a87c772fa329e54fb4d0a8bba432ee01512fd7cf2b8732607eca3`  
		Last Modified: Sat, 16 Sep 2023 03:17:06 GMT  
		Size: 57.5 MB (57507195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8366d05afd7cc6b88fe7ccabf752a1ba4cfb5e73b6f228ef23190553e16438e5`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85e2dc34bdafb7a98b44902ac50c752adb70fd3589d0341955d65fa15faf61f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170318488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcbfd21648790d5c427728c74b254dd99eefd04cb0f3307199eb133de21cffc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:21:42 GMT
ADD file:c1b7bfaf11bf64b9c1b24345749a98cbd3f593162ea942e12b15c6f2110c1e94 in / 
# Sat, 16 Sep 2023 02:21:43 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:05:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:05:11 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:05:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:05:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:05:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:05:44 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 16 Sep 2023 03:05:44 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Sat, 16 Sep 2023 03:05:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:06:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:06:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:06:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:06:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:06:57 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:06:58 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:06:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:06:58 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:06:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d095360c6402749d9f7a3d7b7cdd417f27e41419f8027f4704ab00d0dd8ae7ee`  
		Last Modified: Sat, 16 Sep 2023 02:22:42 GMT  
		Size: 43.6 MB (43630964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0858301c0b29f5044b8124bf239eb818ea26beb8a761063839d8d22edcd1388`  
		Last Modified: Sat, 16 Sep 2023 03:08:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f442c155184089167742040807da8601460238f51bbfd6744e0c7a27f8f4bf2d`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 913.0 KB (912997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d70ba84e123b2ee603b84a3c4c0b9b247094ea07bb514eda5e8fc996d2bc89`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 4.3 MB (4302778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344316b4b482ae2b698900c186f8d5e55ff4060775edd5acac581058b02af8db`  
		Last Modified: Sat, 16 Sep 2023 03:08:38 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646e59d2b5913ed94c45bb54967c95965ac1c552213bf3fdc044926933196025`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d710d330bbe275dc6d4ab63a0fc43d0937e3d00522e6488a52e882e0be0eca4`  
		Last Modified: Sat, 16 Sep 2023 03:08:42 GMT  
		Size: 57.7 MB (57695529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fa9584c724548ebf9aeac0d3b92cc7b80ae8487599959613f87a44707ed765`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c19adc05d53aee28a6f99e5a4ae5a62539a856353547c8cb25b839e724ef94`  
		Last Modified: Sat, 16 Sep 2023 03:08:44 GMT  
		Size: 63.8 MB (63766659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6b1dad8c4a79d306583a0d88379d0f3cff5dd07bad3d1a97520365a26e6e8f`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:85ab57eb4a48ada2a341dcf7d96733ce2f370fffb8e8e216991b106e50fa6434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:ecf2a95e14266b1d3fb72968b84ba2f32f1a0e9288d4ed2dc72f2012d3bb8587
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da80fe49fcfad1ac311a2e34c42730c943706c2008083f5e4feeb6d77cdbc1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:40:54 GMT
ADD file:1632d5b9918ff63c9e38191b65ad8e6f1e0eb5c2ef274cce4f50534bba2f7493 in / 
# Sat, 16 Sep 2023 02:40:55 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:13:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:13:04 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:13:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:13:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:13:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:13:36 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 16 Sep 2023 03:13:36 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Sat, 16 Sep 2023 03:13:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:14:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:14:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:14:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:14:54 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:14:55 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:14:55 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:14:55 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:14:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bc377bce3181aab0e51009b13b6a6890e49c64e7bf6ab7fa12dce86a95c88bd4`  
		Last Modified: Sat, 16 Sep 2023 02:42:29 GMT  
		Size: 44.9 MB (44911063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bab949ab517e3be7ce2e1a260efa70a0b8d086b9a8eb94421e263202aebec7`  
		Last Modified: Sat, 16 Sep 2023 03:17:00 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73682200afb7af28b17b7f0b43ab59e0f6dee7de613a75eea5cbb9bd6051f034`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c32d486523845672c2afde18b2048f166858bed8cbd70df044ee6c2403cacd`  
		Last Modified: Sat, 16 Sep 2023 03:16:59 GMT  
		Size: 4.6 MB (4606599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54341582c90c5e4c851a5a19299024e784fc074bc89a250e5bb0c54a1e29dbf8`  
		Last Modified: Sat, 16 Sep 2023 03:16:57 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7490cd8f4d9b6814db10f8ac442f731ec4d04f9ec8a8fd3d1c995c2638700a56`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de967683cb3b284286c63a20fe7a0271ec7439c3ee46d39fc4746908a530fa65`  
		Last Modified: Sat, 16 Sep 2023 03:17:04 GMT  
		Size: 58.8 MB (58762808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39564f901a1edbe29de6869cc926733691e90c7fdee348fba590947754e91baa`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95e6efa291a87c772fa329e54fb4d0a8bba432ee01512fd7cf2b8732607eca3`  
		Last Modified: Sat, 16 Sep 2023 03:17:06 GMT  
		Size: 57.5 MB (57507195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8366d05afd7cc6b88fe7ccabf752a1ba4cfb5e73b6f228ef23190553e16438e5`  
		Last Modified: Sat, 16 Sep 2023 03:16:55 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:85e2dc34bdafb7a98b44902ac50c752adb70fd3589d0341955d65fa15faf61f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170318488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcbfd21648790d5c427728c74b254dd99eefd04cb0f3307199eb133de21cffc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 16 Sep 2023 02:21:42 GMT
ADD file:c1b7bfaf11bf64b9c1b24345749a98cbd3f593162ea942e12b15c6f2110c1e94 in / 
# Sat, 16 Sep 2023 02:21:43 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 03:05:11 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 16 Sep 2023 03:05:11 GMT
ENV GOSU_VERSION=1.16
# Sat, 16 Sep 2023 03:05:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Sep 2023 03:05:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 16 Sep 2023 03:05:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 16 Sep 2023 03:05:44 GMT
ENV MYSQL_MAJOR=innovation
# Sat, 16 Sep 2023 03:05:44 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Sat, 16 Sep 2023 03:05:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 16 Sep 2023 03:06:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 16 Sep 2023 03:06:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 16 Sep 2023 03:06:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Sat, 16 Sep 2023 03:06:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 16 Sep 2023 03:06:57 GMT
VOLUME [/var/lib/mysql]
# Sat, 16 Sep 2023 03:06:58 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 16 Sep 2023 03:06:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 03:06:58 GMT
EXPOSE 3306 33060
# Sat, 16 Sep 2023 03:06:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d095360c6402749d9f7a3d7b7cdd417f27e41419f8027f4704ab00d0dd8ae7ee`  
		Last Modified: Sat, 16 Sep 2023 02:22:42 GMT  
		Size: 43.6 MB (43630964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0858301c0b29f5044b8124bf239eb818ea26beb8a761063839d8d22edcd1388`  
		Last Modified: Sat, 16 Sep 2023 03:08:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f442c155184089167742040807da8601460238f51bbfd6744e0c7a27f8f4bf2d`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 913.0 KB (912997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d70ba84e123b2ee603b84a3c4c0b9b247094ea07bb514eda5e8fc996d2bc89`  
		Last Modified: Sat, 16 Sep 2023 03:08:39 GMT  
		Size: 4.3 MB (4302778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344316b4b482ae2b698900c186f8d5e55ff4060775edd5acac581058b02af8db`  
		Last Modified: Sat, 16 Sep 2023 03:08:38 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646e59d2b5913ed94c45bb54967c95965ac1c552213bf3fdc044926933196025`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d710d330bbe275dc6d4ab63a0fc43d0937e3d00522e6488a52e882e0be0eca4`  
		Last Modified: Sat, 16 Sep 2023 03:08:42 GMT  
		Size: 57.7 MB (57695529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fa9584c724548ebf9aeac0d3b92cc7b80ae8487599959613f87a44707ed765`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c19adc05d53aee28a6f99e5a4ae5a62539a856353547c8cb25b839e724ef94`  
		Last Modified: Sat, 16 Sep 2023 03:08:44 GMT  
		Size: 63.8 MB (63766659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6b1dad8c4a79d306583a0d88379d0f3cff5dd07bad3d1a97520365a26e6e8f`  
		Last Modified: Sat, 16 Sep 2023 03:08:36 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
