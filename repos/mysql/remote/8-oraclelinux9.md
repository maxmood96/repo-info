## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:2952e3be7807f06fc18de50b3ea1a632d5c70d63482ff7d7376fe3aa8999babf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:4fc4bca5a26c5aa2246a92779d238bc2d34f0373e65dc083d7b635b02780dd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233200125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7791889374e752a470ed491c5c7684bf91d64c2472721539bef3a64f5276e074`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:12:17 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:12:19 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:12:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:46 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:46 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 18 Apr 2026 00:12:46 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 18 Apr 2026 00:12:46 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:13:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:13:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:13:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 18 Apr 2026 00:13:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:49 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0e913f3fdaa0fc569c88668fe2e9a761352bca579753395f748cb6465c6d1b`  
		Last Modified: Sat, 18 Apr 2026 00:14:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e9fc37ca7f146830e5eae65dd80fa21f7c07d1a33af7cd16de945829e55696`  
		Last Modified: Sat, 18 Apr 2026 00:14:20 GMT  
		Size: 783.6 KB (783562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea3d1b96bc6604bd35db84d6208f5d1eea9e04465ac8af1bb5fc49a8af4400d`  
		Last Modified: Sat, 18 Apr 2026 00:14:20 GMT  
		Size: 6.2 MB (6170288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c72b297542da9c87489add0433bd17e862e59f8cc9333d67b88646aaf624641`  
		Last Modified: Sat, 18 Apr 2026 00:14:20 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02b00ae5ee3ecfaf12800539a8be76bc928b126a7fe85a4d60c9f1a5b6f6e59`  
		Last Modified: Sat, 18 Apr 2026 00:14:21 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d786b1680fa60e999cdce43e95b2a1a10642d7ce21f2b86990faebdc358b4ff`  
		Last Modified: Sat, 18 Apr 2026 00:14:23 GMT  
		Size: 47.8 MB (47800943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120c8f89501932a979c0829d92889d51c5463ff6994d70d336c663ec4ceb7f9d`  
		Last Modified: Sat, 18 Apr 2026 00:14:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a955715b8cd4db7aea169b449163049eaecf5a4ab2b68a8b46e0111cfcf5ad62`  
		Last Modified: Sat, 18 Apr 2026 00:14:25 GMT  
		Size: 131.1 MB (131126042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ccccafb277bafbd4036cbf2464159925a6adb5fa39cb4e1a93688aa868c35a`  
		Last Modified: Sat, 18 Apr 2026 00:14:22 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:8b02164ca2696e534bc18fa345264af8eb8911e26efc9c473b40fc820d2b7e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ef8b1bdafa9cadd18f6ecc7e666ca21b07a27ae7f8cc40f4c5640e31461d1c`

```dockerfile
```

-	Layers:
	-	`sha256:8d5cac692ba261edad5aaecf84d9159705e3e026550163a77bfbf870dc83c907`  
		Last Modified: Sat, 18 Apr 2026 00:14:20 GMT  
		Size: 15.2 MB (15234362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1c8ba56f131826b359cfe59af738d0fcf4401674658b69900cf6a9f415a79c9`  
		Last Modified: Sat, 18 Apr 2026 00:14:19 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d850b910de00a58b0f85b0690c88ac2f633db6aff99b86fa7ad4ebc59d8c27d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228673199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bcfd5ef06fdf8de754cd4a1f18991f84b2fccd10f26c8b15755597ff690468f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:11:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Sat, 18 Apr 2026 00:11:59 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 00:11:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 00:12:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:27 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 18 Apr 2026 00:12:27 GMT
ENV MYSQL_MAJOR=8.4
# Sat, 18 Apr 2026 00:12:27 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Sat, 18 Apr 2026 00:12:27 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Sat, 18 Apr 2026 00:12:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Sat, 18 Apr 2026 00:12:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Sat, 18 Apr 2026 00:12:58 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Sat, 18 Apr 2026 00:13:34 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Sat, 18 Apr 2026 00:13:34 GMT
VOLUME [/var/lib/mysql]
# Sat, 18 Apr 2026 00:13:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Apr 2026 00:13:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Apr 2026 00:13:34 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Sat, 18 Apr 2026 00:13:34 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89255e92e4ee52a1bcce2f408b02057d70ea2f7b7616944f411035b73de8921`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e6bf16c0fccda71de3c8790c6f557f6b6b3bf142fdcbe130c04fab33d51026`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26ce327ac7fe89f2b63575213bb4a1821bb6e6514da233ad2369a35dba0f108`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 5.8 MB (5793282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79edfb89c55442344e72c360cebef7fa54187e54520632a11e9a45d88d936952`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b292f3b932d25ce43bc4c58c0733534a96922b9571b350375d4e3b1be1caa653`  
		Last Modified: Sat, 18 Apr 2026 00:14:06 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ca6e27633516ecbf61cf52f48a9b5a977c857b96cefd53a556178654504b1a`  
		Last Modified: Sat, 18 Apr 2026 00:14:08 GMT  
		Size: 46.7 MB (46694158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafd35ec4acd3d501d5d5d140cdcdbba9bf1329a6f2ffdd6867bbf686cc3f8de`  
		Last Modified: Sat, 18 Apr 2026 00:14:06 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf9002ad0bd065fe230d611fd95428096b74aebdf1754695750e397277ca039`  
		Last Modified: Sat, 18 Apr 2026 00:14:09 GMT  
		Size: 129.5 MB (129538965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1204a4c6184cf9fdde814e5e668fdc6edbc989c4c5a60964ea2536794a9d4e1d`  
		Last Modified: Sat, 18 Apr 2026 00:14:07 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6ceb9d7b4b06f3c177686d1b105fb84e30aa20e02b540747c5defe506fdfca55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c4818a4af0056d8250b77b945b4e16d7d0077fbf34c8f881c97c40207b937a`

```dockerfile
```

-	Layers:
	-	`sha256:a87857b783b153e0361d5c1e68bbd1a4aab70059d950c8dafd6b4a6a6f277c0f`  
		Last Modified: Sat, 18 Apr 2026 00:14:05 GMT  
		Size: 15.2 MB (15232782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eba0d239fc28055d6661dd282495468bc29d0f4ae6c759a8041602ec3c1e463`  
		Last Modified: Sat, 18 Apr 2026 00:14:04 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json
