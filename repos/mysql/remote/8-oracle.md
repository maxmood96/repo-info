## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:f1c7674d8dd3c94f439b0d607792187d55bd861f94e8c6d683b959b577152bdc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8b3be4876b08746f2caa509afae13bac0aca1885ce967d1bb5ca0d177000f3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233227949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4511f663fb18c6cde7e5d9bdaafeed8c1c7019732b77279315145eb430e85dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:11:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:11:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:35 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:35 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:12:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:39 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:39 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad075f4936cf8a36f21e937e90b1d698baa6b0e625d13c69beef2586416bd2b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2ec557f75a04fa223e3c0bd71f6cc48ecc59f12a6c5e31a4ed48df3205387b`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c1d58a53d79eac5a138b2337dda522a36661053c302535c365fc5f64af2ad`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 6.2 MB (6172774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c60e0e578e332d62e541d2460840ae181c04522af7b87a815b50532a0cd0b9`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0125f072a0a55ba4ae0188f2dcd165d077cf20a27ed19e114cb325eb5256a1cc`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c356f1b5fd3fb93d5570a71077cff86a0af06026ef7a77b257d5d83f73166d16`  
		Last Modified: Wed, 28 Jan 2026 22:13:12 GMT  
		Size: 47.8 MB (47810258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cb4bc116b0506e2ea4ab9fa6bc54cc451e350fa3274fa025479c731cbaad6d`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce6e8837913ee62730f9a78f444b9a4cdb9f29bd6e248340731f67a1c261849`  
		Last Modified: Wed, 28 Jan 2026 22:13:14 GMT  
		Size: 131.1 MB (131139180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885e95c29fdf0877c6ec82ac693521e9735cf0c19a64d0d6d950afeb84929b31`  
		Last Modified: Wed, 28 Jan 2026 22:13:11 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:798a0bad5920617757611d4a42a351558a280acbec05ebd5596f7aa5f9b00d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7698ea2fc5e9501ff603ff4bd1d0a97505093033193881b8e631982bb6483280`

```dockerfile
```

-	Layers:
	-	`sha256:c823f2fc76110ec949a1d955075948f84148e5766bc8d9751774c7fd1ddf24b5`  
		Last Modified: Wed, 28 Jan 2026 22:13:10 GMT  
		Size: 15.2 MB (15234310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c856894eeb424a1604d601f5379bd90c5520e1e86430ff879bc9a4b675c5678`  
		Last Modified: Wed, 28 Jan 2026 22:13:09 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e51f27439b7a2119f9322da62672bf29db9733dfe5efda7fe14a95b1978b77f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228695273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a187cad11f0bae46349c98546b174514318cd9934ece1aaf891d8bb165f437`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:10:45 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 28 Jan 2026 22:10:47 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 22:10:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 22:11:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 28 Jan 2026 22:11:15 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:11:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 28 Jan 2026 22:11:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Wed, 28 Jan 2026 22:12:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Jan 2026 22:12:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 22:12:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 22:12:23 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Jan 2026 22:12:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b8014f3539c98ae4d9db79063d0ac6da20c561da597e5080428d7fa2a81045`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581c2da28c304c8a55c89ffc142dfe9b49523660a41d23868aabdb3746f9b14e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311e3508c6b08056182bbc122c5da5bf25d876d8f0bd1eb0921f401aa6e4e794`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 5.8 MB (5792078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dac3a350ad94d3b3ff38d83b364f9dfeb47f767e8586aacb3733b7ba672656`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbefc80b7213ccab583b4d0250ca47d5a5ffbfcc700eb995807fb9e9c824552`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6900ac85f3c3185bf951b4c2ff044719ab72a728e44d91c4aeed766ee05b847d`  
		Last Modified: Wed, 28 Jan 2026 22:12:56 GMT  
		Size: 46.7 MB (46700971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc870ee9e6c819f59ecc85a2e7df376e613358eb45f4a14ebe822cf57fe76a26`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f95bece7002a8fd4dd526ef950d925ffb02f0937885175169806d3ec1ab8e1`  
		Last Modified: Wed, 28 Jan 2026 22:12:58 GMT  
		Size: 129.6 MB (129551997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923168c7bf209bd6189f93d4cb04d2c82f17faf0ae36433ab67dd1e72ec3ca29`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ae951e3a0f700ccaab54d8aa559d60b9d07b96bd8f3121b6ed86971368f04b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282b71728f5dbf3f9d4b34689d6b80dc2aa9c48da7c3fe42eada863a8d347d0`

```dockerfile
```

-	Layers:
	-	`sha256:d66e901a34db0d11a63eea540fdacb6235f7c53a2a0b8b51cf5d898c1c80b2f7`  
		Last Modified: Wed, 28 Jan 2026 22:12:54 GMT  
		Size: 15.2 MB (15232730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf852e8614823f7b667b3de07ca7069909c56a682daa323b1433a790564d9d2e`  
		Last Modified: Wed, 28 Jan 2026 22:12:53 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json
