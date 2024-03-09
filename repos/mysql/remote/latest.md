## `mysql:latest`

```console
$ docker pull mysql@sha256:9d1c923e5f66a89607285ee2641f8a53430a1ccd5e4a62b35eb8a48b74b9ff48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:eeabfa5cd6a2091bf35eb9eae6ae48aab8231fd760f5a61cd0129df454333b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019814493c7ab16a057af0399b1288a1208b75ba852b915541840095c0fedfd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e77c3a95bf244837ef3176e72e05de7ec1d014ef3a1a76c9030016f9013f047`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b279a2086e00211e98e27d35c4fde07bb0b4c25ea9b49a4c6bafbe489e4bcd4`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bfbcde78826dc45fa2e00e48e5a0741b73d0ae60f7d8730aa48985af5832c5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 4.6 MB (4607369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35b074b68ec4634aec857bc99877e4c74b828f5c9d11f53ef034847f09262e5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beea5014e6afeae9ff205e80d71a77fcff7c97e39aa7a143fc80452c759a6c6c`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3791a61558d7758d9e9b0dc0b83b1d85f4c46b52ec9f0ba5bbefdcf98ba6e6`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.1 MB (63093875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f9323b9f0e9f41d474a790a61a9564bf7dd4568558ff259668b44ad28de3b1`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7391eab49be09805709ed6f59591af2e8117478bbf07407a33147993b5b148`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.4 MB (63419208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2f04b287ee751034e7ce212ee82abdfc4980faac13cb8627f916b3b268d93e`  
		Last Modified: Fri, 08 Mar 2024 19:50:31 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:88da9eaf220c976f76ce899a778bdcf0903c5cb334642551129100281dda34a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14287264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72cc37ca916c71906c35b179e686d535917b5fea8aae85ceb445df88a97b9b`

```dockerfile
```

-	Layers:
	-	`sha256:da913236dd60a694478dd288273763675c2d5fd16fcebe48f5d5620dc62492b3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 14.3 MB (14252010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a92219d33adf98def615c71489ec87651ac9aecd930144d6f8e9d751c15187d`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cf2ece69590c9306aea19dbcc6880fd2f839378b5a0599fc2144d8fd53d7c79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181350870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68e2614955cad9955f5bf3eab032c5c5356e00ae1e7725e850cc0beec446214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc99c3c88bd6a34b9545aaf31cc887e6593c8de6b75462e970c17b6f719d7033`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970181cc0aa652b91de7ef5d3a4a8334ca1aa33ba6c056d9e40b3393c55f8e7a`  
		Last Modified: Wed, 14 Feb 2024 11:00:35 GMT  
		Size: 62.0 MB (62038818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77b716c39d5b0ea63d0ceede4cf7561556f433b87b57469ffb08dfff917341a`  
		Last Modified: Wed, 14 Feb 2024 11:00:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e650d7f9f83be21b6573f6e6928f6feca92eeda8d3fff9b87ce692342008aaf`  
		Last Modified: Wed, 14 Feb 2024 11:00:36 GMT  
		Size: 64.0 MB (64020429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc21ff36b4b883c5f94497fb34e8b488b8fc405d527d4fa78eb88716f04a150`  
		Last Modified: Wed, 14 Feb 2024 11:00:34 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:2992bb8f887541d31fd2620bca3517c79493d221c2e574237eccb197f2c6f044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943f63e9e568384c0c1fd4311e13ef90099e33afefef87dd105743d4594af20`

```dockerfile
```

-	Layers:
	-	`sha256:4d1c8b0d984b5d7fdeeade25631416d5bf469b14276110d512cb50e74d30823a`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd46473e3d612a62cf79ea1ac033c73ba240026e52911972dc2808d3aa221dc`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 35.3 KB (35285 bytes)  
		MIME: application/vnd.in-toto+json
