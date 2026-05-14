## `postgres:16-alpine3.22`

```console
$ docker pull postgres@sha256:32689bc7f1e87fa33ca190d57c1e97f8149d12dd45810cfc76a2399ba9e95e7c
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

### `postgres:16-alpine3.22` - linux; amd64

```console
$ docker pull postgres@sha256:34f930aa0165362d109e1c53d6270b883792a4ee86884b4d108ce87e051619c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109565618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa558280508542ca5bbfc4761e1091bff01d9ca808fe429b4f7e3977e3ca385`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 19:01:35 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 19:01:38 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 19:01:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:01:38 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 May 2026 19:01:38 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:01:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:01:39 GMT
ENV PG_MAJOR=16
# Thu, 14 May 2026 19:01:39 GMT
ENV PG_VERSION=16.14
# Thu, 14 May 2026 19:01:39 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Thu, 14 May 2026 19:01:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:03:43 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:03:43 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:03:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:03:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:03:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:03:44 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:03:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:03:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:03:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:03:44 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:03:44 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:03:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155dd17e4bf8f24f91cf88c9871b80ce06b1b1faa418e8aff159dc53c19d740a`  
		Last Modified: Thu, 14 May 2026 19:03:58 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea23c92947ff2ae76072f7086ce8fab33e019902f4d9e82ff3e331d8f65d212`  
		Last Modified: Thu, 14 May 2026 19:03:59 GMT  
		Size: 917.4 KB (917417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2431aa69872fa529a666cc656d3c2d4e263b4dbf1045d858ab88428db721d39`  
		Last Modified: Thu, 14 May 2026 19:03:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91ae17d2f9b1742f42c532441f5ed2caec63603a36fe41bf2b5d4768ffd1849`  
		Last Modified: Thu, 14 May 2026 19:02:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057a0688784fcd41d9f6e97d356e6b0d763ef6b0363f29ad2d795b2e31448f7c`  
		Last Modified: Thu, 14 May 2026 19:04:02 GMT  
		Size: 104.8 MB (104822553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a01cdc03e61d45c528317fd473c4c9acad3a751481c25138d9432e76337dc8`  
		Last Modified: Thu, 14 May 2026 19:04:00 GMT  
		Size: 9.6 KB (9617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f1757dfa419d12d855fbff4dd116226b2ba33e373c1b757693405576c903fc`  
		Last Modified: Thu, 14 May 2026 19:04:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01f4f7a73c6a974bf3a53ab83959621e124745be3971bc3d049f849d92b2f6a`  
		Last Modified: Thu, 14 May 2026 19:04:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f47e7f2587a5a5578a36ab5f584a09ec12b48b1f95e82cd47b699e9b3099632`  
		Last Modified: Thu, 14 May 2026 19:04:01 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f64acd2908364318df203477d271dfe42653f4d6d51437ac1a4ee4539580e10`  
		Last Modified: Thu, 14 May 2026 19:04:01 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:d1e2be5e1440f03b7437da209784a5a9e15cc097c143d36fbfab54e9a54b18f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 KB (639998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63949a3ed2c39c962a1426fd88ea622824ac711b48f173e51ea02182651ce8bc`

```dockerfile
```

-	Layers:
	-	`sha256:6bafdd383855b63c7d459b92a66f162028e6e5cd5f1784f6eacc24239393a086`  
		Last Modified: Thu, 14 May 2026 19:03:59 GMT  
		Size: 596.3 KB (596315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa104e660708ef920136c3ae4736abcf6bb5385dc18f85cf64795fe843a54c73`  
		Last Modified: Thu, 14 May 2026 19:03:59 GMT  
		Size: 43.7 KB (43683 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:2e89dfe9c9f2594fb94dfb2dd8c122445b466daa0f5a2be576f48b488b7e80f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89094076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06344f3e8436c26f24a57cd51d285fb8209526952a75c1ecf62fd1897fa37cb2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 19:21:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 19:21:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 19:21:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:21:40 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 May 2026 19:21:40 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:21:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:21:40 GMT
ENV PG_MAJOR=16
# Thu, 14 May 2026 19:21:40 GMT
ENV PG_VERSION=16.14
# Thu, 14 May 2026 19:21:40 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Thu, 14 May 2026 19:21:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:24:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:24:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:24:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:24:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:24:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:24:30 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:24:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:24:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:24:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:24:30 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:24:30 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:24:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565dbd2e61146ad1e899178373d1360678040d95f3467d090ed0cc8f70edf2fe`  
		Last Modified: Thu, 14 May 2026 19:24:40 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68be5fcab084fa70b8eefba9e6e14851924d6bf6d2ffb84dcab53cdc77a81df`  
		Last Modified: Thu, 14 May 2026 19:24:41 GMT  
		Size: 885.2 KB (885152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ec0169ae32b012ce9fc4c5ba8b7f1e468d0d5cfbd8b80d51ee60b80a4ad34d`  
		Last Modified: Thu, 14 May 2026 19:24:40 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff6bca1a9bcf8a8cdea72d057012ea7fb7fdd0e2c57abcb45300756921147b7`  
		Last Modified: Thu, 14 May 2026 19:24:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ba201db273810155907e15c65cd257cdcbc9f81cdafa23c448ea0e831792e9`  
		Last Modified: Thu, 14 May 2026 19:24:44 GMT  
		Size: 84.7 MB (84684085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ab19ced053812482372655a4a4438cb889a69c497911c7589b2e02c402a129`  
		Last Modified: Thu, 14 May 2026 19:24:42 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980c4286334fbdfeb42aff8589240a390fde7278c80b5443cb0ebc6b28eea774`  
		Last Modified: Thu, 14 May 2026 19:24:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18cc9df6495af2ccd977d7d64a921ccf6cb834827055c9281e24908698adc72`  
		Last Modified: Thu, 14 May 2026 19:24:42 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e83903d246982a62b6f37e63487ba25f8cfcc15e1519adb4ca4ba80b9c8127e`  
		Last Modified: Thu, 14 May 2026 19:24:43 GMT  
		Size: 6.1 KB (6094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeba095d5084cfe5bcf20cdab7c47a6526a11a4a58ccf50a264c8d3b109dbbe`  
		Last Modified: Thu, 14 May 2026 19:24:43 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:d39a075f9a926fdafcde64bf6a1fc0b43daa1d5a9c256ea20a5949e39b6b2ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 KB (43631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a607e0ede8c39053813d383059184d4dc2189bc08a38f224c3cfeab9b7ebe5`

```dockerfile
```

-	Layers:
	-	`sha256:12ead305791433a34a1d5d3290df96cbed35346fed288f3b148b2894e31cafa8`  
		Last Modified: Thu, 14 May 2026 19:24:41 GMT  
		Size: 43.6 KB (43631 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:cd0190abb64048c3c29376cedac2d988e144b1a633701b8800cef9a7b068a5e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84366771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5bf1a5fa965f59acf657d83328bbe3d0400a6fb46ef694c8610ef853e7bf680`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 19:21:12 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 19:21:15 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 19:21:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:21:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 May 2026 19:21:15 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:21:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:21:15 GMT
ENV PG_MAJOR=16
# Thu, 14 May 2026 19:21:15 GMT
ENV PG_VERSION=16.14
# Thu, 14 May 2026 19:21:15 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Thu, 14 May 2026 19:21:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:23:59 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:23:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:23:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:23:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:23:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:23:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:23:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:23:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:23:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:23:59 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:23:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:23:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b0ad477144d2d204e49bb257a248bfa8049c1612ada3368ba396160e9fffc2`  
		Last Modified: Thu, 14 May 2026 19:24:10 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb256128401d95d08bd2e733e21576933510643bdc881e1a83f16a0b5061031`  
		Last Modified: Thu, 14 May 2026 19:24:11 GMT  
		Size: 885.2 KB (885161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fa4b14519fd522ae500fc1a059540df60c9c19a90e4b121d4e6741f2ff3c63`  
		Last Modified: Thu, 14 May 2026 19:24:10 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78190535848de5126ffd02cf3156471424bb5af65b59d8a2f635b26f4bd2d152`  
		Last Modified: Thu, 14 May 2026 19:24:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb46f5e38db94f8a1004bedc4b462e4b6b007735a61faa27c62654f6dd02933`  
		Last Modified: Thu, 14 May 2026 19:24:14 GMT  
		Size: 80.2 MB (80238323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba6a1909482e872ce1e679bc3715e731a9ada845311e7dd18ac113233b23e3c`  
		Last Modified: Thu, 14 May 2026 19:24:12 GMT  
		Size: 9.6 KB (9618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1721f778e0949b33d0af45bc868d084ed8a396b9b70a2bf14f8c95aa7d6ba9`  
		Last Modified: Thu, 14 May 2026 19:24:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615db7c7966013ce001b17c2a24b98e59621a692587f24433f7989b612ed260e`  
		Last Modified: Thu, 14 May 2026 19:24:12 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82d2e831d27acb4d01275a441765d61a3f4834e290db5f767fc9a0f91f98aee`  
		Last Modified: Thu, 14 May 2026 19:24:13 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfb207ba8c86e27a465eca06ece94a802851a5edb0c3e41097badcf8236703f`  
		Last Modified: Thu, 14 May 2026 19:24:13 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:d37b5835f470a9d1104e2e940584c893c80213829f79466a126ce3c161f07a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c193f37f79bb194ff7c145c58046008ffe6f049dd57ee65a35ced377c727ba`

```dockerfile
```

-	Layers:
	-	`sha256:25f6ce4c77f5402d8d9516ee785915085b76a7bcc81b68b989d4f9244d8d1e57`  
		Last Modified: Thu, 14 May 2026 19:24:10 GMT  
		Size: 596.3 KB (596335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc981c16a03f5b876d0942f20945eb87cf2048ce5eb1df9ba41919386f0ad8b2`  
		Last Modified: Thu, 14 May 2026 19:24:10 GMT  
		Size: 43.8 KB (43844 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:4b65ad5bf852855a1fe4dd21630071f462f026de94304425d6098e2e233d53bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105521685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d2aa9a41a54a6b626ddccfe67fb7aa0ff9e322c884789493936797ad432e9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 18:59:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 18:59:11 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 18:59:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 18:59:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 May 2026 18:59:11 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 18:59:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 18:59:11 GMT
ENV PG_MAJOR=16
# Thu, 14 May 2026 18:59:11 GMT
ENV PG_VERSION=16.14
# Thu, 14 May 2026 18:59:11 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Thu, 14 May 2026 18:59:11 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:01:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:01:38 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:01:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:01:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:01:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:01:38 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:01:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:01:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:01:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:01:38 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:01:38 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:01:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec4949fedc807786cfb0f7e3a1e9d45f5434d6729ce53244d6725f00ec458d9`  
		Last Modified: Thu, 14 May 2026 19:01:53 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c20f879288aee74d45ad5ed73204cb7f2d9a001a836867958eb9b2a6e6a4177`  
		Last Modified: Thu, 14 May 2026 19:01:53 GMT  
		Size: 873.1 KB (873134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519a33fced37b1716852665c653b8f162d1a99cf3cb4c84c03ff41da732e3986`  
		Last Modified: Thu, 14 May 2026 19:01:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ddb7679c6712fad770cd56439d9ac011c8551348a16eab3901c71b49bccf82`  
		Last Modified: Thu, 14 May 2026 19:01:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e167bef92b2ab196856a8ec243017c06b8ca4e70d4a11b128c2a18e519df51`  
		Last Modified: Thu, 14 May 2026 19:01:58 GMT  
		Size: 100.5 MB (100489195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479c23f07b1232e58c42a61c02592ac0b9422a61075b129e43de32177f4f5872`  
		Last Modified: Thu, 14 May 2026 19:01:54 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1f099895700d12fb3aba8cc14de2e9c21d56cdf43e1905e764787b8d2160c9`  
		Last Modified: Thu, 14 May 2026 19:01:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad434da23cf5e3d63eabad9360dd50a335c52d5c6053cf4353509b513585914`  
		Last Modified: Thu, 14 May 2026 19:01:55 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62310e1a327e9ddb34ddc744c3e1b846fce14e9aed010004a2fed4e6068ddeea`  
		Last Modified: Thu, 14 May 2026 19:01:56 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff01d42fae5511fcd503e71dabf98b932909414a1f2a59de4037da40dc5e4954`  
		Last Modified: Thu, 14 May 2026 19:01:56 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:c629ebefd090d6eff806879352ebe18b67e77d4791f7e5ae88f8019eb2802c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72993c5611d01bd0b9131479fbe5fbaef5d77ba7c22c9c29fc5c059f717d6878`

```dockerfile
```

-	Layers:
	-	`sha256:7902d98cf0975cfbab098d869035bf3664a10d4abefc988fd7f04f1ed6c44ec7`  
		Last Modified: Thu, 14 May 2026 19:01:53 GMT  
		Size: 596.3 KB (596347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:994d65c91604748ca8c9ec6e15632ae0ee8f1c8a76c52197ac1498289b0245d9`  
		Last Modified: Thu, 14 May 2026 19:01:53 GMT  
		Size: 43.9 KB (43884 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:c8285c4a11db5af136b84b123c405eb1e2a02d6a6edecc3fca1727083bd0c9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115793978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e814e42df2b5b67a9b8293f51501132928c65bec09ef2e54f6b9f7f21bdca558`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 18:58:31 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 18:58:37 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 18:58:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:02:05 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 May 2026 19:02:05 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:02:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:02:05 GMT
ENV PG_MAJOR=16
# Thu, 14 May 2026 19:02:05 GMT
ENV PG_VERSION=16.14
# Thu, 14 May 2026 19:02:05 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Thu, 14 May 2026 19:02:05 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:04:38 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:04:38 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:04:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:04:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:04:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:04:38 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:04:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:04:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:04:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:04:38 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:04:38 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:04:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadf06fd1d7c48a29dfe032ce547ff71ee7378a811647be9ab69c88e1ff0a175`  
		Last Modified: Thu, 14 May 2026 19:01:55 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e50e354813035b6f1ed38320da9bcda56426d9677d012bf8f4828075c934a1`  
		Last Modified: Thu, 14 May 2026 19:01:55 GMT  
		Size: 889.7 KB (889748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab189ce5f7a9f7e0971d141f86c8fba46da621ded38d00d03f38f3d628051d62`  
		Last Modified: Thu, 14 May 2026 19:04:56 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a33629c84638f03256c274b6122493b3dc1a455fb76baa730d348d2292e9fcf`  
		Last Modified: Thu, 14 May 2026 19:04:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b11f21bc6d250843ab2c20d80b4d25e798fa45849e418e606a8289cc485048`  
		Last Modified: Thu, 14 May 2026 19:05:01 GMT  
		Size: 111.3 MB (111262043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36596ed6e1cb9c7fca941cab4aa9de56e282a619db85e4275a1e9f2eaf79ed3e`  
		Last Modified: Thu, 14 May 2026 19:04:57 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96a7f4887b02ce9379e15ea0de562e233e8efa7f1ae68b5c71f7bb84acd98b7`  
		Last Modified: Thu, 14 May 2026 19:04:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b3959dfe69e53f2b11c2fce4168f852bbb60e9ff82c27025fcd30b5f644481`  
		Last Modified: Thu, 14 May 2026 19:04:58 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c47bace80d41c0bd34eea0126b6aefda013bd2bf62d2c450bb4481285b5fb9`  
		Last Modified: Thu, 14 May 2026 19:04:59 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935bb78bf3c0e3ae6a877256811ac01b6a30cef72e2fa086fd116bcda9a7bd90`  
		Last Modified: Thu, 14 May 2026 19:05:00 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:5733bd14ccbb150b0dcb399c5fec92bb7770cf196da4e193f3dc54c124ddd68d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.9 KB (639946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87621ca62a33d919675198da6f077458d9655803d9a76abd01d4f52051a17d18`

```dockerfile
```

-	Layers:
	-	`sha256:def130f3a5e66790b98049067e4711fb6597761394e694b1afbec53b59ede60d`  
		Last Modified: Thu, 14 May 2026 19:04:57 GMT  
		Size: 596.3 KB (596300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71335660fa9616d77857bb05887dc7c721f078781751d4a6d5ef468cb6a80ebb`  
		Last Modified: Thu, 14 May 2026 19:04:57 GMT  
		Size: 43.6 KB (43646 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:cc027a7682a53b33194bfdbc6548d528f809c804f73bdaf13e80e921d4fde7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93330074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7397368fe21d9b8138d4f876625fb0f4159e455a94b65ea181dacd3c4e8a4fc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 19:32:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 19:32:48 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 19:32:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:43:00 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 May 2026 19:43:00 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:43:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:43:00 GMT
ENV PG_MAJOR=16
# Thu, 14 May 2026 19:43:00 GMT
ENV PG_VERSION=16.14
# Thu, 14 May 2026 19:43:00 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Thu, 14 May 2026 19:43:00 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:46:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:46:21 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:46:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:46:21 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:46:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:46:22 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:46:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:46:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:46:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:46:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:46:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:46:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063a9d5349dd7c559d9d4da649111e6f9ab000e140d7cddeb891987f33961190`  
		Last Modified: Thu, 14 May 2026 19:36:37 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf0cfbfef73e4ce590e63f32fa324f98af1783d6550c842d675efb1004954ec`  
		Last Modified: Thu, 14 May 2026 19:36:37 GMT  
		Size: 878.3 KB (878314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4796daed0dde9f1f97a712616dffc62702d477bdf4462233f5b1ddd5168b7c25`  
		Last Modified: Thu, 14 May 2026 19:46:48 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e7b581ed5f595b5f506f502069a68df3e715783a65588c878d1a2e13e609ae`  
		Last Modified: Thu, 14 May 2026 19:46:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8172a4f8775be15ed24ca0e0c41079370120d0607c308fc7b26a6b6bb5d3e1a8`  
		Last Modified: Thu, 14 May 2026 19:46:52 GMT  
		Size: 88.7 MB (88697631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb5317623f05ac94bd7094d65da4433490dad082055bab64fa8db5b5d716454`  
		Last Modified: Thu, 14 May 2026 19:46:48 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e11f03f47299c1a82ee664abf64dfc463c9fa7a86910c220abeff7d9aa8baff`  
		Last Modified: Thu, 14 May 2026 19:46:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85cc5a414412172de6def02f1e1ccde35fa73f2a8c12ee3d5e9d3cfb7b56c920`  
		Last Modified: Thu, 14 May 2026 19:46:49 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05679b53c52529f55ed182547d5718031c84553473d8c7ab4b7978787574a8a3`  
		Last Modified: Thu, 14 May 2026 19:46:49 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5577781c52d082493b47ff0a9c74a7ec588c3a2bf3262be7690b2770ad997aae`  
		Last Modified: Thu, 14 May 2026 19:46:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:cf9a040a769a99aabf02faa6388e75a313478a28928e09295fc602a3b780941b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.5 KB (636450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d1f3834e32dc433f57e19394ae869dc62b188a833fac042d7b0962063e14a1`

```dockerfile
```

-	Layers:
	-	`sha256:6cef9e1c0b2908ded39e7c52f0b31d5c5a33fe04c3723ba2ebe8b91c64eaa752`  
		Last Modified: Thu, 14 May 2026 19:46:48 GMT  
		Size: 592.7 KB (592724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c187f02d6e12d4c3ec9529873193e705a822f34b46e2b0f999dbed4b469b96e`  
		Last Modified: Thu, 14 May 2026 19:46:48 GMT  
		Size: 43.7 KB (43726 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:50ac318686ff1a7b450a12e94f7baec518c03b2a818a70387b5995917d6cde70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109509535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8925c23fca116ed4371c81f1728c9ee4147c06ea044cf7b041d902a9d37966c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Apr 2026 22:19:29 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 18 Apr 2026 22:19:41 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 22:19:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 19 Apr 2026 00:09:40 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Sun, 19 Apr 2026 00:09:40 GMT
ENV LANG=en_US.utf8
# Sun, 19 Apr 2026 00:09:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 19 Apr 2026 00:09:40 GMT
ENV PG_MAJOR=16
# Sun, 19 Apr 2026 00:09:40 GMT
ENV PG_VERSION=16.13
# Sun, 19 Apr 2026 00:09:40 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Sun, 19 Apr 2026 00:09:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sun, 19 Apr 2026 00:59:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sun, 19 Apr 2026 00:59:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sun, 19 Apr 2026 00:59:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sun, 19 Apr 2026 00:59:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 Apr 2026 02:43:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 22 Apr 2026 02:43:22 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 Apr 2026 02:43:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:43:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 Apr 2026 02:43:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:43:22 GMT
STOPSIGNAL SIGINT
# Wed, 22 Apr 2026 02:43:22 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 Apr 2026 02:43:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587d8e2fd99fe429bf8f22467e93aa876a5641cf7de4fb04ba99bc68a0de695d`  
		Last Modified: Sat, 18 Apr 2026 23:12:22 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a506d334faeab2227b02d175475320187eefeaba57ea193e2009ba29e541869c`  
		Last Modified: Sat, 18 Apr 2026 23:12:22 GMT  
		Size: 865.7 KB (865729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f543374540548ed25d21a9e27ed05634b45db7d52ac867c7012b33d97d3c10d5`  
		Last Modified: Sun, 19 Apr 2026 01:02:00 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d359d51e2e8031e5cfd1dd7c3bffcfedc6a35698e11754161def0ed81d40b1d8`  
		Last Modified: Sun, 19 Apr 2026 01:02:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5df64524e3a115aead5178ed7b78f5828abe2ec888d161c7d95be21d1a596f`  
		Last Modified: Sun, 19 Apr 2026 01:02:16 GMT  
		Size: 105.1 MB (105105451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b04615657019c4de354ea1dc9066fdd6fed450be6f42c28b11b142047d6db22`  
		Last Modified: Sun, 19 Apr 2026 01:02:00 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2993afb9c3a2d0cf6b80a49ac4a397ed140752a83bbbb7b5a6b761782b595053`  
		Last Modified: Sun, 19 Apr 2026 01:02:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193b4e891662fda8e16345a112f7296b25a3a0975f58806f65a0ca1876a76378`  
		Last Modified: Wed, 22 Apr 2026 02:44:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7092058199b0cd6616669741f60f79fe964b46cbd5b9b24dbfd0f33df06cc90f`  
		Last Modified: Wed, 22 Apr 2026 02:44:37 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b709e3d137b21dc1302bc2d69b7e625177eb131329945a3dde89c99c23c2c`  
		Last Modified: Wed, 22 Apr 2026 02:44:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:be4a928e6d474085d3feceb687ff274c63a162045ce03309ae73a693581f4235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.1 KB (638114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3a7d0b217bfc1329ad7bfb82c9a5d0a6499dc61c5c87fb769942f82e8c13ef`

```dockerfile
```

-	Layers:
	-	`sha256:3293e6ff8627f64b79904346056356ddb810570b23916332980b84f24c411774`  
		Last Modified: Wed, 22 Apr 2026 02:44:37 GMT  
		Size: 594.4 KB (594382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d74d51657458051a78a435cc2319b9c59faa3ba953591cb51e4887a58e3f8b96`  
		Last Modified: Wed, 22 Apr 2026 02:44:37 GMT  
		Size: 43.7 KB (43732 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:835614f9e1564ad2b3c8f6b6b8cdee7ab238a59a46911b5b23052271660c901c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118263523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf6cc00f4182d6e00f421fc3c2de9fcdbf516e17f8063020afd0dfe3e7863b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 18:56:45 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 18:56:48 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 18:56:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:15:29 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 May 2026 19:15:29 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:15:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:15:29 GMT
ENV PG_MAJOR=16
# Thu, 14 May 2026 19:15:29 GMT
ENV PG_VERSION=16.14
# Thu, 14 May 2026 19:15:29 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Thu, 14 May 2026 19:15:29 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:18:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:18:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:18:15 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:18:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:18:15 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:18:15 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:18:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:18:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:18:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:18:15 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:18:15 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:18:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e81ceb38917acc4cf3d16bd98043e33a3e2c28415750a8e7da557756eba88c`  
		Last Modified: Thu, 14 May 2026 19:00:13 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ba055b6cddec7c6e4795ffdf5ed7ca4139e686e84c442c3304cfa93062746b`  
		Last Modified: Thu, 14 May 2026 19:00:14 GMT  
		Size: 894.2 KB (894241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cb7ac96de663dd2155f796798e81cfeda611f8d24fcff9b074f0eb95f5d8da`  
		Last Modified: Thu, 14 May 2026 19:18:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894bd021bd9427470d9fc59298b7f68bf02c14e8bbad6a1fa5c0b1135017a976`  
		Last Modified: Thu, 14 May 2026 19:18:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e3f18c7bf3503d0685749b2999bc7dd08c825632254078e6ff60b0c47ddf74`  
		Last Modified: Thu, 14 May 2026 19:18:41 GMT  
		Size: 113.7 MB (113697947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10442fe74311775feff5fdb609a22aa4326092c17b9b6c303a76bf9c8621a10e`  
		Last Modified: Thu, 14 May 2026 19:18:38 GMT  
		Size: 9.6 KB (9621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da5efaab47187b011aaa9d5f174c3356dd67266fbadd63ba883fddc2e70a44`  
		Last Modified: Thu, 14 May 2026 19:18:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b58ea2952b202c9fc5c965228782bd3aaa416191c2fe0cc18bfbe89c81433ad`  
		Last Modified: Thu, 14 May 2026 19:18:39 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63987c3f2ba4ad687636e0765c1b34dad75c97aaeebc338b218b0db3c63822cb`  
		Last Modified: Thu, 14 May 2026 19:18:40 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c0d0189ba30d18638b6b3737ad8a050bf79e6e043bf1dd75d9cbff786e6993`  
		Last Modified: Thu, 14 May 2026 19:18:40 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:397a2c3182100661598649f4c38ed396583379fc65f4ab74db158b745897077e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.0 KB (638048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa16c4303be23f5149981899bcdc6fd4cd028cc77950f9be99cd6591ad7244c`

```dockerfile
```

-	Layers:
	-	`sha256:1675de9988b6e6078c0efa654cb8ddd43ff82b4ac46b326f7e31bf36b71b00f7`  
		Last Modified: Thu, 14 May 2026 19:18:39 GMT  
		Size: 594.4 KB (594364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18317d7e7e8c829135a79142b84e536af1650c8bee9f4ba44617d2daf95f79b6`  
		Last Modified: Thu, 14 May 2026 19:18:38 GMT  
		Size: 43.7 KB (43684 bytes)  
		MIME: application/vnd.in-toto+json
