## `postgres:16-alpine3.20`

```console
$ docker pull postgres@sha256:ec6bbb8cb912be8fc882bc89ebd7bd5a43ed9e7fb2491013aeed60dc67fec837
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

### `postgres:16-alpine3.20` - linux; amd64

```console
$ docker pull postgres@sha256:c137164dd3c47df166864befaf7dba5da8f564bcb16f74d72537abfff34bcb93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97257466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb295c20d6c83e678c3047bcdbbcc76441a8bd33f277dec8c406f550a4861585`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 18:32:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_MAJOR=16
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_VERSION=16.9
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_SHA256=07c00fb824df0a0c295f249f44691b86e3266753b380c96f633c3311e10bd005
# Thu, 08 May 2025 18:32:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 18:32:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 18:32:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 18:32:48 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 18:32:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 18:32:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 18:32:48 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 18:32:48 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 18:32:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4042a856b0567ea6e33a8f887fc795963cd3f4dcfd1b50d91f87c5a3149e52f`  
		Last Modified: Thu, 08 May 2025 19:18:47 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d3cb86f5c16a311ab5e45b275bf4494d870e589a79f2ab6dcb9d995efc4792`  
		Last Modified: Thu, 08 May 2025 20:19:57 GMT  
		Size: 1.1 MB (1120284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa60f157e270db2d32b72127a5f0941b6e5919b1df0a82b9f7111e08c9810d8e`  
		Last Modified: Thu, 08 May 2025 20:19:57 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe9344ac2ba97b5228099b74cc6303338b2398e6c2fcf6ff6f1ad04ec3300db`  
		Last Modified: Thu, 08 May 2025 20:16:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ba9ca82ead4c37715a408049ede20386337e6720a691e5857ca502f5fe5341`  
		Last Modified: Thu, 08 May 2025 20:20:08 GMT  
		Size: 92.5 MB (92493493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8539a1c2fe3bce0699d1905cd2da0044b07c4a2f3ee205b5b845eae14dab5850`  
		Last Modified: Thu, 08 May 2025 20:19:57 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7435f7dfe9b538ebc0f44f60a4459844a8e4010df5e131900812fec7fda466f4`  
		Last Modified: Thu, 08 May 2025 20:19:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61fc15c7fc2142e7850e080385d0f4b3632f1104cefb6d0db1184f63322a4df`  
		Last Modified: Thu, 08 May 2025 20:19:59 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4e0a4db29b45489f49d72f30b88606dda38ee0d5d51f99304295792dc4406b`  
		Last Modified: Thu, 08 May 2025 20:20:00 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ebd91263e38f17a092fa039d719160252a027c938a718c11f15c8333e639f2`  
		Last Modified: Thu, 08 May 2025 20:20:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:35883c9fb5c93308855d0cefdfe4633de742f40ea6e7fb9263eb77918332c702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.2 KB (633163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745a390112037520d863375a1edbaa833e4800d67bc1da95438071315ae6ad70`

```dockerfile
```

-	Layers:
	-	`sha256:c6bd557c1afec6f4c388fcfb1c6fad400346cef78e4ba578443b3394e9904512`  
		Last Modified: Thu, 08 May 2025 20:12:09 GMT  
		Size: 589.4 KB (589350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6960923a74643829b0bca11e2bd22b1af60e0228825cf772dd4bce8612acf608`  
		Last Modified: Thu, 08 May 2025 20:12:09 GMT  
		Size: 43.8 KB (43813 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:b0bf1f9825307a6fce8e92a282c933d458c66d15ee135ac8472aa1bcb2b3f381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95923588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3916e63f74c0ef4ba53e1f09e444724ccc3dd47037f41042533695c00dd6374`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 18:32:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_MAJOR=16
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_VERSION=16.9
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_SHA256=07c00fb824df0a0c295f249f44691b86e3266753b380c96f633c3311e10bd005
# Thu, 08 May 2025 18:32:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 18:32:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 18:32:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 18:32:48 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 18:32:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 18:32:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 18:32:48 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 18:32:48 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 18:32:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 19:26:24 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f562bdeccc677affba17117a3e71eed437842fbd24407b2ce425aa5819d3dab5`  
		Last Modified: Sat, 15 Feb 2025 00:09:21 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c15f54b7c7b9df1d9b4f973855ca80d075a47a5343b27c0f6e4ae7774389b5`  
		Last Modified: Sat, 15 Feb 2025 00:09:21 GMT  
		Size: 1.1 MB (1086525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d568e84a40aff368bdcb0f2c0209c899ecf6614f22d843f7855cc038d42ed61d`  
		Last Modified: Sat, 15 Feb 2025 00:09:21 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464e90337bafdf4dac44e92da85d96c873b18c4c579abd3dd0ee24ba0ae61dc9`  
		Last Modified: Sat, 15 Feb 2025 00:09:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ce71e3a85090dd874ba2e889910ebad2e1847ae79487f7b22400aca8b6155f`  
		Last Modified: Thu, 08 May 2025 20:14:12 GMT  
		Size: 91.4 MB (91447741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e772523af2a07d406640a7b9963b6208d9b70ce1400888a4c6161aca59d4317a`  
		Last Modified: Thu, 08 May 2025 19:28:31 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318881ddf2ec3e3be7beb4dfe52d1883d80b366329993cf285e70755594a2eae`  
		Last Modified: Thu, 08 May 2025 19:28:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d31ac2182feae917647c1c1658b3bc209c560084383fa631e7d0d759971e51b`  
		Last Modified: Thu, 08 May 2025 19:28:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e110a8832bf2f6d813a4933e79964190085bf726165c0d1eb41651b4c751f8b`  
		Last Modified: Thu, 08 May 2025 19:28:34 GMT  
		Size: 5.5 KB (5472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d13264e439635435c460f3667ae28a68f574a8dfa2f6847102b482b8c5ecc3`  
		Last Modified: Thu, 08 May 2025 19:28:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:7508c886ed2d75512697b1340e632f70b9bfcb02632d0657c77bc096ff93b418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 KB (43762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8387cdfa9d28d2e72f4a45a0c2076ff9f29d66bc718e4333a125f0549394b720`

```dockerfile
```

-	Layers:
	-	`sha256:deb53c17f21d05e8c0f3bf75337daf63a6a6b5015766ab0cb6fc3e18526dd1c3`  
		Last Modified: Thu, 08 May 2025 20:12:12 GMT  
		Size: 43.8 KB (43762 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:fdcaa87dfd9b972a990886dbd590a9d61e3327119574c1b99bcce41b3685173e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90173876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b585e8db75cf5f219d94a40fcf003216d5e42c751e2156010906d5072a58763`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=16
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=16.8
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_SHA256=9468083a56ce0ee7d294601b74dad3dd9fc69d87aff61f0a9fb63c813ff7efd8
# Thu, 27 Feb 2025 00:53:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 14:35:10 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25896e659de9add0d4b908897850cbf64b7928b4104747d7d2f865d03c785b5e`  
		Last Modified: Sat, 15 Feb 2025 00:24:03 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f74483a18f569a1fa2c939344a028b1612c307bf93662a4fdaf02c3f961ae8e`  
		Last Modified: Sat, 15 Feb 2025 00:23:59 GMT  
		Size: 1.1 MB (1086514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eadf93718700a6ae0148ccbb835c2325930ee0d12ad9dac188ce36572109a18`  
		Last Modified: Sat, 15 Feb 2025 00:23:55 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b8c5e4ce7a3e3769bc68c603e910cda8c227d7c7644ade020fd071c0811efb`  
		Last Modified: Sat, 15 Feb 2025 00:23:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a0d77a6a745d294f6e8c8c16aceda24cfbab54b7eb53448cd02dbb7ebe6f5a`  
		Last Modified: Thu, 08 May 2025 21:22:06 GMT  
		Size: 86.0 MB (85974590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6ac0f4da2e2eec1c770601dfabfe33e69e0e51bde121c8fd85dea29cdf1d64`  
		Last Modified: Thu, 08 May 2025 21:22:01 GMT  
		Size: 9.6 KB (9563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cf74dd7bcc31c1d7abf04cb890b8dba0ee6fc00ceaa33fb0c27f1c50ee33ae`  
		Last Modified: Thu, 08 May 2025 21:22:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3672a8fbfc42ac997d1c8ca1ac2e6bb77307d8a37eb026c397d0e71e16322551`  
		Last Modified: Thu, 08 May 2025 21:22:02 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e774ddf3047e3c551dde2278b359b6f0458ba63c25d3e78b06b2ba64c00f4a92`  
		Last Modified: Thu, 08 May 2025 21:22:02 GMT  
		Size: 5.5 KB (5476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5a0d7c2d0decb2f58d66f621ed9b779e73cfcd9766d4ee8d94315fa23f4a6d`  
		Last Modified: Thu, 08 May 2025 21:22:03 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:f75e9d1548dc9dd7571e222f1e463440a8ac9c9e2588430cb68f45a5a43699fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.4 KB (634419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77eaf4b6cc04881aab949e4b3eb1c9a0b25ccfd58fe736007396284627b543dd`

```dockerfile
```

-	Layers:
	-	`sha256:fc310b7e7014d2e8ae23ba3f3111c5173ccca28bc69df03128d43c39f414a4c3`  
		Last Modified: Thu, 08 May 2025 20:12:14 GMT  
		Size: 589.5 KB (589542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeef54e6c9f2576670fb3778a14930546dc23b68e49d22557de3ac390aca921d`  
		Last Modified: Thu, 08 May 2025 20:12:15 GMT  
		Size: 44.9 KB (44877 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:612f02d6f57c00b4214f3cbc8d9d09767b56ce1cae1e64f57b2efd4f80203e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96492224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5e2a5f839e4a4cb6fe4dba1b5517494fa8e152841d20deaba46c6154130828`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 18:32:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_MAJOR=16
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_VERSION=16.9
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_SHA256=07c00fb824df0a0c295f249f44691b86e3266753b380c96f633c3311e10bd005
# Thu, 08 May 2025 18:32:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 18:32:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 18:32:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 18:32:48 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 18:32:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 18:32:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 18:32:48 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 18:32:48 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 18:32:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b949cfa537b4b00f0c9fbb677fc05c7340a9657a97f297f1ac99fcaedde0ca1b`  
		Last Modified: Thu, 08 May 2025 19:25:42 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f90ded49ab5b36051bb7de88892fda63b83f028c323214c600f11bd1ec362b`  
		Last Modified: Thu, 08 May 2025 19:25:44 GMT  
		Size: 1.0 MB (1049758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01c3bb46b836e40a11842cb587f914d8028b6e8520d3ab4453596583955efbf`  
		Last Modified: Thu, 08 May 2025 19:33:02 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8041779c1e5633fd28783dae293287d6f5e5787aae2031a35c0d61c00eb9a651`  
		Last Modified: Thu, 08 May 2025 19:33:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259cf1fc42f4052bee832da385ec5463b9e060d3acfc6d86140b3ac5ecbce3ff`  
		Last Modified: Thu, 08 May 2025 19:33:16 GMT  
		Size: 91.3 MB (91334514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916217254c736d7b36fa56a06ea241a82de7487cc2c76ae3b9b0998d4023ab46`  
		Last Modified: Thu, 08 May 2025 19:33:04 GMT  
		Size: 9.6 KB (9562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be3bff94e2a2efd8795856d8bcbcf94304ecc551930143eef568b048a2c6852`  
		Last Modified: Thu, 08 May 2025 19:33:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8d8aba8d4d44a77472790ed6e1a4682d41033a54db65017707f8306739730a`  
		Last Modified: Thu, 08 May 2025 19:33:04 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fd20f22b9d572b732bc9d8ce8228fb4223e75ac4f911a368d2836d55075805`  
		Last Modified: Thu, 08 May 2025 19:33:05 GMT  
		Size: 5.5 KB (5472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc7faa6154f09e72519b5459668b60ec76ec21a79d67c6121cb22f2e4a728c0`  
		Last Modified: Thu, 08 May 2025 19:33:05 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:77f94883cf7460e723da195537a171aa97458047e41815d15818aa220ac7890b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.4 KB (633395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70a3e7e703f9d5412d40ca2305bbdcc4c94dd23edeb508f7fdcd4a8309ae58e`

```dockerfile
```

-	Layers:
	-	`sha256:5873f8426b44df423b20b0d87ba71505102b3fe993b611a1da4ade762ac2a3da`  
		Last Modified: Thu, 08 May 2025 20:12:17 GMT  
		Size: 589.4 KB (589382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1a6a9b744040bfd7ddc1d3c0dab2ee8e99ea4b0db6aa9bdb7090d6ac3f6749a`  
		Last Modified: Thu, 08 May 2025 20:12:18 GMT  
		Size: 44.0 KB (44013 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:e29176478d8dee91090c77a14c17e7a778a402287cb493760ebdcbbb7cc15532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102555517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ecf0c2de35bb23aceb416984894998eb0f56e8eeb56b5ae8edf0a68d2f2f9c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 18:32:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_MAJOR=16
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_VERSION=16.9
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_SHA256=07c00fb824df0a0c295f249f44691b86e3266753b380c96f633c3311e10bd005
# Thu, 08 May 2025 18:32:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 18:32:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 18:32:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 18:32:48 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 18:32:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 18:32:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 18:32:48 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 18:32:48 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 18:32:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 14:36:27 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85cb74f368c228299d69552137a0251b3e2858145103bda233b04724ba98246a`  
		Last Modified: Thu, 08 May 2025 20:21:00 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d291b8453dbf0e3c9029576fb93af2e056b41f4f8b37b5df8a04305660c0c4`  
		Last Modified: Thu, 08 May 2025 19:19:18 GMT  
		Size: 1.1 MB (1095374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42748a90da279705c30b410b765916b762fb653b34d17911b6c4d9b605075ce4`  
		Last Modified: Thu, 08 May 2025 19:19:19 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a81f3f0f5a42937146d4dc1eb6c3cf98156d7ce9b36b9ed180b8753bf26ffb`  
		Last Modified: Thu, 08 May 2025 20:16:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d19d935e87aaf62cc759b194e1a45ff2df22cf897f96ef0714d47ebf6fe86`  
		Last Modified: Thu, 08 May 2025 19:19:34 GMT  
		Size: 98.0 MB (97971688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a60505d9711fe537cd7fecbe506f95b6ec427d75c52a2af864fe9c5cfe9f99d`  
		Last Modified: Thu, 08 May 2025 19:19:20 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08cff261d431c6755a4fe1cf4aee3c31040a6007a6e548304dd0e81f138a3f9`  
		Last Modified: Thu, 08 May 2025 19:19:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2a19cb73683eceb509aa4d6e92ace551a56cf7dbffd28df6b9a0ee6be1e936`  
		Last Modified: Thu, 08 May 2025 20:21:03 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bc48153fb92c76d219d57dbd010cdb85ab7fa0fdb7938d66089a1d91eb6164`  
		Last Modified: Thu, 08 May 2025 20:21:03 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9789c3a1ed1c1f250ab90f25bc87a83e8b5f9757ae5439e9b587ad43aeda410`  
		Last Modified: Thu, 08 May 2025 20:21:03 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:a1aa8f962b462e1392c2b45b5f51699c8b0c93c12a13753618df088f1ee94ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.1 KB (633110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4977dee2c26b96e751fcd29772f1f8a82da8f6307f9251782ac067cdedc0eca`

```dockerfile
```

-	Layers:
	-	`sha256:626c2f386115348055e44364bd47c0850845fd9d003ad36c420947296e2ffbc3`  
		Last Modified: Thu, 08 May 2025 20:12:20 GMT  
		Size: 589.3 KB (589335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:171a28246e23dd24d25654a76cdbaded3f88c1093c5df6befaa9eef5732f07d4`  
		Last Modified: Thu, 08 May 2025 20:12:21 GMT  
		Size: 43.8 KB (43775 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:2eac1e842ce12a8aec3fa88ff25993d1e6f4f4bf2786daa59973bcf4df464588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101849189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8e3e96810ddfd2737e8fc8ed212c51b47eee060c9ea6ab729aa1d0cd0e2c98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 18:32:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_MAJOR=16
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_VERSION=16.9
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_SHA256=07c00fb824df0a0c295f249f44691b86e3266753b380c96f633c3311e10bd005
# Thu, 08 May 2025 18:32:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 18:32:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 18:32:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 18:32:48 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 18:32:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 18:32:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 18:32:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 18:32:48 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 18:32:48 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 18:32:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 14:35:49 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccab5a3936de15bd4dfed2b854b39d894202280d8c72c44681874f2aec8cc011`  
		Last Modified: Thu, 08 May 2025 19:31:21 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d153d5c172f847bdfd04d146875662017fd0434ab6a659fabf2d2fc13f41523`  
		Last Modified: Thu, 08 May 2025 19:31:22 GMT  
		Size: 1.0 MB (1040036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4e3d91feaf316d765d1dd2edc118ef29773c0daca7fc2a7e1e4bc4741118c4`  
		Last Modified: Thu, 08 May 2025 19:39:54 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92ea4ef539f61096aed49b514942d05b0a1b9463a558168d67bd00272acf454`  
		Last Modified: Thu, 08 May 2025 19:39:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e87c15a9b3d514b2f1738b847268d221b9e24b1f31a8bbc3972ce310895263`  
		Last Modified: Thu, 08 May 2025 19:40:05 GMT  
		Size: 97.2 MB (97216671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f07c0ea21f9c4a3fdd510070b15514d872177ac530095b62fd04950cfcca64`  
		Last Modified: Thu, 08 May 2025 19:39:56 GMT  
		Size: 9.6 KB (9563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8493dcd744e13636738d096e6ee01e20f51ca8f3601ded5f4d0ac0ac9cf0e7`  
		Last Modified: Thu, 08 May 2025 19:39:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16f1c132ec088a8fdd9ae265709006be76beb6781ce39aafef374731a7d07af`  
		Last Modified: Thu, 08 May 2025 19:39:47 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf68478f1fe1f8db9a36ab99d35afb9cc05f39929041986ef4a8cd4341fadfa`  
		Last Modified: Thu, 08 May 2025 19:39:47 GMT  
		Size: 5.5 KB (5477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf3699b8f5f850407bd00386b2c9580f59c9d19a32cc5b794a6b8cf77f81bd0`  
		Last Modified: Thu, 08 May 2025 19:39:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:fdb8e53b6077e203724a0f38ea4607e59180fafcca569bcbcb22621ad43b17ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.6 KB (629619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683cb4cd3f85c7dcf8379d3e8df4b7849d351e42b0c13f9d019b6d86ad769fd9`

```dockerfile
```

-	Layers:
	-	`sha256:a47e75d85d6b456fce7fd008465e56fb9c5203b685a8ae83853613ab606c05ad`  
		Last Modified: Thu, 08 May 2025 20:12:23 GMT  
		Size: 585.8 KB (585759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef9fca1ba794aeca5483e95904c7c67efbbb76a40d50eddf80947113f9c5d82a`  
		Last Modified: Thu, 08 May 2025 20:12:24 GMT  
		Size: 43.9 KB (43860 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; riscv64

```console
$ docker pull postgres@sha256:b3746c26ace3b92c3cc2adf1200322491036946395e7bfc9bbcb896ce4dfcf4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97210372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071511446520928c53820522bca2b9d273d6629c893be0bd21d79360e7924831`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=16
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=16.8
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_SHA256=9468083a56ce0ee7d294601b74dad3dd9fc69d87aff61f0a9fb63c813ff7efd8
# Thu, 27 Feb 2025 00:53:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 19:30:36 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a667969f118faf629e202aac4ad97cc21b7c3811a145f4275dbf42e59555a`  
		Last Modified: Sun, 16 Feb 2025 01:00:44 GMT  
		Size: 987.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebfd62b87648c7ac5476d245882fa59a55ae434a2214feefa5b371c5fd1aa34`  
		Last Modified: Sun, 16 Feb 2025 01:00:45 GMT  
		Size: 1.1 MB (1089587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffc75644aa9015c4524a4803b8c615bea6844883b9b28d09659887f6b8ac372`  
		Last Modified: Sun, 16 Feb 2025 04:43:49 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8547faef1dc20f0ac9c1e4a1a6905e277340905ae7669c32a1f72cdd475d64c`  
		Last Modified: Sun, 16 Feb 2025 04:43:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a37e01aab1c1589263e195b0a2100a2e26630232c8b8f86eb66f81927943d7b`  
		Last Modified: Sat, 22 Feb 2025 04:23:13 GMT  
		Size: 92.7 MB (92730737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcb5e119f291ad283faef34f8c3addab7ddce3e925e06dad49e691e7c17380d`  
		Last Modified: Sat, 22 Feb 2025 04:22:59 GMT  
		Size: 9.6 KB (9570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b350216fcc03fbac057689b4a57baadef1443b119339e8e8e2d8dafcb869abd`  
		Last Modified: Sat, 22 Feb 2025 04:22:59 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163f1da397c2de78ca3256a47ad6678feaee4d899a29de61518fb94733181cec`  
		Last Modified: Sat, 22 Feb 2025 04:22:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608de28c5b82984ee0d51c4e30b29cb9c71171d453f069779b24964c0b1c2e32`  
		Last Modified: Sat, 01 Mar 2025 00:07:23 GMT  
		Size: 5.5 KB (5480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f47ead0790ee2e3237da26eec26796813871a960ac1af8e01237642ee62646`  
		Last Modified: Sat, 01 Mar 2025 00:07:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:33d647e0125e022392703bdb1436d8d23499c33c221d6e6bc1a7d60070e75964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.4 KB (632350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9c2a1b32091afbf0fb803abbe076af0393be10d1dd60f75f2b0edb95e64d64`

```dockerfile
```

-	Layers:
	-	`sha256:470d4e256c4cd1bc2728a733b5d7905f60fcbc07f45afb895c3278f2e2d0d52e`  
		Last Modified: Thu, 08 May 2025 20:12:26 GMT  
		Size: 587.6 KB (587589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e4d81e61d695af513c140c3dbed7388ac3bcee8aecb37e114cafcc4c8cd6a5e`  
		Last Modified: Thu, 08 May 2025 20:12:27 GMT  
		Size: 44.8 KB (44761 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; s390x

```console
$ docker pull postgres@sha256:1744e9013b32503a1b6755519b3c33ebff07398fe06cd4d4fdb9d565c010d0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (106034984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdffef3f13b5e4e24aec25cf5838ed9233b3d066e7c788039886e9f39e75c29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=16
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=16.8
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_SHA256=9468083a56ce0ee7d294601b74dad3dd9fc69d87aff61f0a9fb63c813ff7efd8
# Thu, 27 Feb 2025 00:53:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 14:36:22 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bd808fe0e001bd5a66a02c69406d4cdeb252f933c590cb4d320052ea3b3546`  
		Last Modified: Sat, 15 Feb 2025 00:16:42 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b626b09720dc73a31296f38e3ebe6c64e8a0f0170f1d84c424109e9cbbfb03`  
		Last Modified: Sat, 15 Feb 2025 00:16:35 GMT  
		Size: 1.1 MB (1084163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5bfd3e663523426c97298e108c7d05f57cc63e280ad958b0489b777f37f192`  
		Last Modified: Sat, 15 Feb 2025 00:16:29 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2ec1e1feb3ecea6aa9ce13b57efbf5c29523f7ac7d7955c245fbebb7d1741a`  
		Last Modified: Sat, 15 Feb 2025 00:16:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d86fa5a3371ac489663049a65df326147ee0aa4ff4f4775dc02a4ca150d353`  
		Last Modified: Fri, 28 Feb 2025 23:53:22 GMT  
		Size: 101.5 MB (101469902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c1bf452852df9802583fcacba909c2315e4cd7eca226786ab62ed884852150`  
		Last Modified: Fri, 28 Feb 2025 23:53:21 GMT  
		Size: 9.6 KB (9564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f5bc7a0ae2836d163b6ed8398c662e95867e1d69ac20193a25e11db1f6eb8`  
		Last Modified: Fri, 28 Feb 2025 23:53:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4c50f5f626bfcdeddf328591c1ea951bebc0f4f3771368087c7890a21cb57a`  
		Last Modified: Fri, 28 Feb 2025 23:53:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5bf96c9dbbcb03a74e891ed587ae827ac869d9f82a4ed4c74f0aa39415b4e4`  
		Last Modified: Fri, 28 Feb 2025 23:53:21 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47211f8d6c0a3cebd91f77bd07552cabc8dab81dcdf93eb9dfaa7c994b96c6d`  
		Last Modified: Fri, 28 Feb 2025 23:53:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:26aa68a39c8a0bc599513467378539a2fbc22c51de2a24a3c1d06ca44d880ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.3 KB (632290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d306d87feb3a28775c825f73ad6a49802061614b4148425122119df287e9bd9c`

```dockerfile
```

-	Layers:
	-	`sha256:bdb0bfb9eb2987e7aae7088d7cb9e960412bb22e9a8527cb9ed37aea238b5359`  
		Last Modified: Thu, 08 May 2025 20:12:29 GMT  
		Size: 587.6 KB (587571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61568e56c1173b7d10f8cc922bf6a0cd98548c041628554db6516fbb3b47a1f8`  
		Last Modified: Thu, 08 May 2025 20:12:30 GMT  
		Size: 44.7 KB (44719 bytes)  
		MIME: application/vnd.in-toto+json
