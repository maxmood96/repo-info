## `postgres:17-alpine3.21`

```console
$ docker pull postgres@sha256:4c9a29ec48d5636cf6ac1480cf0194417bd999235c65ddf20b92af45f64cd2f0
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

### `postgres:17-alpine3.21` - linux; amd64

```console
$ docker pull postgres@sha256:f52ad28bf25c673f748f9002f553c0c60b0f9c3502034211a305986293ba13de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112885355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bca9c00531eeb3a1194af6e26ac860aa83c8d7b9d94af91f718d4d9a0230d9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=17
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=17.6
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463ca7ced14bd1f040b4430f73a09690c8b5473f1289a793882eab4e2c1dd960`  
		Last Modified: Wed, 01 Oct 2025 00:34:32 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06af10b3be71fa1f1c54491b265e612923a88ad22c7ed21139a247fb0aa75462`  
		Last Modified: Wed, 01 Oct 2025 00:34:33 GMT  
		Size: 915.4 KB (915356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dda958cc04d7f30745eeb87a4bcd51c45327e15ec9cea50a4ec11483219c50`  
		Last Modified: Wed, 01 Oct 2025 00:34:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a714be8c20e5e97b01f80b7e7a0b7004da1e8416baf52d01a5dfa18062d8f9`  
		Last Modified: Wed, 01 Oct 2025 00:34:42 GMT  
		Size: 108.3 MB (108315056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7276c324a73973a5323146f5a5788fa747805eae7e423a18c6ad2c62cd91470`  
		Last Modified: Wed, 01 Oct 2025 00:34:33 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6527d7fc05954332940f4ea88e527ee8ab2f19eaa08247d309a123b04712869`  
		Last Modified: Wed, 01 Oct 2025 00:34:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9a2ce26581a05664e8ca34d53a43808ea4214e5e23321ed459457b8391d4bc`  
		Last Modified: Wed, 01 Oct 2025 00:34:34 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88980a9a752668123a671fe08d9d4bbf24f6d8fb4af1c1dec01f13ad2063001e`  
		Last Modified: Wed, 01 Oct 2025 00:34:34 GMT  
		Size: 5.9 KB (5925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78586b8e52e3e536e745080f4297ad8d234d06fad313f0172e65561b515a853b`  
		Last Modified: Wed, 01 Oct 2025 00:34:34 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:282659fea780a963295d5986fdf63f21199016aec4db210a5f9f01e24fd98d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.8 KB (639789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67b2e392feb77370c844aa005ee12ed51ee4fca032bb2ecf3f2ef836a81a862`

```dockerfile
```

-	Layers:
	-	`sha256:a175a3655834232da6bfee47d850596f7da26b2f8e6ecc52f931851264cedcbe`  
		Last Modified: Wed, 01 Oct 2025 14:15:36 GMT  
		Size: 598.7 KB (598688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91563575895ea85d28b2c1ecf2f922b72a957471e76e2c6abf0c97ecc47efe7a`  
		Last Modified: Wed, 01 Oct 2025 14:15:37 GMT  
		Size: 41.1 KB (41101 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; arm variant v6

```console
$ docker pull postgres@sha256:6bfb61b61c9edd988c90e382dd270e5c308544d415f15970ca7b1f122bba8b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90140840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad2d02011c494303560c6a20e37eca8a000aab32a323c5102eca0598eb47b51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 30 Sep 2025 18:58:13 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=17
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=17.6
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c45f99f36c996df203effa8ac65507799a9dd6a03104282093a4d3ff82a6021`  
		Last Modified: Wed, 08 Oct 2025 22:05:03 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff5536f6f7f722d19c131b1d8b040c09c751b679ca7dc8d7d0d0acd28137782`  
		Last Modified: Wed, 08 Oct 2025 22:05:04 GMT  
		Size: 886.1 KB (886097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c957830ae3f7dc0ad37961f0a258cc595b1041fe4083d58ee0d6cc4814a46e`  
		Last Modified: Wed, 08 Oct 2025 22:05:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1da03d57d06c5c7ea4194cc00d468fe950b4dc528dbf967fad2363fdc9ff9d`  
		Last Modified: Wed, 08 Oct 2025 22:05:12 GMT  
		Size: 85.9 MB (85871911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3d1ac8e3c4ee342b51e5521ee205db891c2c596d9aa62480f049af481fedc0`  
		Last Modified: Wed, 08 Oct 2025 22:05:03 GMT  
		Size: 9.9 KB (9880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e5d26ac1c4e537395c341a249ae8986c9111fe6fe179449ae5a5551dd784db`  
		Last Modified: Wed, 08 Oct 2025 22:05:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2097fa9c13c5705d3149b61f988a579364c9997c22f396cb3d9dccb445d076b7`  
		Last Modified: Wed, 08 Oct 2025 22:05:04 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7f42eaca4a408a5b098bc6c958a4d7bfa25f1eab13677956a190a886059c75`  
		Last Modified: Wed, 08 Oct 2025 22:05:03 GMT  
		Size: 5.9 KB (5923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1615a94f2bf06f4df5fa26e860c00e7af7077023aba5d29b91a14da2f9ed124`  
		Last Modified: Wed, 08 Oct 2025 22:05:03 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:416644c5ebc0461becebc3e5f3b508ad5fbbb8dc6731fa52ad9c2232ff1f79a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 KB (41035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4fbc29c4d97697c8d907600fe8594c488c74ee825712fbf46567813783f451`

```dockerfile
```

-	Layers:
	-	`sha256:c576a86f6b9c4a17a60f16f0c8c03a2345acc75bfd12224eec4c9d698613d898`  
		Last Modified: Wed, 08 Oct 2025 23:11:43 GMT  
		Size: 41.0 KB (41035 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; arm variant v7

```console
$ docker pull postgres@sha256:1892869011ed69a8b4bec201d90ae887592c5e0c8174239eb2ebb9d39094532f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.3 MB (85314317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2be2b0022e4b097ddfb28089ffde40c0047a46400b0fdaa487f768a0558a634`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 30 Sep 2025 18:58:13 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=17
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=17.6
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f446e8a0dbbbb9833091f5756b424b7e3f6ba19cf732624c9b6da449f5111`  
		Last Modified: Wed, 08 Oct 2025 22:07:24 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ef49e0c88cac103d09dd2707a085e88f25a438f1107fc5e743e7303df0f7ca`  
		Last Modified: Wed, 08 Oct 2025 22:07:24 GMT  
		Size: 886.1 KB (886102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d5634b8da0ecfd87fbd321c64ec5ce8e3e6c01528470c91ec938690f18a9b4`  
		Last Modified: Wed, 08 Oct 2025 22:07:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6720c73589463abc575ec8e2047d23247024aabe0c2e28e673eb042bfc887260`  
		Last Modified: Wed, 08 Oct 2025 22:07:31 GMT  
		Size: 81.3 MB (81312223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac00d27ceeb3b549f97621147e8352b8a58f705db8eeb5703819b9cf1ad5127`  
		Last Modified: Wed, 08 Oct 2025 22:07:24 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfacc5109abd853aaed367776fa29a48f4e76bb58ec0d812ef0555c38c2e1141`  
		Last Modified: Wed, 08 Oct 2025 22:07:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b3027fe1e731afd35e183b815dbcefc6c38460cefc1c175dbc870f7f11619a`  
		Last Modified: Wed, 08 Oct 2025 22:07:24 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66068db285d68ad90b9bdfd3efdf47adcfe1431a859b1c1c7c62d99164822468`  
		Last Modified: Wed, 08 Oct 2025 22:07:24 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ed5c0cf297b5a9042507bf320739ae4247cab27b4c6a7c16f16788ae890b08`  
		Last Modified: Wed, 08 Oct 2025 22:07:24 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:239ae86800f4f969b6bda5a39b281c20bd088a08430f2eacfefda8b34292eb5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 KB (639958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce779b4cffa7b89c9b928aa6840c9149ca2565f64d25ea62c0d5fc4dd210274`

```dockerfile
```

-	Layers:
	-	`sha256:1c6b90d5bc98e4f94dfd1bd0ff748e7404d1aef01d1ec2b266ec9bc1ed1c81d4`  
		Last Modified: Wed, 08 Oct 2025 23:11:47 GMT  
		Size: 598.7 KB (598708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:780f127ab37f7a0ae3d117a85cd844577355359a95ad8cd39647b8294900609a`  
		Last Modified: Wed, 08 Oct 2025 23:11:48 GMT  
		Size: 41.2 KB (41250 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:c094cf6a1b1f9396449f0b705da7cb4abe7d245516ee9a309fc1a76917a96a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106505122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a617fa5dcb13c6a09d400d2f1a189da62678d55bd906776a0f7242b1818927b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 30 Sep 2025 18:58:13 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=17
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=17.6
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccb25555adbc0d036c0914fa61ca53fd6722013c75f52eebafb07458f8bdb4a`  
		Last Modified: Wed, 08 Oct 2025 21:43:09 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a569c5fb3f2ba39b1e6a576c962f2bd942b11d5856f9850d707348de2483c1fb`  
		Last Modified: Wed, 08 Oct 2025 21:43:09 GMT  
		Size: 873.5 KB (873463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfff5362f9cf80159f58a8a0d3999674e0ede8fb2598602f5aaf5e4c3184a1c`  
		Last Modified: Wed, 08 Oct 2025 21:43:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffda995a80314c00f019fcb66adb0bec7a9e550fdfd191d33e98f1831be8393`  
		Last Modified: Wed, 08 Oct 2025 21:43:20 GMT  
		Size: 101.6 MB (101621937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e515b70e51452bdcc682a432eb36aa56173452934a247f8ede5b2fe37cc62452`  
		Last Modified: Wed, 08 Oct 2025 21:43:09 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433e590da69a28c2cdb1edc61b4b5604928e8f38d083a901d5ab679053dc2f2d`  
		Last Modified: Wed, 08 Oct 2025 21:43:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5377a732cb560d46e9972e6b5ebd01912cff7b921202fa0035a3d3f3a2378fa8`  
		Last Modified: Wed, 08 Oct 2025 21:43:09 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b31b955a366f7741cc09319888a66176a4eac7e4e6234de95a1878d3bfcf09`  
		Last Modified: Wed, 08 Oct 2025 21:43:09 GMT  
		Size: 5.9 KB (5923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb064ea11cfb43c4a67d1f71252d2aa48efa33ecc861105f0ae5ec2ee6cff356`  
		Last Modified: Wed, 08 Oct 2025 21:43:09 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:703fc64bc6019b638f57a5c516250d0eac58f6f21972ccd19b33880db36d00b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 KB (640006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df2e17e9614523a00ad5811224873ae15c37087e78bc8905acbbb77c7325d64`

```dockerfile
```

-	Layers:
	-	`sha256:c5114fa773d284c6585e672f84e66efd34764df1cc3aac4a69e7156c6e3a4b47`  
		Last Modified: Wed, 08 Oct 2025 23:11:51 GMT  
		Size: 598.7 KB (598720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c5dcb1250d39ac4562d0f81d2cbcc937be2bea5ae813879cbe97dcf1916201c`  
		Last Modified: Wed, 08 Oct 2025 23:11:52 GMT  
		Size: 41.3 KB (41286 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; 386

```console
$ docker pull postgres@sha256:0244eef50d64a8b6cb3fa4e2771388115a77d4481a0f6026b230ed8f47f603ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116778805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab590d200fd688bbf61257e90ed6eba8708546e0607b1f2d7f547a8e7605ae9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 30 Sep 2025 18:58:13 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=17
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=17.6
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c65ad99693d8ee85d97b13a00eb581fa664748747665a0d0de5fb13ec5ff207`  
		Last Modified: Wed, 08 Oct 2025 21:39:12 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395299b12983c3f29a4bcb495b8b39872654bedbd8f70ae30a4e37b7559b2617`  
		Last Modified: Wed, 08 Oct 2025 21:39:12 GMT  
		Size: 890.6 KB (890612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a337f0eaa8e574023472f5fbfdfcb2b2bbf63382cce775632d1c03e612ab6d5`  
		Last Modified: Wed, 08 Oct 2025 21:39:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cf5c062cb781b800ce127854693f123de0272be4ba94ddb5dbdb9546870df4`  
		Last Modified: Wed, 08 Oct 2025 21:39:40 GMT  
		Size: 112.4 MB (112406108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e437cd5044bb23851f15c114b4cdc2a64b4cdc1abb216132a044080e15f9be`  
		Last Modified: Wed, 08 Oct 2025 21:39:14 GMT  
		Size: 9.9 KB (9885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094655078cb93d93f4141bda6dbb02ba7c40ce75cd2a8c62a226a12e468ffec2`  
		Last Modified: Wed, 08 Oct 2025 21:39:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d415c9b4955624227422fe5c02a0654247aab04416a7fa270472cc1cfe13a1aa`  
		Last Modified: Wed, 08 Oct 2025 21:39:15 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6753c928eb8175bb47d1c34338604e13afafec90931c02774ad51219571d5f85`  
		Last Modified: Wed, 08 Oct 2025 21:39:15 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5238278f4652e21a6d85b14a96cb1ecf8624210c663eda1f4338840f66d71ab4`  
		Last Modified: Wed, 08 Oct 2025 21:39:09 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:914151c65bcec84ed7ef48d48227aaacf8e70ea96087a20e43990784b814fc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.7 KB (639737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d992f17097fdf0a59473d049f7c49989abe92da12a3fbcc26bae8e411e34461`

```dockerfile
```

-	Layers:
	-	`sha256:19eb6f0726cf2f7becf7dc96bfca116d43adbcc64e5d49cfd95c221fac10e374`  
		Last Modified: Wed, 08 Oct 2025 23:11:55 GMT  
		Size: 598.7 KB (598673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c39b39948d6eda3ba525a2be092614e6a25125c9648a7a85b8080b5709dc11`  
		Last Modified: Wed, 08 Oct 2025 23:11:56 GMT  
		Size: 41.1 KB (41064 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; ppc64le

```console
$ docker pull postgres@sha256:dfaab808273207f9f24e5dc91735d0fb0f616ac613308d18cb0edfdb9cc53b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96585185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9162194ccfa0d1060103a9c4840a3c472682c72f4bf01a980788094d32fe72be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=17
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=17.6
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747bf6778b8e7ed31d4743686f1f50485c5c074620417743c59a087cdb5f9186`  
		Last Modified: Wed, 01 Oct 2025 08:36:58 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ded0eec492104ecd2eae20f50bf37ad15ee8c2428edc86b79a41ad80e9addb`  
		Last Modified: Wed, 01 Oct 2025 08:36:58 GMT  
		Size: 873.8 KB (873763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945b6b6d1d53681606965ab264b776b8bb57d1abfef335c32cdd28e6de23f19f`  
		Last Modified: Wed, 01 Oct 2025 08:36:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c971105d6e3a92ea54ecffa0628cbdd73c0fb5ba3486c5f8efcaf5836d19a38`  
		Last Modified: Wed, 01 Oct 2025 08:45:11 GMT  
		Size: 92.1 MB (92124903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761183bfe25add963c67b5c178fabf35320b33dad546b8fc6582bad50459ee1f`  
		Last Modified: Wed, 01 Oct 2025 08:45:03 GMT  
		Size: 9.9 KB (9892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f053c524d9d61a27bb0806da773809a357505d75837d7913671475b7588deb7`  
		Last Modified: Wed, 01 Oct 2025 08:45:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcfdd7d894ff140015c92a4bf98dfe5927d18eba36654f29c6b3fdf9ed9dbf6`  
		Last Modified: Wed, 01 Oct 2025 08:45:03 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b076405eb2d851d60e8117a508305e67b6d0f7a7ceae49a590b80d7ad4296b30`  
		Last Modified: Wed, 01 Oct 2025 08:44:59 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b199180818b39a4b7447f0fa02d051e6e33c260c4f4b6796d09b274d294284`  
		Last Modified: Wed, 01 Oct 2025 08:44:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:eefaccc00a91ed06050c88fac176f1b5ae174a78ed508d048b4a6ea4a60c6ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.2 KB (636238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72913b2c90d2e40b7047dd0aba537747bda64385bd9119bac4c4768bb92ee85e`

```dockerfile
```

-	Layers:
	-	`sha256:bb3ae6cbe65bd1fdc074adde7886e9e4c47c837a43d70631440a6a09d1637943`  
		Last Modified: Wed, 01 Oct 2025 20:16:07 GMT  
		Size: 595.1 KB (595097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8a6ca62de12b8444fee26e5a0c2b25ad23b10899f751c748da509031435b403`  
		Last Modified: Wed, 01 Oct 2025 20:16:07 GMT  
		Size: 41.1 KB (41141 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; riscv64

```console
$ docker pull postgres@sha256:2ca5919df55cf3f194e47bef7c91fc99f5053e9688d804910ca3c7b437fd67d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112635470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a12e89a4416524e119841b5a4b4846af45601b39e55511f5cf03cdad3fbeebe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=17
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=17.6
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f442f14b9fc184be7b5b23f9b5362306d14b41b75f0fc847fcc5851ab3402e5`  
		Last Modified: Wed, 24 Sep 2025 00:47:22 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a806fe08f5cb13a300574c46c89d7d784c57ea301fece231af5a28695589eac`  
		Last Modified: Wed, 24 Sep 2025 00:47:23 GMT  
		Size: 860.8 KB (860848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb7abe1548e88b5e00e91420dec591721dc5e28906366569ea3c754484cf079`  
		Last Modified: Wed, 24 Sep 2025 00:47:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05d4fc0d0f0dca006624904475282e768075a2b1ca394743405327ea02e6eb8`  
		Last Modified: Thu, 02 Oct 2025 16:55:06 GMT  
		Size: 108.4 MB (108408142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87901a15ab00df826e65f9ddeb85a699907bc59d7b0e11d480ca2bf2bed60ada`  
		Last Modified: Thu, 02 Oct 2025 16:54:59 GMT  
		Size: 9.9 KB (9890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78297bf6b5e7d8730c84555fcf3515ee54fca0a34f60b57a3e21762028dd0dd1`  
		Last Modified: Thu, 02 Oct 2025 16:54:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8273715c3151396b0454aab99ffbb69fb930ffd05492b3568ed954d4a8c95f`  
		Last Modified: Thu, 02 Oct 2025 16:54:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07392e697c23b9db96e8dad3562e7a1994e4535e365a14f518343c3135c9ee9f`  
		Last Modified: Thu, 02 Oct 2025 16:54:59 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018cb8069302199dbca7e0c29108502d8817137bf2a3df44278565707d7c51e4`  
		Last Modified: Thu, 02 Oct 2025 16:54:59 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:2b4898f89c88727d53b5c2261f4e2198849735e78dddc0ff3a2e94f81d6749cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.9 KB (637902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772d8972467f459bd7ad2db3b91a71190388fa0b805a9f7138acf6d818b18e4e`

```dockerfile
```

-	Layers:
	-	`sha256:f5be591910a8d7876d2b51d2fd48e4f12a3aaad2d0ffe687ec7c2c194a2a2dae`  
		Last Modified: Thu, 02 Oct 2025 20:09:13 GMT  
		Size: 596.8 KB (596755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12cb098b88c1ba0b4edf49395b3c4344ad21ee4abd8350db8ca2bcb28d337c53`  
		Last Modified: Thu, 02 Oct 2025 20:09:14 GMT  
		Size: 41.1 KB (41147 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; s390x

```console
$ docker pull postgres@sha256:8f81145dc6e542a769db51ef51512f6a316c61f05d9bd56c8b2688d1be3d6af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121250224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598bc8dbff140e2fcd38d316b0baebc3f564f60b2af92cf6be096b789219639b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=17
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=17.6
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3a0b3e42a00821c504172afe5ad33497b04821fb945d8f1762c22b804de062`  
		Last Modified: Tue, 23 Sep 2025 22:00:10 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfde9cde752b53d44f7ef28a4eaabe5d98c6054f6df4adb3d525fe6d7846494`  
		Last Modified: Wed, 01 Oct 2025 04:51:03 GMT  
		Size: 891.2 KB (891242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84ebe1c43984ac63d7ccb1f231905711b31a9170693143fcb9b288eb62b2ab6`  
		Last Modified: Wed, 01 Oct 2025 04:51:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e67674d3fc62a8bc9a1dd61bffd0e6d7de02b1abb31dd1f48d0e1e9ccb06a6`  
		Last Modified: Wed, 01 Oct 2025 05:00:13 GMT  
		Size: 116.9 MB (116879502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f564f7ea052b6fd9af94743f12bb90d0fc4c145ce5a55819cc74ff9edd8076`  
		Last Modified: Wed, 01 Oct 2025 05:00:05 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74caff874eda4908291c1f89f87a83cdc1ce3c3c4e14036e93086784db2a90e0`  
		Last Modified: Wed, 01 Oct 2025 05:00:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29deb8cc8cf589c51d3958688ccec396f0e712d5ff5c2af433df8246542e4446`  
		Last Modified: Wed, 01 Oct 2025 05:00:05 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f350b041ed188ee1d7fb753e33f5d6064960f134df35402e4e12ccc46c708d4f`  
		Last Modified: Wed, 01 Oct 2025 05:00:05 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79456e996181f28a112f2159b2599a78acb2bbdc7672adf70242cbc3363a8645`  
		Last Modified: Wed, 01 Oct 2025 05:00:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:7530dc3b2789273f479deb5ce89cfac23d508fe9a865b5ddfc1b4b648778a7fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.8 KB (637838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1724e96479a70c796ca2e5de2fde339511102a48f0828f6409cf20fbc818cdf0`

```dockerfile
```

-	Layers:
	-	`sha256:0aeea3d885024404dc6b876e97b7f8a6e86bd2f56f69e7932ca52a027145c859`  
		Last Modified: Wed, 01 Oct 2025 20:16:13 GMT  
		Size: 596.7 KB (596737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:907f40a4273cffe78b350480eca792be9642571cc4fdda2edd325c8bf593d9ca`  
		Last Modified: Wed, 01 Oct 2025 20:16:14 GMT  
		Size: 41.1 KB (41101 bytes)  
		MIME: application/vnd.in-toto+json
