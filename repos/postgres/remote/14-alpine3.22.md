## `postgres:14-alpine3.22`

```console
$ docker pull postgres@sha256:24edb669d247dd33551a8574e75b3b12bdc1afd1eea4d148ec44d21c2c2c5596
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

### `postgres:14-alpine3.22` - linux; amd64

```console
$ docker pull postgres@sha256:efc1a7609f139b9ebf6f46ac3803a04ee4500b261286c71a3f851953b0c731d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108102325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b618517f8f44bb00d92b688aa19160bd5a48d3f8fa5b1bc47180e1568233a5cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:06:28 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:06:31 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:06:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:06:31 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 12 Feb 2026 21:06:31 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:06:31 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:06:31 GMT
ENV PG_MAJOR=14
# Thu, 12 Feb 2026 21:06:31 GMT
ENV PG_VERSION=14.21
# Thu, 12 Feb 2026 21:06:31 GMT
ENV PG_SHA256=5b30f19347efff32b6e09ed2cdff0b04e9aee913ec9bb7414de2b7c17b17f1f9
# Thu, 12 Feb 2026 21:06:31 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:08:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:08:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:08:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:08:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:08:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:08:44 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:08:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:08:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:08:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:08:44 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:08:44 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:08:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b094645d942865bc5bc7ae6064d445290609fd3d77b20f60af74e4a4ed7df6e`  
		Last Modified: Thu, 12 Feb 2026 21:09:00 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7975b804ce826de1da68fb81da455d50b302ff08643349da7d5c3a568698b24`  
		Last Modified: Thu, 12 Feb 2026 21:09:00 GMT  
		Size: 918.3 KB (918291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa218898d5d96565da0c1e156e5dbf55ce9998d4e0f83344b8f7faed1ed4dda`  
		Last Modified: Thu, 12 Feb 2026 21:09:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f00b139db6ada6fcb8ac86a7a8a92c5ee6b12fb6f5e5560e7ef3a36902202d`  
		Last Modified: Thu, 12 Feb 2026 21:09:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cbe416de424123d105e51b1fb498e4eb86c5a990191529c1eb3ea4d44fac9b`  
		Last Modified: Thu, 12 Feb 2026 21:09:04 GMT  
		Size: 103.4 MB (103362365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d53403cf7102f486c6d2f6a25e98c07c2a90815f678a6bb4732ccae9284ba7`  
		Last Modified: Thu, 12 Feb 2026 21:09:01 GMT  
		Size: 9.2 KB (9208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baed350074d7ffccdd9d2768f9d5e7d00b17e155ebe983466a532122a589e751`  
		Last Modified: Thu, 12 Feb 2026 21:09:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d6561473674ee3c76ee990c03dcbdf73e030f9ee4d83a013d41c1b627d765c`  
		Last Modified: Thu, 12 Feb 2026 21:09:01 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e6a673440178ea0c4b2b6a57027b80f1d16775dab954f92dc7804f87668137`  
		Last Modified: Thu, 12 Feb 2026 21:09:02 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1236a57977f2fab3db59308287ff2139a6596d10a680a5cd0ebfb89289f445f1`  
		Last Modified: Thu, 12 Feb 2026 21:09:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:e8c6e363b51f829fd8c35dc8d271b045a5d306522e1bf85400b33b92300bd0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.8 KB (639764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16b77535b9271b1e141257b1f000949b5d33180c6e39b195860ea76a6d7321c`

```dockerfile
```

-	Layers:
	-	`sha256:9b46e43410d8541225bb4d33a253366187aa54019d46bddc29263f594c18782b`  
		Last Modified: Thu, 12 Feb 2026 21:09:00 GMT  
		Size: 596.3 KB (596315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4fd495825384f0be3f15a3451c4f5268abf5e5e01f4608d11a2269588db37fb`  
		Last Modified: Thu, 12 Feb 2026 21:09:00 GMT  
		Size: 43.4 KB (43449 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:8b2ca76f65528ff1e9e739d37118777385449556c48d1961a7c2e4169fb90e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87717082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d617d530f5433c36adabdaa2ad8dfde680d53b0b60b98b9cee0ccbce60c0904`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:26:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:26:20 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:26:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:26:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 12 Feb 2026 21:26:20 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:26:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:26:20 GMT
ENV PG_MAJOR=14
# Thu, 12 Feb 2026 21:26:20 GMT
ENV PG_VERSION=14.21
# Thu, 12 Feb 2026 21:26:20 GMT
ENV PG_SHA256=5b30f19347efff32b6e09ed2cdff0b04e9aee913ec9bb7414de2b7c17b17f1f9
# Thu, 12 Feb 2026 21:26:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:32:11 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:32:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:32:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:32:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:32:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:32:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:32:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:32:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:32:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:32:12 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:32:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:32:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a397dde5dd7a730bb58dd40d9a248ed78469b86e6ae29b66f36fa72e39f6e002`  
		Last Modified: Thu, 12 Feb 2026 21:29:18 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87b2b96543699650c8fdbb5226367abfd14e872bead4f291066243c70dc6fa1`  
		Last Modified: Thu, 12 Feb 2026 21:29:18 GMT  
		Size: 886.1 KB (886134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d8a929257b20d010f49c64f4c6ad1a4859e501b32d15b05cbd5d7459da8a41`  
		Last Modified: Thu, 12 Feb 2026 21:29:18 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bbd2025e960e01c889567b61bc6d7397449f06fddf2bc4f801c92f96979f52`  
		Last Modified: Thu, 12 Feb 2026 21:29:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99848bed6fb0df5649283d3adc36f413c138be836ba57b53a09234528735a89d`  
		Last Modified: Thu, 12 Feb 2026 21:32:24 GMT  
		Size: 83.3 MB (83309112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915f1ed5a324f62cdaeaf13396b7f60f89fc7183b897166d56f9b072a3e5db49`  
		Last Modified: Thu, 12 Feb 2026 21:32:22 GMT  
		Size: 9.2 KB (9206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fe457c4fb5c09849ca1ad00f90e6bb012b15b2f329bc74d38395c25942a565`  
		Last Modified: Thu, 12 Feb 2026 21:32:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672020a72ec1642c726623af3d672a9505d5bf416465dedc70687ef7b1c5bcfd`  
		Last Modified: Thu, 12 Feb 2026 21:32:22 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d16413f873d2f2d35ba90767ea5b9f99ec63785cbd39bbf2558072473376802`  
		Last Modified: Thu, 12 Feb 2026 21:32:23 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78b0804c552845bec196f522ab4c5d55b5c3cd8e1ce8d93e4ed9c82539c7fe1`  
		Last Modified: Thu, 12 Feb 2026 21:32:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:db2c1fbff981869404aa90ec08659ef61ff139e56c813a07e17f11584019acfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 KB (43396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56190261801e1e7120b2c56f2ae944fee23461cff7430456ca2cb815049a3a51`

```dockerfile
```

-	Layers:
	-	`sha256:fb282db09497e9ae53bab332261480f1c8e6f35334965505908ed8add1e81087`  
		Last Modified: Thu, 12 Feb 2026 21:32:22 GMT  
		Size: 43.4 KB (43396 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:9da2e9984e40c5c094ef1b98a7c78a2c6f14d4052d23c8c042ec3dc9b3fb108f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83024362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb9b137465d733d119b8b4ada05c35220402635a6e9c2472ea24cf7d110ada1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:35:53 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:35:57 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:35:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:35:57 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 12 Feb 2026 21:35:57 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:35:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:35:57 GMT
ENV PG_MAJOR=14
# Thu, 12 Feb 2026 21:35:57 GMT
ENV PG_VERSION=14.21
# Thu, 12 Feb 2026 21:35:57 GMT
ENV PG_SHA256=5b30f19347efff32b6e09ed2cdff0b04e9aee913ec9bb7414de2b7c17b17f1f9
# Thu, 12 Feb 2026 21:35:57 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:38:33 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:38:33 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:38:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:38:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:38:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:38:33 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:38:33 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:38:33 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:38:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:38:33 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:38:33 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:38:33 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8007d13b70e44b25cfa5ca4aefbee37d3a9cfae1bee221b632217703ca93f`  
		Last Modified: Thu, 12 Feb 2026 21:38:44 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa1a68f6761356b2db4ba111435184accdfd53bfb255eaed8b4d14bfe409544`  
		Last Modified: Thu, 12 Feb 2026 21:38:44 GMT  
		Size: 886.1 KB (886136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b0f39aa085ebab1dbb4689adbd25d01ba2caa04d8ac9f02806db9c9ea5ba9b`  
		Last Modified: Thu, 12 Feb 2026 21:38:44 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5180e55ac38137b6e0ba5ef47df4a7a4184b725282ec45848ce0ac68aa8c4986`  
		Last Modified: Thu, 12 Feb 2026 21:38:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6be190c8a6f922ae62449e30f43be9ea7feb9d684d350e5cf20a46429828b9`  
		Last Modified: Thu, 12 Feb 2026 21:38:48 GMT  
		Size: 78.9 MB (78897805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7ea3dd03b00853db56fd7c55fb16601d6c55c909b3eb2d0cb55390d2cf60ba`  
		Last Modified: Thu, 12 Feb 2026 21:38:45 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41693300e5fa97a0151233671776a2e8f5c173b48c808f52942078c0c030eabf`  
		Last Modified: Thu, 12 Feb 2026 21:38:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f14c00be884ebf47290ab71f6f97e609d657abf9e276457738884da9027972`  
		Last Modified: Thu, 12 Feb 2026 21:38:46 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa860245c6fc2a9b4379a3e4539c222fadbe576af11a81eccd84a1bb2e30b98c`  
		Last Modified: Thu, 12 Feb 2026 21:38:46 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d93fb7b67d85d63608ecd7e929a7dd040487a1baae3bca12e9d833f1a65340`  
		Last Modified: Thu, 12 Feb 2026 21:38:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:8265803b14e012786da40a67b1bbda937ee0324a9af8fd2e8a24cefccba8343c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.9 KB (639946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6888a1a3e5246b0b79a8001c289a96c89445d9d81e6cef7c3662b31a567126`

```dockerfile
```

-	Layers:
	-	`sha256:371332c683025e32dc4ef3ab0ba168148d96af2d82542b6883d103358f42d2e2`  
		Last Modified: Thu, 12 Feb 2026 21:38:44 GMT  
		Size: 596.3 KB (596335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ce214e324ae7409b84a43425e6f2dd3a29bc8dc5cad513a543e2619b6b2871`  
		Last Modified: Thu, 12 Feb 2026 21:38:44 GMT  
		Size: 43.6 KB (43611 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:37d80c743c589d55adeebb744d7a6ceb6dabdc0df4d64706e57c74764a77fe81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104073646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b813609e133ff5062111dd53fbc2ee0e20f003bf64561a20eef03b813f2b1f56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:06:59 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:07:02 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:07:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:07:02 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 12 Feb 2026 21:07:02 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:07:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:07:02 GMT
ENV PG_MAJOR=14
# Thu, 12 Feb 2026 21:07:02 GMT
ENV PG_VERSION=14.21
# Thu, 12 Feb 2026 21:07:02 GMT
ENV PG_SHA256=5b30f19347efff32b6e09ed2cdff0b04e9aee913ec9bb7414de2b7c17b17f1f9
# Thu, 12 Feb 2026 21:07:02 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:09:26 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:09:26 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:09:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:09:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:09:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:09:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:09:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:09:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:09:26 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:09:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:09:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269c5e439b00c3a91018f6a1c2eaa3a31922bc3cc02f5785054d49fe21f5ffe5`  
		Last Modified: Thu, 12 Feb 2026 21:09:40 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235d3ab7ef057f05919c10c2a3a28720fb1a55c4b341bc0893842a13a9774bff`  
		Last Modified: Thu, 12 Feb 2026 21:09:40 GMT  
		Size: 873.5 KB (873484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fd7d8e6d72aef64ac6791cc67b05edfc1b612dfb6928f8f2896f79aabcb892`  
		Last Modified: Thu, 12 Feb 2026 21:09:40 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8370515ee8ad8af76df295ee582aa6b8fc1f6df048a0a0a2c891feb56c98d40d`  
		Last Modified: Thu, 12 Feb 2026 21:09:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f761f678412cf737248bb9951193cc9c74b550188bba5841c6614b20a9c4b4`  
		Last Modified: Thu, 12 Feb 2026 21:09:44 GMT  
		Size: 99.0 MB (99043846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa8fbbf201518907088a91e1dcf8b59941fa99cad6c45aaa44ec53b1b7e9598`  
		Last Modified: Thu, 12 Feb 2026 21:09:42 GMT  
		Size: 9.2 KB (9208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a7476f6388e6353e7367ae675593b36904fa89d64b833865e33175f2158d6a`  
		Last Modified: Thu, 12 Feb 2026 21:09:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf335717d373c8b7770baae3320187567673b68befe0a8ecb19bdaaec8859b5`  
		Last Modified: Thu, 12 Feb 2026 21:09:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b95f2bfff72eca31aebbb8c943ed4da0f1ff9d6ba46ac1fa83acd32af6b0d9`  
		Last Modified: Thu, 12 Feb 2026 21:09:43 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a414e66e55852b51f5242d025ece2c596419f13c639b451ba02a206770853a`  
		Last Modified: Thu, 12 Feb 2026 21:09:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:0b76800236f27a3eb539586f930a546d12a417f8803d5f5ba58cad39c278b2ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 KB (639989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecadda037d421c3ae02d8a7f36269c59c728b29b0c7bf2e268d48269705938e`

```dockerfile
```

-	Layers:
	-	`sha256:04e76a681708e1748477c936847c5a27f97a9e77b87055f343c5a59f186900af`  
		Last Modified: Thu, 12 Feb 2026 21:09:41 GMT  
		Size: 596.3 KB (596347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25c34fdaf6930e20e038114da74481348db7f9832a4cfcb54fc60d2b3ddaef5`  
		Last Modified: Thu, 12 Feb 2026 21:09:40 GMT  
		Size: 43.6 KB (43642 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:43f0af82248ff3b328fd3f033505cb637cdfc240e5cf5ada730ddfe566ef970f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114330302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4104e4dbcd9d8777aa1e96e9849132f87503df5a44e5749d11598f7f8176c36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:14:53 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:14:57 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:14:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:14:57 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 12 Feb 2026 21:14:57 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:14:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:14:57 GMT
ENV PG_MAJOR=14
# Thu, 12 Feb 2026 21:14:57 GMT
ENV PG_VERSION=14.21
# Thu, 12 Feb 2026 21:14:57 GMT
ENV PG_SHA256=5b30f19347efff32b6e09ed2cdff0b04e9aee913ec9bb7414de2b7c17b17f1f9
# Thu, 12 Feb 2026 21:14:57 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:17:35 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:17:35 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:17:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:17:35 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:17:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:17:35 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:17:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:17:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:17:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:17:35 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:17:35 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:17:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1bad5c151a9893218826094ac6d4f20f5f6993c7830b7731b8f4c5c243873a`  
		Last Modified: Thu, 12 Feb 2026 21:17:52 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431551acbbedff7423b0305f531ee279b1f2d45b77d8d46ca1868a17d7e1dddf`  
		Last Modified: Thu, 12 Feb 2026 21:17:52 GMT  
		Size: 890.6 KB (890639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d0d79102415ecc8395624b760cb790f0d1316c986679d744bd085d31de48c2`  
		Last Modified: Thu, 12 Feb 2026 21:17:52 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f83c5f5ed8fe5db1fea24403becc35695c37f16990bd49581d70207e2175dd`  
		Last Modified: Thu, 12 Feb 2026 21:17:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796cfdb9aa46941019381d7c4c69b2badb45cf1ad0f047d972e682624da24a23`  
		Last Modified: Thu, 12 Feb 2026 21:17:55 GMT  
		Size: 109.8 MB (109802146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbaf6d327dbd820a340df54a4d57e69ec9e3eb06b0d552e4a766ac4ed2c0943`  
		Last Modified: Thu, 12 Feb 2026 21:17:53 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7941f50b4eaa07d24dc632a40bf53b8b7933e31d573e47519640bbe1d837f61`  
		Last Modified: Thu, 12 Feb 2026 21:17:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc04e279e95f221b1307beb9c18c73bb8575dc1821711161b05d3389c1960524`  
		Last Modified: Thu, 12 Feb 2026 21:17:53 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bb78a869709baf5b7ed7ad1469cb75d267f94d3b9c14302c319609161bfd8a`  
		Last Modified: Thu, 12 Feb 2026 21:17:54 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bae550ba26b924ceeb0740a45789704b9b1d44526f986a98244bfabb2f88ba`  
		Last Modified: Thu, 12 Feb 2026 21:17:54 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:5b4c218f043b82eaee24b5414dedd71363956f2c9b985371867df57cba7a50a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.7 KB (639711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5756694ec2cb5fabac76a5d4d98826c6b4ec1e55737ffdb84aad8aca05ef9c8`

```dockerfile
```

-	Layers:
	-	`sha256:8c3f81672bef0af106b89f59de63a8c280da4f9ce8c998ca534a419bf22537e8`  
		Last Modified: Thu, 12 Feb 2026 21:17:52 GMT  
		Size: 596.3 KB (596300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0604fd228f7b818c6471adbf8de9a77c850c6e08b360cb9b73f3b3b2c8212b73`  
		Last Modified: Thu, 12 Feb 2026 21:17:52 GMT  
		Size: 43.4 KB (43411 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:a82b15fb4612ab0e97f1226ad9da7dc0523f8a18ce6e5a061940a6bac278a442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91802305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea48c5daa971c953e4f3f5fd65c43942a0356bfb30543315bfb4b6ad95ec396`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:06:00 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:06:12 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:06:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:20:55 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 12 Feb 2026 21:20:55 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:20:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:20:55 GMT
ENV PG_MAJOR=14
# Thu, 12 Feb 2026 21:20:55 GMT
ENV PG_VERSION=14.21
# Thu, 12 Feb 2026 21:20:55 GMT
ENV PG_SHA256=5b30f19347efff32b6e09ed2cdff0b04e9aee913ec9bb7414de2b7c17b17f1f9
# Thu, 12 Feb 2026 21:20:55 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:37:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:37:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:37:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:37:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:37:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:37:27 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:37:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:37:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:37:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:37:29 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:37:29 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:37:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c65175e4a78e75c1adc1c569354fe719e50457fdbdd1612adccbd559da08c1`  
		Last Modified: Thu, 12 Feb 2026 21:11:11 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47af42dfcd093de1f52666dfa1cb8ed4291e124998435eea188cac1feb2ef729`  
		Last Modified: Thu, 12 Feb 2026 21:11:11 GMT  
		Size: 879.0 KB (879036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ad419382e4519d75f62994b2c5bec169e780789538a63d941296bcf7f49126`  
		Last Modified: Thu, 12 Feb 2026 21:25:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7389cbb885ef73ff25cacff4abbf31ba700e476d89b7e2ef481dc9d61cf2b503`  
		Last Modified: Thu, 12 Feb 2026 21:25:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73ddee897699b58cae1680069b6b2ebb0295fa477eadb6ec78cf5caf33efbdf`  
		Last Modified: Thu, 12 Feb 2026 21:38:06 GMT  
		Size: 87.2 MB (87172168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e73e343701f31323fd8a07efa98ea0d8523ff6517ab2f29b3fbbea20c16f81`  
		Last Modified: Thu, 12 Feb 2026 21:38:03 GMT  
		Size: 9.2 KB (9211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d517f7278cb2f11997d80672c88aa0fb8975a89753369bafc0a016640fcee72`  
		Last Modified: Thu, 12 Feb 2026 21:38:03 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5bb040fe8dd2d5ea5d0ee30a9e56160aa1a89b646f5e94acf86c1effb588bd`  
		Last Modified: Thu, 12 Feb 2026 21:38:03 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29403c0c396b244ff395d9c752fd347ebe0a8ee705b4d31c4220b99c008c804f`  
		Last Modified: Thu, 12 Feb 2026 21:38:04 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cf2aa5199a12278e75032843fc4f5fc83cfce09ecebcd693c65e262777ff5a`  
		Last Modified: Thu, 12 Feb 2026 21:38:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:ccd8f73344fb978323d4ef55e2e8f77b787dabfeadd4a824011516e8c8c288e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.2 KB (636215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2380ee4d2980f8e969ad3265fb70690b97bf8b064757033e75858c2ac1de5006`

```dockerfile
```

-	Layers:
	-	`sha256:e1b9b02a50754f5c4bef1a9751377bec3974ba9952d71098254fe066b39c2f84`  
		Last Modified: Thu, 12 Feb 2026 21:38:03 GMT  
		Size: 592.7 KB (592724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9023a82ee68900edfbf58505ac113074d046ca582f4771325b389344350b4211`  
		Last Modified: Thu, 12 Feb 2026 21:38:03 GMT  
		Size: 43.5 KB (43491 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:2dd50e7b67e320eaa81a5c7a794cb67b7a777a6d141c3d32f26bbcb1e01cb3bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (107958205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6515332a4894edbae37008fd95ee41fdf926e6b87335f6bf1fcacc23f64758`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Fri, 13 Feb 2026 00:03:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 13 Feb 2026 00:03:22 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Feb 2026 00:03:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Feb 2026 08:02:34 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 13 Feb 2026 08:02:34 GMT
ENV LANG=en_US.utf8
# Fri, 13 Feb 2026 08:02:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 13 Feb 2026 08:02:34 GMT
ENV PG_MAJOR=14
# Fri, 13 Feb 2026 08:02:34 GMT
ENV PG_VERSION=14.21
# Fri, 13 Feb 2026 08:02:34 GMT
ENV PG_SHA256=5b30f19347efff32b6e09ed2cdff0b04e9aee913ec9bb7414de2b7c17b17f1f9
# Fri, 13 Feb 2026 08:02:34 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 13 Feb 2026 16:14:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 13 Feb 2026 16:14:58 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 13 Feb 2026 16:14:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 13 Feb 2026 16:14:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 13 Feb 2026 16:14:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 13 Feb 2026 16:14:59 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 13 Feb 2026 16:14:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 16:14:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 13 Feb 2026 16:14:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Feb 2026 16:14:59 GMT
STOPSIGNAL SIGINT
# Fri, 13 Feb 2026 16:14:59 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 13 Feb 2026 16:14:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9a8d29c18a7aa35e1e673e585403324e4011c659e3a9af9631eeef53eb1abe`  
		Last Modified: Fri, 13 Feb 2026 00:55:28 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56f6ced6daa9dca5801962fab9724b150e63d0b23f3667a8a57104fdc08d51d`  
		Last Modified: Fri, 13 Feb 2026 00:55:28 GMT  
		Size: 866.6 KB (866630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fefaa019570f036a479949adc1cff90d83d62dfcccda924ecbc9fb276d79751`  
		Last Modified: Fri, 13 Feb 2026 08:54:08 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c700cb03d9440f65627954050639f9bd8240858a9a31624103d7f2d177b38f8`  
		Last Modified: Fri, 13 Feb 2026 08:54:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345a42ce01e78b48650fe08ecb4e8b45d9cfaa19815a264688ca9e2e12c3cb97`  
		Last Modified: Fri, 13 Feb 2026 16:17:59 GMT  
		Size: 103.6 MB (103557345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60280662d1fd3f5b98c1b0a17b0c9ca0be72ea26363b04f8f7c8787b5dfb92d9`  
		Last Modified: Fri, 13 Feb 2026 16:17:43 GMT  
		Size: 9.2 KB (9212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f713c378fec9449bcdc5e33b1eee930764f94a685528020c73c53f31b8e765d5`  
		Last Modified: Fri, 13 Feb 2026 16:17:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2df25f3d7b57433a52630e58753c3abdd1b12c7eb49243a6e944dba94dbe9d`  
		Last Modified: Fri, 13 Feb 2026 16:17:43 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4febdad82c626f9d37ea4789cf9deaea1e68454667345a0db1aab3f6d13d567`  
		Last Modified: Fri, 13 Feb 2026 16:17:45 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0871420f92c21610937c19d3de9a870c7232d25838cabccc47cf3fd56b2ae3e8`  
		Last Modified: Fri, 13 Feb 2026 16:17:45 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:a7c701ab290f301047ef37bd56e19bff4145a05366db9cf277bb2b088659ec8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.9 KB (637879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9b2d66fa88c40b91f486977bc3b62e6644f862f1b719a6d0877f1d8a1a2a3a`

```dockerfile
```

-	Layers:
	-	`sha256:58982de57774d8f3f68921c51c7c56fb028bdc2690e0e74db482693789d1019c`  
		Last Modified: Fri, 13 Feb 2026 16:17:44 GMT  
		Size: 594.4 KB (594382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8590ff2a26a2344900cb34c69c8e538cfc191b53f5a953556d654c07b629bb1e`  
		Last Modified: Fri, 13 Feb 2026 16:17:44 GMT  
		Size: 43.5 KB (43497 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:bd4396022aab60ad3f91ad859edf765827ed99bb06ecb5e59e0e1a9de066197d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116775411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0350e7f5effcd87eda357cc0919de55569dc22895f475d2961a07a0c86cef2af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:34:10 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:34:14 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:34:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:34:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 12 Feb 2026 21:34:14 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:34:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:34:14 GMT
ENV PG_MAJOR=14
# Thu, 12 Feb 2026 21:34:14 GMT
ENV PG_VERSION=14.21
# Thu, 12 Feb 2026 21:34:14 GMT
ENV PG_SHA256=5b30f19347efff32b6e09ed2cdff0b04e9aee913ec9bb7414de2b7c17b17f1f9
# Thu, 12 Feb 2026 21:34:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:40:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:40:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:40:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:40:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:40:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:40:44 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:40:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:40:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:40:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:40:45 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:40:45 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:40:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c3205a31422db5f1d21f9287edffcb4c15fd82e299f125e6c299903e2fae0a`  
		Last Modified: Thu, 12 Feb 2026 21:37:33 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7d2414ef6dbefbb62ac460a104ea7740c3ff2b1a1ecd11a590a50c5ea0837f`  
		Last Modified: Thu, 12 Feb 2026 21:37:33 GMT  
		Size: 894.4 KB (894417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88392939a0c808ed836ad928ac5958babab18c4135732563dd013cd106fbf192`  
		Last Modified: Thu, 12 Feb 2026 21:37:33 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652432cea04bc794584eae84181beeb3468384d4879d8e44aca63f753d0543c0`  
		Last Modified: Thu, 12 Feb 2026 21:37:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e565d9a1bd830a7694f175a50af0357f7c55ce6601a21b533da67b5155bd15`  
		Last Modified: Thu, 12 Feb 2026 21:41:11 GMT  
		Size: 112.2 MB (112213775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e92ddf0672abb7406aaf1ab864b907c77532411ec0142d6c0554b7d5ffe6cae`  
		Last Modified: Thu, 12 Feb 2026 21:41:09 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241846f75b6c295b0b6ffda6c11487404360260cdfc47009432f8323ff75a134`  
		Last Modified: Thu, 12 Feb 2026 21:41:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28302e78a9924a8d51353ca4e37ed0fbd5ac3ee7abbe2bddb6e15424b75da9bf`  
		Last Modified: Thu, 12 Feb 2026 21:41:09 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e5c00f0b4e30896d07a4eb67d14fe56d8dda58ebd0b681dec51ea5e19b2980`  
		Last Modified: Thu, 12 Feb 2026 21:41:10 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d489a9b6481c2ce397e6095b8ae58c2c1aa6a45fc2a07145f39961af29e1c7f4`  
		Last Modified: Thu, 12 Feb 2026 21:41:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:7dcacad3293a0149928374e9313027879bd60a64fc274ddc62185cd9d7b3380c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.8 KB (637812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c317c1c84fe54324538b9593c52bf2851908e523f26727a2264c9b1008e96eb`

```dockerfile
```

-	Layers:
	-	`sha256:b620219bb882c9c42de246621ca41f9b1d651e8188cfb5176b8124dbc00af6b2`  
		Last Modified: Thu, 12 Feb 2026 21:41:09 GMT  
		Size: 594.4 KB (594364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f9887cce726a7947f0fef577d33d24f551a6891ca066ce7f58c5da035c0f808`  
		Last Modified: Thu, 12 Feb 2026 21:41:09 GMT  
		Size: 43.4 KB (43448 bytes)  
		MIME: application/vnd.in-toto+json
