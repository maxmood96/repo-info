## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:b306273d4d36bc1a7f265130c3dd93c0462253af7634203e569add0403a7b273
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:dd7588878e4b257ab9ff4bd9c6e437210d8243fedb2b4d411db69e75189f9311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235813004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67471052edd59d6f346dd094fdce8520ada706feafb86716b0e005fed935e5de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0f6627363906cbf08b2919d3b38ba777fec2c930a76414a043932bd04fcfdb`  
		Last Modified: Wed, 22 Oct 2025 02:42:44 GMT  
		Size: 6.8 MB (6819663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d6105636e6b36492c9e178a5ec6b71956dc0c9cec8a72502c6c87252978f4`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3763684269ad32c161812dfd28b4f40f8b90169c0a035ff5372eef48c1cdf750`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c524da3882b31699d87fa654f47a443b343a458c1e65f1f6a904b72543cdc2`  
		Last Modified: Wed, 22 Oct 2025 02:42:47 GMT  
		Size: 47.8 MB (47789253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824d865d5643bc90b27c7659acb0c47f52e09eff8f3dc7249f83d7e5f4aafb66`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270bbb610640d761d420264741f74b869c323d4e1992ae71831b882de094e9a0`  
		Last Modified: Wed, 22 Oct 2025 05:10:39 GMT  
		Size: 130.9 MB (130914552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8b60e8a15af08080b99e0173420bb8fdbf98222e058ce1d647ef2225d0d119`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1063c9a7e8315acdfaaba4381a89a34a19c534e5c79d1d749f5cf5b4ca6586d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14946531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f57015c91019b81b2b0210f75358ad46d0220e30f62d2d52e3322e5b371e85`

```dockerfile
```

-	Layers:
	-	`sha256:2074df902b8297d69cc4b7bbde8559ffe14dc41581d2bafd73a4fe89585dd1b9`  
		Last Modified: Wed, 22 Oct 2025 06:02:18 GMT  
		Size: 14.9 MB (14912281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655361bfaae1991f8c62031c6f5cc851b034ed5985ebd7fe15abb0b9a6441912`  
		Last Modified: Wed, 22 Oct 2025 06:02:19 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json
