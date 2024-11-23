## `postgres:13-alpine3.19`

```console
$ docker pull postgres@sha256:401a3d5c6ae6880a2dfafdc29f64ba83955f60a31556bbcd0fc04d71fe721b5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `postgres:13-alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:159a4e8038d4446ff722957fa96705b4dee34a4e398bbe5f8f39b46756e9097e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95891303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9eda2d1ff98f9aa02e86f743c055a478f6df84b1b743e077b9bebdd763cdaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:07:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_MAJOR=13
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_VERSION=13.18
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_SHA256=ceea92abee2a8c19408d278b68de6a78b6bd3dbb4fa2d653fa7ca745d666aab1
# Thu, 21 Nov 2024 20:07:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:07:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:07:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:07:48 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:07:48 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:07:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a131ad200dfe8bc788cc01e4739eb00623b97ba675d0751d2b88794de48fdcd`  
		Last Modified: Fri, 22 Nov 2024 20:27:35 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8441d0cb8c4f353f7362db7e34cc1fcd41d85f5838ab5b2449fdf1c0c17cfb`  
		Last Modified: Fri, 22 Nov 2024 20:27:36 GMT  
		Size: 1.1 MB (1120291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626d4a6668a9afec75800e2e8701d483e971397c8d907972bf374a711a2d240e`  
		Last Modified: Fri, 22 Nov 2024 20:27:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04122fdccbe4a626bc7d72b62ec34b8db231e187906eb3910aa752e3bfa8e392`  
		Last Modified: Fri, 22 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7176e539319acf12a08826c6b5fa2c46be2fee18034b70892d582f3845a4c88e`  
		Last Modified: Fri, 22 Nov 2024 20:27:37 GMT  
		Size: 91.3 MB (91334811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c17720e5ede9ae101ff4b6e9d6031ccef84da5adfa1b231b9448b7f5fc7e504`  
		Last Modified: Fri, 22 Nov 2024 20:27:36 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1398030510615028745c5ab171817eaf5d0fa2cb8300f36f43eae77f80bb81c9`  
		Last Modified: Fri, 22 Nov 2024 20:27:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868d76aef9701d10863619da52507b6e6094b064721d2d0bdac5e77967d3a4c3`  
		Last Modified: Fri, 22 Nov 2024 20:27:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e916d122ab294245464032381ae1a9b26f32125a1637b659e4259e878266ad5`  
		Last Modified: Fri, 22 Nov 2024 20:27:37 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86ff8262877def61b77ab31a740cdf6314edc68b93b6819dbbc420683c07a6b`  
		Last Modified: Fri, 22 Nov 2024 20:27:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:54268aef957e4c6d5595def9c37829fe6183571ae8f393038407d64b50c51a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ba3e240ff3b44eac5a404e20ea2c6037fee56f3bfa335a4550e901bde4eac1`

```dockerfile
```

-	Layers:
	-	`sha256:1ed5b003a7386fa4955959bd659f899d7267eac853830c094b67797c11896d04`  
		Last Modified: Fri, 22 Nov 2024 20:27:35 GMT  
		Size: 966.1 KB (966055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5b829a42e215a7262d2cb468bc9d5f34ac4b6181776634389c64c7e35d71743`  
		Last Modified: Fri, 22 Nov 2024 20:27:35 GMT  
		Size: 44.7 KB (44698 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:1cb4bb407b991e43d49749e6ac5d622677d53dc9941a9fa8f5ac06456e1667fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94360418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc17c88c91417a71448e755960a85c95df340d000f071e6a8615d68c50213c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:07:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_MAJOR=13
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_VERSION=13.18
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_SHA256=ceea92abee2a8c19408d278b68de6a78b6bd3dbb4fa2d653fa7ca745d666aab1
# Thu, 21 Nov 2024 20:07:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:07:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:07:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:07:48 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:07:48 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:07:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1129eba1c516693bf2f340f0343f658e37e7812832c7f2e7493ce214856d3fc0`  
		Last Modified: Tue, 12 Nov 2024 05:41:41 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1855f1ed4c4392b8709ed6c84e2a119012e83c080f39bb8faf7f1bbc735a9252`  
		Last Modified: Tue, 12 Nov 2024 05:41:41 GMT  
		Size: 1.1 MB (1086678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255e16740a45a54b3ba44f9bce09b1f67b316dd94e12dc4ddfcfe274678036ac`  
		Last Modified: Tue, 12 Nov 2024 05:49:37 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8874dbe6c02989a5e3c4a6f7b2a59292b8f32afd21211d3933902093d814455`  
		Last Modified: Tue, 12 Nov 2024 05:49:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5708e3983addb21a18d5cebd5c47918ec7155a3e293bdc2a34a28e666951a7c8`  
		Last Modified: Fri, 22 Nov 2024 21:03:28 GMT  
		Size: 90.1 MB (90080834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3fd556b882d60133cdbb0b3d8b8b59206d1252fa137cac4f018c8f22d5fba9`  
		Last Modified: Fri, 22 Nov 2024 21:03:25 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34debccce60de7a23d73a5322a09f8cce1112dde103a79b93ee017b3e5f38404`  
		Last Modified: Fri, 22 Nov 2024 21:03:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167ed644ac8f7f8d06c09f851c6212b7f3cb5e7e2203f3df827a5f4b1fc518b6`  
		Last Modified: Fri, 22 Nov 2024 21:03:25 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040df7192bc52c75221846468cce2925f2017548fd919500067d882513826e84`  
		Last Modified: Fri, 22 Nov 2024 21:03:26 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb48d34de83d0bde76cbada3dc6c9e04cbd02313bd5edfed2c6048b684fb3d6`  
		Last Modified: Fri, 22 Nov 2024 21:03:26 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:c9370884723f193169e9dba7181b22b8ea43cb17930da051e2956440ade4861e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 KB (44647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c28b61b31a982003dd8c6628e4f4970fa7716a7c13e7df186a51eb0f741afb4`

```dockerfile
```

-	Layers:
	-	`sha256:ff185c5cf33ad30f0c46a3cbdf946ba138dfb69a1f20bebd87e89de9ef045092`  
		Last Modified: Fri, 22 Nov 2024 21:03:25 GMT  
		Size: 44.6 KB (44647 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:cac2a88f797af4702595438fab6d556ccd0ec15a6a3018e8ed11941bc514f9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88746660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b520a52ee5ac3d065bfdce0c9f9faf8d91fd060b7aa0a50c78288374efd5370c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:07:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_MAJOR=13
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_VERSION=13.18
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_SHA256=ceea92abee2a8c19408d278b68de6a78b6bd3dbb4fa2d653fa7ca745d666aab1
# Thu, 21 Nov 2024 20:07:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:07:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:07:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:07:48 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:07:48 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:07:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5db41ad436d5f7ebd4024d28883a253bc45e3577ec71b917f3af8f6247e0a49`  
		Last Modified: Tue, 12 Nov 2024 11:50:40 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ec4ab37e54f1eaa5a6a0648af6ccfa09df4dda8aebd4bfd4c95a09aeeaf220`  
		Last Modified: Tue, 12 Nov 2024 11:50:41 GMT  
		Size: 1.1 MB (1086691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694d2ecd365071d47a25ce95fec93acb0830747395eb32752556c88eb3dc3a81`  
		Last Modified: Tue, 12 Nov 2024 12:37:58 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a6ddb81e5151f0e21e0c3fd043dcd36f52e92d27d808d8967dacc037ccb4ca`  
		Last Modified: Tue, 12 Nov 2024 12:37:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e8b93a26509331544bec9497182d402f65b4ce62731e233907cf2b2ffc5e01`  
		Last Modified: Fri, 22 Nov 2024 23:27:28 GMT  
		Size: 84.7 MB (84715763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b3160d75baba6bbee323d4091b5de84f189cf53d9bbb53811064ddee62aa24`  
		Last Modified: Fri, 22 Nov 2024 23:27:26 GMT  
		Size: 9.0 KB (9016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e93acd990108985e2f1cb67a5c1557f321975d94598ca2d33676c83968f2dd`  
		Last Modified: Fri, 22 Nov 2024 23:27:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6625e63de5950251838be5a1587171ff5b1e4af11918d5d4b7285b7d57e70b6f`  
		Last Modified: Fri, 22 Nov 2024 23:27:26 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af3acef4a1d383a21f9f99b5546294839af4a014c2bd48766c594af3232c05e`  
		Last Modified: Fri, 22 Nov 2024 23:27:27 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2251c7048d2d6b390dfd72e19bf803e4eff6f14d2f1431347385453620e8bf0b`  
		Last Modified: Fri, 22 Nov 2024 23:27:27 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:8816681a40ee92b8aa166b937fa4b558eb652e868bf88119adb171ff2bb4ee0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f6ffb9f8e06c22cf036a5b943ab52a102cf60290cd20aa2dc2bf14c72aa538`

```dockerfile
```

-	Layers:
	-	`sha256:5fe5855122c995b3f4bedf4629a66e04a617b50714d31f70782b901119c8b1eb`  
		Last Modified: Fri, 22 Nov 2024 23:27:26 GMT  
		Size: 966.1 KB (966075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90141f59e2d35fef1cbc95cd7ce481fa497ea5abfb1898b3d98c9b1ab78b3dcd`  
		Last Modified: Fri, 22 Nov 2024 23:27:26 GMT  
		Size: 44.9 KB (44862 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:5ef439fe0f119a2ddbc595bfcdd06cde5a19d66b5e3f61f800f3ca218e18a855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94528812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d1b2a5dda59ed196d4fa418a26cb077cff478927ffa8983764285c5e2de1b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:07:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_MAJOR=13
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_VERSION=13.18
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_SHA256=ceea92abee2a8c19408d278b68de6a78b6bd3dbb4fa2d653fa7ca745d666aab1
# Thu, 21 Nov 2024 20:07:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:07:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:07:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:07:48 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:07:48 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:07:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12908080ef4c1fe1084233332d7f38ee24d4d9205cf67d2efaaf56b48161c8`  
		Last Modified: Fri, 22 Nov 2024 20:34:07 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108f2378d159809cd20c16968f33184d490c2aeb6efac4b1ab24cb3014f9012e`  
		Last Modified: Fri, 22 Nov 2024 20:34:07 GMT  
		Size: 1.0 MB (1049362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56e305cc8981dd87964d1f003a738a758f1d1875083f70573b5ec28ec25e1a1`  
		Last Modified: Fri, 22 Nov 2024 20:42:10 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66eff82c1eeaedb859d806f658b6b1559962da775f8f66e9a8de0a5763a5868f`  
		Last Modified: Fri, 22 Nov 2024 20:42:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966e0b40347db92ff322ec7ba1ee6c8606fe05ccc569818db70b568d773f4856`  
		Last Modified: Fri, 22 Nov 2024 21:05:34 GMT  
		Size: 90.1 MB (90103729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c099fd070d1d9a59cf2e94c72b3856d54a102c534e1fc23c4803b79d8a71cf4b`  
		Last Modified: Fri, 22 Nov 2024 21:05:31 GMT  
		Size: 9.0 KB (9016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a53ff8e455c27054f2105b5191b1d597622cce78295ee7572a1d5f1f2a50104`  
		Last Modified: Fri, 22 Nov 2024 21:05:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f2eb2b58edb771446e0889f22a2009dc8d52a0128811f21c828be490d5587b`  
		Last Modified: Fri, 22 Nov 2024 21:05:31 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6798480a31573916e33ee48ee38d98edca9cb4c0f61adbb26125f26958355567`  
		Last Modified: Fri, 22 Nov 2024 21:05:32 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff8416ed047e1bcc610e8dd8bac7ab0fe97692df78398f7445fcc6ac6cea02f`  
		Last Modified: Fri, 22 Nov 2024 21:05:32 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:ebbd1ff83c0e0e5f2cb1954204b21a1921365b8b4ceb188aee9d92ddbec1f4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba0b704178799189ee8a468e42fa4ede4ecbdf4ceb1ce57c408b767e8470b8c`

```dockerfile
```

-	Layers:
	-	`sha256:d6a6d77061b73951b4ea3f49479abb96f7e19d0abd9189cd23f04c28ce075358`  
		Last Modified: Fri, 22 Nov 2024 21:05:32 GMT  
		Size: 966.1 KB (966087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1d2cf868fcff0f1197de2b280848b1f19b437a59d2472e2a35bbc20f66bae7`  
		Last Modified: Fri, 22 Nov 2024 21:05:31 GMT  
		Size: 44.9 KB (44898 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:89af39c5fc04142897a5d7288296b3872b1025a65c1a1d3884313733d2d256b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100938234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355e4d60dec11b7b0295ff849d62cc2d01000f89d588f9d952c343965b0d8cbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:07:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_MAJOR=13
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_VERSION=13.18
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_SHA256=ceea92abee2a8c19408d278b68de6a78b6bd3dbb4fa2d653fa7ca745d666aab1
# Thu, 21 Nov 2024 20:07:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:07:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:07:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:07:48 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:07:48 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:07:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0d5105d2155612c64a041f7abeaa62a2b7d40a614e696146626dab5819ee16`  
		Last Modified: Fri, 22 Nov 2024 20:27:55 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a343a2c765b2d7ec17f0e90606aa558684450afec589b8bd46b07f14721523`  
		Last Modified: Fri, 22 Nov 2024 20:27:55 GMT  
		Size: 1.1 MB (1095461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7e8fd7a2f30f4f659287810bd5ea44fb9fd9dcec934e03d0a4584aff278c7e`  
		Last Modified: Fri, 22 Nov 2024 20:27:55 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a034184b87c3b6799417866291554bb14207e631e5a711bc29caf001c1480a`  
		Last Modified: Fri, 22 Nov 2024 20:27:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17bc61ddf12d2a5e0db65a5d1acb344c4faa9160100b7641c4e67ceb2ab2b7d`  
		Last Modified: Fri, 22 Nov 2024 20:27:58 GMT  
		Size: 96.6 MB (96572637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e56eb35022e71376ab003d5e917f4affeb781ec646b838d566133dc5c0577c`  
		Last Modified: Fri, 22 Nov 2024 20:27:56 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6095b5c81c37e545018380a11d9195368714a1f2be1dbcf4b4877196bd9e`  
		Last Modified: Fri, 22 Nov 2024 20:27:56 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971c659c6f144bb6a502d8b77a0a299436736bf5c0de5367b84d643bcf039e6c`  
		Last Modified: Fri, 22 Nov 2024 20:27:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c211264f456d17c4ffca227e9da2acade7094fbfb0d91b4745e39eac28d359ea`  
		Last Modified: Fri, 22 Nov 2024 20:27:56 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0fc5892cf6c5e3af9bdd167f911523149606af4841128badda289df970db5e`  
		Last Modified: Fri, 22 Nov 2024 20:27:56 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:ee9c60922b5e7cfada35d11aafa3a0c45380226d52c3903d82c1975e76324bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2284c52f8c5af9540da0ca3cbdee5ce41a5bea64f6c95630364195b63570a60d`

```dockerfile
```

-	Layers:
	-	`sha256:5954bf7765e6d1ed43f2832a826a834984dc205d083eb56cfc7edea39c5445aa`  
		Last Modified: Fri, 22 Nov 2024 20:27:55 GMT  
		Size: 966.0 KB (966040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:762a76ce3c07e4db074aa796558b60fa1383dca1bc5109df18844d069dd0702c`  
		Last Modified: Fri, 22 Nov 2024 20:27:55 GMT  
		Size: 44.7 KB (44660 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:b120ce907a9f04075ed13324a87c8dc15e1bd414f37bbcbc2c903b98379786b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100145633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e38f2d3dd2ff24b5dc12b16b6965d91c8d5f9daaa4eadec4792c083c802903`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:07:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_MAJOR=13
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_VERSION=13.18
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_SHA256=ceea92abee2a8c19408d278b68de6a78b6bd3dbb4fa2d653fa7ca745d666aab1
# Thu, 21 Nov 2024 20:07:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:07:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:07:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:07:48 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:07:48 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:07:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b210ec8ed1260138487b366b6cc6cf870563d4506a35f0a64ccdc7db288b503`  
		Last Modified: Fri, 22 Nov 2024 20:39:39 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f569b818764a75b625723057d18967c65a9adae20004f6d1aa2a6a6f141f80`  
		Last Modified: Fri, 22 Nov 2024 20:39:39 GMT  
		Size: 1.0 MB (1039701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63aaaafb14cd321df8b5ca67c848dc45a2338f4035ab70e99b0ac6389005a932`  
		Last Modified: Fri, 22 Nov 2024 20:49:33 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f154c1764c5654b15d98e0100301c9ff6316930d0b36d0661aae65faff846b4c`  
		Last Modified: Fri, 22 Nov 2024 20:49:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d1ec3508ef9e410fe8ba4163ed5129e0865156b8498df509fb229534884464`  
		Last Modified: Fri, 22 Nov 2024 21:17:51 GMT  
		Size: 95.7 MB (95724947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261d702bfd9e8eec9870a8e344895b805de3149df3c3b30a66ca1b8436a26c7d`  
		Last Modified: Fri, 22 Nov 2024 21:17:48 GMT  
		Size: 9.0 KB (9020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c152056c489be9bd9fe843474e54833a263e9021c89fe45b9fd5985e304ec5`  
		Last Modified: Fri, 22 Nov 2024 21:17:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69cf3c2cf00fdfe4379a8965b04697461f1788b0fa231fa9555de04bcc58347`  
		Last Modified: Fri, 22 Nov 2024 21:17:48 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedf490555f54731c14e89c5b7fa1826db8dca367279bbe5d0fd03ac647755b7`  
		Last Modified: Fri, 22 Nov 2024 21:17:49 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd10ca8cdfc7669cf84231e3769faa7f588d0ce9b24e46f22850417b45117449`  
		Last Modified: Fri, 22 Nov 2024 21:17:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:53c83ddb971d19e7c05c45309f5a94fe2015b3f025bf4ef372145388e65bdcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1007204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c584115d8f9c40d5befb4df3581cac4e99d1c09a85ca94197480c2fcab926efc`

```dockerfile
```

-	Layers:
	-	`sha256:30f0ff762131257c13d8df9b108ab900df7f87a4119a2bc1acc23198cffd53a9`  
		Last Modified: Fri, 22 Nov 2024 21:17:48 GMT  
		Size: 962.5 KB (962459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e52208633d1b768ed5cde17a01a9c0805b66ddac4fb77fd35357e3f6076cd91`  
		Last Modified: Fri, 22 Nov 2024 21:17:48 GMT  
		Size: 44.7 KB (44745 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:1b6dcd366cee803bbee4bd32f48023fe29ab86884fa0f9b6de67e8b9ebceeeed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104440674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c28f08862d416930838f2ab15064039e5f324aef8c4ef45807c3107f9010fb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:07:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_MAJOR=13
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_VERSION=13.18
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_SHA256=ceea92abee2a8c19408d278b68de6a78b6bd3dbb4fa2d653fa7ca745d666aab1
# Thu, 21 Nov 2024 20:07:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:07:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:07:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:07:48 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:07:48 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:07:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7508d4d6ac64ab81f5f150e33662bfd19f23a5c43a2e417c08da4ef9669ea599`  
		Last Modified: Fri, 22 Nov 2024 20:36:47 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50692ebd9455b35336c3bbf6d65952fc740571194ad1404bee4b68c65a2d5eda`  
		Last Modified: Fri, 22 Nov 2024 20:36:47 GMT  
		Size: 1.1 MB (1083900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0fc7b1619a2ef674c606069a975f0de7c57938bd6bd30094ae92a0850cb056`  
		Last Modified: Fri, 22 Nov 2024 20:46:08 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec9e98c8f2fafd55b33b7ef1022974a43f4a5dcfd94b9c1258dbaf476372cb6`  
		Last Modified: Fri, 22 Nov 2024 20:46:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28dea5cbfb056ecbb74415903c3dc2ad353bf9c35a8164e7699c959bcac33f76`  
		Last Modified: Fri, 22 Nov 2024 21:17:09 GMT  
		Size: 100.1 MB (100086898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffecfd221def3ed81d8f9e7c71ea21643d45cf5687d1e033417bb807ae8d9c5`  
		Last Modified: Fri, 22 Nov 2024 21:17:07 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d6b4e5d9020b853de5d0f577e7f035c222638882093cb5b4a51ebe1c075f1b`  
		Last Modified: Fri, 22 Nov 2024 21:17:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c9b04adbafb8b7f686c47ec4349b43ef0bedc8352dc72bfe6b1deab0352a9b`  
		Last Modified: Fri, 22 Nov 2024 21:17:07 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e4005286df94acb6e1cfd048de662a0843eb212691650463fcad75ae175810`  
		Last Modified: Fri, 22 Nov 2024 21:17:08 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e78324aecd77c4678c3b9288e933551cf861a14a63fba1c4ee360f089cc6309`  
		Last Modified: Fri, 22 Nov 2024 21:17:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:1b007c7603636e2c969249e02cc2d9f4fb12eb7cf5f97155c960573dd7fa6445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1008805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610e66800b602a776e0fd0489cc81262ffa04401557b89d88a8647b1ed7ff431`

```dockerfile
```

-	Layers:
	-	`sha256:0e5272d592a40571fb9cc6ee48cca8916b857ed8abe2341683c22a694d280e88`  
		Last Modified: Fri, 22 Nov 2024 21:17:07 GMT  
		Size: 964.1 KB (964101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1dd514b6392ddbbc8593068da3c454886bff4990a2354e82c76e6e532b6db0a`  
		Last Modified: Fri, 22 Nov 2024 21:17:07 GMT  
		Size: 44.7 KB (44704 bytes)  
		MIME: application/vnd.in-toto+json
