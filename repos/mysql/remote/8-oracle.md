## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:4a4e5e2a19aab7a67870588952e8f401e17a330466ecfc55c9acf51196da5bd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e193c837211ee976fd9b638740a0264eff9b1d602d3affed7938ddbde7ff3035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168706003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9387c13ed83ab7915ed1cf73d505c6604c1f237b9f059ca26000ea70fa9dafb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:95cf7039855dd392d2faa5bb16415fdb79680afe50aecf7c299b8b2dd377328e in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fcbdc4090331ae224779b095ccebf7fa4fd896fb807b7d6bdb37776132e9710f`  
		Last Modified: Thu, 09 May 2024 22:31:50 GMT  
		Size: 49.0 MB (48998671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95eb5073c36f30976aef5c5876c27e105ed7068504d504b2f535c67e8e6710ce`  
		Last Modified: Thu, 09 May 2024 23:53:23 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5ba0e6412a570c371688b010532498352ceaf4a51713a4b492da307f15867d`  
		Last Modified: Thu, 09 May 2024 23:53:23 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4654eb29b74e8402e80c09a1a8438cac321cc5301a16c2326202bc70640c2d`  
		Last Modified: Thu, 09 May 2024 23:53:23 GMT  
		Size: 6.7 MB (6713316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2218160b86ee6f07b36e812cb6cb0ef139af74751e84e5d195373f0680de86`  
		Last Modified: Thu, 09 May 2024 23:53:23 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe712936412b80e3c07f2dcf56a1ec2a6e4365bc7033ed880a7e174a6cefa25`  
		Last Modified: Thu, 09 May 2024 23:53:24 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6efa1526090bef2174cc7c141756e7264e6b0c2fc714d7633caad928fa054b`  
		Last Modified: Thu, 09 May 2024 23:53:26 GMT  
		Size: 47.2 MB (47215669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7c3b67bb2b4660908b9fdffdd685a9b7e79c382b5b3b3a2c694b01552abe5b`  
		Last Modified: Thu, 09 May 2024 23:53:24 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccd17e83c8af6ea04e0ebf1f21d63ff25bb6b777c8806bb1fd7da53267dd6a2`  
		Last Modified: Thu, 09 May 2024 23:53:26 GMT  
		Size: 64.8 MB (64786021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bf2c116556046ae26a0c94d0bb53863e20e5ba1ca620a8a89134d159d73280`  
		Last Modified: Thu, 09 May 2024 23:53:25 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:0e58aef73dd0a7b787428875aa2b64600c048aa5e55e8529b0bb716d4678ede9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13594966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684e6fc6f27c968fe57023d36ffb91acf9c55f5386bae115cb8e0bece2148818`

```dockerfile
```

-	Layers:
	-	`sha256:90a79ca1251f4df5853d89c397e219bb1522324e191acdef77aecb69b8a2600c`  
		Last Modified: Thu, 09 May 2024 23:53:23 GMT  
		Size: 13.6 MB (13559875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4e3e46818461813a47d05334932cb3deb7ee534c3a114ec812ecf03ee802a2b`  
		Last Modified: Thu, 09 May 2024 23:53:23 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:79bf3d05d420c85d21702dcde491ec36be535c79200cc83f1298dd838a6f1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165936004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c9c15d9ea6c54c2b01a6711d3dae4412f67eb89d27509ca857e592f23929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69999011c03fe9caa79c25b4cc5b668950bf164c0529da1cd5a707b2230b546`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f05d9006da74f47862396c0649055f72490479abcff23198e262e143f3d5`  
		Last Modified: Thu, 09 May 2024 23:39:18 GMT  
		Size: 46.1 MB (46084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598a5053b5cad951d8eaaedaebfdbc5463a880de8c075a48f7c2e5eae7c08d3`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4462059cc5c84ea3164bd0179dc65734627f2a496a0c56a1002054ee36aab`  
		Last Modified: Thu, 09 May 2024 23:39:19 GMT  
		Size: 65.0 MB (64960942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca92666741087fc28d7590e97b73f8c452955effa4f061f16451c05ba0934a3`  
		Last Modified: Thu, 09 May 2024 23:39:17 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ad0644d4ea4c2291a9c3990d2e0373112058f7e7d8a3da4865c0c079b9c878cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db833d8a95d398a7d7abb7248afc9a264d2df8542ff5040708dec1968ca905c`

```dockerfile
```

-	Layers:
	-	`sha256:f10b193dff936fdc257b9489b413aa675fa6d6268749f4398581f7bd61a68873`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 13.6 MB (13555047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4f13cdab2d2ed579bf08f115518bdcf6b9957b97ef28e61a960a5077aa6431`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json
