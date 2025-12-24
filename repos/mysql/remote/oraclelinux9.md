## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:5ca0a273ed28c73acaef91da8bf1eca3711bee94bce4c378d42846375e645a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:63cfc76dd50bc5da75cc4cc758ef1c396ea5c7df07065240c593ce3783b53b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274743760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43463387c19a19c69fd00f32d492cb747cf738c30ef0628664280f49a3f4f55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:06 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:12:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:11 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518fdee9efbea5e86e637e429fc5305ba659433ef540a929bd56bd86aa3358b1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4739ccce10fef39d33dc6bb0eb200524c4d79475f2755547c44be0e53d691b26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ade15623158f018e163bf9f1e90eb96de7a4eb6e528ba2883c3036d9e2bb88`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7494a5617c302b456243d415c53fe84ca25c3002ce56258e577cfbc3cf0030`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c977bb8125788e8bc0f7fe950bb54ef5cfe7af769b56a060959f67e5c35b5d26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94829adeb7d577cc316253253ea4f4743a36d91e5e4eb9e62cdf5a4010350d6d`  
		Last Modified: Wed, 24 Dec 2025 06:13:05 GMT  
		Size: 51.3 MB (51339376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33d02f9e9dd93519837963c518dfe0f1a06e23a48b54ee7305af65f9aec0df`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc357b5ee6d221661a87283a9d5ef70812046bf6c430755a5f876cb2c04d6a2a`  
		Last Modified: Wed, 24 Dec 2025 06:13:27 GMT  
		Size: 169.1 MB (169118652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd9dbd900b6d31b0f791ac15f95720064ddd084b130d6acd6d2201f5e5c0dd1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5ed4dc7ecf7cc5cd98ec23cee55c866fe8e132c4de54c25fb7e52a5043301fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764317e87c39aafee8b7f55b056352f3652bd0e2179fc24a4b6016e49c03b73a`

```dockerfile
```

-	Layers:
	-	`sha256:4fdb571547772cf1740c1332b92f27bcbfa9ac263e87d62c99a67e967fea62f3`  
		Last Modified: Wed, 24 Dec 2025 10:03:11 GMT  
		Size: 17.8 MB (17811684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64911a6c79e2708a3d0d05552812d1b887bcebf22ca6b7522c14f67c77c7e98a`  
		Last Modified: Wed, 24 Dec 2025 10:03:21 GMT  
		Size: 35.3 KB (35273 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:680dc1e3ad62053eaf4a462be20f2477be4f6591e3f14a92c6c54f818bd2e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269809702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3266b6b77f63a9064496565abe1d16fd04705b1343257bd112f2ba43b993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:16 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fd8b6499592fd29b866d82e00c902dc0cf011626b9e4d7c5b359337c9d5c2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a69bbc706bc44e212923825ae863066d80f00788c91a7e8b71062005e6ecf2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324e82b6f8b9ae03ce4ee03088d040b7bfad2a74bf0ff7fb6b1e068b54ebb8e2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 5.8 MB (5799305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7841c3476196b92477b0dd4ca4c0eef34e2479e14be94f513d6d7b1e606de99`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81e5be81314066f565ac92b06f6ae72fbb0a9822deb7c687a60061eb1fd5324`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f54d7164805c698578999f62b9235542d8ebfe400b865080c1df43651161f23`  
		Last Modified: Wed, 24 Dec 2025 06:12:42 GMT  
		Size: 50.0 MB (49963256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0508c5e2469fb3678807c0c60746f538dba179d8e0605b09a20b4303cb7b5e3a`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31529acca3c94289a71c7f6fb2a7da7cf211cb86a0ee0fc26d9aa21ae97035`  
		Last Modified: Wed, 24 Dec 2025 07:13:56 GMT  
		Size: 167.4 MB (167397125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea9e2fa7b259a7f696c6b504bf2e25d81be3b389761ac76a356902dbb092322`  
		Last Modified: Wed, 24 Dec 2025 06:12:44 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fe7ebea6123c82aa390e8830f44dfe337bc3839dadb3e038bc8c9f5d5d817ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3cd9b380ac05c6ec1a40edae73b4008071c2daa78804d0d8f0dc98ea680643`

```dockerfile
```

-	Layers:
	-	`sha256:29a176dedfcc07d16a5456839c883bbc0fa2ce727dd9a42009c02f22590701dc`  
		Last Modified: Wed, 24 Dec 2025 10:03:35 GMT  
		Size: 17.8 MB (17806823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddd08d119f921e48f76173ea46938b5eb831a5be1bb60e444f688565113b7b2`  
		Last Modified: Wed, 24 Dec 2025 10:03:36 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json
