## `mysql:latest`

```console
$ docker pull mysql@sha256:e4054c2973be8766370769312786404fbb4557fb591d9ad37beb2d00a2c574a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:96c332225878600240197ae810767dd7e4e5e246bc1f57c2ec94cad14d315640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171750074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3df03e3cfc9471071296cc2456a66e238e7f84b6f2c8dd91330422505502804`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
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
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed19546d518d0f164f97177682a5f85144e1de05c24b62d0c8439e023cce00`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501aa8e883deb323ac6b074d691f213a333cadf707a23b7fcea6d623dc27d9da`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c0b888a0f7e9043d1bc59384e4358443fe39429349dee365a030a4b717328`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 9.8 MB (9755190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4670b7e1bbfd0e5cd441b36b56a307b909cb59be10b778e456922efe40c9ad26`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d50b789abe8f3bf3c7dc066ec2ec4d838cf0502558840d1cb6d7fbff0562e2`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd9fbae13f7c396a235c6e2f37ed5b4c4b649897c83e9124346f72756664dce`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 47.2 MB (47234025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b7592f6de1dd34b1cf3d6962b44203c6b3bea8457a671b37741d0fccd47e74`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6795b8ab791a09064c3b3c69853cf89b86706fca1cb6d4912efa98b63a95f90e`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 64.8 MB (64803395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cffac37cee141de0d62bd62b64127dfe273a5c6b7f54752170168d40c5633e`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:1983fbbc4e5e49e340c8225c12bf9036597783c8269f9f842f65c2ca985cf02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13595041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb676d2fd76b8a8e3566d1290684689d65d650e2e194e0b52d9c6b5478ccc58`

```dockerfile
```

-	Layers:
	-	`sha256:c92df696b83eb6f8d8b25ded2f6431e2ba36bebc2977149081bb68389db533f8`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 13.6 MB (13559950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21909f5a3aef56695e2889d19b5901504445511b0ea4f65cf0bc7cc90ea32595`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9c775bfbb32aa68de2aae2dc3801e1b27e6816deff71f5e9e71071cd1389d1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168851017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a1b6f60db861741e0daf178410ac370c0433ab51c6b4c9debf8e59c73c470a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 23:29:31 GMT
ADD file:25023c55a282c7a0be958dc9555d115ad07185cff37f25566562575bc91f2d6e in / 
# Wed, 24 Apr 2024 23:29:32 GMT
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
	-	`sha256:6c095c52d5d232eeebfdc7173cf1b5de6af5dfcf6cc906a66496ba14cf0ffcee`  
		Last Modified: Wed, 24 Apr 2024 23:30:37 GMT  
		Size: 47.7 MB (47662476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae186b7bd2a4bf79217c3f00080aba9dbd3987825f4302b4bda158308ae2678`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4130f1dda4331229753037f918a7af3edacea070f4ab495a51c39dac81847685`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e957ad183cfb465a682a104902c6dd1c737cc9d03361976b92eca15ddcc92`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 9.2 MB (9169807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748ca1e5c1679df097a564d719108bb40f8cc51dda66b88432b4e38b67c1815`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c9bd2b73010e9a5b472150ef6ffe20ddae8c8dfe066aece2c532cbb6d8b87b`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c62009fa89483168a4927bfdb86267d703b3520f0fbdda4757a1eb20fbf552`  
		Last Modified: Mon, 06 May 2024 17:41:02 GMT  
		Size: 46.1 MB (46111987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d96d7b1886937e2e53358881528e8540afb88d588b7d77eb8101af303d0b4c`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0ca5475bbeb66ebddd6460d9ec4a3eff42ad2febdd494e79ca4060fccc0d43`  
		Last Modified: Mon, 06 May 2024 17:41:03 GMT  
		Size: 65.0 MB (64983980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415aecb3e424bb192460b9f5f8b97284b4d43241b104638cbe0e58a85236676`  
		Last Modified: Mon, 06 May 2024 17:41:01 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:f44c38693f0ce23ee05f5383885e54aef4d4eda8e58d4cd4c6156107a9b1a475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab65333fd304809a8de2b3a4909249d80ae7d4a1ed7acfefffccfc4b896cd41`

```dockerfile
```

-	Layers:
	-	`sha256:d38f5494c566d0d25d112390ead0e21721abecc9a600965527f64d4ec5ac22f1`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 13.6 MB (13555122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899b753352bb8048a26710116e1973c1b170079da5bd83afc4fe4910a12b4470`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json
