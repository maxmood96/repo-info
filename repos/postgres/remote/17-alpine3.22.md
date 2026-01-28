## `postgres:17-alpine3.22`

```console
$ docker pull postgres@sha256:4b0cbeb16d6507544651344dc873324b4a17ab64a07d0a0e0e679cca515c1adb
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

### `postgres:17-alpine3.22` - linux; amd64

```console
$ docker pull postgres@sha256:97e6f8eefd4ef104583526c907efd3212b3276ae384cc6fc176bce84c8694a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110613898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d8abbb835d855022ab3f3ceb1814cc88786a4b110cca864996b1c4713a4a98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:29:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:29:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:29:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:29:43 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:29:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:29:43 GMT
ENV PG_MAJOR=17
# Wed, 28 Jan 2026 02:29:43 GMT
ENV PG_VERSION=17.7
# Wed, 28 Jan 2026 02:29:43 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Wed, 28 Jan 2026 02:29:43 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:32:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:32:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:32:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:32:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:32:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:32:08 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:32:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:32:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:32:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:32:08 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:32:08 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:32:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85aec37af180bb78a134ee2e68a77cd6df92a06cb7e29fd0a7ec07114cf24c47`  
		Last Modified: Wed, 28 Jan 2026 02:32:13 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2201b8e8a61ea7724878c2e3e6efb00ca2d2681ac7866469ca54b0778d7cd530`  
		Last Modified: Wed, 28 Jan 2026 02:32:24 GMT  
		Size: 918.3 KB (918290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26cc44de3968d043bc283cc8783b225c08484af1afcbbd88309f36ea0a6c01a`  
		Last Modified: Wed, 28 Jan 2026 02:32:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cebd94b171b801187cf49eec2cc5d01387892088cf8bdc329d7993f8b7c32b3`  
		Last Modified: Wed, 28 Jan 2026 02:32:26 GMT  
		Size: 105.9 MB (105873436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27c9d73697fc5de5d595c22b5892ea5e8be3a28e6424d0964ab4527fa30168b`  
		Last Modified: Wed, 28 Jan 2026 02:32:23 GMT  
		Size: 9.9 KB (9887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc121384798436e18f65ef4029d54c47e46eefbf787ff569cea79ee9b36718c`  
		Last Modified: Wed, 28 Jan 2026 02:32:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fa2ad95c7a086f61b5402818ddd7a0c6f6836808903f5d1fc7ff4d8dbc2813`  
		Last Modified: Wed, 28 Jan 2026 02:32:25 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93300567c591c35ba5445b27a80a43e0d88dd47ebc94e424bef9475548e3c0ab`  
		Last Modified: Wed, 28 Jan 2026 02:32:25 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99f8849fd36d1dfdbba46aa7a9d2e557f1e23514cd5be3a6ea909d9a671a87e`  
		Last Modified: Wed, 28 Jan 2026 02:32:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:10502fcba713c14b2fee69371c249b51af3dcf0dd9bf6755347819a663bcd6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.4 KB (637368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56ef21d7bbdc8d3150c748d0a6f757b78c6efcd1bc6df57ea20c5955fc94884`

```dockerfile
```

-	Layers:
	-	`sha256:fb396a10865664bde934d0ea5815c569f17812ec7091835df2ec5ebf2e3e3277`  
		Last Modified: Wed, 28 Jan 2026 02:32:24 GMT  
		Size: 596.3 KB (596311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b4e1736ced895c20a70377547f1fc532aaf039532ff84e8727b47df85824b39`  
		Last Modified: Wed, 28 Jan 2026 02:32:23 GMT  
		Size: 41.1 KB (41057 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:08a9b88cf715b6534ca6c72b80f777ff0b8af0fc78b6dbda6524dacc41c711e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90129881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f520b1bd2b0f01d74035d691985ed4483f7368a68f034512e26721658f4fd08e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:16:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:16:43 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:16:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:16:43 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:16:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:16:43 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 19:16:43 GMT
ENV PG_VERSION=17.7
# Fri, 14 Nov 2025 19:16:43 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Fri, 14 Nov 2025 19:16:43 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:19:53 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:19:53 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:19:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:19:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:19:53 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:19:53 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:19:53 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:19:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:19:53 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:19:53 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:19:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:10 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d747b4495e300d8d86bec1f2e70800c38ff0d1629c7cfa79d26535c03ec6ff`  
		Last Modified: Fri, 14 Nov 2025 19:20:04 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea33d9347f314fd31d2580279613454f5a86770ee95b3005e22a0b3ecb43b9f2`  
		Last Modified: Fri, 14 Nov 2025 19:20:04 GMT  
		Size: 886.1 KB (886135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c3319c62b3c16874a4c1cee65de5e835770d43b6248ca033472f0439c6c53e`  
		Last Modified: Fri, 14 Nov 2025 19:20:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75cbe407e19a6f17ff1d22e7c88920ea3b3045d01a632130c09387c91115c24`  
		Last Modified: Fri, 14 Nov 2025 19:20:07 GMT  
		Size: 85.7 MB (85722374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f59dd3c8a1ccb29ed556e1fd6bebec53bce5307691a550eda5954b11a6e11f`  
		Last Modified: Fri, 14 Nov 2025 19:20:05 GMT  
		Size: 9.9 KB (9885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf0f3eed6ef7f7376af061ff70ae24160779f880225df100f1d327c5cbeab37`  
		Last Modified: Fri, 14 Nov 2025 19:20:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78a82204a6a2ef0006d1af9fd7121b6f7d290fd1f2ea3a1404c7b3dfab13f57`  
		Last Modified: Fri, 14 Nov 2025 19:20:06 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25162a5ad9b86f1eb69b7fa0edc9799713996a2483f3368c39ad5c8f6ae67467`  
		Last Modified: Fri, 14 Nov 2025 19:20:06 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92f1814988f2ec9324b890ddc8a26a514d1949382ddf39380003c54798e0e19`  
		Last Modified: Fri, 14 Nov 2025 19:20:07 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:6eecb9d22a9de9e090799759725d52ee795784201a640b5f57901410e2f0a8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 KB (41627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f280b0dac4bc955fe044dd8149ef862587ce95aa12d4cd6a648855c2d01e7b9d`

```dockerfile
```

-	Layers:
	-	`sha256:44e93fdf3ec47638e46629c9ed14f14761c0c30ae446a8dffc07921b15797261`  
		Last Modified: Fri, 14 Nov 2025 19:20:04 GMT  
		Size: 41.6 KB (41627 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:1c8db99a4d9c7908725522dae45e80e1669a6e217bf7c0a72ae379cb689ff7f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85368775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c2c5e3ca5bf0467f934d20fdab9c62c60ff185d1d1f379a8a03483b3589460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:45:17 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:45:21 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:45:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:45:21 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:45:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:45:21 GMT
ENV PG_MAJOR=17
# Wed, 28 Jan 2026 02:45:21 GMT
ENV PG_VERSION=17.7
# Wed, 28 Jan 2026 02:45:21 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Wed, 28 Jan 2026 02:45:21 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:48:32 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:48:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:48:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:48:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:48:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:48:32 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:48:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:48:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:48:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:48:32 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:48:32 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:48:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056a914872caf87ac6394c5831ba45b004ed3d714d61d3b15d17fbdda6f24d47`  
		Last Modified: Wed, 28 Jan 2026 02:48:43 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684ec608444c75ce0bacd7980a71484b3e80210d5b91851b0cf6ea09035e94ef`  
		Last Modified: Wed, 28 Jan 2026 02:48:43 GMT  
		Size: 886.1 KB (886130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6209dd61de38dbd4857eb48beb58a11018dfe905a6f38d7d561d4481b7ac8dd`  
		Last Modified: Wed, 28 Jan 2026 02:48:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d96b6bf6a4daf130d56000c8ba69cf13294a01cac112c257bcb965ee66c5c1`  
		Last Modified: Wed, 28 Jan 2026 02:48:45 GMT  
		Size: 81.2 MB (81241720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60484a1962d16c29ca6d09f69dd139fd16c79b99e6c202bb0f1a4dca1fe1ae52`  
		Last Modified: Wed, 28 Jan 2026 02:48:44 GMT  
		Size: 9.9 KB (9886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497e1f8b55e43479c8e18bde61b0aa366e05e505b7a70f72a125ad0031bfb2f8`  
		Last Modified: Wed, 28 Jan 2026 02:48:45 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad40355c6d65474a653ea086a89dbd706446ce1508a5ed65f40d9d99bd28b3e`  
		Last Modified: Wed, 28 Jan 2026 02:48:45 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed0a699a1f90b9775c5299be3ac1c2baa97512deb9a8e1145fe2c06e7eedff9`  
		Last Modified: Wed, 28 Jan 2026 02:48:46 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58cbffd011d45905dbcd59251c5315dbc0398804d00711b5c9bc8e13d939a16`  
		Last Modified: Wed, 28 Jan 2026 02:48:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:29b571a9a7c6f053af6bc194feec33d55eaa8617f9c67c138076839fe8c65741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.5 KB (637538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1a828294bd9e323ef4654c6a5c2291fe27391730b2e1de74e7aaa52b188cda`

```dockerfile
```

-	Layers:
	-	`sha256:01ada90feadd68ea9f933b659b3e92fb3094821c77680dbab069af942238915f`  
		Last Modified: Wed, 28 Jan 2026 02:48:43 GMT  
		Size: 596.3 KB (596331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a70d96c8a20e5aa5d60205f73b996e47ea4de4b6eb11d5daf6b207792888c31c`  
		Last Modified: Wed, 28 Jan 2026 02:48:43 GMT  
		Size: 41.2 KB (41207 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:1879b6390c3f578c5dd38f1bf6fe3dd92e265dc5ef6960f0e6f8717c97dfe065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106572168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e3c4040b5a9d45c4da7f5ccd81eaf7c006a430c233c61e377e6d3a08bb59fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:31:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:31:51 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:31:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:31:51 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:31:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:31:51 GMT
ENV PG_MAJOR=17
# Wed, 28 Jan 2026 02:31:51 GMT
ENV PG_VERSION=17.7
# Wed, 28 Jan 2026 02:31:51 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Wed, 28 Jan 2026 02:31:51 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:34:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:34:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:34:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:34:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:34:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:34:39 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:34:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:34:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:34:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:34:40 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:34:40 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:34:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196d1623507f672b369af50522d33d6828ec11e44df4cd2405765a1967e8a047`  
		Last Modified: Wed, 28 Jan 2026 02:34:54 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb0d9173de15f29d8c7c6934bfee31faf73e18c322ba3177e901dbc9845b189`  
		Last Modified: Wed, 28 Jan 2026 02:34:55 GMT  
		Size: 873.5 KB (873482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3092db012d8794439381e3c8c951f5c27b80b1f8d5160965cce7b9e079e5558e`  
		Last Modified: Wed, 28 Jan 2026 02:34:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23d63bc332a021e3b8e719496543a26dc851e9b80d00117fc1c0cff43526e1a`  
		Last Modified: Wed, 28 Jan 2026 02:34:57 GMT  
		Size: 101.5 MB (101541882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9577170ec9208a3a1a9f726d7aeaed73dc77bbf3ae8750906350cd7aff204a5`  
		Last Modified: Wed, 28 Jan 2026 02:34:56 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39295bebacb18244ef6586da8012550759dbc6376822737eed863e72863fb775`  
		Last Modified: Wed, 28 Jan 2026 02:34:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df30baae511c4e1a8084cef25689d33bdc18dfb3e69d0c9b63f1e92bcdb9b7b`  
		Last Modified: Wed, 28 Jan 2026 02:34:56 GMT  
		Size: 165.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c1f24ea6bfeb9dcb76859323b4569043325fab624d5f95d76222719e7c7c65`  
		Last Modified: Wed, 28 Jan 2026 02:34:57 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a5f28f1913274dec65600b3ad653ee0edeb8b073b82e7ece33a28f599322e8`  
		Last Modified: Wed, 28 Jan 2026 02:34:57 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:acd97950393175637f17b46fcca5ff5781a7adb7594a271507be53ef1435c079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.6 KB (637585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d754b32ba079a5176fd8cddfffe9f9fd66f5be979588e61aaaa360f1f5d09a`

```dockerfile
```

-	Layers:
	-	`sha256:d92d82ea52084c39c656f5c2e3c781b36bb2db0f0f94e5c03f63c0c1e77317fd`  
		Last Modified: Wed, 28 Jan 2026 02:34:54 GMT  
		Size: 596.3 KB (596343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f88de75e17a6a4a0f7df6f3b2fd2506b1db3cc843b77cbc48132aa874d53e2c`  
		Last Modified: Wed, 28 Jan 2026 02:34:54 GMT  
		Size: 41.2 KB (41242 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:82f71448ef94df4ecb45f6f364d40d355ac38bb56d33a3a4b6a72a94364b3c65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116903344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f58bb444a11029c15a28a8cd7e5ed4ea4492c953f2ee5a702f19c7a0cdb14d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:26:07 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:26:10 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:26:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:26:10 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:26:10 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:26:10 GMT
ENV PG_MAJOR=17
# Wed, 28 Jan 2026 02:26:10 GMT
ENV PG_VERSION=17.7
# Wed, 28 Jan 2026 02:26:10 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Wed, 28 Jan 2026 02:26:10 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:29:02 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:29:02 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:29:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:29:02 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:29:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:29:02 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:29:02 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:29:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:29:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:29:02 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:29:02 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:29:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1095f73bf916bb55248222632efcf742dcbaa82a769f182516f16c70217d8a`  
		Last Modified: Wed, 28 Jan 2026 02:29:18 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f354acacc90cc3005948e0a7391fb4e4ffcb60edf1b11cc9cf68f6d328ee2b2`  
		Last Modified: Wed, 28 Jan 2026 02:29:19 GMT  
		Size: 890.6 KB (890633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fcc18037eaecc30f0f99309f08cc022412f503f6e4ef23b5d2e40d48e40665`  
		Last Modified: Wed, 28 Jan 2026 02:29:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc87a4c36b0bb0dc71c088f1f49b8fb2d090d7b1c541d94cbb627ba0159324f`  
		Last Modified: Wed, 28 Jan 2026 02:29:21 GMT  
		Size: 112.4 MB (112374687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3673f65381471cc301255e1a5dbe1d59f4279d6ba687388de13e8ac7affc1f06`  
		Last Modified: Wed, 28 Jan 2026 02:29:20 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e90722984bc75fd1d17bfb6a58cc84941aba57f3b5ed0914859ed7fbdbb23a1`  
		Last Modified: Wed, 28 Jan 2026 02:29:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de72545f6eb99f1e5bfedd97102bfc4285bfe41d6cba92f9ad717c6fa575c8c`  
		Last Modified: Wed, 28 Jan 2026 02:29:20 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a0c29b578923e98efeaee3f6fb9f5607974aff52b75bf45129e67676afef7c`  
		Last Modified: Wed, 28 Jan 2026 02:29:21 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9c6bd1a5d1020160b15dae8422a1e3885de6fa8d62394abcbe8eb62c55e8a9`  
		Last Modified: Wed, 28 Jan 2026 02:29:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:37b358088de92c2bfe85dc197f44588347a0da077141575b82535c9be42eedc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.3 KB (637317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b106bfeb8793a0bc2384d2a67aab7b8539264d27eb5f20099c19bbd10adf9b8a`

```dockerfile
```

-	Layers:
	-	`sha256:e45f01abfcf794c64ecf6b81a4c8ee0932a16b9709cc85368cff0ca167a50a64`  
		Last Modified: Wed, 28 Jan 2026 02:29:19 GMT  
		Size: 596.3 KB (596296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5060efd4a8aadb0528cc8a53e6c8d3ded058794fc426a027a5f6c5068c42e6e6`  
		Last Modified: Wed, 28 Jan 2026 02:29:18 GMT  
		Size: 41.0 KB (41021 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:1e6b4e8b38644d011835f4d84769b0715175b44e3dba56505d9c3e373e168169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90faebcefaf9dba7f28b2e84a8bd21a89cfad2db147cacae214f684e3ff626fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:33:17 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 03:33:21 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 03:33:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 03:33:21 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 03:33:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 03:33:22 GMT
ENV PG_MAJOR=17
# Wed, 28 Jan 2026 03:33:22 GMT
ENV PG_VERSION=17.7
# Wed, 28 Jan 2026 03:33:22 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Wed, 28 Jan 2026 03:33:22 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 03:40:12 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 03:40:12 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 03:40:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 03:40:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 03:40:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 03:40:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 03:40:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:40:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 03:40:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:40:14 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 03:40:14 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 03:40:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cf718fa459d8840034db063bb9424e81c3d9174a32a4c9dfc267b33036ad07`  
		Last Modified: Wed, 28 Jan 2026 03:36:40 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9227b35430cc92748ff2ebf224e67d8d43cd96411ecdffb11f93f8780a00bd1e`  
		Last Modified: Wed, 28 Jan 2026 03:36:40 GMT  
		Size: 879.0 KB (879034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5804c3d9b1f7ab711750ef41dbdef64801760ee13d225f03da0373cbaf9601a9`  
		Last Modified: Wed, 28 Jan 2026 03:36:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3760bbfa5f1febc2b8741a125f7fff992aaea6eb86c31a6556e71aa1fcab90f5`  
		Last Modified: Wed, 28 Jan 2026 03:40:48 GMT  
		Size: 89.8 MB (89833214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1f66b71f290889c04734ac1c811ce8fb42238727ca3aa26d4f501c32403130`  
		Last Modified: Wed, 28 Jan 2026 03:40:45 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5321c8f39dfaf085e228e2ce52f03de7d64d6fc742c8e7db571833886429ee`  
		Last Modified: Wed, 28 Jan 2026 03:40:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ee79d58eda82175aaad8d8414e38e38fcc78e2b59c70b2402b11f4e477ad5f`  
		Last Modified: Wed, 28 Jan 2026 03:40:45 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e785a0fb94bcc27640e82e7354fd76f3cbec907101bc92315b42a84d480750ac`  
		Last Modified: Wed, 28 Jan 2026 03:40:47 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d4468d4a0b6b48c1b6dc165c51e3d6a620518326b2527b67e49e3d594fbdb3`  
		Last Modified: Wed, 28 Jan 2026 03:40:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:57c23971abc5dc32732424afb302feaa50d345268b631728e59e4a3484d9a53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.8 KB (633818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076e8e4218615e4c7109973fe8a570dba7f8926a2af1d6c5e5037f06ab1d2600`

```dockerfile
```

-	Layers:
	-	`sha256:9fd4890d62f1f02ff89968d5efbbe6f5c93791f72d226f6ca47031c36315eca9`  
		Last Modified: Wed, 28 Jan 2026 03:40:45 GMT  
		Size: 592.7 KB (592720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e5ee343a6746470b10f61f7e191d9f4fe1b387c4f6f6f40dc8833557cd6459d`  
		Last Modified: Wed, 28 Jan 2026 03:40:45 GMT  
		Size: 41.1 KB (41098 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:7c8692da732bc4eec4f757bad5c47d5b8590a04eb3f460a12cc49ecb67f6f7bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110692968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9306a4f63907ad80183d6ec14c3be5b4acb34dadfa14202738a0836761fbd4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 00:10:01 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 00:10:13 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 00:10:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 00:10:13 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 00:10:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 00:10:14 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 00:10:14 GMT
ENV PG_VERSION=17.7
# Fri, 14 Nov 2025 00:10:14 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Fri, 14 Nov 2025 00:10:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 05:01:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 05:01:38 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 05:01:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 05:01:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 05:01:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 05:01:39 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 15 Nov 2025 06:42:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 15 Nov 2025 06:42:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 15 Nov 2025 06:42:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 15 Nov 2025 06:42:25 GMT
STOPSIGNAL SIGINT
# Sat, 15 Nov 2025 06:42:25 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 15 Nov 2025 06:42:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:17:39 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d16d13f9766542076f489b4bde8f2b9299f759730ca1132f12a478b4ab5317`  
		Last Modified: Fri, 14 Nov 2025 01:02:08 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f681bb079be6f40bd7adede139f20494c17a8116703e2d4d80cdafbeac44ec0f`  
		Last Modified: Fri, 14 Nov 2025 01:02:09 GMT  
		Size: 866.6 KB (866631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e52b4b277261b1ac3d2524fe15cdca0bad28cdd8d178e74d9fcdc38870c8f45`  
		Last Modified: Fri, 14 Nov 2025 01:02:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bfee44a95c2692e0be95cd1de3ccf422d1dae2d3106275c20b3fc5c413593a`  
		Last Modified: Fri, 14 Nov 2025 05:04:46 GMT  
		Size: 106.3 MB (106293785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5d54e1613593bfb94c66fd0899c56767ab464a0e5c520206d8de2e3134e7c7`  
		Last Modified: Fri, 14 Nov 2025 05:04:29 GMT  
		Size: 9.9 KB (9892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782122b5d1cc069c59afc87cd1a20b097f6d4332247ba9dccfe974af52d4144`  
		Last Modified: Fri, 14 Nov 2025 05:04:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc9a04bb26a1312b2cfe81cb8b3290a3b5bd5659162af6868ff24ccdba909b4`  
		Last Modified: Fri, 14 Nov 2025 05:04:29 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51acceafee787db144b1f8115258302f3fe54a5b5abe4d922fa3818992b15ae6`  
		Last Modified: Sat, 15 Nov 2025 06:43:41 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7eacdcb01f8e11af93d8386386b56fbf9c6587824351ff15b5b5bd988fe4001`  
		Last Modified: Sat, 15 Nov 2025 06:43:41 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:f3826bc748f178b382b792a22f089463d2f581ab09e54f8d2d8fed7dccd0c9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.7 KB (636746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b2591a1f19eaf3378cf76275024a69c598f31850da66ac8dffe7a0d8a3a662`

```dockerfile
```

-	Layers:
	-	`sha256:df0be019d0918f066f8d55b5698dc5825ec2a09dd7f7e640dd347c468374f6b6`  
		Last Modified: Sat, 15 Nov 2025 06:43:40 GMT  
		Size: 595.0 KB (595010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40d074232820c1151886e4d3850a4a0040ea9e76f37c5d8c14294842c17e2688`  
		Last Modified: Sat, 15 Nov 2025 06:43:40 GMT  
		Size: 41.7 KB (41736 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:9a6d20c8e5a30502fbbbff0dc8e0a8db5c269cc1447a27411196d6da09b38600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119335733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f608de7f8f0d6df607a6e12442c11e40dda431a66e226836e4780b2666720d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 01:24:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 01:24:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 01:24:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 01:24:11 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:15:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:15:53 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 19:15:53 GMT
ENV PG_VERSION=17.7
# Fri, 14 Nov 2025 19:15:53 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Fri, 14 Nov 2025 19:15:53 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:33:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:33:57 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:33:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:33:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:33:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:33:57 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:33:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:33:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:33:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:33:58 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:33:58 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:33:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:18 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d27f93166421531fe4a5435a9bca3ea4e7a361893fc542ed1fd5124e07175f`  
		Last Modified: Fri, 14 Nov 2025 01:27:26 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5428b16fd632d91d3982d2d488bfbd69daf3b4db82a5d75683ec8a2731260b2b`  
		Last Modified: Fri, 14 Nov 2025 01:27:26 GMT  
		Size: 894.4 KB (894417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c27c21eb6784d7fdff28110f50d2f82caadfe48875a7c67cae465d1149a4aae`  
		Last Modified: Fri, 14 Nov 2025 19:19:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e356ee2d0b9c6efd5140b6dda606cc8b4d24a7b56799f4fc7838c3f5f78a03c6`  
		Last Modified: Fri, 14 Nov 2025 19:34:25 GMT  
		Size: 114.8 MB (114774780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23ff3a76b9e5fb887343e1526d8cd05816a25c615bce0d9b3418930c40ca405`  
		Last Modified: Fri, 14 Nov 2025 19:34:21 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232cb81ef013770267183e4a07a17978101f8931eeb60e04bc5d5c2fc8b9ce20`  
		Last Modified: Fri, 14 Nov 2025 19:34:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286eb4cb17a8f2121af656a98941b16ef4660a95f5af5b6a1074ad862aa9006a`  
		Last Modified: Fri, 14 Nov 2025 19:34:21 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc0c372469f52d07f66c97c8a77e8c3353b8986169fc0cf2a016d22a00aae5f`  
		Last Modified: Fri, 14 Nov 2025 19:34:22 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a438a549b252826dbd1deba7329e81001b5ec9ede27452234e0581badee70aa`  
		Last Modified: Fri, 14 Nov 2025 19:34:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:2c5a26e3470208276d98809c9f3355cedb31861647bbecd5049837a06b5c7151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.7 KB (636658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c010cba5c02b2fb21f8177060469aa15e6d9702db1a3fa3228ca10211cf651b1`

```dockerfile
```

-	Layers:
	-	`sha256:8b5a69c8458c70256e2e33d9d22cfe4ab7bc2eb9b1ff9f4457fef02a82fb667c`  
		Last Modified: Fri, 14 Nov 2025 19:34:22 GMT  
		Size: 595.0 KB (594980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3514306b6a716df73c964b516bcd502f2f06fde0cd8c50ab4649d4390ba64c8f`  
		Last Modified: Fri, 14 Nov 2025 19:34:21 GMT  
		Size: 41.7 KB (41678 bytes)  
		MIME: application/vnd.in-toto+json
