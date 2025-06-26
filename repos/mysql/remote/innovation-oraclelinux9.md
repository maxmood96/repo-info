## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:5c9a1dbb3ec76947f7ca06df17a35e74366180591107f672a3b830a3892c8227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5d29b2fd39615706179d7fc46b68c9fc3234c7e31197280947aab5da9e49ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103520d778e41b5e1033f4dc6ce8cf4ab401656c89e938e5ad7dedb86a1611af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af7a034b8b97178bcf870b6c177401cbc755d5aa22ffe1c1b7e3a082fbce51b`  
		Last Modified: Thu, 26 Jun 2025 00:09:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87129af36c90cd3f61550a2856f3c5d2f3f1713c1e3e9144176c0146e4d44ba3`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cecf14f09b5d3edb4a3544a1d05853818f7680628359f4a7c02f88de177aca`  
		Last Modified: Thu, 26 Jun 2025 00:10:03 GMT  
		Size: 6.8 MB (6814485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028720beb240215be0ca3bab5089c7bb51f696b156156593ac9bb5f379e3e053`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba8db0f2bd8681f010f9753421001ad9aea9a9e4ac26af3336e6d347d6eec7`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead6a62c24e914e3d8f75b8246854a9fa450ea23ed1caf351cbb9188d5684fc9`  
		Last Modified: Thu, 26 Jun 2025 00:10:04 GMT  
		Size: 48.4 MB (48428284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20478bf3bbf8646fbb42fba1aac9a1b9e9b2ed963dd1db840fc86126f8a50fe`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a26ee8a4dfe4addf458c1c923a4b386ae1878a2588a3854159b087e2f49e3c9`  
		Last Modified: Thu, 26 Jun 2025 03:02:52 GMT  
		Size: 152.4 MB (152370564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4657dc0fd6eebc28ad4e5d7d9608fd6d1bbec29e3426108440618692cda2b961`  
		Last Modified: Thu, 26 Jun 2025 00:10:00 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ea3498ea06120af985f4bf13c4856f8ad8c6071c8fa3a12396a07e3cbb570d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d8bdecc7c16720142350a3e870dd4dfdb4fd4b24c1f78171369b9a7558e620`

```dockerfile
```

-	Layers:
	-	`sha256:e2253cb185aa17da6bd5329fa6eea3042508121827f017e05e6f1ca2c321d285`  
		Last Modified: Thu, 26 Jun 2025 03:02:46 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92fcbfeabca9d4a242a81802e78e9d29dfe815cacdc60c3ad66c1c127e5b21c6`  
		Last Modified: Thu, 26 Jun 2025 03:02:47 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5c332061735be22e6c4db5511da7ba36d59ac9c265203d4d23157c7efbe9a750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253380797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7958658f926cc6946ef547ecdeab9e53f83dd08e5ea8af9260c206eb51d4ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a492f1b8dd4473fe6e95db0fffd529acccbc6bf7ae83c1a54ea24816607b8c`  
		Last Modified: Thu, 12 Jun 2025 05:06:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d652dc25083530b034f97e48178f26efe3f6fd734a381391d823538335b92c`  
		Last Modified: Thu, 12 Jun 2025 05:06:49 GMT  
		Size: 913.4 KB (913443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd736c905de7e346ceade7885949bce6d40c69fb5eca28a2da9597a83c2a95`  
		Last Modified: Thu, 12 Jun 2025 05:09:59 GMT  
		Size: 6.4 MB (6448759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b5c0a118ebe829a193aa321a4f8e76ab4e58fa0cbb10b6e56218ded03e93b`  
		Last Modified: Thu, 12 Jun 2025 05:06:53 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8868fca330e665d4f2f7e8847ca738cf45a0fbff88f9c893f4e015c560b2264`  
		Last Modified: Thu, 12 Jun 2025 05:10:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00735954ac4b14bc4b1453cd8169e1d79e634de273ff5802a47750eee5159ca9`  
		Last Modified: Thu, 12 Jun 2025 05:10:06 GMT  
		Size: 47.3 MB (47278322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca07bba4ff383ee7dc38989679c75726821fcc3c8a311686a1f83ac318d5c6e6`  
		Last Modified: Thu, 12 Jun 2025 05:10:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c452914633fb8047a344179c565f7da73f5f4fa01a194d30e0fee6eeaf015`  
		Last Modified: Thu, 12 Jun 2025 05:10:20 GMT  
		Size: 150.6 MB (150640991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874233f830cb44464faeb87c1d4b1da35ec39cd68421add8c324793d6b70daa`  
		Last Modified: Thu, 12 Jun 2025 05:10:10 GMT  
		Size: 5.3 KB (5336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:46eb3de4847a92612f2dac7a4096df5fd11ee91fc69d2167399208e685556924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc46feaf880dad6ed53bdc533e7369f5643a51cdf258d7e57bcf7d62cbc01fc`

```dockerfile
```

-	Layers:
	-	`sha256:175db574d245f917ad6631e43a75597896c3ddee12daab7dc77e7e4b67a14720`  
		Last Modified: Thu, 12 Jun 2025 06:02:49 GMT  
		Size: 15.1 MB (15075027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17666eacc6afae7ef1a6c2ecf43089a8339521ac602aa1ca5c935f6d9bf0c88`  
		Last Modified: Thu, 12 Jun 2025 06:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json
