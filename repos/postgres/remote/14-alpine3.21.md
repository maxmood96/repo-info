## `postgres:14-alpine3.21`

```console
$ docker pull postgres@sha256:f570e7807aa5387121c52f6457a195c39e95e4088040940d48212c77684ab0a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:14-alpine3.21` - linux; amd64

```console
$ docker pull postgres@sha256:0c794c18e953923230b35acfdceb6237bbb298db037b48b5255430bdb832d577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108248236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919eab2f108d0c700077342e49a9d4652551990321863cc165ffecd6165bff23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:17:09 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:17:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_MAJOR=14
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_VERSION=14.16
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_SHA256=673c26f15ebb14306ad0ea051d8acfb3915dd342de942f5b502e5354a0ab760c
# Thu, 13 Feb 2025 18:17:09 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:17:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:17:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:17:09 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:17:09 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:17:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfe5a1c572f4a3adac265948bd8e9e745e1d0d206c2f596e9ac418fe1ad2954`  
		Last Modified: Sat, 15 Feb 2025 00:08:45 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9595ab4038155f825707107fcd353c5de4070a77ea484b97089f15bd72f503f`  
		Last Modified: Sat, 15 Feb 2025 00:08:45 GMT  
		Size: 1.1 MB (1120325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a568080a6cbf54db2fba8478ebb88be5fe240221a0467ce6e16907358e21d44`  
		Last Modified: Sat, 15 Feb 2025 00:08:45 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3df0349e4ce37cfd8e5b42a801f066618027c2c4a1edd63ec8ca3dab92f3c4`  
		Last Modified: Sat, 15 Feb 2025 00:08:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15228a173ec2f401faa79bd5b96476935d338ead839f565b7b6b5f7c8594185`  
		Last Modified: Sat, 15 Feb 2025 00:08:50 GMT  
		Size: 103.5 MB (103469304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8915458bce052e3529bbdd6f6c3a293436dec81f0060465dc1a29b1032b2309`  
		Last Modified: Sat, 15 Feb 2025 00:08:46 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fdac1c483d0702955d07dffa2db77653bd617f5f312cd9a09c94b1e88a0c8d`  
		Last Modified: Sat, 15 Feb 2025 00:08:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28daed7347446148e1671a3f39bd89d7dc4811ddab9a351e5fdc04c78768d89d`  
		Last Modified: Sat, 15 Feb 2025 00:08:47 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cffb0cc189e8bc09237e64c5e76dc1b3a8553e783f80a2b7ff6d87bbe5129c7`  
		Last Modified: Sat, 15 Feb 2025 00:08:47 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488c651daa3404f0f74accb7b9ed5944d4a76ccd39beffd7a7219cd8823c7da2`  
		Last Modified: Sat, 15 Feb 2025 00:08:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:5a1c3de5a722cdfc7059468757ee7123e61b99a5c0470779f69df328f36c3b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f1c46ff6e2250bcd76526079f8bdc1e534d31e88764115e7dd5ab5ced2bae3`

```dockerfile
```

-	Layers:
	-	`sha256:fdf336bc144534b621496aa95b21a2244a596e37e77ac107ced3fe95cb3a84b0`  
		Last Modified: Sat, 15 Feb 2025 00:08:46 GMT  
		Size: 595.1 KB (595069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9d8b1877afd737df1b56f442a2f577bd3b7a650e0a4552369c2c19e06485784`  
		Last Modified: Sat, 15 Feb 2025 00:08:46 GMT  
		Size: 45.1 KB (45113 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; arm variant v6

```console
$ docker pull postgres@sha256:c3286b19063ce01a31b7ffbc7748573eac8df10d5424cb7dbeecd674ddb12af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87866981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aec3ae1e70ce7b40ef6ebe9937c40e90d968deafdfd61a75ef665754bf2c0fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:17:09 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:17:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_MAJOR=14
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_VERSION=14.16
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_SHA256=673c26f15ebb14306ad0ea051d8acfb3915dd342de942f5b502e5354a0ab760c
# Thu, 13 Feb 2025 18:17:09 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:17:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:17:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:17:09 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:17:09 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:17:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e8cc19bee9308afcbf52843a00e4ef4972c49cf21acd9b92368cecf528ff49`  
		Last Modified: Sat, 15 Feb 2025 00:09:03 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781627176b8f9e10a830d9e3a634776cd0db6531992b444881c58b767652e146`  
		Last Modified: Sat, 15 Feb 2025 00:09:03 GMT  
		Size: 1.1 MB (1086598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5c66ed96baf47284abdd1941a68e679209bcd67c5115885f337bd99a0c6008`  
		Last Modified: Sat, 15 Feb 2025 00:09:03 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221e19b745e47706571cde1555189229d670f7c69c24c2b57e6260be58b7045a`  
		Last Modified: Sat, 15 Feb 2025 00:09:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745d4f1f3224f0186b5cc952720d27469afcc3b80d95504a04ba7d7f8ef80400`  
		Last Modified: Sat, 15 Feb 2025 00:09:35 GMT  
		Size: 83.4 MB (83399282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e786a2c7b7b77b0a75167394f18c7b87f55036a4ca857348581871d6417b1f15`  
		Last Modified: Sat, 15 Feb 2025 00:09:29 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8519509dcf0ff911257bccb137b114a3f1e849fb39f25ec5b81170e0f1e6c6`  
		Last Modified: Sat, 15 Feb 2025 00:09:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d1cb9e58fd558d8e566d12a6f4df0bca7b871adeaba7edbc9c6a67e9360a70`  
		Last Modified: Sat, 15 Feb 2025 00:09:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e002a6ea6847ca9409737acc58e0fa5e4377822dfda4076d918fbaba67a8494`  
		Last Modified: Sat, 15 Feb 2025 00:09:29 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb3dcc8e04d66d3bc1c987848fa661c68586d4c9f9a23311e498608d5aac9d0`  
		Last Modified: Sat, 15 Feb 2025 00:09:29 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:bf3cf235d7a1232f44ada47d3ed36ba45dc58f6c99143cad518e87477768962c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 KB (45071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eccfbeeaee4c3f9db89b1c7aeb9009ff256b2cb4efe8462544c000fca02698c`

```dockerfile
```

-	Layers:
	-	`sha256:8fafd9c73a5fcac4d8f967b40c0d1841b3ec21a30dd996e95cd3d56be5f545ca`  
		Last Modified: Sat, 15 Feb 2025 00:08:47 GMT  
		Size: 45.1 KB (45071 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; arm variant v7

```console
$ docker pull postgres@sha256:e9d1d34f3fbd9f33b16f8e3f95878fa811f8f0971a134966c63314f3fa1c4d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83117716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ada3e09b8e1cc43a088d560ffdacdc6a136293279f9eb9a64906685b07defe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:17:09 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:17:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_MAJOR=14
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_VERSION=14.16
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_SHA256=673c26f15ebb14306ad0ea051d8acfb3915dd342de942f5b502e5354a0ab760c
# Thu, 13 Feb 2025 18:17:09 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:17:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:17:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:17:09 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:17:09 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:17:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7024250a83f264a63fbff534638a3450b2f72ad8d8b35fe376f3e85aa54086d`  
		Last Modified: Sat, 15 Feb 2025 00:09:42 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4a8c8d36a5e942fa57e2ceda06a6b7f36ee0bfcc9dea6dea13a291bac3ff68`  
		Last Modified: Sat, 15 Feb 2025 00:09:42 GMT  
		Size: 1.1 MB (1086586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e35cdea82ca5630226b82d28e392522daaf6209398481688120f3198202889`  
		Last Modified: Sat, 15 Feb 2025 00:09:42 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d49d5df43279d9ad2270901f444af104f5ba3ce219b96ceb2020802a9b82c2e`  
		Last Modified: Sat, 15 Feb 2025 00:09:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09db5e482e4f29ff7e35c86dd82cccbad7657c0bb649e8e3c762267723196c2c`  
		Last Modified: Sat, 15 Feb 2025 00:09:45 GMT  
		Size: 78.9 MB (78916639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05e7df121d16cbb6af83dd1be8954f19d11312604fb25c2b372fd0a3ed84d3f`  
		Last Modified: Sat, 15 Feb 2025 00:09:43 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8796cf1d8cdf14e2c9c430b4eda60ea38c3072b1f7af6087468399f9e996fdbe`  
		Last Modified: Sat, 15 Feb 2025 00:09:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20464af045cbf28213bfa8f67f429db0de9ba33e9d4930af49a04075631bc228`  
		Last Modified: Sat, 15 Feb 2025 00:09:43 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2323c0e94c2471dd2a898f7c515b8a795f1aa5581b84750a7f2d2dd4dfe930cf`  
		Last Modified: Sat, 15 Feb 2025 00:09:43 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2abc07e2b8edeb1d0b3c68a86b57f75374f40f1769d15324f24e12904088bb`  
		Last Modified: Sat, 15 Feb 2025 00:09:43 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:bae58bed62bec22bbe160040e987ee71c5bd5902e275a614bfc7c09de87e55ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.4 KB (640391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f8aa55045cb29601740b0c6a46da2697df27abc063bb872947d217f055832f`

```dockerfile
```

-	Layers:
	-	`sha256:e65145495afb175b2ecfd1eba293e54b604e2bbf9728d5dc9771c88b46beea92`  
		Last Modified: Sat, 15 Feb 2025 00:08:48 GMT  
		Size: 595.1 KB (595105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10f64ce5a5298e2baa3f8a2c61bbdf09205c2710da8796a5b46dc3f5d2c8080c`  
		Last Modified: Sat, 15 Feb 2025 00:08:49 GMT  
		Size: 45.3 KB (45286 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:db8009bfa7524501e0b8157d2638d16bf2b6b428d0b6cec3686fa9a8079695dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104146804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e75236a3e28c864679c38c1a9fa30d8796fffe6c57c3f3103a989b8771de630`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:17:09 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:17:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_MAJOR=14
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_VERSION=14.16
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_SHA256=673c26f15ebb14306ad0ea051d8acfb3915dd342de942f5b502e5354a0ab760c
# Thu, 13 Feb 2025 18:17:09 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:17:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:17:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:17:09 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:17:09 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:17:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d48755775e41959c11dbae67c73e508794c4507936bb8d9d1c54a5bf9baf7a`  
		Last Modified: Sat, 15 Feb 2025 00:07:57 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35fcfe67dcaa92daec92707019371dd6c15793f8d326a1e2d0d2434dbd35c2b`  
		Last Modified: Sat, 15 Feb 2025 00:07:58 GMT  
		Size: 1.1 MB (1050047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe9af599f16a632d2f7095a66eae673a693b85ebff7f57530d7b7c92e777bf`  
		Last Modified: Sat, 15 Feb 2025 00:07:58 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768b1e3f7c9524ab0ed8549a61794969506c0a5b3999b7be7a96ca53574538a8`  
		Last Modified: Sat, 15 Feb 2025 00:07:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83ebfa2c0189b36f8358b2f4da7e6224129585f232bda561f9024c6f2acb63a`  
		Last Modified: Sat, 15 Feb 2025 00:08:59 GMT  
		Size: 99.1 MB (99087361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3c2413ce5565622ee80d172bfd8f9992e9e64a7d26ed14f1dd753c2391d38d`  
		Last Modified: Sat, 15 Feb 2025 00:08:56 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac66044c5f0ca7f505b29f77795c377b2c912b9a214e96d49b55d0e5b2b8ef0`  
		Last Modified: Sat, 15 Feb 2025 00:08:56 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00daaf27fd0bcc7c6fe15074d27c3af712c11185f503c9636170ad60ce5573f7`  
		Last Modified: Sat, 15 Feb 2025 00:08:57 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56813b2ae08bd8ac8cfaccd6764f71f341026384bd3e5c9b8ee7d127d018324e`  
		Last Modified: Sat, 15 Feb 2025 00:08:57 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0442e9aa5f3d1cd21fa229c3b63e973bae434f03fd2bec7d952226941afcda`  
		Last Modified: Sat, 15 Feb 2025 00:08:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:6164183227b98cb2eadc9e7fed52920e3fecc066242d802d6a93bd937284579d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.5 KB (640456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04035c7606aae10b537dabee4a46e5f69f58b0bf45ecd5827931490f9afe25c3`

```dockerfile
```

-	Layers:
	-	`sha256:8aa6d9d451644f3ec8550190963d6e52d57ce21178a50ffe23f952fc7e3fadac`  
		Last Modified: Sat, 15 Feb 2025 00:08:50 GMT  
		Size: 595.1 KB (595125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88c43e0f74abe01178d38a71c039813eb3d549bf752c1dc80072589f79aeeed1`  
		Last Modified: Sat, 15 Feb 2025 00:08:51 GMT  
		Size: 45.3 KB (45331 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; 386

```console
$ docker pull postgres@sha256:36afafd1c873bf11652a6d1dd47b0da7b611730a85edb081b98a1cfce48d8745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114373591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f335f1dd6e4650533680d945c71cf493c4f6a4b0406c31a4e4466a6303ba32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:17:09 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:17:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_MAJOR=14
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_VERSION=14.16
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_SHA256=673c26f15ebb14306ad0ea051d8acfb3915dd342de942f5b502e5354a0ab760c
# Thu, 13 Feb 2025 18:17:09 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:17:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:17:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:17:09 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:17:09 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:17:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525b09999a3861226d7bf8b980d7b907f0da2be6e03e7fab1a1353c3a7a373b6`  
		Last Modified: Sat, 15 Feb 2025 00:10:19 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5760672701c74588b7c501761e3a3fa1aaf062446c1b8af9907eea7d41af69f`  
		Last Modified: Sat, 15 Feb 2025 00:10:19 GMT  
		Size: 1.1 MB (1095264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbfa4b6de16d022b1325df1e10894eea8629f2d96888b6d20839ef26acacf79`  
		Last Modified: Sat, 15 Feb 2025 00:10:19 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84d11ae63d63d787d200b7efce8e7925079d9f766ded1b1f35e013ac2d9231f`  
		Last Modified: Sat, 15 Feb 2025 00:10:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2437876834c3ae2475fa9047a982ccadb07c13dbf7ef30fb54c957e258185f1`  
		Last Modified: Sat, 15 Feb 2025 00:10:22 GMT  
		Size: 109.8 MB (109798346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a12321ead36b81b2cbfe4aecc10b80399e0b953c80311e6d1202507322fb3c`  
		Last Modified: Sat, 15 Feb 2025 00:10:19 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d69186f179aeb249d5da268c609e138cbf8826c145be3721f0d019ef0a79cf4`  
		Last Modified: Sat, 15 Feb 2025 00:10:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b24bdf08ade335a836530750c127c0d015ec1e78cbd37465a365e51a41cf4e4`  
		Last Modified: Sat, 15 Feb 2025 00:10:19 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f07dcc43e018b9858fc2fdfbc0f27cc21a3627d22802988e171c5eae72c66f`  
		Last Modified: Sat, 15 Feb 2025 00:10:20 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5f5ffd40cc9c2ea6efe612cd7766fa0ef52d5a9eac544bf5949482a8b9a5fe`  
		Last Modified: Sat, 15 Feb 2025 00:10:20 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:3a7c72806aa28d3eb24a9fbebc1def14c32dab933bfc9cf886e37c179eafd6b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.1 KB (640109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af102d49a5e61fd2580ac2ce0bc32f4e9e0b9c090abb2206fec03cbbfb9f2a00`

```dockerfile
```

-	Layers:
	-	`sha256:465e7762a66310245fec95763dba7dd31ab47788647279f2795ac9833f54cb71`  
		Last Modified: Sat, 15 Feb 2025 00:08:52 GMT  
		Size: 595.0 KB (595044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667938d5976c9e0cec1a0cb0cc99236a7cadea09eceb0e6e25ea5fc00086a7f0`  
		Last Modified: Sat, 15 Feb 2025 00:08:52 GMT  
		Size: 45.1 KB (45065 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; ppc64le

```console
$ docker pull postgres@sha256:2123c3647eb119c94e41fc946dd15b6d2932179cf3ef63e477bcbc78bb55e169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91927203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613d33a623cbc0812e38ce07c4011ac617922dc05048ed820f6d579666380407`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:17:09 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:17:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_MAJOR=14
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_VERSION=14.16
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_SHA256=673c26f15ebb14306ad0ea051d8acfb3915dd342de942f5b502e5354a0ab760c
# Thu, 13 Feb 2025 18:17:09 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:17:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:17:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:17:09 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:17:09 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:17:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445e99db265c0b2b24bb099e387b3896a1d680cdf434b8d5fc9b60613f95d401`  
		Last Modified: Sat, 15 Feb 2025 00:10:43 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740c8b42ea00e71e56ee2f8845ddb88b0043664d66dce013e9653781102c9743`  
		Last Modified: Sat, 15 Feb 2025 00:10:43 GMT  
		Size: 1.0 MB (1040364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df5ff7dc3d2a95e98648907460997bb178580f4dc23ed150bc9cd8c4ea47172`  
		Last Modified: Sat, 15 Feb 2025 00:10:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26178a34c59aebd1951ce327448b8ae2028ee840520c620eab51ab9db6be8875`  
		Last Modified: Sat, 15 Feb 2025 00:10:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a414cc5abfc233bc6a69b9a831cb69f65577f53eebe75c52d49cd98ace3214`  
		Last Modified: Sat, 15 Feb 2025 00:10:46 GMT  
		Size: 87.3 MB (87296134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84429a99c6992cef2a9900d6359b6f72cba5852dbf07505374bfb8c87e7f7755`  
		Last Modified: Sat, 15 Feb 2025 00:10:43 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31355442eb715aa36bc5148df983c97fede91150038e63a640e42cb1630afd0`  
		Last Modified: Sat, 15 Feb 2025 00:10:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3203c72e40f41aa1118a7cb52c3cefdc9cbb932fe6476a217483b032ad9cfdc1`  
		Last Modified: Sat, 15 Feb 2025 00:10:43 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e3d2f90b169d42d021296ec9b2736c7909e249e319b197e571c76d4d14f02c`  
		Last Modified: Sat, 15 Feb 2025 00:10:44 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e2e2df63f07c1964824765f9c4e56b2160d39e920e92ba321fe89daefb587a`  
		Last Modified: Sat, 15 Feb 2025 00:10:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:a353e6c150ba36fdc08d56d5ab3c45b7560f7f7daa80566b6b363ac143f9352b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.7 KB (636657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4c69f54fa1f3954c0e02400226555032acf2e07a35fac9098885245a924751`

```dockerfile
```

-	Layers:
	-	`sha256:c69008107c5e35803dbc29c3e3efc242dac585c8b06a952777cea45ebc308907`  
		Last Modified: Sat, 15 Feb 2025 00:08:53 GMT  
		Size: 591.5 KB (591490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c2ec337d44dbfd147e1e3b46c84cc8adfc96e87f78d1a94a424d4f6008d1511`  
		Last Modified: Sat, 15 Feb 2025 00:08:54 GMT  
		Size: 45.2 KB (45167 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; riscv64

```console
$ docker pull postgres@sha256:2faf4b94ee5940a1a9f6f83e97f112d41348fe4f483791daa3e3190abc726d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110519191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed0b375789f747bc163d8cc76f4d84d3a55bf95e79dde75aa503baeda6c1f17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:17:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_MAJOR=14
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_VERSION=14.16
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_SHA256=673c26f15ebb14306ad0ea051d8acfb3915dd342de942f5b502e5354a0ab760c
# Thu, 13 Feb 2025 18:17:09 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:17:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:17:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:17:09 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:17:09 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:17:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa70428e43128e29ea85c02b9ad8867c57f3c57d80ee4c8367e06d1044bc81a`  
		Last Modified: Wed, 15 Jan 2025 02:15:04 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b30861d9a22965c9c8ab0e3148f19b31c48adac4184db37373b16aeb1836e26`  
		Last Modified: Wed, 15 Jan 2025 02:15:04 GMT  
		Size: 1.1 MB (1089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ee96017ef0ba8a5e5adc67c305a2bb47d5c776594a60202ef59765710d8a19`  
		Last Modified: Tue, 14 Jan 2025 23:03:24 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ecc705b39b2ca8d6e5ca7d9227c696d64688b012cc93494869f3a75ac26b68`  
		Last Modified: Tue, 14 Jan 2025 23:03:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b325091a2125809e64cd3f15a290d6cafe3e6c8d682ba751dcde3b3f103a33d8`  
		Last Modified: Fri, 14 Feb 2025 06:27:20 GMT  
		Size: 106.1 MB (106062757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6251fd0502ca4e00c41775fc61c0f7ca2841c70f2a1b38de1873077210c9466e`  
		Last Modified: Fri, 14 Feb 2025 06:27:21 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061492eb24df4723dda26672154544ff5bda4717c3096dd2b788dffdd69c4732`  
		Last Modified: Fri, 14 Feb 2025 06:27:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5940828aebe55d10dc590738b5326ccd0597d3afaa05ac4312d728c0c606c2a`  
		Last Modified: Fri, 14 Feb 2025 06:27:22 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11de768171403daf75677e573361a391e7cc18b61d878437683773d8d896b35`  
		Last Modified: Fri, 14 Feb 2025 04:42:45 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9647609769371f65b16a6c7c4675ecf4e352559ba2cb29a8d0c5f42c34daa1b2`  
		Last Modified: Fri, 14 Feb 2025 06:27:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:340841203e3347e0399fb3992efaa9376dcfcc1a05f572cd8816787879b44387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.3 KB (639336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a44e1ec294a5566cf95026717fc764c1211107eb4714e4363ee80d530a3645`

```dockerfile
```

-	Layers:
	-	`sha256:9508e556d5a42bd823302f31d1b308369f4fbb554997d164dc3d728f45ce990f`  
		Last Modified: Fri, 14 Feb 2025 06:08:01 GMT  
		Size: 594.2 KB (594163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9101575c59483f7f39308a539da72a6b134248ab169b5013762d4f6c1dabcb3c`  
		Last Modified: Fri, 14 Feb 2025 06:08:02 GMT  
		Size: 45.2 KB (45173 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; s390x

```console
$ docker pull postgres@sha256:8ad5fa396c6a1a66e620be4e1e1bd89fc21cea81df4a6c6d3c60a8e72c0ba532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119281013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe735e1b324978a990ef2f7db9f45cdc6135f3086974daf471bd4f88ab462416`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:17:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_MAJOR=14
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_VERSION=14.16
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PG_SHA256=673c26f15ebb14306ad0ea051d8acfb3915dd342de942f5b502e5354a0ab760c
# Thu, 13 Feb 2025 18:17:09 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:17:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:17:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:17:09 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:17:09 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:17:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c56695c85edb37ce406b4667f090721587f7d2dc9452e0ec86dae6902585d0`  
		Last Modified: Wed, 05 Feb 2025 01:05:37 GMT  
		Size: 982.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4ac9ad3604d910dc8b794cb00cccd50d1a63d5ec97b3256b4a8d034e01945e`  
		Last Modified: Wed, 05 Feb 2025 01:30:57 GMT  
		Size: 1.1 MB (1084567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae6505784918dbcf00ac2a80ef08d1b47355616628edee04c6679dbab5f4083`  
		Last Modified: Wed, 05 Feb 2025 01:02:40 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4b1780e171a060bacf653b2becb7b116054fcde6d16bdd688463bb751452d8`  
		Last Modified: Wed, 05 Feb 2025 02:02:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962381b9efb6ea835787c5b5635842bf2f6708e8713478e06607c4e987b33b41`  
		Last Modified: Fri, 14 Feb 2025 03:19:58 GMT  
		Size: 114.7 MB (114713194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8c5e49d4c9a877e95e1e92bff46f8b157d449d12fce227c9ae7bd6f4c06ed1`  
		Last Modified: Fri, 14 Feb 2025 03:19:59 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e371f2f6c61dd8eeab8e6968e402b33fe4cdd72a1bb2f852ac0562fa3b16e80`  
		Last Modified: Fri, 14 Feb 2025 03:20:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3629b6d8061104a8763e899ef027f266d012766bc8a56091f12f9845a575d97a`  
		Last Modified: Fri, 14 Feb 2025 03:20:01 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a07cef34c342be4de62d51a18dac3b1526b652228f47e6e57323afe9f46f6ca`  
		Last Modified: Fri, 14 Feb 2025 03:20:02 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40cc6aed693520afcf2c6203419b824192fdf4f9c447635d3bdbf286f346d8b2`  
		Last Modified: Fri, 14 Feb 2025 03:20:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:6ab5e7fc0f1eb497af5b5b322f3a2031a7454c612d831b884cb56738410c3fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 KB (639246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8387c682a70896a658c6561e2cc9777582ef986a9c8b6e7161a1cd9ec67c790`

```dockerfile
```

-	Layers:
	-	`sha256:bba57cb29608f8847c9b24e7fac3d6d5762cfb3680813843669185d7e2788d9e`  
		Last Modified: Fri, 14 Feb 2025 03:08:39 GMT  
		Size: 594.1 KB (594133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffed0028c424dab55e3c3d96029325b8d31413eb3a65836ea86fcf399642648c`  
		Last Modified: Fri, 14 Feb 2025 03:08:39 GMT  
		Size: 45.1 KB (45113 bytes)  
		MIME: application/vnd.in-toto+json
