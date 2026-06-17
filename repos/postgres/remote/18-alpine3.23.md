## `postgres:18-alpine3.23`

```console
$ docker pull postgres@sha256:c14378294b5806d846c5e659143ab28c04b7000e130deb030a64bd65c854ffcc
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

### `postgres:18-alpine3.23` - linux; amd64

```console
$ docker pull postgres@sha256:c31d2bb4e47fc8305d8ffdc4b27d51646c9c8bb4fabc80918491777ac2b4e1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121977488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8523264eb45ef29566bbc56de2869bbf94fc5644a8f6eebe1feae53fde8c3de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:58:09 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:58:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:58:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:58:12 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:58:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:58:12 GMT
ENV PG_MAJOR=18
# Tue, 16 Jun 2026 22:58:12 GMT
ENV PG_VERSION=18.4
# Tue, 16 Jun 2026 22:58:12 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Tue, 16 Jun 2026 22:58:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:37 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 16 Jun 2026 23:00:37 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:00:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:37 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:37 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f4fdb4f37dcb80e7e9be77bb755f30de1c2cde8b1b5a27f5c77585c567701f`  
		Last Modified: Tue, 16 Jun 2026 23:00:54 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dee13702dcef1fc64b9446afdddba1224c0a8e0c2357efd87ed8d18935297d`  
		Last Modified: Tue, 16 Jun 2026 23:00:54 GMT  
		Size: 919.1 KB (919059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abaa4c89c13d867990812536bb0e9ad52060426e225e3348cbae9ad6790c3d82`  
		Last Modified: Tue, 16 Jun 2026 23:00:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c273d5bfad994051d4698c0e119b61c9c5491d3598ab9b1aa4746cf189518ed`  
		Last Modified: Tue, 16 Jun 2026 23:01:07 GMT  
		Size: 117.2 MB (117167827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58831e0285ea1e1ac5b6c15a2b67b43c19ce53eafbb5aec64d283f8d5039afbf`  
		Last Modified: Tue, 16 Jun 2026 23:00:55 GMT  
		Size: 18.9 KB (18920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4424ddda78af9167d4c6ebf8fcd4caaeed1171be2164159d00d9e2077b695e7`  
		Last Modified: Tue, 16 Jun 2026 23:00:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8f460ca737af581336d2ecc11b0d15b8d571fe4fd391d481608ea0ead6bf20`  
		Last Modified: Tue, 16 Jun 2026 23:00:56 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecafcbdba50cf479e7cbdf7d4d8e9cc1f75f783392d250c8457c63a1eb460838`  
		Last Modified: Tue, 16 Jun 2026 23:00:58 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:49d93b6510db56d2af85b622a8820e2c70ba400dbe5073c249924dc5c6ce0cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.5 KB (656508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd44be3293bbc0ac434e28517fc180d9bdedf036cd51f5f4f99385eff6a460e`

```dockerfile
```

-	Layers:
	-	`sha256:1bc826a8353193aad7456246630a590288593a39cd029e18201438b3406cbe85`  
		Last Modified: Tue, 16 Jun 2026 23:00:54 GMT  
		Size: 616.4 KB (616382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd1517290ef3e8f4349a700a642defce11021ea5d87408e64496c6df34fc3e0`  
		Last Modified: Tue, 16 Jun 2026 23:00:55 GMT  
		Size: 40.1 KB (40126 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; arm variant v6

```console
$ docker pull postgres@sha256:492d23233748b19a1ac19a7eaf2804cf01cd7bf664d5ff16cf1d4869d35c2de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117798066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d46ab4d04734204c93d7a4ee143edc6e215d094488528a09943b83753af4bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:58 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:58:02 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:58:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:58:02 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:58:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:58:02 GMT
ENV PG_MAJOR=18
# Tue, 16 Jun 2026 22:58:02 GMT
ENV PG_VERSION=18.4
# Tue, 16 Jun 2026 22:58:02 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Tue, 16 Jun 2026 22:58:02 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:50 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:50 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:50 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 16 Jun 2026 23:00:50 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:00:50 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:50 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:50 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:50 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd59d2f0dcf84650ba722cc0f3d18f1b89b27985b389ae5c2a83b5d35e308c19`  
		Last Modified: Tue, 16 Jun 2026 23:01:04 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955cbba7221c3dab216cd282da7a5c3e7c080472ab30469c4acc2039d7ea92c7`  
		Last Modified: Tue, 16 Jun 2026 23:01:04 GMT  
		Size: 887.1 KB (887125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248a64a1f5790f4c876b0a63ce2bd0e70f05f12ed182b592a4a43411c54d65c1`  
		Last Modified: Tue, 16 Jun 2026 23:00:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ad61df8077d603a9ce2d391ad4531312d07283721230930aba91d0a53e7607`  
		Last Modified: Tue, 16 Jun 2026 23:01:07 GMT  
		Size: 113.3 MB (113312663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf10ef4cb782c47fd395d95898c888a1867096e28533f3ba0ed659ab0297b57c`  
		Last Modified: Tue, 16 Jun 2026 23:01:05 GMT  
		Size: 18.9 KB (18919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1acda4dd9f4f505835939145da189b04f27432f78a99ec645824e6cce1b6f9`  
		Last Modified: Tue, 16 Jun 2026 23:01:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00dceb1be5689ecf28e36e11a557faeb0cca9f36188bcc0ce710cb05d33e863d`  
		Last Modified: Tue, 16 Jun 2026 23:01:06 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e823efa6d1abaa20346d731138cb0d7a5f0791638e35a1bbf8d869807a6fd1e`  
		Last Modified: Tue, 16 Jun 2026 23:01:07 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:d30cef31b8deeef81213ddda68b5a3ff267717012f003ae4dbe8ed8a4ed0f38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9feea264d77825488de9eb4dcf6afe1d4efb8fc7c9b879df5f06593cf67489`

```dockerfile
```

-	Layers:
	-	`sha256:5da1d037beca7c668a3d8893b4afb9204ab69cdda6fc67708a84e7a954e3a6f3`  
		Last Modified: Tue, 16 Jun 2026 23:01:04 GMT  
		Size: 40.1 KB (40061 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; arm variant v7

```console
$ docker pull postgres@sha256:4fbfcc198b1db3425ea1f0b8df7c62370595fd63d45e152abb31fa580c839051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111212477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546456fef94310c7426c1b74619a3637c53ff6a7abefb591d95e42d869164c74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:42 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:57:45 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:57:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:57:45 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:57:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:57:45 GMT
ENV PG_MAJOR=18
# Tue, 16 Jun 2026 22:57:45 GMT
ENV PG_VERSION=18.4
# Tue, 16 Jun 2026 22:57:45 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Tue, 16 Jun 2026 22:57:45 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:33 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:34 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:34 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:34 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 16 Jun 2026 23:00:34 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:00:34 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:34 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:34 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:34 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:34 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876eb986eeb25e1f3a8d32ab0b9bd468f34b94044ea73b55f92ab2b21058d272`  
		Last Modified: Tue, 16 Jun 2026 23:00:48 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fae3fc34d4b579afd120e1f9a61412f0886e242e91e701317bd131161850ce3`  
		Last Modified: Tue, 16 Jun 2026 23:00:49 GMT  
		Size: 887.1 KB (887125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d0ded4ff4434ec6d6603e04a46121306c924ab90a5ae5de12fee7cb06f8a31`  
		Last Modified: Tue, 16 Jun 2026 23:00:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bbc31b2c17940521b994ae0544aed33302d9ab79eb92e5773e1ffa5d7caf69`  
		Last Modified: Tue, 16 Jun 2026 23:00:52 GMT  
		Size: 107.0 MB (107015807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39da7f4466b6344463c9541a4b436b7b2979212f865ad3f6b7442588d1291e99`  
		Last Modified: Tue, 16 Jun 2026 23:00:49 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f9ea716c3edfb0e13282fbf75b05aa56b96ad41eea4793de3fee51a8e50862`  
		Last Modified: Tue, 16 Jun 2026 23:00:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee4526fe2c00070b8a1201e87cd879277d2524ba0e16eac97a8ff6b1fa8a3e3`  
		Last Modified: Tue, 16 Jun 2026 23:00:50 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fc19d6fd70c8e3670b45dc966fa38deb4dd880c4f0f1b4992a9e5da2dc7d02`  
		Last Modified: Tue, 16 Jun 2026 23:00:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:5ddad0e820aaaa2d90c8bb4915cf872c4717288d14f774418774a92c235198ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.0 KB (656036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1be04e34ea59d5b9b166570c6c99ec43049cfa1bfd2c419b86de6fd52486cab`

```dockerfile
```

-	Layers:
	-	`sha256:7e94463993718416d4e4dc8d245ad61b4f4d4e89ea5697c5bf38fc5211551855`  
		Last Modified: Tue, 16 Jun 2026 23:00:48 GMT  
		Size: 615.8 KB (615760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:926857c6b5c696c585c6d7776ccdb69737b3a0b7583a436ec25e47d984c59370`  
		Last Modified: Tue, 16 Jun 2026 23:00:48 GMT  
		Size: 40.3 KB (40276 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:09b5df7b977ba4ea2e9ac84c30f5093a01b3614b65831fc5ebf44e20df887b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120104994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659891c5569153824509888f6a2dba50b8e174b324b4af3918ac34c97b7b7316`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:50 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:57:53 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:57:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:57:53 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:57:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:57:53 GMT
ENV PG_MAJOR=18
# Tue, 16 Jun 2026 22:57:53 GMT
ENV PG_VERSION=18.4
# Tue, 16 Jun 2026 22:57:53 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Tue, 16 Jun 2026 22:57:53 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:18 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 16 Jun 2026 23:00:18 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:00:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:18 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:18 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d52009b920591c8655c3decd8fa28fa7e458332b406a5a35e0a8c77f7dd18e6`  
		Last Modified: Tue, 16 Jun 2026 23:00:34 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8290c98b2ed52b40d383bfc55576f82fedce324c5e3bd6c873e797dec881842f`  
		Last Modified: Tue, 16 Jun 2026 23:00:34 GMT  
		Size: 874.7 KB (874715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9ee48591084fa70748fd476da612f648db9e2107623d78212aa57aa2094957`  
		Last Modified: Tue, 16 Jun 2026 23:00:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e605676802ffeb7845904541406b289fd923e783a528aee97af9fcbe36b5f220`  
		Last Modified: Tue, 16 Jun 2026 23:00:37 GMT  
		Size: 115.0 MB (115003989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7523697fa4f51667a7d19b126e8e90f63bf27449bd782ebaec9615291a8ccc`  
		Last Modified: Tue, 16 Jun 2026 23:00:36 GMT  
		Size: 18.9 KB (18920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfc226cbd670fb80774fecab367ccb6e0ee41521fae9c8dd4dac624716e6495`  
		Last Modified: Tue, 16 Jun 2026 23:00:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0496bc1b735a56de4eb4e2d071dbb759bb4dad4b0077608dec8727a564de8ebf`  
		Last Modified: Tue, 16 Jun 2026 23:00:37 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5178312aa8156eb4478e70e98cfb38389f339a207172666aeb335443469a06`  
		Last Modified: Tue, 16 Jun 2026 23:00:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:c8c5c614c44a377c1eba9f733a3bc701d8ee9ca2ac3a6a5f070f821305687c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.1 KB (656083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136d598dfe7c6b9ec606d17bf89ec780d7b19faa16e09bb7060272dc4ca87c0c`

```dockerfile
```

-	Layers:
	-	`sha256:5800e8df420929d91841d60787ad8892ee30b528c4340e408cc358336aca9823`  
		Last Modified: Tue, 16 Jun 2026 23:00:34 GMT  
		Size: 615.8 KB (615776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:272d23b881705a253693a95adc6e312a9b8b28e616c5f4e15d0befa663260c5d`  
		Last Modified: Tue, 16 Jun 2026 23:00:34 GMT  
		Size: 40.3 KB (40307 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; 386

```console
$ docker pull postgres@sha256:4926c3f2940005c0e242eedfb5e1fd76a9381441ea9656b7fd79bdc8c7b35d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128588906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05048f4a8f589a242bde4c532d45f3e7db0ad6f4b464976f20ac1e8d0eca8d1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:58:00 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:58:03 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:58:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:58:03 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:58:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:58:03 GMT
ENV PG_MAJOR=18
# Tue, 16 Jun 2026 22:58:03 GMT
ENV PG_VERSION=18.4
# Tue, 16 Jun 2026 22:58:03 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Tue, 16 Jun 2026 22:58:03 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:49 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:49 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:50 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 16 Jun 2026 23:00:50 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:00:50 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:50 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:50 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:50 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7381a73827151d4c90e304bc0b5994d60b7a0a14671e28a334c6afc0821e5a`  
		Last Modified: Tue, 16 Jun 2026 23:01:07 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8be5433388082d9d9648882b0fe3f57c2ad129ba7f8ef727a109e7eeac7b10`  
		Last Modified: Tue, 16 Jun 2026 23:01:07 GMT  
		Size: 891.6 KB (891645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f1e66cb6269a38ef3ec72cf3962db15744503e2d05be8dbb4f3a0a1fec2aca`  
		Last Modified: Tue, 16 Jun 2026 23:01:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95bbc70b77ec9315e6c1e6c129db4b2bb823f9091cbfd7a6d7a28415811f6f7`  
		Last Modified: Tue, 16 Jun 2026 23:01:14 GMT  
		Size: 124.0 MB (123980398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a8789f03ca34ed4a5de08480a83717a1bb5dba8b6934c8463c1d06a74618b2`  
		Last Modified: Tue, 16 Jun 2026 23:01:08 GMT  
		Size: 18.9 KB (18919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1acda4dd9f4f505835939145da189b04f27432f78a99ec645824e6cce1b6f9`  
		Last Modified: Tue, 16 Jun 2026 23:01:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6472d94e2bcfc7ca0fc054474ab44d7c524046ca9c8395e1c502588b8bf01c70`  
		Last Modified: Tue, 16 Jun 2026 23:01:09 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e07202515d89f1325fda8b00c44b20dae8f5ae3f5ab6617655f49a966436a9e`  
		Last Modified: Tue, 16 Jun 2026 23:01:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:46789b5228db1750ec6e6892f7e83585713afa131ae0594bb7a1da7aa89baa37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.4 KB (656449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6304152acc873342a04a3738c6360855394730349476675df385d8154243072`

```dockerfile
```

-	Layers:
	-	`sha256:447150f14e92e19687faefdf0c70e1e1121577c1dba19b238ca9fa1c15c50f4d`  
		Last Modified: Tue, 16 Jun 2026 23:01:07 GMT  
		Size: 616.4 KB (616362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88457e4d065b1ca8b7c17688545d883e21bfc95f81cec629e512fa62a7c3fbb1`  
		Last Modified: Tue, 16 Jun 2026 23:01:07 GMT  
		Size: 40.1 KB (40087 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; ppc64le

```console
$ docker pull postgres@sha256:6286ed11795b788a2d6ee2a52fdf1c253925b547777930dba90acc12ba0d2302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124824582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd334a08910928bcae09b65c3f9ab14c399b94fa6b7f76746e495fda21f21db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:56:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:56:30 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:56:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:56:30 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:56:31 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:56:31 GMT
ENV PG_MAJOR=18
# Tue, 16 Jun 2026 22:56:31 GMT
ENV PG_VERSION=18.4
# Tue, 16 Jun 2026 22:56:31 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Tue, 16 Jun 2026 22:56:31 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:05:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:05:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:05:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:05:48 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 16 Jun 2026 23:05:48 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:05:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:05:49 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:05:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:05:49 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:05:49 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:05:49 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeb214de6218b60491f673adf9db82be71ea034b0f77f7368c52371e738b5b2`  
		Last Modified: Tue, 16 Jun 2026 23:01:33 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6afa0b71083646c91abee705158ea148e7247c5befb4dabd9b4d97a65cfb4b`  
		Last Modified: Tue, 16 Jun 2026 23:01:33 GMT  
		Size: 880.1 KB (880129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301da0e7fa1c03833d438a0704514f0a9b1269117d1e36308f156f140fbd8f27`  
		Last Modified: Tue, 16 Jun 2026 23:01:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32d72cb848f469a83839863b9b0c9e7dd17193428c30a67a353eea4820e444b`  
		Last Modified: Tue, 16 Jun 2026 23:06:25 GMT  
		Size: 120.1 MB (120087097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72e6ad0244478dd05ce90baff7c7e9b05901680b29335fc02a1ba0551dccd50`  
		Last Modified: Tue, 16 Jun 2026 23:06:22 GMT  
		Size: 18.9 KB (18929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10a9fc1572ff176e4a22d95ba31d47d45dc20cb4071b8da61eab26239577b13`  
		Last Modified: Tue, 16 Jun 2026 23:06:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2237098c6a9a928da227f322c7823e8c33e99de81d9f83126bd48224c11fca1`  
		Last Modified: Tue, 16 Jun 2026 23:06:22 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720dd017521059a74f854cb270dcd175cabe9d7f4d6c922f66a15cfef5dd2793`  
		Last Modified: Tue, 16 Jun 2026 23:06:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:5f50a5bdec539435ec2e63571bca6531a451eb9faf16ebc5d5db14c75d56b049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.3 KB (654273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c5a095b6f3f11805ef4538a970054142e902f8febbe7227c722dad064cf065`

```dockerfile
```

-	Layers:
	-	`sha256:c2e0a4ea1bf8a0c9de287bb3714630dce210ef929feeb72491328b1ae6c9b449`  
		Last Modified: Tue, 16 Jun 2026 23:06:22 GMT  
		Size: 614.1 KB (614097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:813f8d8673568ebb31a6ede401c7881036d674d859b9b89d91fe805b097a7bef`  
		Last Modified: Tue, 16 Jun 2026 23:06:22 GMT  
		Size: 40.2 KB (40176 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; riscv64

```console
$ docker pull postgres@sha256:36781805e39edd3876a5892d12f3fbedbed87de29248ad23dc46355c4e69f0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115403494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c79beec488926eb5dc56685c5abc8960b47d3075f67684005484c947e1631e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Sat, 16 May 2026 00:27:17 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 16 May 2026 00:27:27 GMT
ENV GOSU_VERSION=1.19
# Sat, 16 May 2026 00:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 16 May 2026 00:27:27 GMT
ENV LANG=en_US.utf8
# Sat, 16 May 2026 00:27:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 16 May 2026 00:27:28 GMT
ENV PG_MAJOR=18
# Sat, 16 May 2026 00:27:28 GMT
ENV PG_VERSION=18.4
# Sat, 16 May 2026 00:27:28 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Sat, 16 May 2026 00:27:28 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 16 May 2026 01:17:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 16 May 2026 01:17:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 16 May 2026 01:17:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 16 May 2026 01:17:47 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Sat, 16 May 2026 01:17:47 GMT
VOLUME [/var/lib/postgresql]
# Sat, 16 May 2026 01:17:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 16 May 2026 01:17:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 16 May 2026 01:17:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2026 01:17:48 GMT
STOPSIGNAL SIGINT
# Sat, 16 May 2026 01:17:48 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 16 May 2026 01:17:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fc5c0cb4a400efb4e105952285f11d0626c07992180eb0853f87e0ce2f7354`  
		Last Modified: Sat, 16 May 2026 01:20:38 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf44bdc6ba3679d0bd44cb3e7e4489e8861ae94fe90bd24a0ac704d1738e7c6`  
		Last Modified: Sat, 16 May 2026 01:20:39 GMT  
		Size: 867.5 KB (867539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d096693773ef1ab1f365597af46ef410d83ec51c5fce75d9f32918061858a636`  
		Last Modified: Sat, 16 May 2026 01:20:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eea3aea5279cff9c4d7480a101d62d74374764f173b7102993872a920a60a11`  
		Last Modified: Sat, 16 May 2026 01:20:55 GMT  
		Size: 110.9 MB (110921862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d6619c709ead0e87a75696b401159f78a7fda2a45190301d5a3a8a47a1917c`  
		Last Modified: Sat, 16 May 2026 01:20:40 GMT  
		Size: 18.9 KB (18925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba5ebd19a61bef0c27982ff4e96cbd99488438a8f872dfb06355a98e8665d9a`  
		Last Modified: Sat, 16 May 2026 01:20:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0724689426764f0b8a8aad84f25797ec732890d22ed494368384e33ef23e385a`  
		Last Modified: Sat, 16 May 2026 01:20:40 GMT  
		Size: 6.1 KB (6104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c07ed9af6c93a9bc475031f29455711b49b100301abf486acfe6aaafc856cd`  
		Last Modified: Sat, 16 May 2026 01:20:41 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:09465e7bdfeb1a0be90886b14818eae5de602469c2e6fb390db089c75bac8af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.4 KB (659433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5ca3d35f04a13028b2fb733365dad5d2af2ef0b8cd0592154ede15a155e02b`

```dockerfile
```

-	Layers:
	-	`sha256:8840e7a67fce035f5cfa5c2ea699c162a521959817f1548a257ac695042e7e16`  
		Last Modified: Sat, 16 May 2026 01:20:38 GMT  
		Size: 618.3 KB (618317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:511e596eca695ccca2eabab8dfe3e37b8c6dae3ee4283941392a53cd40e9ec6d`  
		Last Modified: Sat, 16 May 2026 01:20:38 GMT  
		Size: 41.1 KB (41116 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; s390x

```console
$ docker pull postgres@sha256:8d9292364775011ae4d40ee46f10137eb8e2a3ca2b6bbc2ea3f01600afaf736a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128350027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7f585adb232ffc12b007afea09cb9f53b9e43de8ee07af34a57363539e89e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:56:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:56:34 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:56:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:56:34 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:56:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:56:34 GMT
ENV PG_MAJOR=18
# Tue, 16 Jun 2026 22:56:34 GMT
ENV PG_VERSION=18.4
# Tue, 16 Jun 2026 22:56:34 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Tue, 16 Jun 2026 22:56:34 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:01:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:01:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:01:15 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:01:15 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 16 Jun 2026 23:01:15 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:01:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:01:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:01:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:01:16 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:01:16 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:01:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a8a72f53607dbf8cd589056be2b745d04ebbaf4d52be196c64bc35bbf95885`  
		Last Modified: Tue, 16 Jun 2026 23:01:40 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11419c9366bc730f0718bf89d5a07be3299457434c8b0b533f803d2c1ba3e62a`  
		Last Modified: Tue, 16 Jun 2026 23:01:40 GMT  
		Size: 895.8 KB (895799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25afd8b2db677bb30b49528aabcdca1265a11efa62c177e4a6416ad35f153003`  
		Last Modified: Tue, 16 Jun 2026 23:01:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aff89054ce1a10722feea289688729fe82f77a7b54c32f8f3be815e8187ee33`  
		Last Modified: Tue, 16 Jun 2026 23:01:42 GMT  
		Size: 123.7 MB (123701278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e103d547144e4798c6c0ad6f8c46bfbf65aba77b297d5b3bda6f1defa6e2a78f`  
		Last Modified: Tue, 16 Jun 2026 23:01:41 GMT  
		Size: 18.9 KB (18919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce56784de5f32274a30d0c61f3326c5d4d8d1dde4ecab0dcc38232846f2f80a`  
		Last Modified: Tue, 16 Jun 2026 23:01:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1d8139aec34fd1602a6b0295970bf54bcd17edd418fcf9179d795de986a328`  
		Last Modified: Tue, 16 Jun 2026 23:01:41 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbf6b56beb6f5f53c19ba1ea301f56fa67227eda39fd77b7beb0c06cfb60921`  
		Last Modified: Tue, 16 Jun 2026 23:01:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:1b7fd9bb142a2d9d34f55fcc887f4849f811c00ccbdeb5b748e7b8a0919d18e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.9 KB (655857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93235e1c4974cf8c547b670310f5c83fb311f0c90e0f50092c68a3fbf87e0568`

```dockerfile
```

-	Layers:
	-	`sha256:d8a357f0f53b06c42494e326ee69bf00f0cfcb50dab6c347886a0c284e6c7b35`  
		Last Modified: Tue, 16 Jun 2026 23:01:40 GMT  
		Size: 615.7 KB (615731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6cc4557cea92567793bc89a91b3414a3006dedffeacd1983112541994da2256`  
		Last Modified: Tue, 16 Jun 2026 23:01:40 GMT  
		Size: 40.1 KB (40126 bytes)  
		MIME: application/vnd.in-toto+json
