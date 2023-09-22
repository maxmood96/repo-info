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
$ docker pull mysql@sha256:566007208a3f1cc8f9df6b767665b5c9b800fc4fb5f863d17aa1df362880ed04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:fa3d07406ef9c95681e6a95c5abc036355c5e3ac20abfb37865ccc3539e4bd50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166876333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2013ac9910129ded1da4c96495142b2ed0638ddf7e86e65156400d9a8503777`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:24:01 GMT
ADD file:909c07f3bad92a80d3917d583769a01bf62c2cbf3dd24f450fb303b1db92a83e in / 
# Thu, 21 Sep 2023 23:24:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:41:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:41:01 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:41:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:41:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:41:34 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:41:34 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 21 Sep 2023 23:41:34 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 21 Sep 2023 23:41:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:42:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:42:10 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:42:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:42:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:42:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:42:51 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:42:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:42:51 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:42:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5262579e8e45cb87fdc8fb6182d30da3c9e4f1036e02223508f287899ea434c0`  
		Last Modified: Thu, 21 Sep 2023 23:25:18 GMT  
		Size: 45.0 MB (44959147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b767e25b7494c443d7dee268bc45577e90fcb4ece6c6f23c3fc93b7f4f319`  
		Last Modified: Thu, 21 Sep 2023 23:44:42 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e0c37837cfca7152f3fa4b752cc088e69f92e7bd9953229c7344de7335cd4c`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 982.8 KB (982820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f5d3670db7f8c371cd0aa2306cbf90e70e88aefa5a8ad7d15c5f426e69bf62`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 4.6 MB (4620337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c567b29c3ec4335f466d1b027ff9ab6ab1275da314da8eb088c38b2cde8cf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6effcc6561c9792f2e42dcee38c1b79c50d573dfae21a4c15d56cdf116b3faf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1493d45d9c24bf2946229eb3808d5603ad083f49ed16edab012e849485040f`  
		Last Modified: Thu, 21 Sep 2023 23:44:47 GMT  
		Size: 58.8 MB (58777440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7101609fa7d97ae2dabcc48d18271b8013cd59fd2cb18646cd8e5269d6a2b644`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a1261dc2ab100e2f5cd2582a00da9c7c03d56dcd7524c3e32103975617b8a`  
		Last Modified: Thu, 21 Sep 2023 23:44:48 GMT  
		Size: 57.5 MB (57527025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865a24d6d1f28b65e14fdcc535e8a07e6214872929f0b3647ef860c098c92f77`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c0f7818fc533e4dfb17cdbfb8a1832d03f15c4acededcc4fbe67435b8b893541
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170377422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3503aa5f07519bad58f17ca0bc9b3ae21a66133942fbd915936c60d336a6142e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:40:46 GMT
ADD file:c630310324edbc0dd09d0912b8e7074d17ac71b1be8a14af9663872c081c4632 in / 
# Thu, 21 Sep 2023 23:40:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:57:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:57:07 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:57:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:57:34 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:57:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:57:35 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 21 Sep 2023 23:57:35 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 21 Sep 2023 23:57:36 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:58:06 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:58:08 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:58:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:58:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:58:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:58:44 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:58:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:58:45 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:58:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:286c1c922769d7608c32cf62931e95d7d169a0306164d24ce7d7a8a065959315`  
		Last Modified: Thu, 21 Sep 2023 23:41:39 GMT  
		Size: 43.7 MB (43657726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2045d234108f24e754e675bd763120bca5713bfbd34f917cef312b16b8eaeb84`  
		Last Modified: Fri, 22 Sep 2023 00:00:26 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e96650b64b585d497570d68ed967ef978298a63dcc9de51061e94b04ef316a`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e078f368c90db174893b4ac4586b3f26efd45a6cb77eb8803ce1d916121d1e37`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 4.3 MB (4307237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e3454b5c5a94b323b466e6bcaecb9d3310c242dd8b2c6880913c2477fbec43`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2babac95cc038ef3da37b9e01cf3d22d2ef66a1d4353f0bc2969d38b858ce9a1`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa3f01ac3f924ae70b2fc8bb2f909031a6ab25a7922183d5682c7d9fb531dfd`  
		Last Modified: Fri, 22 Sep 2023 00:00:28 GMT  
		Size: 57.7 MB (57712118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69a1f6641e4c90e2761fd42f3bad7499bcff043b48bccdcdb1925688c8a6e6`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 322.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc7d63c8a6ff2afcbc55a78186f338dfcb811708e4bf65c7e1a33b51c28c230`  
		Last Modified: Fri, 22 Sep 2023 00:00:30 GMT  
		Size: 63.8 MB (63777776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc23fd020fd3056f91c4a5f48dc80801ef0614d428304b8712b64bf7424fd84a`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:566007208a3f1cc8f9df6b767665b5c9b800fc4fb5f863d17aa1df362880ed04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:fa3d07406ef9c95681e6a95c5abc036355c5e3ac20abfb37865ccc3539e4bd50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166876333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2013ac9910129ded1da4c96495142b2ed0638ddf7e86e65156400d9a8503777`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:24:01 GMT
ADD file:909c07f3bad92a80d3917d583769a01bf62c2cbf3dd24f450fb303b1db92a83e in / 
# Thu, 21 Sep 2023 23:24:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:41:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:41:01 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:41:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:41:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:41:34 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:41:34 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 21 Sep 2023 23:41:34 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 21 Sep 2023 23:41:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:42:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:42:10 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:42:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:42:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:42:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:42:51 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:42:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:42:51 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:42:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5262579e8e45cb87fdc8fb6182d30da3c9e4f1036e02223508f287899ea434c0`  
		Last Modified: Thu, 21 Sep 2023 23:25:18 GMT  
		Size: 45.0 MB (44959147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b767e25b7494c443d7dee268bc45577e90fcb4ece6c6f23c3fc93b7f4f319`  
		Last Modified: Thu, 21 Sep 2023 23:44:42 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e0c37837cfca7152f3fa4b752cc088e69f92e7bd9953229c7344de7335cd4c`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 982.8 KB (982820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f5d3670db7f8c371cd0aa2306cbf90e70e88aefa5a8ad7d15c5f426e69bf62`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 4.6 MB (4620337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c567b29c3ec4335f466d1b027ff9ab6ab1275da314da8eb088c38b2cde8cf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6effcc6561c9792f2e42dcee38c1b79c50d573dfae21a4c15d56cdf116b3faf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1493d45d9c24bf2946229eb3808d5603ad083f49ed16edab012e849485040f`  
		Last Modified: Thu, 21 Sep 2023 23:44:47 GMT  
		Size: 58.8 MB (58777440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7101609fa7d97ae2dabcc48d18271b8013cd59fd2cb18646cd8e5269d6a2b644`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a1261dc2ab100e2f5cd2582a00da9c7c03d56dcd7524c3e32103975617b8a`  
		Last Modified: Thu, 21 Sep 2023 23:44:48 GMT  
		Size: 57.5 MB (57527025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865a24d6d1f28b65e14fdcc535e8a07e6214872929f0b3647ef860c098c92f77`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c0f7818fc533e4dfb17cdbfb8a1832d03f15c4acededcc4fbe67435b8b893541
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170377422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3503aa5f07519bad58f17ca0bc9b3ae21a66133942fbd915936c60d336a6142e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:40:46 GMT
ADD file:c630310324edbc0dd09d0912b8e7074d17ac71b1be8a14af9663872c081c4632 in / 
# Thu, 21 Sep 2023 23:40:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:57:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:57:07 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:57:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:57:34 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:57:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:57:35 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 21 Sep 2023 23:57:35 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 21 Sep 2023 23:57:36 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:58:06 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:58:08 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:58:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:58:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:58:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:58:44 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:58:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:58:45 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:58:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:286c1c922769d7608c32cf62931e95d7d169a0306164d24ce7d7a8a065959315`  
		Last Modified: Thu, 21 Sep 2023 23:41:39 GMT  
		Size: 43.7 MB (43657726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2045d234108f24e754e675bd763120bca5713bfbd34f917cef312b16b8eaeb84`  
		Last Modified: Fri, 22 Sep 2023 00:00:26 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e96650b64b585d497570d68ed967ef978298a63dcc9de51061e94b04ef316a`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e078f368c90db174893b4ac4586b3f26efd45a6cb77eb8803ce1d916121d1e37`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 4.3 MB (4307237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e3454b5c5a94b323b466e6bcaecb9d3310c242dd8b2c6880913c2477fbec43`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2babac95cc038ef3da37b9e01cf3d22d2ef66a1d4353f0bc2969d38b858ce9a1`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa3f01ac3f924ae70b2fc8bb2f909031a6ab25a7922183d5682c7d9fb531dfd`  
		Last Modified: Fri, 22 Sep 2023 00:00:28 GMT  
		Size: 57.7 MB (57712118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69a1f6641e4c90e2761fd42f3bad7499bcff043b48bccdcdb1925688c8a6e6`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 322.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc7d63c8a6ff2afcbc55a78186f338dfcb811708e4bf65c7e1a33b51c28c230`  
		Last Modified: Fri, 22 Sep 2023 00:00:30 GMT  
		Size: 63.8 MB (63777776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc23fd020fd3056f91c4a5f48dc80801ef0614d428304b8712b64bf7424fd84a`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:a7a96a9dbf6f310703c4e0c61086b23c5835c33a05544cdc952a7cd0b8feb675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:a0757f07e801b6bc5c56966c516ed61bf19be7587917862d52168be18a57125e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166602229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a53f40065fff68a0d8c9c7f0cd91942184d1607b99bce0b97273283791befaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:24:01 GMT
ADD file:909c07f3bad92a80d3917d583769a01bf62c2cbf3dd24f450fb303b1db92a83e in / 
# Thu, 21 Sep 2023 23:24:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:41:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:41:01 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:41:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:41:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:41:34 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:42:54 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 21 Sep 2023 23:42:55 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:42:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:43:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:43:31 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:43:31 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:44:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:44:12 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:44:12 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:44:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 21 Sep 2023 23:44:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:44:13 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:44:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5262579e8e45cb87fdc8fb6182d30da3c9e4f1036e02223508f287899ea434c0`  
		Last Modified: Thu, 21 Sep 2023 23:25:18 GMT  
		Size: 45.0 MB (44959147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b767e25b7494c443d7dee268bc45577e90fcb4ece6c6f23c3fc93b7f4f319`  
		Last Modified: Thu, 21 Sep 2023 23:44:42 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e0c37837cfca7152f3fa4b752cc088e69f92e7bd9953229c7344de7335cd4c`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 982.8 KB (982820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f5d3670db7f8c371cd0aa2306cbf90e70e88aefa5a8ad7d15c5f426e69bf62`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 4.6 MB (4620337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c567b29c3ec4335f466d1b027ff9ab6ab1275da314da8eb088c38b2cde8cf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323a74fdf36b1c06cbae2e64fa2c6d3a633da6739719ba5d0a878e4fa0ba1fd3`  
		Last Modified: Thu, 21 Sep 2023 23:45:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130e11b8eb713cacaf4b4f831d9ed4ac7edd02d74651f6646585a942f7da3e3e`  
		Last Modified: Thu, 21 Sep 2023 23:45:22 GMT  
		Size: 58.5 MB (58507528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92f1f2dd77ca35e3916bb1c57301be82b294af74b4d4c9798d339cc8fce7180`  
		Last Modified: Thu, 21 Sep 2023 23:45:14 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c0f03962c9878e744f644fff422ec54b9b24e7e682282accc61a31ff295c33`  
		Last Modified: Thu, 21 Sep 2023 23:45:24 GMT  
		Size: 57.5 MB (57522718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194c2f9ce134d33a9c303f4e3e96d85ec098f9522a4904a46452c8f52bb3545`  
		Last Modified: Thu, 21 Sep 2023 23:45:14 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a235a73ec4d4399d8b105da41e4aabe7be01c39e05cb15792ff00f08c4a0e5f8`  
		Last Modified: Thu, 21 Sep 2023 23:45:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:af8830366f4019e521beb9abd91c416c3d7647fc23d2accaac459075c2963aae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170136425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659ee6cc1dd35b909daead51fbc9010e2252ce16bc260b56b6d709facb844a7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:40:46 GMT
ADD file:c630310324edbc0dd09d0912b8e7074d17ac71b1be8a14af9663872c081c4632 in / 
# Thu, 21 Sep 2023 23:40:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:57:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:57:07 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:57:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:57:34 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:57:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:58:59 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 21 Sep 2023 23:58:59 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:58:59 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:59:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:59:30 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:59:30 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Fri, 22 Sep 2023 00:00:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 22 Sep 2023 00:00:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Sep 2023 00:00:06 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 22 Sep 2023 00:00:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 22 Sep 2023 00:00:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Sep 2023 00:00:06 GMT
EXPOSE 3306 33060
# Fri, 22 Sep 2023 00:00:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:286c1c922769d7608c32cf62931e95d7d169a0306164d24ce7d7a8a065959315`  
		Last Modified: Thu, 21 Sep 2023 23:41:39 GMT  
		Size: 43.7 MB (43657726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2045d234108f24e754e675bd763120bca5713bfbd34f917cef312b16b8eaeb84`  
		Last Modified: Fri, 22 Sep 2023 00:00:26 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e96650b64b585d497570d68ed967ef978298a63dcc9de51061e94b04ef316a`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e078f368c90db174893b4ac4586b3f26efd45a6cb77eb8803ce1d916121d1e37`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 4.3 MB (4307237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e3454b5c5a94b323b466e6bcaecb9d3310c242dd8b2c6880913c2477fbec43`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c69fbea8e7c6c7e9be3c680df3c72949926510f00838b2447d9f6930a03fcb`  
		Last Modified: Fri, 22 Sep 2023 00:01:01 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428eab90a954e02a3ab1ce3bbe2069b5bdf8e026c08708d0382f38e4d546700a`  
		Last Modified: Fri, 22 Sep 2023 00:01:05 GMT  
		Size: 57.5 MB (57472931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3dddc91cd1bf126fadae67b9e071f2b97ed5d405e33beb6d4dae3e640598d0a`  
		Last Modified: Fri, 22 Sep 2023 00:00:59 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91e3764e65379aadf08f4e91723b7a0269b2ea9f6243e5c2ef319f26b6b7e23`  
		Last Modified: Fri, 22 Sep 2023 00:01:07 GMT  
		Size: 63.8 MB (63775860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace219fec8ec8803e87fca2139f3d5afe0cf04cae4b790c21bb7ef9a8ebd4687`  
		Last Modified: Fri, 22 Sep 2023 00:00:59 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec9269f2cec4c9e9a543a9114351089f17bf36a1c49eb476bbfaa1d1e647fc0`  
		Last Modified: Fri, 22 Sep 2023 00:00:59 GMT  
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
$ docker pull mysql@sha256:a7a96a9dbf6f310703c4e0c61086b23c5835c33a05544cdc952a7cd0b8feb675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a0757f07e801b6bc5c56966c516ed61bf19be7587917862d52168be18a57125e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166602229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a53f40065fff68a0d8c9c7f0cd91942184d1607b99bce0b97273283791befaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:24:01 GMT
ADD file:909c07f3bad92a80d3917d583769a01bf62c2cbf3dd24f450fb303b1db92a83e in / 
# Thu, 21 Sep 2023 23:24:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:41:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:41:01 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:41:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:41:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:41:34 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:42:54 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 21 Sep 2023 23:42:55 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:42:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:43:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:43:31 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:43:31 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:44:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:44:12 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:44:12 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:44:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 21 Sep 2023 23:44:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:44:13 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:44:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5262579e8e45cb87fdc8fb6182d30da3c9e4f1036e02223508f287899ea434c0`  
		Last Modified: Thu, 21 Sep 2023 23:25:18 GMT  
		Size: 45.0 MB (44959147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b767e25b7494c443d7dee268bc45577e90fcb4ece6c6f23c3fc93b7f4f319`  
		Last Modified: Thu, 21 Sep 2023 23:44:42 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e0c37837cfca7152f3fa4b752cc088e69f92e7bd9953229c7344de7335cd4c`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 982.8 KB (982820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f5d3670db7f8c371cd0aa2306cbf90e70e88aefa5a8ad7d15c5f426e69bf62`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 4.6 MB (4620337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c567b29c3ec4335f466d1b027ff9ab6ab1275da314da8eb088c38b2cde8cf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323a74fdf36b1c06cbae2e64fa2c6d3a633da6739719ba5d0a878e4fa0ba1fd3`  
		Last Modified: Thu, 21 Sep 2023 23:45:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130e11b8eb713cacaf4b4f831d9ed4ac7edd02d74651f6646585a942f7da3e3e`  
		Last Modified: Thu, 21 Sep 2023 23:45:22 GMT  
		Size: 58.5 MB (58507528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92f1f2dd77ca35e3916bb1c57301be82b294af74b4d4c9798d339cc8fce7180`  
		Last Modified: Thu, 21 Sep 2023 23:45:14 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c0f03962c9878e744f644fff422ec54b9b24e7e682282accc61a31ff295c33`  
		Last Modified: Thu, 21 Sep 2023 23:45:24 GMT  
		Size: 57.5 MB (57522718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194c2f9ce134d33a9c303f4e3e96d85ec098f9522a4904a46452c8f52bb3545`  
		Last Modified: Thu, 21 Sep 2023 23:45:14 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a235a73ec4d4399d8b105da41e4aabe7be01c39e05cb15792ff00f08c4a0e5f8`  
		Last Modified: Thu, 21 Sep 2023 23:45:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:af8830366f4019e521beb9abd91c416c3d7647fc23d2accaac459075c2963aae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170136425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659ee6cc1dd35b909daead51fbc9010e2252ce16bc260b56b6d709facb844a7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:40:46 GMT
ADD file:c630310324edbc0dd09d0912b8e7074d17ac71b1be8a14af9663872c081c4632 in / 
# Thu, 21 Sep 2023 23:40:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:57:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:57:07 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:57:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:57:34 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:57:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:58:59 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 21 Sep 2023 23:58:59 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:58:59 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:59:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:59:30 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:59:30 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Fri, 22 Sep 2023 00:00:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 22 Sep 2023 00:00:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Sep 2023 00:00:06 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 22 Sep 2023 00:00:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 22 Sep 2023 00:00:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Sep 2023 00:00:06 GMT
EXPOSE 3306 33060
# Fri, 22 Sep 2023 00:00:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:286c1c922769d7608c32cf62931e95d7d169a0306164d24ce7d7a8a065959315`  
		Last Modified: Thu, 21 Sep 2023 23:41:39 GMT  
		Size: 43.7 MB (43657726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2045d234108f24e754e675bd763120bca5713bfbd34f917cef312b16b8eaeb84`  
		Last Modified: Fri, 22 Sep 2023 00:00:26 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e96650b64b585d497570d68ed967ef978298a63dcc9de51061e94b04ef316a`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e078f368c90db174893b4ac4586b3f26efd45a6cb77eb8803ce1d916121d1e37`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 4.3 MB (4307237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e3454b5c5a94b323b466e6bcaecb9d3310c242dd8b2c6880913c2477fbec43`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c69fbea8e7c6c7e9be3c680df3c72949926510f00838b2447d9f6930a03fcb`  
		Last Modified: Fri, 22 Sep 2023 00:01:01 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428eab90a954e02a3ab1ce3bbe2069b5bdf8e026c08708d0382f38e4d546700a`  
		Last Modified: Fri, 22 Sep 2023 00:01:05 GMT  
		Size: 57.5 MB (57472931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3dddc91cd1bf126fadae67b9e071f2b97ed5d405e33beb6d4dae3e640598d0a`  
		Last Modified: Fri, 22 Sep 2023 00:00:59 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91e3764e65379aadf08f4e91723b7a0269b2ea9f6243e5c2ef319f26b6b7e23`  
		Last Modified: Fri, 22 Sep 2023 00:01:07 GMT  
		Size: 63.8 MB (63775860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace219fec8ec8803e87fca2139f3d5afe0cf04cae4b790c21bb7ef9a8ebd4687`  
		Last Modified: Fri, 22 Sep 2023 00:00:59 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec9269f2cec4c9e9a543a9114351089f17bf36a1c49eb476bbfaa1d1e647fc0`  
		Last Modified: Fri, 22 Sep 2023 00:00:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.34`

```console
$ docker pull mysql@sha256:a7a96a9dbf6f310703c4e0c61086b23c5835c33a05544cdc952a7cd0b8feb675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.34` - linux; amd64

```console
$ docker pull mysql@sha256:a0757f07e801b6bc5c56966c516ed61bf19be7587917862d52168be18a57125e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166602229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a53f40065fff68a0d8c9c7f0cd91942184d1607b99bce0b97273283791befaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:24:01 GMT
ADD file:909c07f3bad92a80d3917d583769a01bf62c2cbf3dd24f450fb303b1db92a83e in / 
# Thu, 21 Sep 2023 23:24:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:41:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:41:01 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:41:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:41:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:41:34 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:42:54 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 21 Sep 2023 23:42:55 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:42:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:43:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:43:31 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:43:31 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:44:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:44:12 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:44:12 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:44:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 21 Sep 2023 23:44:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:44:13 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:44:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5262579e8e45cb87fdc8fb6182d30da3c9e4f1036e02223508f287899ea434c0`  
		Last Modified: Thu, 21 Sep 2023 23:25:18 GMT  
		Size: 45.0 MB (44959147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b767e25b7494c443d7dee268bc45577e90fcb4ece6c6f23c3fc93b7f4f319`  
		Last Modified: Thu, 21 Sep 2023 23:44:42 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e0c37837cfca7152f3fa4b752cc088e69f92e7bd9953229c7344de7335cd4c`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 982.8 KB (982820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f5d3670db7f8c371cd0aa2306cbf90e70e88aefa5a8ad7d15c5f426e69bf62`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 4.6 MB (4620337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c567b29c3ec4335f466d1b027ff9ab6ab1275da314da8eb088c38b2cde8cf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323a74fdf36b1c06cbae2e64fa2c6d3a633da6739719ba5d0a878e4fa0ba1fd3`  
		Last Modified: Thu, 21 Sep 2023 23:45:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130e11b8eb713cacaf4b4f831d9ed4ac7edd02d74651f6646585a942f7da3e3e`  
		Last Modified: Thu, 21 Sep 2023 23:45:22 GMT  
		Size: 58.5 MB (58507528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92f1f2dd77ca35e3916bb1c57301be82b294af74b4d4c9798d339cc8fce7180`  
		Last Modified: Thu, 21 Sep 2023 23:45:14 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c0f03962c9878e744f644fff422ec54b9b24e7e682282accc61a31ff295c33`  
		Last Modified: Thu, 21 Sep 2023 23:45:24 GMT  
		Size: 57.5 MB (57522718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194c2f9ce134d33a9c303f4e3e96d85ec098f9522a4904a46452c8f52bb3545`  
		Last Modified: Thu, 21 Sep 2023 23:45:14 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a235a73ec4d4399d8b105da41e4aabe7be01c39e05cb15792ff00f08c4a0e5f8`  
		Last Modified: Thu, 21 Sep 2023 23:45:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.34` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:af8830366f4019e521beb9abd91c416c3d7647fc23d2accaac459075c2963aae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170136425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659ee6cc1dd35b909daead51fbc9010e2252ce16bc260b56b6d709facb844a7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:40:46 GMT
ADD file:c630310324edbc0dd09d0912b8e7074d17ac71b1be8a14af9663872c081c4632 in / 
# Thu, 21 Sep 2023 23:40:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:57:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:57:07 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:57:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:57:34 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:57:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:58:59 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 21 Sep 2023 23:58:59 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:58:59 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:59:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:59:30 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:59:30 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Fri, 22 Sep 2023 00:00:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 22 Sep 2023 00:00:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Sep 2023 00:00:06 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 22 Sep 2023 00:00:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 22 Sep 2023 00:00:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Sep 2023 00:00:06 GMT
EXPOSE 3306 33060
# Fri, 22 Sep 2023 00:00:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:286c1c922769d7608c32cf62931e95d7d169a0306164d24ce7d7a8a065959315`  
		Last Modified: Thu, 21 Sep 2023 23:41:39 GMT  
		Size: 43.7 MB (43657726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2045d234108f24e754e675bd763120bca5713bfbd34f917cef312b16b8eaeb84`  
		Last Modified: Fri, 22 Sep 2023 00:00:26 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e96650b64b585d497570d68ed967ef978298a63dcc9de51061e94b04ef316a`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e078f368c90db174893b4ac4586b3f26efd45a6cb77eb8803ce1d916121d1e37`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 4.3 MB (4307237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e3454b5c5a94b323b466e6bcaecb9d3310c242dd8b2c6880913c2477fbec43`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c69fbea8e7c6c7e9be3c680df3c72949926510f00838b2447d9f6930a03fcb`  
		Last Modified: Fri, 22 Sep 2023 00:01:01 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428eab90a954e02a3ab1ce3bbe2069b5bdf8e026c08708d0382f38e4d546700a`  
		Last Modified: Fri, 22 Sep 2023 00:01:05 GMT  
		Size: 57.5 MB (57472931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3dddc91cd1bf126fadae67b9e071f2b97ed5d405e33beb6d4dae3e640598d0a`  
		Last Modified: Fri, 22 Sep 2023 00:00:59 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91e3764e65379aadf08f4e91723b7a0269b2ea9f6243e5c2ef319f26b6b7e23`  
		Last Modified: Fri, 22 Sep 2023 00:01:07 GMT  
		Size: 63.8 MB (63775860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace219fec8ec8803e87fca2139f3d5afe0cf04cae4b790c21bb7ef9a8ebd4687`  
		Last Modified: Fri, 22 Sep 2023 00:00:59 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec9269f2cec4c9e9a543a9114351089f17bf36a1c49eb476bbfaa1d1e647fc0`  
		Last Modified: Fri, 22 Sep 2023 00:00:59 GMT  
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
$ docker pull mysql@sha256:a7a96a9dbf6f310703c4e0c61086b23c5835c33a05544cdc952a7cd0b8feb675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.34-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a0757f07e801b6bc5c56966c516ed61bf19be7587917862d52168be18a57125e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166602229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a53f40065fff68a0d8c9c7f0cd91942184d1607b99bce0b97273283791befaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:24:01 GMT
ADD file:909c07f3bad92a80d3917d583769a01bf62c2cbf3dd24f450fb303b1db92a83e in / 
# Thu, 21 Sep 2023 23:24:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:41:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:41:01 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:41:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:41:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:41:34 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:42:54 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 21 Sep 2023 23:42:55 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:42:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:43:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:43:31 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:43:31 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:44:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:44:12 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:44:12 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:44:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 21 Sep 2023 23:44:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:44:13 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:44:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5262579e8e45cb87fdc8fb6182d30da3c9e4f1036e02223508f287899ea434c0`  
		Last Modified: Thu, 21 Sep 2023 23:25:18 GMT  
		Size: 45.0 MB (44959147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b767e25b7494c443d7dee268bc45577e90fcb4ece6c6f23c3fc93b7f4f319`  
		Last Modified: Thu, 21 Sep 2023 23:44:42 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e0c37837cfca7152f3fa4b752cc088e69f92e7bd9953229c7344de7335cd4c`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 982.8 KB (982820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f5d3670db7f8c371cd0aa2306cbf90e70e88aefa5a8ad7d15c5f426e69bf62`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 4.6 MB (4620337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c567b29c3ec4335f466d1b027ff9ab6ab1275da314da8eb088c38b2cde8cf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323a74fdf36b1c06cbae2e64fa2c6d3a633da6739719ba5d0a878e4fa0ba1fd3`  
		Last Modified: Thu, 21 Sep 2023 23:45:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130e11b8eb713cacaf4b4f831d9ed4ac7edd02d74651f6646585a942f7da3e3e`  
		Last Modified: Thu, 21 Sep 2023 23:45:22 GMT  
		Size: 58.5 MB (58507528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92f1f2dd77ca35e3916bb1c57301be82b294af74b4d4c9798d339cc8fce7180`  
		Last Modified: Thu, 21 Sep 2023 23:45:14 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c0f03962c9878e744f644fff422ec54b9b24e7e682282accc61a31ff295c33`  
		Last Modified: Thu, 21 Sep 2023 23:45:24 GMT  
		Size: 57.5 MB (57522718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194c2f9ce134d33a9c303f4e3e96d85ec098f9522a4904a46452c8f52bb3545`  
		Last Modified: Thu, 21 Sep 2023 23:45:14 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a235a73ec4d4399d8b105da41e4aabe7be01c39e05cb15792ff00f08c4a0e5f8`  
		Last Modified: Thu, 21 Sep 2023 23:45:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.34-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:af8830366f4019e521beb9abd91c416c3d7647fc23d2accaac459075c2963aae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170136425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659ee6cc1dd35b909daead51fbc9010e2252ce16bc260b56b6d709facb844a7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:40:46 GMT
ADD file:c630310324edbc0dd09d0912b8e7074d17ac71b1be8a14af9663872c081c4632 in / 
# Thu, 21 Sep 2023 23:40:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:57:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:57:07 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:57:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:57:34 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:57:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:58:59 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 21 Sep 2023 23:58:59 GMT
ENV MYSQL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:58:59 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:59:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:59:30 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:59:30 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Fri, 22 Sep 2023 00:00:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 22 Sep 2023 00:00:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 22 Sep 2023 00:00:06 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 22 Sep 2023 00:00:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 22 Sep 2023 00:00:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Sep 2023 00:00:06 GMT
EXPOSE 3306 33060
# Fri, 22 Sep 2023 00:00:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:286c1c922769d7608c32cf62931e95d7d169a0306164d24ce7d7a8a065959315`  
		Last Modified: Thu, 21 Sep 2023 23:41:39 GMT  
		Size: 43.7 MB (43657726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2045d234108f24e754e675bd763120bca5713bfbd34f917cef312b16b8eaeb84`  
		Last Modified: Fri, 22 Sep 2023 00:00:26 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e96650b64b585d497570d68ed967ef978298a63dcc9de51061e94b04ef316a`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e078f368c90db174893b4ac4586b3f26efd45a6cb77eb8803ce1d916121d1e37`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 4.3 MB (4307237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e3454b5c5a94b323b466e6bcaecb9d3310c242dd8b2c6880913c2477fbec43`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c69fbea8e7c6c7e9be3c680df3c72949926510f00838b2447d9f6930a03fcb`  
		Last Modified: Fri, 22 Sep 2023 00:01:01 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428eab90a954e02a3ab1ce3bbe2069b5bdf8e026c08708d0382f38e4d546700a`  
		Last Modified: Fri, 22 Sep 2023 00:01:05 GMT  
		Size: 57.5 MB (57472931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3dddc91cd1bf126fadae67b9e071f2b97ed5d405e33beb6d4dae3e640598d0a`  
		Last Modified: Fri, 22 Sep 2023 00:00:59 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91e3764e65379aadf08f4e91723b7a0269b2ea9f6243e5c2ef319f26b6b7e23`  
		Last Modified: Fri, 22 Sep 2023 00:01:07 GMT  
		Size: 63.8 MB (63775860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace219fec8ec8803e87fca2139f3d5afe0cf04cae4b790c21bb7ef9a8ebd4687`  
		Last Modified: Fri, 22 Sep 2023 00:00:59 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec9269f2cec4c9e9a543a9114351089f17bf36a1c49eb476bbfaa1d1e647fc0`  
		Last Modified: Fri, 22 Sep 2023 00:00:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.1`

```console
$ docker pull mysql@sha256:566007208a3f1cc8f9df6b767665b5c9b800fc4fb5f863d17aa1df362880ed04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.1` - linux; amd64

```console
$ docker pull mysql@sha256:fa3d07406ef9c95681e6a95c5abc036355c5e3ac20abfb37865ccc3539e4bd50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166876333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2013ac9910129ded1da4c96495142b2ed0638ddf7e86e65156400d9a8503777`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:24:01 GMT
ADD file:909c07f3bad92a80d3917d583769a01bf62c2cbf3dd24f450fb303b1db92a83e in / 
# Thu, 21 Sep 2023 23:24:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:41:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:41:01 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:41:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:41:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:41:34 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:41:34 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 21 Sep 2023 23:41:34 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 21 Sep 2023 23:41:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:42:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:42:10 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:42:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:42:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:42:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:42:51 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:42:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:42:51 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:42:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5262579e8e45cb87fdc8fb6182d30da3c9e4f1036e02223508f287899ea434c0`  
		Last Modified: Thu, 21 Sep 2023 23:25:18 GMT  
		Size: 45.0 MB (44959147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b767e25b7494c443d7dee268bc45577e90fcb4ece6c6f23c3fc93b7f4f319`  
		Last Modified: Thu, 21 Sep 2023 23:44:42 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e0c37837cfca7152f3fa4b752cc088e69f92e7bd9953229c7344de7335cd4c`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 982.8 KB (982820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f5d3670db7f8c371cd0aa2306cbf90e70e88aefa5a8ad7d15c5f426e69bf62`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 4.6 MB (4620337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c567b29c3ec4335f466d1b027ff9ab6ab1275da314da8eb088c38b2cde8cf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6effcc6561c9792f2e42dcee38c1b79c50d573dfae21a4c15d56cdf116b3faf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1493d45d9c24bf2946229eb3808d5603ad083f49ed16edab012e849485040f`  
		Last Modified: Thu, 21 Sep 2023 23:44:47 GMT  
		Size: 58.8 MB (58777440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7101609fa7d97ae2dabcc48d18271b8013cd59fd2cb18646cd8e5269d6a2b644`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a1261dc2ab100e2f5cd2582a00da9c7c03d56dcd7524c3e32103975617b8a`  
		Last Modified: Thu, 21 Sep 2023 23:44:48 GMT  
		Size: 57.5 MB (57527025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865a24d6d1f28b65e14fdcc535e8a07e6214872929f0b3647ef860c098c92f77`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.1` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c0f7818fc533e4dfb17cdbfb8a1832d03f15c4acededcc4fbe67435b8b893541
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170377422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3503aa5f07519bad58f17ca0bc9b3ae21a66133942fbd915936c60d336a6142e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:40:46 GMT
ADD file:c630310324edbc0dd09d0912b8e7074d17ac71b1be8a14af9663872c081c4632 in / 
# Thu, 21 Sep 2023 23:40:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:57:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:57:07 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:57:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:57:34 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:57:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:57:35 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 21 Sep 2023 23:57:35 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 21 Sep 2023 23:57:36 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:58:06 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:58:08 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:58:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:58:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:58:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:58:44 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:58:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:58:45 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:58:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:286c1c922769d7608c32cf62931e95d7d169a0306164d24ce7d7a8a065959315`  
		Last Modified: Thu, 21 Sep 2023 23:41:39 GMT  
		Size: 43.7 MB (43657726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2045d234108f24e754e675bd763120bca5713bfbd34f917cef312b16b8eaeb84`  
		Last Modified: Fri, 22 Sep 2023 00:00:26 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e96650b64b585d497570d68ed967ef978298a63dcc9de51061e94b04ef316a`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e078f368c90db174893b4ac4586b3f26efd45a6cb77eb8803ce1d916121d1e37`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 4.3 MB (4307237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e3454b5c5a94b323b466e6bcaecb9d3310c242dd8b2c6880913c2477fbec43`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2babac95cc038ef3da37b9e01cf3d22d2ef66a1d4353f0bc2969d38b858ce9a1`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa3f01ac3f924ae70b2fc8bb2f909031a6ab25a7922183d5682c7d9fb531dfd`  
		Last Modified: Fri, 22 Sep 2023 00:00:28 GMT  
		Size: 57.7 MB (57712118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69a1f6641e4c90e2761fd42f3bad7499bcff043b48bccdcdb1925688c8a6e6`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 322.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc7d63c8a6ff2afcbc55a78186f338dfcb811708e4bf65c7e1a33b51c28c230`  
		Last Modified: Fri, 22 Sep 2023 00:00:30 GMT  
		Size: 63.8 MB (63777776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc23fd020fd3056f91c4a5f48dc80801ef0614d428304b8712b64bf7424fd84a`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.1-oracle`

```console
$ docker pull mysql@sha256:566007208a3f1cc8f9df6b767665b5c9b800fc4fb5f863d17aa1df362880ed04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.1-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:fa3d07406ef9c95681e6a95c5abc036355c5e3ac20abfb37865ccc3539e4bd50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166876333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2013ac9910129ded1da4c96495142b2ed0638ddf7e86e65156400d9a8503777`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:24:01 GMT
ADD file:909c07f3bad92a80d3917d583769a01bf62c2cbf3dd24f450fb303b1db92a83e in / 
# Thu, 21 Sep 2023 23:24:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:41:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:41:01 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:41:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:41:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:41:34 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:41:34 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 21 Sep 2023 23:41:34 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 21 Sep 2023 23:41:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:42:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:42:10 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:42:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:42:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:42:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:42:51 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:42:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:42:51 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:42:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5262579e8e45cb87fdc8fb6182d30da3c9e4f1036e02223508f287899ea434c0`  
		Last Modified: Thu, 21 Sep 2023 23:25:18 GMT  
		Size: 45.0 MB (44959147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b767e25b7494c443d7dee268bc45577e90fcb4ece6c6f23c3fc93b7f4f319`  
		Last Modified: Thu, 21 Sep 2023 23:44:42 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e0c37837cfca7152f3fa4b752cc088e69f92e7bd9953229c7344de7335cd4c`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 982.8 KB (982820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f5d3670db7f8c371cd0aa2306cbf90e70e88aefa5a8ad7d15c5f426e69bf62`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 4.6 MB (4620337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c567b29c3ec4335f466d1b027ff9ab6ab1275da314da8eb088c38b2cde8cf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6effcc6561c9792f2e42dcee38c1b79c50d573dfae21a4c15d56cdf116b3faf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1493d45d9c24bf2946229eb3808d5603ad083f49ed16edab012e849485040f`  
		Last Modified: Thu, 21 Sep 2023 23:44:47 GMT  
		Size: 58.8 MB (58777440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7101609fa7d97ae2dabcc48d18271b8013cd59fd2cb18646cd8e5269d6a2b644`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a1261dc2ab100e2f5cd2582a00da9c7c03d56dcd7524c3e32103975617b8a`  
		Last Modified: Thu, 21 Sep 2023 23:44:48 GMT  
		Size: 57.5 MB (57527025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865a24d6d1f28b65e14fdcc535e8a07e6214872929f0b3647ef860c098c92f77`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.1-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c0f7818fc533e4dfb17cdbfb8a1832d03f15c4acededcc4fbe67435b8b893541
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170377422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3503aa5f07519bad58f17ca0bc9b3ae21a66133942fbd915936c60d336a6142e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:40:46 GMT
ADD file:c630310324edbc0dd09d0912b8e7074d17ac71b1be8a14af9663872c081c4632 in / 
# Thu, 21 Sep 2023 23:40:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:57:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:57:07 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:57:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:57:34 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:57:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:57:35 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 21 Sep 2023 23:57:35 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 21 Sep 2023 23:57:36 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:58:06 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:58:08 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:58:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:58:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:58:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:58:44 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:58:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:58:45 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:58:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:286c1c922769d7608c32cf62931e95d7d169a0306164d24ce7d7a8a065959315`  
		Last Modified: Thu, 21 Sep 2023 23:41:39 GMT  
		Size: 43.7 MB (43657726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2045d234108f24e754e675bd763120bca5713bfbd34f917cef312b16b8eaeb84`  
		Last Modified: Fri, 22 Sep 2023 00:00:26 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e96650b64b585d497570d68ed967ef978298a63dcc9de51061e94b04ef316a`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e078f368c90db174893b4ac4586b3f26efd45a6cb77eb8803ce1d916121d1e37`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 4.3 MB (4307237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e3454b5c5a94b323b466e6bcaecb9d3310c242dd8b2c6880913c2477fbec43`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2babac95cc038ef3da37b9e01cf3d22d2ef66a1d4353f0bc2969d38b858ce9a1`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa3f01ac3f924ae70b2fc8bb2f909031a6ab25a7922183d5682c7d9fb531dfd`  
		Last Modified: Fri, 22 Sep 2023 00:00:28 GMT  
		Size: 57.7 MB (57712118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69a1f6641e4c90e2761fd42f3bad7499bcff043b48bccdcdb1925688c8a6e6`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 322.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc7d63c8a6ff2afcbc55a78186f338dfcb811708e4bf65c7e1a33b51c28c230`  
		Last Modified: Fri, 22 Sep 2023 00:00:30 GMT  
		Size: 63.8 MB (63777776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc23fd020fd3056f91c4a5f48dc80801ef0614d428304b8712b64bf7424fd84a`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.1.0`

```console
$ docker pull mysql@sha256:566007208a3f1cc8f9df6b767665b5c9b800fc4fb5f863d17aa1df362880ed04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.1.0` - linux; amd64

```console
$ docker pull mysql@sha256:fa3d07406ef9c95681e6a95c5abc036355c5e3ac20abfb37865ccc3539e4bd50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166876333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2013ac9910129ded1da4c96495142b2ed0638ddf7e86e65156400d9a8503777`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:24:01 GMT
ADD file:909c07f3bad92a80d3917d583769a01bf62c2cbf3dd24f450fb303b1db92a83e in / 
# Thu, 21 Sep 2023 23:24:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:41:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:41:01 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:41:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:41:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:41:34 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:41:34 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 21 Sep 2023 23:41:34 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 21 Sep 2023 23:41:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:42:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:42:10 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:42:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:42:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:42:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:42:51 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:42:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:42:51 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:42:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5262579e8e45cb87fdc8fb6182d30da3c9e4f1036e02223508f287899ea434c0`  
		Last Modified: Thu, 21 Sep 2023 23:25:18 GMT  
		Size: 45.0 MB (44959147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b767e25b7494c443d7dee268bc45577e90fcb4ece6c6f23c3fc93b7f4f319`  
		Last Modified: Thu, 21 Sep 2023 23:44:42 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e0c37837cfca7152f3fa4b752cc088e69f92e7bd9953229c7344de7335cd4c`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 982.8 KB (982820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f5d3670db7f8c371cd0aa2306cbf90e70e88aefa5a8ad7d15c5f426e69bf62`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 4.6 MB (4620337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c567b29c3ec4335f466d1b027ff9ab6ab1275da314da8eb088c38b2cde8cf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6effcc6561c9792f2e42dcee38c1b79c50d573dfae21a4c15d56cdf116b3faf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1493d45d9c24bf2946229eb3808d5603ad083f49ed16edab012e849485040f`  
		Last Modified: Thu, 21 Sep 2023 23:44:47 GMT  
		Size: 58.8 MB (58777440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7101609fa7d97ae2dabcc48d18271b8013cd59fd2cb18646cd8e5269d6a2b644`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a1261dc2ab100e2f5cd2582a00da9c7c03d56dcd7524c3e32103975617b8a`  
		Last Modified: Thu, 21 Sep 2023 23:44:48 GMT  
		Size: 57.5 MB (57527025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865a24d6d1f28b65e14fdcc535e8a07e6214872929f0b3647ef860c098c92f77`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.1.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c0f7818fc533e4dfb17cdbfb8a1832d03f15c4acededcc4fbe67435b8b893541
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170377422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3503aa5f07519bad58f17ca0bc9b3ae21a66133942fbd915936c60d336a6142e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:40:46 GMT
ADD file:c630310324edbc0dd09d0912b8e7074d17ac71b1be8a14af9663872c081c4632 in / 
# Thu, 21 Sep 2023 23:40:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:57:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:57:07 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:57:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:57:34 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:57:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:57:35 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 21 Sep 2023 23:57:35 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 21 Sep 2023 23:57:36 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:58:06 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:58:08 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:58:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:58:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:58:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:58:44 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:58:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:58:45 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:58:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:286c1c922769d7608c32cf62931e95d7d169a0306164d24ce7d7a8a065959315`  
		Last Modified: Thu, 21 Sep 2023 23:41:39 GMT  
		Size: 43.7 MB (43657726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2045d234108f24e754e675bd763120bca5713bfbd34f917cef312b16b8eaeb84`  
		Last Modified: Fri, 22 Sep 2023 00:00:26 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e96650b64b585d497570d68ed967ef978298a63dcc9de51061e94b04ef316a`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e078f368c90db174893b4ac4586b3f26efd45a6cb77eb8803ce1d916121d1e37`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 4.3 MB (4307237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e3454b5c5a94b323b466e6bcaecb9d3310c242dd8b2c6880913c2477fbec43`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2babac95cc038ef3da37b9e01cf3d22d2ef66a1d4353f0bc2969d38b858ce9a1`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa3f01ac3f924ae70b2fc8bb2f909031a6ab25a7922183d5682c7d9fb531dfd`  
		Last Modified: Fri, 22 Sep 2023 00:00:28 GMT  
		Size: 57.7 MB (57712118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69a1f6641e4c90e2761fd42f3bad7499bcff043b48bccdcdb1925688c8a6e6`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 322.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc7d63c8a6ff2afcbc55a78186f338dfcb811708e4bf65c7e1a33b51c28c230`  
		Last Modified: Fri, 22 Sep 2023 00:00:30 GMT  
		Size: 63.8 MB (63777776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc23fd020fd3056f91c4a5f48dc80801ef0614d428304b8712b64bf7424fd84a`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.1.0-oracle`

```console
$ docker pull mysql@sha256:566007208a3f1cc8f9df6b767665b5c9b800fc4fb5f863d17aa1df362880ed04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.1.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:fa3d07406ef9c95681e6a95c5abc036355c5e3ac20abfb37865ccc3539e4bd50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166876333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2013ac9910129ded1da4c96495142b2ed0638ddf7e86e65156400d9a8503777`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:24:01 GMT
ADD file:909c07f3bad92a80d3917d583769a01bf62c2cbf3dd24f450fb303b1db92a83e in / 
# Thu, 21 Sep 2023 23:24:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:41:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:41:01 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:41:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:41:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:41:34 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:41:34 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 21 Sep 2023 23:41:34 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 21 Sep 2023 23:41:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:42:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:42:10 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:42:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:42:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:42:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:42:51 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:42:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:42:51 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:42:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5262579e8e45cb87fdc8fb6182d30da3c9e4f1036e02223508f287899ea434c0`  
		Last Modified: Thu, 21 Sep 2023 23:25:18 GMT  
		Size: 45.0 MB (44959147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b767e25b7494c443d7dee268bc45577e90fcb4ece6c6f23c3fc93b7f4f319`  
		Last Modified: Thu, 21 Sep 2023 23:44:42 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e0c37837cfca7152f3fa4b752cc088e69f92e7bd9953229c7344de7335cd4c`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 982.8 KB (982820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f5d3670db7f8c371cd0aa2306cbf90e70e88aefa5a8ad7d15c5f426e69bf62`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 4.6 MB (4620337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c567b29c3ec4335f466d1b027ff9ab6ab1275da314da8eb088c38b2cde8cf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6effcc6561c9792f2e42dcee38c1b79c50d573dfae21a4c15d56cdf116b3faf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1493d45d9c24bf2946229eb3808d5603ad083f49ed16edab012e849485040f`  
		Last Modified: Thu, 21 Sep 2023 23:44:47 GMT  
		Size: 58.8 MB (58777440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7101609fa7d97ae2dabcc48d18271b8013cd59fd2cb18646cd8e5269d6a2b644`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a1261dc2ab100e2f5cd2582a00da9c7c03d56dcd7524c3e32103975617b8a`  
		Last Modified: Thu, 21 Sep 2023 23:44:48 GMT  
		Size: 57.5 MB (57527025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865a24d6d1f28b65e14fdcc535e8a07e6214872929f0b3647ef860c098c92f77`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.1.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c0f7818fc533e4dfb17cdbfb8a1832d03f15c4acededcc4fbe67435b8b893541
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170377422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3503aa5f07519bad58f17ca0bc9b3ae21a66133942fbd915936c60d336a6142e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:40:46 GMT
ADD file:c630310324edbc0dd09d0912b8e7074d17ac71b1be8a14af9663872c081c4632 in / 
# Thu, 21 Sep 2023 23:40:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:57:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:57:07 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:57:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:57:34 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:57:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:57:35 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 21 Sep 2023 23:57:35 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 21 Sep 2023 23:57:36 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:58:06 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:58:08 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:58:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:58:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:58:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:58:44 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:58:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:58:45 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:58:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:286c1c922769d7608c32cf62931e95d7d169a0306164d24ce7d7a8a065959315`  
		Last Modified: Thu, 21 Sep 2023 23:41:39 GMT  
		Size: 43.7 MB (43657726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2045d234108f24e754e675bd763120bca5713bfbd34f917cef312b16b8eaeb84`  
		Last Modified: Fri, 22 Sep 2023 00:00:26 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e96650b64b585d497570d68ed967ef978298a63dcc9de51061e94b04ef316a`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e078f368c90db174893b4ac4586b3f26efd45a6cb77eb8803ce1d916121d1e37`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 4.3 MB (4307237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e3454b5c5a94b323b466e6bcaecb9d3310c242dd8b2c6880913c2477fbec43`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2babac95cc038ef3da37b9e01cf3d22d2ef66a1d4353f0bc2969d38b858ce9a1`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa3f01ac3f924ae70b2fc8bb2f909031a6ab25a7922183d5682c7d9fb531dfd`  
		Last Modified: Fri, 22 Sep 2023 00:00:28 GMT  
		Size: 57.7 MB (57712118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69a1f6641e4c90e2761fd42f3bad7499bcff043b48bccdcdb1925688c8a6e6`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 322.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc7d63c8a6ff2afcbc55a78186f338dfcb811708e4bf65c7e1a33b51c28c230`  
		Last Modified: Fri, 22 Sep 2023 00:00:30 GMT  
		Size: 63.8 MB (63777776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc23fd020fd3056f91c4a5f48dc80801ef0614d428304b8712b64bf7424fd84a`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:innovation`

```console
$ docker pull mysql@sha256:566007208a3f1cc8f9df6b767665b5c9b800fc4fb5f863d17aa1df362880ed04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:fa3d07406ef9c95681e6a95c5abc036355c5e3ac20abfb37865ccc3539e4bd50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166876333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2013ac9910129ded1da4c96495142b2ed0638ddf7e86e65156400d9a8503777`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:24:01 GMT
ADD file:909c07f3bad92a80d3917d583769a01bf62c2cbf3dd24f450fb303b1db92a83e in / 
# Thu, 21 Sep 2023 23:24:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:41:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:41:01 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:41:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:41:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:41:34 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:41:34 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 21 Sep 2023 23:41:34 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 21 Sep 2023 23:41:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:42:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:42:10 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:42:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:42:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:42:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:42:51 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:42:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:42:51 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:42:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5262579e8e45cb87fdc8fb6182d30da3c9e4f1036e02223508f287899ea434c0`  
		Last Modified: Thu, 21 Sep 2023 23:25:18 GMT  
		Size: 45.0 MB (44959147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b767e25b7494c443d7dee268bc45577e90fcb4ece6c6f23c3fc93b7f4f319`  
		Last Modified: Thu, 21 Sep 2023 23:44:42 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e0c37837cfca7152f3fa4b752cc088e69f92e7bd9953229c7344de7335cd4c`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 982.8 KB (982820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f5d3670db7f8c371cd0aa2306cbf90e70e88aefa5a8ad7d15c5f426e69bf62`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 4.6 MB (4620337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c567b29c3ec4335f466d1b027ff9ab6ab1275da314da8eb088c38b2cde8cf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6effcc6561c9792f2e42dcee38c1b79c50d573dfae21a4c15d56cdf116b3faf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1493d45d9c24bf2946229eb3808d5603ad083f49ed16edab012e849485040f`  
		Last Modified: Thu, 21 Sep 2023 23:44:47 GMT  
		Size: 58.8 MB (58777440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7101609fa7d97ae2dabcc48d18271b8013cd59fd2cb18646cd8e5269d6a2b644`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a1261dc2ab100e2f5cd2582a00da9c7c03d56dcd7524c3e32103975617b8a`  
		Last Modified: Thu, 21 Sep 2023 23:44:48 GMT  
		Size: 57.5 MB (57527025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865a24d6d1f28b65e14fdcc535e8a07e6214872929f0b3647ef860c098c92f77`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c0f7818fc533e4dfb17cdbfb8a1832d03f15c4acededcc4fbe67435b8b893541
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170377422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3503aa5f07519bad58f17ca0bc9b3ae21a66133942fbd915936c60d336a6142e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:40:46 GMT
ADD file:c630310324edbc0dd09d0912b8e7074d17ac71b1be8a14af9663872c081c4632 in / 
# Thu, 21 Sep 2023 23:40:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:57:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:57:07 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:57:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:57:34 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:57:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:57:35 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 21 Sep 2023 23:57:35 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 21 Sep 2023 23:57:36 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:58:06 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:58:08 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:58:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:58:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:58:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:58:44 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:58:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:58:45 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:58:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:286c1c922769d7608c32cf62931e95d7d169a0306164d24ce7d7a8a065959315`  
		Last Modified: Thu, 21 Sep 2023 23:41:39 GMT  
		Size: 43.7 MB (43657726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2045d234108f24e754e675bd763120bca5713bfbd34f917cef312b16b8eaeb84`  
		Last Modified: Fri, 22 Sep 2023 00:00:26 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e96650b64b585d497570d68ed967ef978298a63dcc9de51061e94b04ef316a`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e078f368c90db174893b4ac4586b3f26efd45a6cb77eb8803ce1d916121d1e37`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 4.3 MB (4307237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e3454b5c5a94b323b466e6bcaecb9d3310c242dd8b2c6880913c2477fbec43`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2babac95cc038ef3da37b9e01cf3d22d2ef66a1d4353f0bc2969d38b858ce9a1`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa3f01ac3f924ae70b2fc8bb2f909031a6ab25a7922183d5682c7d9fb531dfd`  
		Last Modified: Fri, 22 Sep 2023 00:00:28 GMT  
		Size: 57.7 MB (57712118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69a1f6641e4c90e2761fd42f3bad7499bcff043b48bccdcdb1925688c8a6e6`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 322.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc7d63c8a6ff2afcbc55a78186f338dfcb811708e4bf65c7e1a33b51c28c230`  
		Last Modified: Fri, 22 Sep 2023 00:00:30 GMT  
		Size: 63.8 MB (63777776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc23fd020fd3056f91c4a5f48dc80801ef0614d428304b8712b64bf7424fd84a`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:566007208a3f1cc8f9df6b767665b5c9b800fc4fb5f863d17aa1df362880ed04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:fa3d07406ef9c95681e6a95c5abc036355c5e3ac20abfb37865ccc3539e4bd50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166876333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2013ac9910129ded1da4c96495142b2ed0638ddf7e86e65156400d9a8503777`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:24:01 GMT
ADD file:909c07f3bad92a80d3917d583769a01bf62c2cbf3dd24f450fb303b1db92a83e in / 
# Thu, 21 Sep 2023 23:24:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:41:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:41:01 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:41:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:41:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:41:34 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:41:34 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 21 Sep 2023 23:41:34 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 21 Sep 2023 23:41:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:42:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:42:10 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:42:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:42:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:42:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:42:51 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:42:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:42:51 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:42:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5262579e8e45cb87fdc8fb6182d30da3c9e4f1036e02223508f287899ea434c0`  
		Last Modified: Thu, 21 Sep 2023 23:25:18 GMT  
		Size: 45.0 MB (44959147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b767e25b7494c443d7dee268bc45577e90fcb4ece6c6f23c3fc93b7f4f319`  
		Last Modified: Thu, 21 Sep 2023 23:44:42 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e0c37837cfca7152f3fa4b752cc088e69f92e7bd9953229c7344de7335cd4c`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 982.8 KB (982820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f5d3670db7f8c371cd0aa2306cbf90e70e88aefa5a8ad7d15c5f426e69bf62`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 4.6 MB (4620337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c567b29c3ec4335f466d1b027ff9ab6ab1275da314da8eb088c38b2cde8cf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6effcc6561c9792f2e42dcee38c1b79c50d573dfae21a4c15d56cdf116b3faf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1493d45d9c24bf2946229eb3808d5603ad083f49ed16edab012e849485040f`  
		Last Modified: Thu, 21 Sep 2023 23:44:47 GMT  
		Size: 58.8 MB (58777440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7101609fa7d97ae2dabcc48d18271b8013cd59fd2cb18646cd8e5269d6a2b644`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a1261dc2ab100e2f5cd2582a00da9c7c03d56dcd7524c3e32103975617b8a`  
		Last Modified: Thu, 21 Sep 2023 23:44:48 GMT  
		Size: 57.5 MB (57527025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865a24d6d1f28b65e14fdcc535e8a07e6214872929f0b3647ef860c098c92f77`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c0f7818fc533e4dfb17cdbfb8a1832d03f15c4acededcc4fbe67435b8b893541
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170377422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3503aa5f07519bad58f17ca0bc9b3ae21a66133942fbd915936c60d336a6142e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:40:46 GMT
ADD file:c630310324edbc0dd09d0912b8e7074d17ac71b1be8a14af9663872c081c4632 in / 
# Thu, 21 Sep 2023 23:40:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:57:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:57:07 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:57:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:57:34 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:57:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:57:35 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 21 Sep 2023 23:57:35 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 21 Sep 2023 23:57:36 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:58:06 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:58:08 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:58:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:58:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:58:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:58:44 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:58:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:58:45 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:58:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:286c1c922769d7608c32cf62931e95d7d169a0306164d24ce7d7a8a065959315`  
		Last Modified: Thu, 21 Sep 2023 23:41:39 GMT  
		Size: 43.7 MB (43657726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2045d234108f24e754e675bd763120bca5713bfbd34f917cef312b16b8eaeb84`  
		Last Modified: Fri, 22 Sep 2023 00:00:26 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e96650b64b585d497570d68ed967ef978298a63dcc9de51061e94b04ef316a`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e078f368c90db174893b4ac4586b3f26efd45a6cb77eb8803ce1d916121d1e37`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 4.3 MB (4307237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e3454b5c5a94b323b466e6bcaecb9d3310c242dd8b2c6880913c2477fbec43`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2babac95cc038ef3da37b9e01cf3d22d2ef66a1d4353f0bc2969d38b858ce9a1`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa3f01ac3f924ae70b2fc8bb2f909031a6ab25a7922183d5682c7d9fb531dfd`  
		Last Modified: Fri, 22 Sep 2023 00:00:28 GMT  
		Size: 57.7 MB (57712118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69a1f6641e4c90e2761fd42f3bad7499bcff043b48bccdcdb1925688c8a6e6`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 322.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc7d63c8a6ff2afcbc55a78186f338dfcb811708e4bf65c7e1a33b51c28c230`  
		Last Modified: Fri, 22 Sep 2023 00:00:30 GMT  
		Size: 63.8 MB (63777776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc23fd020fd3056f91c4a5f48dc80801ef0614d428304b8712b64bf7424fd84a`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:566007208a3f1cc8f9df6b767665b5c9b800fc4fb5f863d17aa1df362880ed04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:fa3d07406ef9c95681e6a95c5abc036355c5e3ac20abfb37865ccc3539e4bd50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166876333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2013ac9910129ded1da4c96495142b2ed0638ddf7e86e65156400d9a8503777`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:24:01 GMT
ADD file:909c07f3bad92a80d3917d583769a01bf62c2cbf3dd24f450fb303b1db92a83e in / 
# Thu, 21 Sep 2023 23:24:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:41:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:41:01 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:41:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:41:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:41:34 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:41:34 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 21 Sep 2023 23:41:34 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 21 Sep 2023 23:41:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:42:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:42:10 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:42:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:42:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:42:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:42:51 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:42:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:42:51 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:42:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5262579e8e45cb87fdc8fb6182d30da3c9e4f1036e02223508f287899ea434c0`  
		Last Modified: Thu, 21 Sep 2023 23:25:18 GMT  
		Size: 45.0 MB (44959147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b767e25b7494c443d7dee268bc45577e90fcb4ece6c6f23c3fc93b7f4f319`  
		Last Modified: Thu, 21 Sep 2023 23:44:42 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e0c37837cfca7152f3fa4b752cc088e69f92e7bd9953229c7344de7335cd4c`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 982.8 KB (982820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f5d3670db7f8c371cd0aa2306cbf90e70e88aefa5a8ad7d15c5f426e69bf62`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 4.6 MB (4620337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c567b29c3ec4335f466d1b027ff9ab6ab1275da314da8eb088c38b2cde8cf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6effcc6561c9792f2e42dcee38c1b79c50d573dfae21a4c15d56cdf116b3faf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1493d45d9c24bf2946229eb3808d5603ad083f49ed16edab012e849485040f`  
		Last Modified: Thu, 21 Sep 2023 23:44:47 GMT  
		Size: 58.8 MB (58777440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7101609fa7d97ae2dabcc48d18271b8013cd59fd2cb18646cd8e5269d6a2b644`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a1261dc2ab100e2f5cd2582a00da9c7c03d56dcd7524c3e32103975617b8a`  
		Last Modified: Thu, 21 Sep 2023 23:44:48 GMT  
		Size: 57.5 MB (57527025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865a24d6d1f28b65e14fdcc535e8a07e6214872929f0b3647ef860c098c92f77`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c0f7818fc533e4dfb17cdbfb8a1832d03f15c4acededcc4fbe67435b8b893541
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170377422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3503aa5f07519bad58f17ca0bc9b3ae21a66133942fbd915936c60d336a6142e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:40:46 GMT
ADD file:c630310324edbc0dd09d0912b8e7074d17ac71b1be8a14af9663872c081c4632 in / 
# Thu, 21 Sep 2023 23:40:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:57:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:57:07 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:57:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:57:34 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:57:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:57:35 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 21 Sep 2023 23:57:35 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 21 Sep 2023 23:57:36 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:58:06 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:58:08 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:58:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:58:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:58:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:58:44 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:58:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:58:45 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:58:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:286c1c922769d7608c32cf62931e95d7d169a0306164d24ce7d7a8a065959315`  
		Last Modified: Thu, 21 Sep 2023 23:41:39 GMT  
		Size: 43.7 MB (43657726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2045d234108f24e754e675bd763120bca5713bfbd34f917cef312b16b8eaeb84`  
		Last Modified: Fri, 22 Sep 2023 00:00:26 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e96650b64b585d497570d68ed967ef978298a63dcc9de51061e94b04ef316a`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e078f368c90db174893b4ac4586b3f26efd45a6cb77eb8803ce1d916121d1e37`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 4.3 MB (4307237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e3454b5c5a94b323b466e6bcaecb9d3310c242dd8b2c6880913c2477fbec43`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2babac95cc038ef3da37b9e01cf3d22d2ef66a1d4353f0bc2969d38b858ce9a1`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa3f01ac3f924ae70b2fc8bb2f909031a6ab25a7922183d5682c7d9fb531dfd`  
		Last Modified: Fri, 22 Sep 2023 00:00:28 GMT  
		Size: 57.7 MB (57712118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69a1f6641e4c90e2761fd42f3bad7499bcff043b48bccdcdb1925688c8a6e6`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 322.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc7d63c8a6ff2afcbc55a78186f338dfcb811708e4bf65c7e1a33b51c28c230`  
		Last Modified: Fri, 22 Sep 2023 00:00:30 GMT  
		Size: 63.8 MB (63777776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc23fd020fd3056f91c4a5f48dc80801ef0614d428304b8712b64bf7424fd84a`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:566007208a3f1cc8f9df6b767665b5c9b800fc4fb5f863d17aa1df362880ed04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:fa3d07406ef9c95681e6a95c5abc036355c5e3ac20abfb37865ccc3539e4bd50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166876333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2013ac9910129ded1da4c96495142b2ed0638ddf7e86e65156400d9a8503777`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:24:01 GMT
ADD file:909c07f3bad92a80d3917d583769a01bf62c2cbf3dd24f450fb303b1db92a83e in / 
# Thu, 21 Sep 2023 23:24:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:41:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:41:01 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:41:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:41:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:41:34 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:41:34 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 21 Sep 2023 23:41:34 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 21 Sep 2023 23:41:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:42:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:42:10 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:42:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:42:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:42:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:42:51 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:42:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:42:51 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:42:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5262579e8e45cb87fdc8fb6182d30da3c9e4f1036e02223508f287899ea434c0`  
		Last Modified: Thu, 21 Sep 2023 23:25:18 GMT  
		Size: 45.0 MB (44959147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b767e25b7494c443d7dee268bc45577e90fcb4ece6c6f23c3fc93b7f4f319`  
		Last Modified: Thu, 21 Sep 2023 23:44:42 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e0c37837cfca7152f3fa4b752cc088e69f92e7bd9953229c7344de7335cd4c`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 982.8 KB (982820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f5d3670db7f8c371cd0aa2306cbf90e70e88aefa5a8ad7d15c5f426e69bf62`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 4.6 MB (4620337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c567b29c3ec4335f466d1b027ff9ab6ab1275da314da8eb088c38b2cde8cf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:40 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6effcc6561c9792f2e42dcee38c1b79c50d573dfae21a4c15d56cdf116b3faf1`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1493d45d9c24bf2946229eb3808d5603ad083f49ed16edab012e849485040f`  
		Last Modified: Thu, 21 Sep 2023 23:44:47 GMT  
		Size: 58.8 MB (58777440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7101609fa7d97ae2dabcc48d18271b8013cd59fd2cb18646cd8e5269d6a2b644`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a1261dc2ab100e2f5cd2582a00da9c7c03d56dcd7524c3e32103975617b8a`  
		Last Modified: Thu, 21 Sep 2023 23:44:48 GMT  
		Size: 57.5 MB (57527025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865a24d6d1f28b65e14fdcc535e8a07e6214872929f0b3647ef860c098c92f77`  
		Last Modified: Thu, 21 Sep 2023 23:44:38 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c0f7818fc533e4dfb17cdbfb8a1832d03f15c4acededcc4fbe67435b8b893541
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170377422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3503aa5f07519bad58f17ca0bc9b3ae21a66133942fbd915936c60d336a6142e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:40:46 GMT
ADD file:c630310324edbc0dd09d0912b8e7074d17ac71b1be8a14af9663872c081c4632 in / 
# Thu, 21 Sep 2023 23:40:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:57:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 21 Sep 2023 23:57:07 GMT
ENV GOSU_VERSION=1.16
# Thu, 21 Sep 2023 23:57:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 21 Sep 2023 23:57:34 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:57:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 21 Sep 2023 23:57:35 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 21 Sep 2023 23:57:35 GMT
ENV MYSQL_VERSION=8.1.0-1.el8
# Thu, 21 Sep 2023 23:57:36 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 21 Sep 2023 23:58:06 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 21 Sep 2023 23:58:08 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 21 Sep 2023 23:58:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1.el8
# Thu, 21 Sep 2023 23:58:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 21 Sep 2023 23:58:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Sep 2023 23:58:44 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 21 Sep 2023 23:58:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:58:45 GMT
EXPOSE 3306 33060
# Thu, 21 Sep 2023 23:58:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:286c1c922769d7608c32cf62931e95d7d169a0306164d24ce7d7a8a065959315`  
		Last Modified: Thu, 21 Sep 2023 23:41:39 GMT  
		Size: 43.7 MB (43657726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2045d234108f24e754e675bd763120bca5713bfbd34f917cef312b16b8eaeb84`  
		Last Modified: Fri, 22 Sep 2023 00:00:26 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e96650b64b585d497570d68ed967ef978298a63dcc9de51061e94b04ef316a`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e078f368c90db174893b4ac4586b3f26efd45a6cb77eb8803ce1d916121d1e37`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 4.3 MB (4307237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e3454b5c5a94b323b466e6bcaecb9d3310c242dd8b2c6880913c2477fbec43`  
		Last Modified: Fri, 22 Sep 2023 00:00:24 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2babac95cc038ef3da37b9e01cf3d22d2ef66a1d4353f0bc2969d38b858ce9a1`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa3f01ac3f924ae70b2fc8bb2f909031a6ab25a7922183d5682c7d9fb531dfd`  
		Last Modified: Fri, 22 Sep 2023 00:00:28 GMT  
		Size: 57.7 MB (57712118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69a1f6641e4c90e2761fd42f3bad7499bcff043b48bccdcdb1925688c8a6e6`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 322.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc7d63c8a6ff2afcbc55a78186f338dfcb811708e4bf65c7e1a33b51c28c230`  
		Last Modified: Fri, 22 Sep 2023 00:00:30 GMT  
		Size: 63.8 MB (63777776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc23fd020fd3056f91c4a5f48dc80801ef0614d428304b8712b64bf7424fd84a`  
		Last Modified: Fri, 22 Sep 2023 00:00:22 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
