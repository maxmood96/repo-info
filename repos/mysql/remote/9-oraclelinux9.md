## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:96245cd3fb1e833793534c6b3a40fbf938bb06f3f50779f6f43e4bad0ba7bba7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:537a1944f2b8623b55a74cde949488d3c46c0068d8eca6f7f54c5310f0a5c72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273451129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac34d07e4eeaa812627077a1ef6fdd881b747bb4dbe03f1742604c84535976b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Thu, 23 Apr 2026 00:59:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 23 Apr 2026 00:59:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 00:59:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 00:59:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_MAJOR=9.7
# Thu, 23 Apr 2026 00:59:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 00:59:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 23 Apr 2026 01:00:27 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Thu, 23 Apr 2026 01:01:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Apr 2026 01:01:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 01:01:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 01:01:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 23 Apr 2026 01:01:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191b09bcaa2f4b6ceac8d0a092752d710c7cb8c158f109fb44b0bc219d315f3e`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9f281a64d5f7c1adee5dd7d5e1c894de430238a10d0c4a41a73e306887b51`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae6deebd2fa83f366083d49c617bc812907f63192a98f714f794a563be07cc6`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 6.2 MB (6170254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b513c0ae344ea5695be1a37fd68ec9245479e1450059015c7d1a2c7be6012be`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9248317979a45744ddcebf6dc864e5b8ef351da623a270a7adbc6829b74b88bd`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7d368319daf4fe7b958b04f96c2a9c60e4359dd4cc134020e22825b4da75be`  
		Last Modified: Thu, 23 Apr 2026 01:01:48 GMT  
		Size: 57.0 MB (56969256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9dca007c40c7e33d142c2e4e063839d976b09a0057b1cf95803a237736a7f8`  
		Last Modified: Thu, 23 Apr 2026 01:01:45 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf1cab22f6a5b111f8a0cbf806b16fdb585114a1cf370a9279286a548e1e77`  
		Last Modified: Thu, 23 Apr 2026 01:01:50 GMT  
		Size: 162.2 MB (162208769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb28e454875147702a01891683ce3520e6e0d48aa0c75e2d9f6d7f3c6bf310b`  
		Last Modified: Thu, 23 Apr 2026 01:01:46 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:35400cf8c23d435d257eb41f611d1cbadde191808588fbfba36f36894ad952d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750613bae6e60c9ed24bac0793e629d92ac14959c02ea82f91346b3438010c8e`

```dockerfile
```

-	Layers:
	-	`sha256:48f6cb45c1a8becbdcbe9a814cea4e8823d670cb435eb4891b6859e25d9bc057`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 16.8 MB (16788746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd260c630db9c35d2f8cc5ceb01ca6a6be0ef9889e54015d3f126fe1b0212e86`  
		Last Modified: Thu, 23 Apr 2026 01:01:44 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2fa34e99773301014cd991ae65b9a4c2e934a4d0403f6eba76e417dab1b8d809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b442b8db2f20d21031594573141abdbf6a2dd63dbfff4087482d7d1a76c37e3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:08:59 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:08:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:10:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658cf3809cdf66916d4ae80f9fbdbf2ce418edd07c0c3d9f15c78a98248852b`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552d15d4bd606fba07bd48aca9d77b5b11edeb2974d8bac400c8498987f68e2a`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e989ffbf19734c8ef04538b2e50bade50c3110bf0586bd92672d3566424130`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 5.8 MB (5790756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5c90f535adb91b18eacda78a9e62b71e5ba5e0a6fe785a566b1cb1dbe7c4e4`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0838d2f46e3df9f2f1b27626c6fe842a8d30523e17bd6bba2c86bdc869deb06f`  
		Last Modified: Mon, 04 May 2026 21:11:24 GMT  
		Size: 57.0 MB (56983090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505aa7f4d7942ecbab4820ec2e34dc8733c5478356c7458c22c40aadd5eb873`  
		Last Modified: Mon, 04 May 2026 21:11:22 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46af6d538acbd6e4654372a8dd246d6cee34096a7e99812c1f3416250dd31605`  
		Last Modified: Mon, 04 May 2026 21:11:26 GMT  
		Size: 160.5 MB (160488794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914ddb25249c7f44ebc5e90b15ff621d12c3a1397c213e92ef7131ffd3f163f6`  
		Last Modified: Mon, 04 May 2026 21:11:23 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3c60b1dac4c0a1b76ca41c7da7a5a29a7aee5f413642229e7d9158610b8a183a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121591fa331c19957701197526c6ee65b99b9c66a9dc3a5a937627ea9f8c1ca6`

```dockerfile
```

-	Layers:
	-	`sha256:d62755c4342059bb85df263aea48b42594129162bbb70379b42b1ba66abcc7b6`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff0ac1686f49579285d64201585ab619c337e630ba98ed1fb47004be03cad17`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json
