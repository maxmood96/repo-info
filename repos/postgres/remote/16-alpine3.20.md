## `postgres:16-alpine3.20`

```console
$ docker pull postgres@sha256:1e59919c179e296eaf3cc701f4d50bab5c393d7ed9746c188c9d519489c998dc
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
$ docker pull postgres@sha256:87e78f4b4d42f6a8f8b66af1487001a2e6f88ed1fdbd6ea2d8b582bda339dd84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96931904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730ab365c318c9f4abd67d6b0204f1e92fc58e03ac8212d62b50df388e39823f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=16
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=16.6
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=23369cdaccd45270ac5dcc30fa9da205d5be33fa505e1f17a0418d2caeca477b
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cebd8fef2e22e938a02b5261ec865a084cff3519c6b4190af1b8cc8cba4515`  
		Last Modified: Tue, 04 Feb 2025 20:35:45 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba08964117e3a2a363a81b957aa3769b05cea9f6205687af656ee94a29a6bf6`  
		Last Modified: Tue, 04 Feb 2025 20:35:45 GMT  
		Size: 1.1 MB (1120288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a434e24eaed9607c68861dfb36a726163048605a69fae7847a1fd8123f5b935`  
		Last Modified: Tue, 04 Feb 2025 20:35:45 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d23f9f3722f9964a4d4492caf829af14fbac2699f53fc329307bde372bd153`  
		Last Modified: Tue, 04 Feb 2025 20:35:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33479f7ed2d14521052ccb89fa2f5d8fc7b56e70809d8755839241b73e3bc3`  
		Last Modified: Tue, 04 Feb 2025 20:35:48 GMT  
		Size: 92.2 MB (92168626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529d237b589fd6c07c3cd02a8c2be035b500019b144297d0336d832be19df5f8`  
		Last Modified: Tue, 04 Feb 2025 20:35:46 GMT  
		Size: 9.6 KB (9559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77313f68d0991ebd6fea64398106e784ccf58165ddf806638e6f77ed118421d`  
		Last Modified: Tue, 04 Feb 2025 20:35:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0358a6e2ddf7c354618bc06446e02f5d2426813bdbc80e094a374fa53b5a568`  
		Last Modified: Tue, 04 Feb 2025 20:35:46 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c285cf7f97e3bb1af80610a338ca372e0c97e21a15bd017587ffeab9653bf42d`  
		Last Modified: Tue, 04 Feb 2025 20:35:47 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bbcc68bf210aab99245cb6604bb89eeda20ce600407a9a7c59df1d1ede8f90`  
		Last Modified: Tue, 04 Feb 2025 20:35:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:61519dedc9f088748871cf585c6f50e2c4ed37de4660e6182a0c08591786ad0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.2 KB (634235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea81caaadee825efef8fb8874ab34fd8a01ca313e46fe49220383675e5c31ad9`

```dockerfile
```

-	Layers:
	-	`sha256:10d91faeb544bdf21961fb79f318026cc6fbf33936d3aeaf0a4375cd5c824f48`  
		Last Modified: Tue, 04 Feb 2025 20:35:45 GMT  
		Size: 589.5 KB (589522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96ef80548899fb37452b2a77f618e3f84f1f552367c9b492b48c653f84e4f55e`  
		Last Modified: Tue, 04 Feb 2025 20:35:45 GMT  
		Size: 44.7 KB (44713 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:ac1dc4f627daaf58e46081520f6277e3f359adec385ae55bfa9787948c06f3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95627581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6940b8af818d91eedfacd8cdda4171b3a50633f9c3dda6aa104fccf371fb9c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=16
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=16.6
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=23369cdaccd45270ac5dcc30fa9da205d5be33fa505e1f17a0418d2caeca477b
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88efc830b0008c442fbf41800df30ca9fb0c00964fddd3e80890961627c5b9b8`  
		Last Modified: Wed, 08 Jan 2025 21:05:18 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0135973424a59bcd09d82651ba32d24eda2b75299b4d2e3f5deba54f7b2553`  
		Last Modified: Wed, 08 Jan 2025 21:05:18 GMT  
		Size: 1.1 MB (1086512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4b0d2c7f42b79dc01dbd3833f6c268867a01749968770c19b0a257a02954cf`  
		Last Modified: Wed, 08 Jan 2025 21:13:33 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b35d591cbe9900f8759fa3be037a5061e3b63755c2fd7f4c9e8ae8112697b1`  
		Last Modified: Wed, 08 Jan 2025 21:13:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c995fd9d068b0ff19548007f279de7b4d15a5518d03c407d8daadfc93d534e`  
		Last Modified: Wed, 08 Jan 2025 21:13:36 GMT  
		Size: 91.2 MB (91152851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95040d0012cbf535a445c4eaec430a0f83a8bc09d5ce2788d289105b9ad00c5`  
		Last Modified: Wed, 08 Jan 2025 21:13:33 GMT  
		Size: 9.6 KB (9564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4038106df95eb8138118e21b55e80766a34f8d71e2a808f0c43b740567661c`  
		Last Modified: Wed, 08 Jan 2025 21:13:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a750684bd994654d83d7fa010342da1076874e547ac5f0ac9289fa27f11104`  
		Last Modified: Wed, 08 Jan 2025 21:13:34 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950bfbbec1b0bcbc00fce4bcdb5401f90622ab727962b19b14bf6a52846632eb`  
		Last Modified: Tue, 04 Feb 2025 20:31:27 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f4ec39ef7d9a4f9bff9f2b31c6e85d96d6ef75dffb1049032e284941dc617a`  
		Last Modified: Tue, 04 Feb 2025 20:31:27 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:3b7fb8c108bab42b8381c0b3663f5bca9e8c5b9682be2b5767e01310e3ec5c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 KB (44662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ab45f16c4266b33e85b9e124fd7c261cc4668fce6c410f7546beb8c4e7dee9`

```dockerfile
```

-	Layers:
	-	`sha256:947c290cefc62868becb3ee50e9eb120139093829034d51a5b9fb24eb8001be7`  
		Last Modified: Tue, 04 Feb 2025 20:31:27 GMT  
		Size: 44.7 KB (44662 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:67371312c023886cf656ad40b9fc112ea05fb81df8e6998a1fca88a7e15d24da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90033971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67410657c09af95f1e471b7888474f929bce3f39525252a510468f142afb2f10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=16
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=16.6
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=23369cdaccd45270ac5dcc30fa9da205d5be33fa505e1f17a0418d2caeca477b
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Wed, 08 Jan 2025 17:34:15 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1fb695e4dc368a8364f548d77e21718a82e73733358d6ec5420b2e02fd888d`  
		Last Modified: Tue, 04 Feb 2025 23:00:19 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9866222c02ea54a9198ab6c7551f7b17377979754101e6c52ad85510165ac0e`  
		Last Modified: Tue, 04 Feb 2025 23:00:20 GMT  
		Size: 1.1 MB (1086504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cad6bb44a86a8f7100fef62a9fc96a6d89106b8a1df7a25e30e43aee9144bc`  
		Last Modified: Tue, 04 Feb 2025 23:12:09 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eee0b71dd1bfd35f11b1e36480e5e2187597b3784b3dc28e5a54a7f0d5d5db6`  
		Last Modified: Tue, 04 Feb 2025 23:12:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6258d99ba5eda02f9355326180b96483e041cbcfdec85f860c16b5af099a2b8a`  
		Last Modified: Tue, 04 Feb 2025 23:12:12 GMT  
		Size: 85.8 MB (85835218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3857bf44d6e14fb02bd477bf2305e864d68ff45a008571329e540668ba3dbd5d`  
		Last Modified: Tue, 04 Feb 2025 23:12:10 GMT  
		Size: 9.6 KB (9559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863685d102ced5baacfd7a881378653623bea87d7d4c91ab260318a25bff85e9`  
		Last Modified: Tue, 04 Feb 2025 23:12:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bb77075dddd0dc45ea04044b4209f0fb4facb157c3a5fe8ecf1e4d667bae20`  
		Last Modified: Tue, 04 Feb 2025 23:12:11 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bc4fe99584672ea28cf8b1f885c5e70363e172c95e1ce4295003d5028bee5c`  
		Last Modified: Tue, 04 Feb 2025 23:12:11 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2b2b8029599061c6a0148ed557b0ec3ad95744b8367e3ff1b1199e39c250fd`  
		Last Modified: Tue, 04 Feb 2025 23:12:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:39eb580ab3dca2c634c6e65e689713ec7301da83d3dab8b39bb1d1e04b81f0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.4 KB (634419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637b8bb967503150d2f40735f3cf8e338b71650f1317521bda361ec44f75fed3`

```dockerfile
```

-	Layers:
	-	`sha256:c93e9eb7cd76204c51b4f559a3eb876e152df4eb7e2a8b82599c0f0492b8ee30`  
		Last Modified: Tue, 04 Feb 2025 23:12:09 GMT  
		Size: 589.5 KB (589542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ca97bd56a91107fd7b656ac82c66be95eb84865e93fffb730a6dc397ea63c4`  
		Last Modified: Tue, 04 Feb 2025 23:12:09 GMT  
		Size: 44.9 KB (44877 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:f734565c08127667b47a1a40e1544175d1fea0d179b0f8495ea682c4ed3f0e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96153801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f221dadf984844ddae8d2257273748763ffcf8af24a9ae66e21baf8aa4c82b0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=16
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=16.6
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=23369cdaccd45270ac5dcc30fa9da205d5be33fa505e1f17a0418d2caeca477b
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a6e743088f98cbf58808b4332ed33916cb59a3a47d14d4e84d6babea8c2d4d`  
		Last Modified: Wed, 05 Feb 2025 01:00:32 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6918dd27455991749057172332462cb1559aaf917757c8c2ee06cc9984337a8a`  
		Last Modified: Wed, 05 Feb 2025 01:00:33 GMT  
		Size: 1.0 MB (1049767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0e47e0599461b5424f86fc5119d0c886b2f2496c32dc247be1bb3f7d4f35d7`  
		Last Modified: Wed, 05 Feb 2025 01:08:05 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0e6b946cff9ff5df0859cbbce617e5e86debba1e749eeeafab246c95e9e593`  
		Last Modified: Wed, 05 Feb 2025 01:08:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23782b78b851c532cdad41ef7ec132a19593e5919739cb1319526adf09f4a7c`  
		Last Modified: Wed, 05 Feb 2025 01:08:08 GMT  
		Size: 91.0 MB (90996531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a183a241a85426a0945c6ef26da5b4ebd1e0fd4be3e7661d5b82d146c474bd`  
		Last Modified: Wed, 05 Feb 2025 01:08:05 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6720948aed27f10dd5bfb7651ed1a02d86edebdcb02006b5f1b1ee6d2598cd`  
		Last Modified: Wed, 05 Feb 2025 01:08:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cce969a8b1a0b4535317c19aabba9e1c8486f391a5c27bb3173048b3dff677`  
		Last Modified: Wed, 05 Feb 2025 01:08:06 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626ccfcde6644c45e7027f7aaab66f170c875d8ba586dd55d4d0e6fcc3c0619f`  
		Last Modified: Wed, 05 Feb 2025 01:08:06 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7001bc3f74cd4bb1711eb34583b29dbec882c70592c78081782bf5b3e8e9c0c5`  
		Last Modified: Wed, 05 Feb 2025 01:08:07 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:0134879850e8ba3614ece9806ab0252c6ddec6dacf244ba5e78c8896f1f2655e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 KB (634467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20ea3a59c9eb2958e5f6087af18ec8fe0a8b61d1bcb7d6c7acb8ec7b1490776`

```dockerfile
```

-	Layers:
	-	`sha256:5b9287997b002f5bd8bf19675d4a7177dfc94e78c4cc7044c02b39440336c548`  
		Last Modified: Wed, 05 Feb 2025 01:08:05 GMT  
		Size: 589.6 KB (589554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:006e26a25a02bcf425379e6bb5e778f6a459828faf06a8a9a594ec487d9c6d44`  
		Last Modified: Wed, 05 Feb 2025 01:08:05 GMT  
		Size: 44.9 KB (44913 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:305c6e8f2f71d872e94b4ae54ebb83071b94dcc77efcaedfc23ed9b9e19def06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102219144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645e9c2946e1e818d592bd8bcc381976418aad5024be2e1fbc2f850ee22a0cd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=16
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=16.6
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=23369cdaccd45270ac5dcc30fa9da205d5be33fa505e1f17a0418d2caeca477b
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4370f67780112ff2c449428db3382af5edd41e3d4efb32695b54e83456b06356`  
		Last Modified: Tue, 04 Feb 2025 20:35:46 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d85cf774b47917351c8469940bb2f42c9e6158aed6cbbb88318ff9a2aefbab6`  
		Last Modified: Tue, 04 Feb 2025 20:35:46 GMT  
		Size: 1.1 MB (1095378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f066f2b0a96f73509a79952dc9cfab181a3c2264a6c7b1f08d64a4a44d501472`  
		Last Modified: Tue, 04 Feb 2025 20:35:38 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96607497d463c9e4cc2359a8a37278b28fef470ff378137aaba3c4d85afc92f`  
		Last Modified: Tue, 04 Feb 2025 20:35:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856e60e73fc2c0de6c99410bfa0e6187d1b626c8725da796d0f0b1af51ffa86c`  
		Last Modified: Tue, 04 Feb 2025 20:35:49 GMT  
		Size: 97.6 MB (97636066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1227b8e8ea971d6cd213e91a8c8510d6bfef39a99f4e61b7d4b062ed99654b04`  
		Last Modified: Tue, 04 Feb 2025 20:35:46 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b175baaa99af8e171608db97062b934c6f60940a0345320ba7870e81e89fb5`  
		Last Modified: Tue, 04 Feb 2025 20:35:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26fa70929f1ea6a6d1bb8bf8927ba33ddd124e26edfa0fbbb8f7e85e363bd50`  
		Last Modified: Tue, 04 Feb 2025 20:35:47 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e582f9075ad3a5616dc9caec0e11aeae25613430d079f43105c4a9fe3bde4446`  
		Last Modified: Tue, 04 Feb 2025 20:35:47 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636974a88e9a27433b1f6bf7083204f23a7e11a4a4c450931b3523f890afa756`  
		Last Modified: Tue, 04 Feb 2025 20:35:48 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:7140a55908781dca3298c9b0b64962f7da56c10ec22505c40f58469aaed58f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.2 KB (634182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4075fea6c4aa659b8e17453940c39868aecc6854c28db2bc5ad53d5c863fcfec`

```dockerfile
```

-	Layers:
	-	`sha256:bf6d7622e086498374cd7f3f913a90929a873f058fd942075e791f4decf752f3`  
		Last Modified: Tue, 04 Feb 2025 20:35:46 GMT  
		Size: 589.5 KB (589507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78273f2d0c9be0affd18d9f20dee694a485cf541f10e6d87a25910c259a4ff0f`  
		Last Modified: Tue, 04 Feb 2025 20:35:46 GMT  
		Size: 44.7 KB (44675 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:f5668046c5c7e11a048dbf8e154e6c999b49354f6eeda27c687032d33ebbc1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101502547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b71682a9affa51fc02e70053bac798e5dcc4dfef11f0698cfe27400ee0fff55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=16
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=16.6
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=23369cdaccd45270ac5dcc30fa9da205d5be33fa505e1f17a0418d2caeca477b
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05116dccfdc2d0bf2a67d0782cf5bd639f2a5ce44e8b447cd282bbc38e622db1`  
		Last Modified: Tue, 04 Feb 2025 21:19:36 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3657ea2875b611c56ede877418a82cff7921c554c0a7222d9e81e9e5fb268180`  
		Last Modified: Tue, 04 Feb 2025 21:19:36 GMT  
		Size: 1.0 MB (1040029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87dfada9cea4f2144066ca8cafe638b4ebbb664115a9df78feaafab04fc58f8`  
		Last Modified: Tue, 04 Feb 2025 21:27:47 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2751d9662874332e649fa7406497271f931e4971691429387954a848326d8`  
		Last Modified: Tue, 04 Feb 2025 21:27:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42337c94215b669a0b8b210678f10cd5c3cc9d5618b82830fbd1e66746c17054`  
		Last Modified: Tue, 04 Feb 2025 21:27:50 GMT  
		Size: 96.9 MB (96871379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1136308f50e2c38dd4aa8f56b54abed7e1133b3aaeeb886faad1ee27ae9c482`  
		Last Modified: Tue, 04 Feb 2025 21:27:47 GMT  
		Size: 9.6 KB (9562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55cc8da96ff819cefb960b111efd76e5e45ffe2234bad70459f06a5b4329baf`  
		Last Modified: Tue, 04 Feb 2025 21:27:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a371966451138259e57212f8a8e66dd055d80ef70427d1b07b288f592112a1`  
		Last Modified: Tue, 04 Feb 2025 21:27:48 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35a6aa78074f93caeb60dd3cfc7b1c698b790c1ed33d92c84b1f134ca9d95cb`  
		Last Modified: Tue, 04 Feb 2025 21:27:48 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8138e20ff0c157ca50733faf8c1fb7a87304e68720ab3b408c8df01fba186173`  
		Last Modified: Tue, 04 Feb 2025 21:27:49 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:0a599ce43f66239c337e1aff80787b4198a24d83e3dc73b512543112b530fa5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.7 KB (630692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5044ee653c5d817f10bea8f5d2011abe41b4104fa682e160ca883cc42d0cae55`

```dockerfile
```

-	Layers:
	-	`sha256:46a41f53666760021e1ea5ae880cdb77bbc2c327ef80e1620fccc27bf303ff4a`  
		Last Modified: Tue, 04 Feb 2025 21:27:47 GMT  
		Size: 585.9 KB (585931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8c818c2e22577520df5d4fc14f027d93373516a4313ebd74f3a6a17c1fdbbe4`  
		Last Modified: Tue, 04 Feb 2025 21:27:47 GMT  
		Size: 44.8 KB (44761 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; riscv64

```console
$ docker pull postgres@sha256:e1eea3d35b0e843ff55963fedd8700e2ff0b9b421edaaf6cca347a25f0640f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97031214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e298dac86eeee703465df56460df0ab9988dbb302b75f924b5f373ff91b87ad3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=16
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=16.6
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=23369cdaccd45270ac5dcc30fa9da205d5be33fa505e1f17a0418d2caeca477b
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Wed, 08 Jan 2025 17:49:41 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc93498547eda47632be52e4f9de0f535264be6b5b13bd695df74d21a445ee4`  
		Last Modified: Fri, 10 Jan 2025 08:04:23 GMT  
		Size: 988.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4379025cfe409827e83762b8ddf18bccb050a044fa62c5ba40f88f35ee905545`  
		Last Modified: Fri, 10 Jan 2025 08:04:23 GMT  
		Size: 1.1 MB (1089578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef0186356e321fef013e99e866a37e8308d9f788f5c47123b149b521575eec0`  
		Last Modified: Fri, 10 Jan 2025 09:45:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24206bd7240c9a3da106ad9224c974a577cee2bb13977c8f2b4de67741d06e77`  
		Last Modified: Fri, 10 Jan 2025 09:45:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dc8e438c09dc2c8b1e31d6766cb81ed4d5b9e103b5f05ef9aab2a1aacbb6e4`  
		Last Modified: Wed, 05 Feb 2025 00:19:19 GMT  
		Size: 92.6 MB (92552960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ac88dd18058bc7fec6bbac4d3cb4ad0f112d9d3cf8daa8df0bcfa729952573`  
		Last Modified: Wed, 05 Feb 2025 00:19:07 GMT  
		Size: 9.6 KB (9570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5a2fa0222120c275a787f61295169bf7088ad3837e30644f7a1d46db50d28d`  
		Last Modified: Wed, 05 Feb 2025 00:19:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447cff6e84db47f14febabe8b2c02abb63208b4ad4e10e09c5f88e85250dc42f`  
		Last Modified: Wed, 05 Feb 2025 00:19:07 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d11778292cfdcdac3d21075ab0593f0bd74b7f148030ed26f705c78a441d7e7`  
		Last Modified: Wed, 05 Feb 2025 00:19:08 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a876e433d32dcf1087c6b40d234a19f5b5f5700e5029a42e8b8e510aaf4e9906`  
		Last Modified: Wed, 05 Feb 2025 00:19:08 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:ec9d5f8f57ae0a2b5f624a9dcf86be1cdd30c6e89eba2479e5e98f6dec4cd78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.3 KB (632349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b925ad0dfbdb7a84fb09f1cfb69a65822f1dac4736e63d0b7618c02035510b39`

```dockerfile
```

-	Layers:
	-	`sha256:1b09ebed4958ef27255bcd5604c770a306e4b88b09b5aa49f320796f46257069`  
		Last Modified: Wed, 05 Feb 2025 00:19:06 GMT  
		Size: 587.6 KB (587589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae897cbdf05b740f26c52a21c2c6b67e984039a50b79b5950e11a94e90f36101`  
		Last Modified: Wed, 05 Feb 2025 00:19:06 GMT  
		Size: 44.8 KB (44760 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; s390x

```console
$ docker pull postgres@sha256:53a935cde5b19d487576423e04c86fa427c992fd308588619e239f65bc771e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105829995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd0d95a338df42182ee1030d475298961c1bef8b2b2634b7191eebb3003db3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=16
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=16.6
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=23369cdaccd45270ac5dcc30fa9da205d5be33fa505e1f17a0418d2caeca477b
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c5037007f5ec5364c664cc7501dcd2d9845232b0a497e9079d9aae1a8a7bed`  
		Last Modified: Tue, 04 Feb 2025 21:52:06 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d1ccf5ea6431e9e56eb085f7603e9caf62abdb8eda29ebf7038252c5b53643`  
		Last Modified: Tue, 04 Feb 2025 21:52:07 GMT  
		Size: 1.1 MB (1084161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6769a9b4ee1a17a041b13661006b51d74b7da02c9d1502cae0a3b7431e2239e`  
		Last Modified: Tue, 04 Feb 2025 22:04:15 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d172d5a8b87a6700a7739a67fea8d0abda3b9215ccbf0429bad1518ceb4f1257`  
		Last Modified: Tue, 04 Feb 2025 22:04:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2150c739f98e6aab881c6bc636e1839fbba15129cbe944f67b4eefaa8e60d33`  
		Last Modified: Tue, 04 Feb 2025 22:04:18 GMT  
		Size: 101.3 MB (101265773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c2262b4aa39465ed93cf0fd03a44b1509740cef1aa537aa1731ef4f1de2851`  
		Last Modified: Tue, 04 Feb 2025 22:04:16 GMT  
		Size: 9.6 KB (9565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28a46fe16fbcbe4443740d211cfe69944aadde12d005e00ff5a67c8d413e742`  
		Last Modified: Tue, 04 Feb 2025 22:04:16 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753b1f4adc0473af775bf86bc441f3cb06520e2377dc18fff5f5bcfad20e72f5`  
		Last Modified: Tue, 04 Feb 2025 22:04:16 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6b851df874d5f85b5da5f7dcdedebdd21d4da10e541a044e537710473f2467`  
		Last Modified: Tue, 04 Feb 2025 22:04:17 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ded82feab27e68d1016aa97a81bb078eb955de6d7b78244d56ffcb198a9ba7`  
		Last Modified: Tue, 04 Feb 2025 22:04:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:dfa4a2a9de392d704fb5cf25b659875740e0db06111a9ec56703bc44558a31f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.3 KB (632290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920e8a9c0ee25deb2f1a42dcc2192e5e51e36fd4f639275c3483d6d3003d886b`

```dockerfile
```

-	Layers:
	-	`sha256:5ab6faeea3063f70356bd735ca19008e0a4acd90c37f46dd38ceeba4ad1cfeb0`  
		Last Modified: Tue, 04 Feb 2025 22:04:15 GMT  
		Size: 587.6 KB (587571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5cbb0ea1c58d9ca04ac376cb4adcc4adb235997602373894aa9a76ec7b70fde`  
		Last Modified: Tue, 04 Feb 2025 22:04:15 GMT  
		Size: 44.7 KB (44719 bytes)  
		MIME: application/vnd.in-toto+json
