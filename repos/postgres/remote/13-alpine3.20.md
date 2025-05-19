## `postgres:13-alpine3.20`

```console
$ docker pull postgres@sha256:05162f3c0226f6df1268e90db2db4e19c41b3e61b440e2293f09f965ab7986e3
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

### `postgres:13-alpine3.20` - linux; amd64

```console
$ docker pull postgres@sha256:7d55bcc4c7b7b2fe0da831c966a093e129a24629a6a43ba852b626f51b317748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94143967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ee702e67b78991e49f8fda4387002a7487f9ca3140b1245ddd7af634ba0186`
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
ENV PG_MAJOR=13
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_VERSION=13.21
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_SHA256=dcda1294df45f033b0656cf7a8e4afbbc624c25e1b144aec79530f74d7ef4ab4
# Thu, 08 May 2025 18:32:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:865f59872daa139b6ddcd60c69f0e39dafb4bd871129e8d2ba3f3fb9078d11c4`  
		Last Modified: Thu, 08 May 2025 19:18:29 GMT  
		Size: 988.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba74407d359a5f2531c1458b6ded0bb4ff3485af6af7db9b372ab3d132e0834b`  
		Last Modified: Thu, 08 May 2025 19:18:31 GMT  
		Size: 1.1 MB (1120293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdba01dec528df7a878cded04713284b079161146a797e76e0dde2222578f98e`  
		Last Modified: Thu, 08 May 2025 19:18:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec79660df704a80572086f19baea47e31116bf3adb39bbdbd1af5fb6e1b4863`  
		Last Modified: Thu, 08 May 2025 19:18:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7657021fa822803f691ddc1c27fdb8888da19103afb5020f2e46a5f1e532cf97`  
		Last Modified: Thu, 08 May 2025 19:18:42 GMT  
		Size: 89.4 MB (89380532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23ccf6f9cd51a5635418afa7af29f6eaae96e06e1603c11c21e27467a900dcb`  
		Last Modified: Thu, 08 May 2025 19:18:29 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250c9a633033b129316e7e1b9847513ae8ad94e7b22a9e8af23657e7b51f974e`  
		Last Modified: Thu, 08 May 2025 19:18:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf14ebf0c589633704319ef9320788f498641aa61b20cf26166ae9fac5d1148`  
		Last Modified: Thu, 08 May 2025 19:18:30 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a265cc661cc98139689c09ceceaa57de4de862a984817dcd6524fca83a7182a`  
		Last Modified: Thu, 08 May 2025 19:18:30 GMT  
		Size: 5.5 KB (5471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620cca8a7b4e5e10fde60ad4bc59bcd776d60243bd02d686eb5d34812688562e`  
		Last Modified: Thu, 08 May 2025 19:18:31 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:75514b0fe2462121397f1313265d08b758bb9d8de0e2123e39d3fac00932d72b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.7 KB (629713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc3bd35774c003294d4fce1d8c74ac80f43eafa24ca3081cbdd669cbca07f38`

```dockerfile
```

-	Layers:
	-	`sha256:a686a83d7263b36acb8e40d29999ba0fd711be7e2eaccd616332827151c3ac1d`  
		Last Modified: Thu, 08 May 2025 23:08:20 GMT  
		Size: 586.4 KB (586409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdfb1a229e317751d7ddfafbb27ed45ae5ce917cdabfee3a375a9ee6a114bd78`  
		Last Modified: Thu, 08 May 2025 23:08:20 GMT  
		Size: 43.3 KB (43304 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:4837f3798891df7134e791f1d3a596ac85154750c4536c6875b082a39f4eb7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92905324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f97bfcef95ead583c37b680cb7dd92e889bef9232c17dcae6e7571304415a0f`
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
ENV PG_MAJOR=13
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_VERSION=13.21
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_SHA256=dcda1294df45f033b0656cf7a8e4afbbc624c25e1b144aec79530f74d7ef4ab4
# Thu, 08 May 2025 18:32:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:e8bbe2fc3faa4e95bb90bb1c52cb0b93c3a3004793af2123d103ab3a63668af9`  
		Last Modified: Thu, 08 May 2025 19:49:26 GMT  
		Size: 88.4 MB (88430025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bb1802136e36c27153460ecaae8b9eb54fd4c55aa2038bdd2e64f82782729c`  
		Last Modified: Thu, 08 May 2025 19:49:16 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005364543724838b856ce9b89da8a68b77651529493cd707ff89726b5d0209fa`  
		Last Modified: Thu, 08 May 2025 19:49:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601439311ccab3846794b004209110458a62dc86889c9548a6ab2fb8ee6879ab`  
		Last Modified: Thu, 08 May 2025 19:49:17 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cca0cdfe97a7f3df48a3aaca116441744d48e32a6ae831d961ac2362c05ad2`  
		Last Modified: Thu, 08 May 2025 19:49:17 GMT  
		Size: 5.5 KB (5472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5f78b7caddc4021283169b8fcd8b527d7005cd460ed56f407408a2ec66c077`  
		Last Modified: Thu, 08 May 2025 19:49:18 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:3b5da2cbcfb7f45bb1878a4644ac74f971c8e3178480fd9e8c450a37caa01688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 KB (43253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9067aa77d48cc3f97c5c4ed284a310f6292d0d142928b985e333166df43943b5`

```dockerfile
```

-	Layers:
	-	`sha256:a28f10451549c9034e93caac9ed6846e2d4d248b101ef08c8f2345f38c8638ee`  
		Last Modified: Thu, 08 May 2025 20:07:35 GMT  
		Size: 43.3 KB (43253 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:29f4af6a6dbe10e60dcc124ab8fdcb2b8ba6d5aa7376c9d3708a809db8cd4cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87365600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1308c58a1033e1007c008031950b39dbe751ba58adbd0d0247e54251baccbc17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
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
ENV PG_MAJOR=13
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_VERSION=13.21
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_SHA256=dcda1294df45f033b0656cf7a8e4afbbc624c25e1b144aec79530f74d7ef4ab4
# Thu, 08 May 2025 18:32:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 14:35:10 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbef8e87d0b643b3fa5e794617e621cb59b4567f3cbc0795d1528c9a02dde43`  
		Last Modified: Thu, 08 May 2025 19:56:16 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5264bd33c0c87b69007461ea6e25e8f1acb036978189c5022f26c3bd00812781`  
		Last Modified: Thu, 08 May 2025 19:56:24 GMT  
		Size: 1.1 MB (1086505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b52020e272542edb0a9a9c6093ce4040aabb84d5ea00a6347a20d232f17bbb`  
		Last Modified: Thu, 08 May 2025 20:32:30 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2815508b129237cf228ecef546e0294e48c331a6b2378e7df8f159f2e81829`  
		Last Modified: Thu, 08 May 2025 20:32:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a50fb681893f2db1cd7ec9989fbe54a3ceabce7ee98597f448c5af9c0e5ce9`  
		Last Modified: Fri, 09 May 2025 01:04:46 GMT  
		Size: 83.2 MB (83166884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ea47df124f0538c6665a7c37ced4fec27c550000466fa2c76b113d659d044c`  
		Last Modified: Fri, 09 May 2025 01:04:46 GMT  
		Size: 9.0 KB (9011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b22adde561a30093f5a525d7a3bc5805388bab82ef95cf5b95f678510d4c04`  
		Last Modified: Fri, 09 May 2025 01:04:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb8d253161dac81762087eaa2820b17c0b46e2d0d80dc6321963b458d904d1f`  
		Last Modified: Fri, 09 May 2025 01:04:48 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4218bbeca7a633032e437101680e3ab75319c1535f19424fb3bf20ddebfe7d1c`  
		Last Modified: Fri, 09 May 2025 01:04:49 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b458667c563aa78aca1282c97593a08098547027e625b07c39fe86680293528`  
		Last Modified: Fri, 09 May 2025 01:04:50 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:f75d20e350a51c34d6c2fd592b497965722c1f91ff7986dd9721862d1ac105fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.9 KB (629897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2301a9a1f4fdf5065a49e5878b9fc7d733af98eb76939238360d3436f160ea0`

```dockerfile
```

-	Layers:
	-	`sha256:41ae25fc938463c16ff194bd9cea66204bcc093df80fdc8667da74f30bd40e5e`  
		Last Modified: Thu, 08 May 2025 23:09:02 GMT  
		Size: 586.4 KB (586429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4580cdcb4a39dbc65340b4e0d91b49d5dfb7b198d41ba8ef8fee05a6b76cf400`  
		Last Modified: Thu, 08 May 2025 23:09:03 GMT  
		Size: 43.5 KB (43468 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:77078d1177370e5589a6b52c0a36fe4cb6191dffdc30f0c191d8a744ce78e02e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93424031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f3cedc25b9f7471eb624df523382cf635198bb93f21690b5003589982b13f`
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
ENV PG_MAJOR=13
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_VERSION=13.21
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_SHA256=dcda1294df45f033b0656cf7a8e4afbbc624c25e1b144aec79530f74d7ef4ab4
# Thu, 08 May 2025 18:32:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:b13817058605d722d531e2aa0a76a62ca6aa4a130a53091e9d4731ef13e3c9fb`  
		Last Modified: Thu, 08 May 2025 19:54:18 GMT  
		Size: 88.3 MB (88266868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b099e7b3dce2b5b62835d6517a12995fa31bb9ac25124ab61a42d5a33f09910`  
		Last Modified: Thu, 08 May 2025 19:54:11 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb8900562a2e3a49e2608eaf32dd4d1d84a8e84b6bcbb178889fbe8bbb26cf3`  
		Last Modified: Thu, 08 May 2025 19:54:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39914283232aa1b2b8b1217d799e185fe35de38bb86f7adc1be1a98ef63ea965`  
		Last Modified: Thu, 08 May 2025 19:54:11 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5183c82a327e431a2b3dc0db810521cda8c8d5147ad27b640f96f4afb5bb7851`  
		Last Modified: Thu, 08 May 2025 19:54:11 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c7a18afea26603b99957f5d20cccc65b7c2c880009b699399235f861926b87`  
		Last Modified: Thu, 08 May 2025 19:54:12 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:fc06b956e478b895796a11999df365204c60ecb960e2105b9428c6044f3c0fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.9 KB (629945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b894a9971eecd6abd099f10f6c01427a9dd5a66332851af7130498c3fa233387`

```dockerfile
```

-	Layers:
	-	`sha256:1aa362458d0301ad863b309f3b773f21e6212817f9947f7218157da1029c381f`  
		Last Modified: Thu, 08 May 2025 23:08:27 GMT  
		Size: 586.4 KB (586441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef5f7ca72b17e4c02fad6cbe1ec93a70298570d30ba468b4c9d41acf09e8a341`  
		Last Modified: Thu, 08 May 2025 23:08:28 GMT  
		Size: 43.5 KB (43504 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:446c29eecd9679380288bc1f21f228f0ba6d9dc9172a268931d8dad80dba8b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99405335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b27555702e9448c2053aa32bacbe49e9b05a2d962974ae43abead19fa71eab3`
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
ENV PG_MAJOR=13
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_VERSION=13.21
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_SHA256=dcda1294df45f033b0656cf7a8e4afbbc624c25e1b144aec79530f74d7ef4ab4
# Thu, 08 May 2025 18:32:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:e8e84a70efa50a6b882dc09c3dc57f3ffc371a0d5357f11f4d4ba1d502bfb23b`  
		Last Modified: Fri, 09 May 2025 01:05:14 GMT  
		Size: 1.1 MB (1095373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3a41094d6f47627bd7c4c5e1abfb3468db9a480815f5b184797c7bf837931b`  
		Last Modified: Fri, 09 May 2025 01:05:14 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a81f3f0f5a42937146d4dc1eb6c3cf98156d7ce9b36b9ed180b8753bf26ffb`  
		Last Modified: Thu, 08 May 2025 20:16:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ae9078b9a741ac02d38e714237489d79d2d7930a5b032f55704746a9b7d0d8`  
		Last Modified: Fri, 09 May 2025 01:05:20 GMT  
		Size: 94.8 MB (94822050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244f46d8b83b7ba893dd4da4ddcb6aa22c3c7dc84a788caf278c69b119cd09b5`  
		Last Modified: Fri, 09 May 2025 01:05:20 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb5f9683e59ea7ab0c9a1741c0548493e13e64b8542dbe8b41416ebf77b7541`  
		Last Modified: Fri, 09 May 2025 01:05:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36a942ed0dc5521a1e663e0a6bd03f82460cffad8e274cdcc24ec679db1e360`  
		Last Modified: Fri, 09 May 2025 01:05:22 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dde5a32907138c4c253078ed482d6c5c193ba3193eb7493c038a495b519ff80`  
		Last Modified: Fri, 09 May 2025 01:05:23 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77435f4ea56e86d33fc841ffb165c3a789b6effeb0783831c0ad0dec359f3432`  
		Last Modified: Fri, 09 May 2025 01:05:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:8084fed1438ee01c948b6271109cf892f66b37d4b4d2457e7b83eab420c8afad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.7 KB (629660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151db31c226490fb94f7dfac0eb5059737bb261c5f072330b0915b88c8b8af81`

```dockerfile
```

-	Layers:
	-	`sha256:2883156f35ec736b686344110ca73b81aad617919b8651ce6065273e208fd9a3`  
		Last Modified: Thu, 08 May 2025 23:08:30 GMT  
		Size: 586.4 KB (586394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:653cdb02575676d9d3fc9489f52a86a4fcbad653df30565dc06a8125e593d9bc`  
		Last Modified: Thu, 08 May 2025 23:08:30 GMT  
		Size: 43.3 KB (43266 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:c6968bf3abd74f7badde29cfd03cf067708f193204242bb358831e0163cf2b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98532365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d04da2b22db0033ef622dd53b76aa87d8d58474d5ff6b9884e959ccd752ca39`
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
ENV PG_MAJOR=13
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_VERSION=13.21
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_SHA256=dcda1294df45f033b0656cf7a8e4afbbc624c25e1b144aec79530f74d7ef4ab4
# Thu, 08 May 2025 18:32:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:c28190dc3cfeda129e91262fdb5d43d52cc8f0b60b8ccda411fa8d7bac1f6878`  
		Last Modified: Thu, 08 May 2025 20:45:01 GMT  
		Size: 93.9 MB (93900396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c8fe40d611623c9a5b00c38a380e0abc0e1f70e1c6e24ffee66f75389ffe0`  
		Last Modified: Thu, 08 May 2025 20:44:57 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b773316acc1ea2219dd338e7c595d1a5f085ad63297c33537debf72071a68e20`  
		Last Modified: Thu, 08 May 2025 20:44:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc50aa5c010affdb6435c57250378cf5b08c2de032fa671d76dbce46eb91d96`  
		Last Modified: Thu, 08 May 2025 20:44:57 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b67046d9b26a83c0b801fd183e5a9b9dfaf8129dcc290de87509919b5d5aed6`  
		Last Modified: Thu, 08 May 2025 20:44:57 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a0261acdc2e0dc7fd39df1822f5cfa6970e3e6981d43bea5824e8ebc5dab9e`  
		Last Modified: Thu, 08 May 2025 20:44:58 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:95cf1596541d32b6ad5e9b6abab32e3194597e29bcc80a842f96c988c7368454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.2 KB (626170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c74b7380f9f21c56c412060465d0db16ce5641acb640f4cd29ce5a3b828e4d`

```dockerfile
```

-	Layers:
	-	`sha256:b2c4ad810577adf5f19385ab111a3bfd93d6b11fee249372f8ce75ae09b529f3`  
		Last Modified: Thu, 08 May 2025 20:07:54 GMT  
		Size: 582.8 KB (582818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eaa87dd2f6e1ae99c4dbc726452e21d8faa9c7da28269fbdeb0fbbc1e16a6f9`  
		Last Modified: Thu, 08 May 2025 20:07:54 GMT  
		Size: 43.4 KB (43352 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; riscv64

```console
$ docker pull postgres@sha256:8078e351550d3d86ea440ff4990546254ee68c96ad7dbdb27ea7b36481b5059e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94291070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f409ca2ff3a608c45b150ed8afe54f889de1bbecbbbc5fcfe88252023745d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
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
ENV PG_MAJOR=13
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_VERSION=13.21
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_SHA256=dcda1294df45f033b0656cf7a8e4afbbc624c25e1b144aec79530f74d7ef4ab4
# Thu, 08 May 2025 18:32:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 19:30:36 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ef72c74639333e9c3f45197d4cfc967d6dc221f9810a1f9c8da4f8a42f31f2`  
		Last Modified: Fri, 09 May 2025 08:07:48 GMT  
		Size: 987.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c23b9a41a4ad4ce8de9b5c59b875d15ee76f3d92a74b0161900666159f0470`  
		Last Modified: Fri, 09 May 2025 08:07:49 GMT  
		Size: 1.1 MB (1089579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2522f783ffda0d63a80a8c72dd51efcdc022f61fd05e53403148af9ec43c8f7d`  
		Last Modified: Fri, 09 May 2025 09:46:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c713f994d86fe0a0446bd31d7ee2c3102db22410c51c1c12b6de7aca0c072bf`  
		Last Modified: Fri, 09 May 2025 09:46:10 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea161a9b9b41198ee54873449912728ac908f9de7a84c57fc936bee4199c353`  
		Last Modified: Mon, 19 May 2025 08:23:07 GMT  
		Size: 89.8 MB (89811994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e2021b41247673a81ff794ac682141466e68bda7b7c08e54d9bba9a7e98485`  
		Last Modified: Fri, 09 May 2025 14:47:00 GMT  
		Size: 9.0 KB (9024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2811523b39dbecf8eb0bb2f4927d4d77692788cc14123a4c8ea6e87afd2d7d26`  
		Last Modified: Fri, 09 May 2025 14:47:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb8c902195de629270b2fad28b22fc1a25c797d3f40910ade1d632ede86d263`  
		Last Modified: Fri, 09 May 2025 14:47:00 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786cdc38d4f41b94170726e601949ada0d6ba7ffaa55091a599eb37250cc05fc`  
		Last Modified: Fri, 09 May 2025 14:47:00 GMT  
		Size: 5.5 KB (5479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2992fb5f7e1d453573dcf65c5828245627e9fcfada49bddf666abe1e59a87e6c`  
		Last Modified: Fri, 09 May 2025 14:47:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:ba075990cd9aaf1e3e5a3f7102b86964b3daa26fc0007ce9fc2a42b7ecb7d52a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.8 KB (627828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db6616faf71fd1dec0bcdce400e287b6384a78029d228b1e6f9f14dd428fc9e`

```dockerfile
```

-	Layers:
	-	`sha256:3dd682a7715084dca1352e2bce39699d61283990d746b7c3a8432e8ea21f7da7`  
		Last Modified: Fri, 09 May 2025 17:07:41 GMT  
		Size: 584.5 KB (584476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5525d2fc07f00736d5c89615106fb4c2b9841a16a3d5655b5fcabc4c5946d6f9`  
		Last Modified: Fri, 09 May 2025 17:07:42 GMT  
		Size: 43.4 KB (43352 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; s390x

```console
$ docker pull postgres@sha256:a13228b7ab30ad1f1c3a09f0e261e16e04b1c9c65422bd91b7ff2717b55cc28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102946027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dbe6d762c148d13f60631a28aa6ebfbcc213448647ec713ef87ce2a6223cb17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
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
ENV PG_MAJOR=13
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_VERSION=13.21
# Thu, 08 May 2025 18:32:48 GMT
ENV PG_SHA256=dcda1294df45f033b0656cf7a8e4afbbc624c25e1b144aec79530f74d7ef4ab4
# Thu, 08 May 2025 18:32:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 May 2025 18:32:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 14:36:22 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55458e575a1f3a149b78f7bf005b40731c98ceae373147897be70ac3ebf81c8`  
		Last Modified: Fri, 09 May 2025 00:03:22 GMT  
		Size: 990.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ba5e02a7b40f084adae3dbde725007a564d1a95cdcd232c26735a6789cef82`  
		Last Modified: Fri, 09 May 2025 00:03:23 GMT  
		Size: 1.1 MB (1084162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89d1751e2cbdb5cbe72bb75779e1a0a81e37135dba8a7c04862f82c6dc8598f`  
		Last Modified: Fri, 09 May 2025 00:03:24 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6f91ae035a89d8e40f819959ddf803a71baef5888b9668031156cc44031555`  
		Last Modified: Fri, 09 May 2025 00:03:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a760159d56b5932008b90655f2b8898cfbeae2a812a3690415a142f0734d33`  
		Last Modified: Fri, 09 May 2025 01:05:54 GMT  
		Size: 98.4 MB (98381495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714b8823bdcadf3f1f53a9f14f8ec2923a49a10e16650b479ab01b0bd847599f`  
		Last Modified: Thu, 08 May 2025 21:11:31 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd55dba1ab07c731d286f8f4d38228d9e76434ee7e31cb24c37bac7e3c9c4b71`  
		Last Modified: Thu, 08 May 2025 21:11:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2b71f558f671c3aebc1b41f6ed64b0b1fa70cb8d676947cb94f297ea2dde00`  
		Last Modified: Thu, 08 May 2025 21:11:32 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d470bae9febb4413438ee61fabe662428b71086f8d4f08e5855bd2a8e6720a65`  
		Last Modified: Thu, 08 May 2025 21:11:32 GMT  
		Size: 5.5 KB (5471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f8565b4cd50e134982eb23fb387bb8ebbaeb425d5818eb364e76ff12a2da84`  
		Last Modified: Thu, 08 May 2025 21:11:32 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:f0ce684fb8631b187551c40e18ee397af32d16290684669f1bdaa3d61553aa40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.8 KB (627762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97349e534a5dab5d0887a92ceb78ca0408d981832d3293ce34a26b1a87d3ac47`

```dockerfile
```

-	Layers:
	-	`sha256:454301573621890983cb64d3dbeccc34d04e228ad959b9504a3ce299eae0434e`  
		Last Modified: Thu, 08 May 2025 23:08:40 GMT  
		Size: 584.5 KB (584458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2ec584c321f4d43c64c1b5c1f81f735efee3613c5fa731601d3b295c6f7662f`  
		Last Modified: Thu, 08 May 2025 23:08:41 GMT  
		Size: 43.3 KB (43304 bytes)  
		MIME: application/vnd.in-toto+json
