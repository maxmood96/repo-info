## `postgres:16-alpine3.20`

```console
$ docker pull postgres@sha256:c82cd39442cde9bba8f7dbaf559a12b94f98bd3af1fcaed8196f0e235f5b1f82
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
$ docker pull postgres@sha256:23ee7be981aeb63bf9c16fa9eba2163cc46a8c2c7b4caad7c1ede4cd448fd4e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97109746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5671b0b568b44c535db127c8279161b802f9972f9bce0738ab980ec4b8249830`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:46:14 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:46:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_MAJOR=16
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_VERSION=16.7
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_SHA256=62e02f77ebfc4a37f1700c20cc3ccd85ff797b5613766ebf949a7899bb2113fe
# Thu, 13 Feb 2025 18:46:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:46:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:46:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:46:14 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:46:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:46:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee2bb871a773a088a4ccdf6d90e502c1bf2cd40f3613ae836abd4675e9a01e6`  
		Last Modified: Sat, 15 Feb 2025 00:27:27 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b2dbc2bf5b1d542b9694a992bce13d70660663e3c4637ef4217a39fa2425d0`  
		Last Modified: Sat, 15 Feb 2025 00:27:17 GMT  
		Size: 1.1 MB (1120294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb91c5885853813e3c7d36019b5835926bb670ee1287bbbafb65fac455b44456`  
		Last Modified: Sat, 15 Feb 2025 00:27:08 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9689cb764991720a60894694d1f818ff8a8a5a3a3e9ee8f311a406b8ab246370`  
		Last Modified: Sat, 15 Feb 2025 00:26:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b61b7d5b225b4f31517a26e611415190cad0f49756b5251de9a28522eea1d6`  
		Last Modified: Sat, 15 Feb 2025 00:26:44 GMT  
		Size: 92.3 MB (92345821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72812f9835d10a7ad9aac347bd1a053b9643c9b06d6700cfcc02e6420f006846`  
		Last Modified: Sat, 15 Feb 2025 00:26:29 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b340717d088ddefefb55b5c7c86b23efc2f09a7d8844962d80dce3e1de58bec0`  
		Last Modified: Sat, 15 Feb 2025 00:26:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46974625ca4288cadf5e950abd823ad29d31d7fdff7e7e7eb4de3e05a77d489a`  
		Last Modified: Sat, 15 Feb 2025 00:26:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e316e7693ca8dc6ad793f0bb7dc648e707d7b77b8bcb8d337a882f03924ab681`  
		Last Modified: Sat, 15 Feb 2025 00:26:16 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758dfcc67a77a16c1faac30ae13c706d58acf4fd80bcff7bd239db19dc624f2e`  
		Last Modified: Sat, 15 Feb 2025 00:26:13 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:eb5db5006237e0a06882b6d585e0734937f36d9fe099d880dab21ae52d7a0290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.2 KB (634235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247f1040387229c4fcaaf0b4746cf8287847258a310e69ee95408157b9dcaf64`

```dockerfile
```

-	Layers:
	-	`sha256:e9bb16e9bbd6e2b72ed5b61e6ab233701f09c295bf2ebe3fd6600f173a883537`  
		Last Modified: Sat, 15 Feb 2025 00:11:13 GMT  
		Size: 589.5 KB (589522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9942a7e2838fa5a1d7b74541d43cd2f97a404d66f3147ee4da1ba5066ded66d8`  
		Last Modified: Sat, 15 Feb 2025 00:11:13 GMT  
		Size: 44.7 KB (44713 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:5ec3d810df2431f05afe12f2523fae898fc7b36dfadd7e621c118bcdd1531743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95780371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfcec81c56cf72e1e4a41e9371e3287002557c1d61a9a427021dde9748a54a9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:46:14 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:46:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_MAJOR=16
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_VERSION=16.7
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_SHA256=62e02f77ebfc4a37f1700c20cc3ccd85ff797b5613766ebf949a7899bb2113fe
# Thu, 13 Feb 2025 18:46:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:46:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:46:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:46:14 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:46:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:46:14 GMT
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
	-	`sha256:11383501d163cdab0611e432069445e7cffcbb037e51b3a3af59561a2256230d`  
		Last Modified: Sat, 15 Feb 2025 00:11:37 GMT  
		Size: 91.3 MB (91304578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62664e6bc5f921f5c767a5266921bd26c6b135426ea55e974cdea27f8410407`  
		Last Modified: Sat, 15 Feb 2025 00:11:30 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0695d5164d1889fe2076cb16c524211db0180007e64fd5dedad401cf925b8d97`  
		Last Modified: Sat, 15 Feb 2025 00:11:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2026f7c8a8db2e9794398ea342784a1b01446c8694d0e4d6285f4efb22132370`  
		Last Modified: Sat, 15 Feb 2025 00:11:30 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a2fa9810c1277cc5d1cfc3c76cd0ce9a646f6c9a0b344d4d799fa643fbbd7f`  
		Last Modified: Sat, 15 Feb 2025 00:11:30 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23281a5862e264c74028f6b431319484b97c9b9ebc2a0568b37f208e0a546afe`  
		Last Modified: Sat, 15 Feb 2025 00:11:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:162c2aa9edafe82708c87f2f62aca601b9d7ae50fa911c854d45679e0e8c44b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 KB (44662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168db0930465e5dc0990be00da13d2fa0c8ca05db9669cab05b84aa177e6405b`

```dockerfile
```

-	Layers:
	-	`sha256:c07ef47517f25d6d666ea5165488b04a33e54199c89f36c116860ee8817a0d34`  
		Last Modified: Sat, 15 Feb 2025 00:11:14 GMT  
		Size: 44.7 KB (44662 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:cd9e41fb52055fa34d60eaba360dd023529994ab487d92fada937144c1cf9447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90174109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d986cd59a465dadcabfccbafb7bd31494587d10cc29001b492f155b4eda15c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:46:14 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:46:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_MAJOR=16
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_VERSION=16.7
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_SHA256=62e02f77ebfc4a37f1700c20cc3ccd85ff797b5613766ebf949a7899bb2113fe
# Thu, 13 Feb 2025 18:46:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:46:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:46:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:46:14 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:46:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:46:14 GMT
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
	-	`sha256:8f771268d2417653ff110ab0a1b30c6b097ba0fb535cf667ddef5a7e3929aa4f`  
		Last Modified: Sat, 15 Feb 2025 00:23:41 GMT  
		Size: 86.0 MB (85974899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bec0611170125857cecb213d8fb14748617d2af5ba42ad498f4953035b445f`  
		Last Modified: Sat, 15 Feb 2025 00:23:29 GMT  
		Size: 9.6 KB (9558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6ee9393b409cdf8c6032e7aee2890db43bc8e17d41f262333733af66af5b9c`  
		Last Modified: Sat, 15 Feb 2025 00:23:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a1e39609261e504ce7189208949736e6e372c81f57a78d54a2605c6655cfe6`  
		Last Modified: Sat, 15 Feb 2025 00:23:11 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8470ae4c3ffc2da47aab89ff750698bea73d44fecd67ec675a7cbae55e488817`  
		Last Modified: Sat, 15 Feb 2025 00:23:07 GMT  
		Size: 5.4 KB (5413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd52dfac9c4edec26e2517f26f14a265f778707cfb7eb8335377fc4150e9294f`  
		Last Modified: Sat, 15 Feb 2025 00:22:58 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:df4439b5c81b30dd34c8e3b4289389503ccfae9339b6717f13b48dd7972266a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.4 KB (634419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a5736e18d008ca9c0aadf28432b08fb509949fcfd6c4fd6ff18a0b7942ceb2`

```dockerfile
```

-	Layers:
	-	`sha256:a4d54f160ffaa5324afe9bd3d1087458b5d1e49e7402dba078acd84d23870160`  
		Last Modified: Sat, 15 Feb 2025 00:11:15 GMT  
		Size: 589.5 KB (589542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f27f5f3e75199b1aca1cf438a46129d52dfb90e2064210b5e2f51596e4daa40`  
		Last Modified: Sat, 15 Feb 2025 00:11:15 GMT  
		Size: 44.9 KB (44877 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:e22949c1ac4ade277b9a18d1eedab2ef7ce7fcb02009e2359207cac69a3feec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96334061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ae5dd140064834a913c8732a0668625902289c1879e784769c7ae437e87081`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:46:14 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:46:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_MAJOR=16
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_VERSION=16.7
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_SHA256=62e02f77ebfc4a37f1700c20cc3ccd85ff797b5613766ebf949a7899bb2113fe
# Thu, 13 Feb 2025 18:46:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:46:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:46:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:46:14 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:46:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:46:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc8827c16e8ec088d48c0b753a38f9b70fa76626b8e70929dbb63cf84cc89b5`  
		Last Modified: Sat, 15 Feb 2025 00:22:17 GMT  
		Size: 979.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0907d060ed36b58b8341b1b05e996014c48ca9a918bb7414420e2e27fa4bc054`  
		Last Modified: Sat, 15 Feb 2025 00:22:10 GMT  
		Size: 1.0 MB (1049755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36da590e94d03388333c8f90ebc9ff573b76757ec31fc8b18a031f6350a39911`  
		Last Modified: Sat, 15 Feb 2025 00:22:00 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba3a5783239b116fcb925eef91e91369b4580402ff73a02ffd413615c3afcf0`  
		Last Modified: Sat, 15 Feb 2025 00:21:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6efc59c69c98755fdf0f28ffbdbb20b332c57574f3eb134ee58c528d7c87cb6`  
		Last Modified: Sat, 15 Feb 2025 00:21:49 GMT  
		Size: 91.2 MB (91176410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5051f2f748a6c5807145231fb66733d62fb7266705ad733c9c1be9b38545157f`  
		Last Modified: Sat, 15 Feb 2025 00:21:33 GMT  
		Size: 9.6 KB (9563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ef5412b9b929154c4a739a57b5da803c40752fe7c39faaf1e8294a1e849b5a`  
		Last Modified: Sat, 15 Feb 2025 00:21:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3e0b2d4ee35c3c2e060261709a835e8a243493303e9144d965e06ecc4a7ae6`  
		Last Modified: Sat, 15 Feb 2025 00:21:25 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af359230e2fdb0b8efde09e8065d47e931cba99cc62c7478a4250ab67b6b38d8`  
		Last Modified: Sat, 15 Feb 2025 00:21:21 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9bdce11d0b72ef6fcc6fabef1a161936b92594292284075b7de9deba555e21`  
		Last Modified: Sat, 15 Feb 2025 00:21:17 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:fa61bc8df082c9974d3cae0902a1054bba2d905cabafed45ba1960fbe743bb5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 KB (634467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7270a9e6865e7c5ad074ecfc4c9eadd8f236e2f536b1506960fd31f38daf8a`

```dockerfile
```

-	Layers:
	-	`sha256:da2b20bd2468a29104d4e1d1ef02fcd1fa30a45a28400ed4add918ca84d8fa61`  
		Last Modified: Sat, 15 Feb 2025 00:11:16 GMT  
		Size: 589.6 KB (589554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1742b22502b8ab64c7c846f0c1796a9d7469cf4b952213daea2033cf67ef2f7`  
		Last Modified: Sat, 15 Feb 2025 00:11:17 GMT  
		Size: 44.9 KB (44913 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:5eef2de37586ca87d31106c4740736989c10543650802a61e6c8ff37444ced65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102416267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65978b0f6d78b5512e1a1811091f1948200c5c2175f76ba1b6f0b04e92403389`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:46:14 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:46:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_MAJOR=16
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_VERSION=16.7
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_SHA256=62e02f77ebfc4a37f1700c20cc3ccd85ff797b5613766ebf949a7899bb2113fe
# Thu, 13 Feb 2025 18:46:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:46:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:46:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:46:14 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:46:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:46:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 14:36:27 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4d910f2326bcd95efb51440b801409f984abfa53623a63e120543807814ea2`  
		Last Modified: Sat, 15 Feb 2025 00:20:41 GMT  
		Size: 982.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d2bd20770b30fbcdd5e7a239099e2506d0be5820e194f46fec71a2c0992e7a`  
		Last Modified: Sat, 15 Feb 2025 00:20:31 GMT  
		Size: 1.1 MB (1095371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6daa705cefc941c47f072f9f2cc8374cf83e7886c11053a028921708132afa4`  
		Last Modified: Sat, 15 Feb 2025 00:20:28 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95258db897871b5bd71c0a9ff897d75bb7230e159125723c1a4a49b6a2fe0245`  
		Last Modified: Sat, 15 Feb 2025 00:20:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1522228bfd52d0fb9ed7d69e18ec3f0f90984181bbe3925a6890b0adb0b7350`  
		Last Modified: Sat, 15 Feb 2025 00:20:10 GMT  
		Size: 97.8 MB (97832504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f180f9bda2b1e19a4714b27c1c1e0d65bedeb9b823805d309a057761e0f436e1`  
		Last Modified: Sat, 15 Feb 2025 00:19:50 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba3c2a697811ec028b71e49c4aa7dd3ed291ad1070669668e1a630e2da84d8f`  
		Last Modified: Sat, 15 Feb 2025 00:19:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9a4649b3df29c1ad673ed5749add903f5e5a7a7465d8197d2e7a41683ea9ff`  
		Last Modified: Sat, 15 Feb 2025 00:19:37 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab84adb560c3b2d8574e2e7c97f6efdf56f3e70a8ba67146b882c01fef1d0d4`  
		Last Modified: Sat, 15 Feb 2025 00:19:33 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4390e31cb43ccee71a8df7474985ee8b136c480ae2ac584b482da42a7f114fe1`  
		Last Modified: Sat, 15 Feb 2025 00:19:28 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:709be3ec802eae73c43a2e4e24043c2815611b220fa4519f46555436e2d32a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.2 KB (634182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b03eb1902df5fb4557aae70de62c956345de71edb9f26ad41c93294f5d8d66`

```dockerfile
```

-	Layers:
	-	`sha256:ca9451dc17143fdbc993f79b9fc928ba2a2e9a496206298d5190842ae2f580c4`  
		Last Modified: Sat, 15 Feb 2025 00:11:18 GMT  
		Size: 589.5 KB (589507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:272d4f58497d282fcff98e210ab4ff5e93e623c51da9e2cfff0bf0fc602ed54b`  
		Last Modified: Sat, 15 Feb 2025 00:11:18 GMT  
		Size: 44.7 KB (44675 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:383cd6fbf5ff2b3669edf2a0331d1ea0377e77633551d7332a98fbb22daea13c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101701592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73122dfc8950088d817cd8ef8e0911dfcf7bac47738cc542e4e3789e33ab37b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:46:14 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:46:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_MAJOR=16
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_VERSION=16.7
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_SHA256=62e02f77ebfc4a37f1700c20cc3ccd85ff797b5613766ebf949a7899bb2113fe
# Thu, 13 Feb 2025 18:46:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:46:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:46:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:46:14 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:46:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:46:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 14:35:49 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4560e6eaf6136fe9ed082dd565c5a37bb5ec3e433bd72a01116ae44bd04994e`  
		Last Modified: Sat, 15 Feb 2025 00:18:37 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a2d29dc8697219ebfcfe5e6e5c56b2549f8e69e4f3f0bdf9803dcbf630c294`  
		Last Modified: Sat, 15 Feb 2025 00:18:31 GMT  
		Size: 1.0 MB (1040018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db695e36d82284dfc46d1fed4f570d9a812b952a1abb41603b09ccb4565b2b1`  
		Last Modified: Sat, 15 Feb 2025 00:18:24 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120127792b9f26a99d1a9584a1747e461b88ea90bd0e37882e377a843cc7930d`  
		Last Modified: Sat, 15 Feb 2025 00:18:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95050b031d7ce09d76824a869a594fc947d2dea94ab75c2b2b14f11d9455a0aa`  
		Last Modified: Sat, 15 Feb 2025 00:18:06 GMT  
		Size: 97.1 MB (97069151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe6b78b122e5124850a52d98de4d96a234a50f43635cdb557d634d77723af8f`  
		Last Modified: Sat, 15 Feb 2025 00:17:45 GMT  
		Size: 9.6 KB (9567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b2ac8b2ba086bfebec5102e5b1e85e70646066ec9bf429c5edb6c1dede62d4`  
		Last Modified: Sat, 15 Feb 2025 00:17:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef66f4825f10c8cd9da3eef57f4c6309ebd76e2a5694f9c08520f5c53b7d038`  
		Last Modified: Sat, 15 Feb 2025 00:17:39 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0d76816e487775320b12a6801bc4f0a7ef927c0b362f97a2870dee9e2fda5f`  
		Last Modified: Sat, 15 Feb 2025 00:17:32 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9b34090ee80bda2b0664954f72ece5581517b80566b4d96ae5d979d9e2e031`  
		Last Modified: Sat, 15 Feb 2025 00:17:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:027fd6e3e60cad08f28a08a3014e5458512b7bc06ff332f40bbfd1fdbc8ee9bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.7 KB (630692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f596138107ad99b6d0856b6b9a7bc825213b8ebd310e62d786e2d64ef82cb49d`

```dockerfile
```

-	Layers:
	-	`sha256:22ef68b283a4aad4e724a5da791c7b10f07e951906f8d25297bb4d8bca9c30a7`  
		Last Modified: Sat, 15 Feb 2025 00:11:19 GMT  
		Size: 585.9 KB (585931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4384cf37be83054bce9033a73c9ad91e17e1fefe869c946a638d0c3d667758a1`  
		Last Modified: Sat, 15 Feb 2025 00:11:20 GMT  
		Size: 44.8 KB (44761 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; riscv64

```console
$ docker pull postgres@sha256:38fdca2dfe768b31836c4648d6d9f8aabf8839a5b9f2eb17a98bc4858ad381eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99601693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4387f3409714b40ecbb30332b7ca91d8097421ebd70abc55ba54492892bfc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:46:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_MAJOR=16
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_VERSION=16.7
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_SHA256=62e02f77ebfc4a37f1700c20cc3ccd85ff797b5613766ebf949a7899bb2113fe
# Thu, 13 Feb 2025 18:46:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:46:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:46:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:46:14 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:46:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:46:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Tue, 14 Jan 2025 20:50:16 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc93498547eda47632be52e4f9de0f535264be6b5b13bd695df74d21a445ee4`  
		Last Modified: Wed, 05 Feb 2025 08:29:23 GMT  
		Size: 988.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4379025cfe409827e83762b8ddf18bccb050a044fa62c5ba40f88f35ee905545`  
		Last Modified: Wed, 05 Feb 2025 13:31:04 GMT  
		Size: 1.1 MB (1089578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef0186356e321fef013e99e866a37e8308d9f788f5c47123b149b521575eec0`  
		Last Modified: Fri, 14 Feb 2025 09:07:20 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24206bd7240c9a3da106ad9224c974a577cee2bb13977c8f2b4de67741d06e77`  
		Last Modified: Wed, 05 Feb 2025 08:29:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4e0c7bd5aae7943e0ca88450ba37f416e7abc8efd0509ad4a2b1658489bce9`  
		Last Modified: Fri, 14 Feb 2025 05:53:11 GMT  
		Size: 95.1 MB (95123436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5af9b4d33a7cf1240db829ea875d702c24c18d17c74c4b842c430db4e0cdda`  
		Last Modified: Fri, 14 Feb 2025 05:52:47 GMT  
		Size: 9.6 KB (9571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c86f7b32ac1bd24d6f4185e69dc0d8776722d6449d9caf817afd6f261e0d7f`  
		Last Modified: Fri, 14 Feb 2025 05:52:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fd0b082717211616d5b568829a98579b41e1b36d3c31c454bfd12e6dd409e0`  
		Last Modified: Fri, 14 Feb 2025 05:52:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe3b54f2871a829ef819e5d984ef37172c785b951cd36675fb8f3367cad6bba`  
		Last Modified: Fri, 14 Feb 2025 02:26:45 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f570de335aef151f090c90fce063e95d9c1e3fc537a1cf7f3e226a570e8814a7`  
		Last Modified: Fri, 14 Feb 2025 05:52:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:e7d5f0874e2342bba85824150f36b1c04fd2aaf81b76938eb5c2a0b0b3817ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.4 KB (633371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a000b1a6d58294b10a20868c1964130904e4b6d3385ead2d06cb72b47cc581f`

```dockerfile
```

-	Layers:
	-	`sha256:8e623f1c527baa6924944191058b66805e99be1a75b6e88c1c2e8d1046ee6221`  
		Last Modified: Fri, 14 Feb 2025 03:10:23 GMT  
		Size: 588.6 KB (588610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce1703fd7a44c6c1e8865f1d526a3739f944514b3cc6c3fb6466b3347993fec7`  
		Last Modified: Fri, 14 Feb 2025 03:10:23 GMT  
		Size: 44.8 KB (44761 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; s390x

```console
$ docker pull postgres@sha256:9b7c2d16bfc2eba47d1fec404677aea90b3101ef3d43bf4cbf53fd273d84b00b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (106035696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c93372e7d31d5b909958a6b4c2f8a1658bb5bca9068b1120fb6a53b9a19ef5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:46:14 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:46:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_MAJOR=16
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_VERSION=16.7
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PG_SHA256=62e02f77ebfc4a37f1700c20cc3ccd85ff797b5613766ebf949a7899bb2113fe
# Thu, 13 Feb 2025 18:46:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:46:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:46:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:46:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:46:14 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:46:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:46:14 GMT
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
	-	`sha256:82a85b13fd9d8ecdb15823ebaec80aae00233e2a963abbdebbc3e6060af550c3`  
		Last Modified: Sat, 15 Feb 2025 00:16:06 GMT  
		Size: 101.5 MB (101470676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f6160e72e152d45c731d2b7e66743eb5bb902f3ebf6fe227346bc42f07138d`  
		Last Modified: Sat, 15 Feb 2025 00:15:50 GMT  
		Size: 9.6 KB (9565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75aab756a82a80e42ab169cf6aa717444b79226383d2665973f9a4b350afecb`  
		Last Modified: Sat, 15 Feb 2025 00:15:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccdd1af9fa5454307cdf570dd84d343ec55b1796bde736f2db85608be858c23`  
		Last Modified: Sat, 15 Feb 2025 00:15:37 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7102838909187f560b4185d702f398dfcbb6e0904c7631f2fa8a056983043898`  
		Last Modified: Sat, 15 Feb 2025 00:15:34 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da8b531bb0dc54f2dafe19a505b5b735dd4de10224f3aedc742428e317fd4ca`  
		Last Modified: Sat, 15 Feb 2025 00:15:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:dd0d19e1b8ebb53dace4c6b5118d8f7490da6f1d5da5c962e8be9aa254b68820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.3 KB (632290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf2b0e8325dd1629d01ef41de3a5472c0ca7d48c56e1ba5d52721a9a234d6f4`

```dockerfile
```

-	Layers:
	-	`sha256:5e8e4b9e0ce428aede6070ad6554d73c2c9c8a081743df688f28827b56b1a314`  
		Last Modified: Sat, 15 Feb 2025 00:11:22 GMT  
		Size: 587.6 KB (587571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20189b6860c93d7b3423ac4b199bffda8754a5d144d0f7f9f189d74d6154ba6`  
		Last Modified: Sat, 15 Feb 2025 00:11:22 GMT  
		Size: 44.7 KB (44719 bytes)  
		MIME: application/vnd.in-toto+json
