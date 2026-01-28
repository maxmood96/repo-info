## `postgres:15-alpine3.22`

```console
$ docker pull postgres@sha256:62ad5432bc4c18c5189c3e72f92f6ba41810f128c431bd451a68295bf90d3055
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

### `postgres:15-alpine3.22` - linux; amd64

```console
$ docker pull postgres@sha256:8692bebfeb775980f742fd3df0452a40e854d2e2ddaeafb8211fafd3e0901881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.7 MB (108678217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a75c23ca2ba5ec153724be7899d069bd0f63bc3eb44d608e4974fa40224846b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:31:35 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:31:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:31:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:31:37 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 02:31:37 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:31:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:31:38 GMT
ENV PG_MAJOR=15
# Wed, 28 Jan 2026 02:31:38 GMT
ENV PG_VERSION=15.15
# Wed, 28 Jan 2026 02:31:38 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Wed, 28 Jan 2026 02:31:38 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:33:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:33:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:33:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:33:42 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:33:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:33:42 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:33:42 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:33:42 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:33:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:33:42 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:33:42 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:33:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54b887d3b44826f37bd787a7ff0b291e94eecdef5d361b28ca7797bbac128a2`  
		Last Modified: Wed, 28 Jan 2026 02:33:57 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f4a2b07d6653b2ef9f75c618ed422b32f1dce2a225c0e9961e63bef094c654`  
		Last Modified: Wed, 28 Jan 2026 02:33:57 GMT  
		Size: 918.3 KB (918291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8ccea1bbf1cabd608fa2b68d566e5fcb81ee8b2121f6ffea2029acdd64b5c`  
		Last Modified: Wed, 28 Jan 2026 02:33:57 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3716bdff25f8ced0f4ee240224bce4a858eafaa9569b6885e9ec6da67c2fb81`  
		Last Modified: Wed, 28 Jan 2026 02:33:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f7c844e842fa046b839850fb99913a7618c5d0b941ad6f2f0576f017b46df4`  
		Last Modified: Wed, 28 Jan 2026 02:34:00 GMT  
		Size: 103.9 MB (103938030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158a68a1c9741cf69f1db8de8ca2e2bbabb18a8174ec5c122053386854ebd96b`  
		Last Modified: Wed, 28 Jan 2026 02:33:58 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8243ba4b9bcfd1fcb431d7bc5ac8b6d20b818563c0bb9357ee3d83f090f39181`  
		Last Modified: Wed, 28 Jan 2026 02:33:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368f9348894fc9fd3f47d9989211ca2f15fda5693001d9dc84582c7d2f531122`  
		Last Modified: Wed, 28 Jan 2026 02:33:58 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253d32bbdfa0525a1556589c97967b2826f99cf7b100af96dd9e141ede9c100f`  
		Last Modified: Wed, 28 Jan 2026 02:33:59 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fff989b60db97de41aeb94adbbe5914b9cb67413b4f51007b1cf00c40ec8fb1`  
		Last Modified: Wed, 28 Jan 2026 02:33:59 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:88bf1520188af5b7358e8f3d77b3697a4f3c69e20b6de66d2a676d25bda7bb49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.1 KB (640082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf02a1552e9a8895983f6af02180e6d8402bb5f0121df4da2233da720051a93`

```dockerfile
```

-	Layers:
	-	`sha256:17c2d131c9a7e61f0ebf677d2b88b26b7c7b28cab940b12073c9717183482c45`  
		Last Modified: Wed, 28 Jan 2026 02:33:57 GMT  
		Size: 596.3 KB (596315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:643fba34bd3bad600bcfbb0b6090f234d43a3de6357f6a9055bbb56aed65701c`  
		Last Modified: Wed, 28 Jan 2026 02:33:57 GMT  
		Size: 43.8 KB (43767 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:d3194ef787dad6b93a66b95fc0eee096229a4fd3309e47ff7279ca89ca496d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88288701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1075868005ec2d43ac6acd7fe7ac7589beeb9290beb0908ae331974283a6d48b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:35:02 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:35:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:35:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:41:38 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:41:38 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:41:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:41:38 GMT
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 19:41:38 GMT
ENV PG_VERSION=15.15
# Fri, 14 Nov 2025 19:41:38 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Fri, 14 Nov 2025 19:41:38 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:44:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:44:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:44:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:44:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:44:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:44:24 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:44:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:44:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:44:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:44:25 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:44:25 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:44:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:10 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff394fcf6f7178033c7c58216211e2ab0860f1a390a7687ede66b0574d0858b8`  
		Last Modified: Fri, 14 Nov 2025 19:37:58 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25ff5be3dbe79b60122e717c8fd55fca21449ac3798e8687fdae2c833035d51`  
		Last Modified: Fri, 14 Nov 2025 19:37:58 GMT  
		Size: 886.1 KB (886131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13dd79c8739f8e51bea30ae0706d5f9463796007d2c627dea4be31a9c080400`  
		Last Modified: Fri, 14 Nov 2025 19:44:35 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4050bceb1f56fad4ccab7d205d1969a12de5a2ba95027f4f9a76f403a9c4df00`  
		Last Modified: Fri, 14 Nov 2025 19:44:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a15296ddde85f09c1978ad6c7eae092471067277e81e63b0fbcc867ebeb2ee`  
		Last Modified: Fri, 14 Nov 2025 19:44:37 GMT  
		Size: 83.9 MB (83881464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b2217e1f1cf0e1f4ec54499f58f988b2da3ceb695d8b6590c2730ee4d8f537`  
		Last Modified: Fri, 14 Nov 2025 19:44:35 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e475fe2066cb134504eea3b42b46e21e4c57bb78cfa62637595798523f599c`  
		Last Modified: Fri, 14 Nov 2025 19:44:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ea6fab2f515be520edda1894b6f9ae869b895fc68ab72974338442545b910c`  
		Last Modified: Fri, 14 Nov 2025 19:44:36 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e0a1274111bd4627ac9491d073f936c6c9f221336c323b5c923db8b743ff77`  
		Last Modified: Fri, 14 Nov 2025 19:44:37 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd00420e075f129b7e5a0a706b0aa1d38e22f1b7f8d419d4f6837ecbee1552a2`  
		Last Modified: Fri, 14 Nov 2025 19:44:37 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:0feb21cfee3c22be5fba677b197c4479a4682773aa16941dff5840f8fbafabf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 KB (44350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c263a2a5017cc85571de4a784984425646baaf4fcb72068e533d3c8080c1e515`

```dockerfile
```

-	Layers:
	-	`sha256:ff79a4133e632033b55d495e2bb769e33b98cd7cdba81c5dc87ec9dd3a2c6e51`  
		Last Modified: Fri, 14 Nov 2025 19:44:35 GMT  
		Size: 44.4 KB (44350 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:122ad57c9161aa18de19bc08f825ff8f556aae43e5dca73d8b52f293cf043e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83573934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c951d903aec9d740437baf4cc1f491a0bdba41f015e6d42f537b6940654b34e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:49:19 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:49:23 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:49:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:49:23 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 02:49:23 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:49:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:49:23 GMT
ENV PG_MAJOR=15
# Wed, 28 Jan 2026 02:49:23 GMT
ENV PG_VERSION=15.15
# Wed, 28 Jan 2026 02:49:23 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Wed, 28 Jan 2026 02:49:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:52:04 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:52:04 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:52:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:52:04 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:52:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:52:04 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:52:04 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:52:04 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:52:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:52:04 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:52:04 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:52:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139083fc08b0d5c94bec5b23a34e72e31be20cb9df33f464d97c0a4ecf317f64`  
		Last Modified: Wed, 28 Jan 2026 02:52:15 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38137c6822c27331f550d88a615051e324bf0d3838f881a5002f63eb70b4b56`  
		Last Modified: Wed, 28 Jan 2026 02:52:15 GMT  
		Size: 886.1 KB (886132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2723fa66436353ac2b41e7e70c9af5718598315b7cbc8b71ce67acc53881c369`  
		Last Modified: Wed, 28 Jan 2026 02:52:15 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6168c5707c833653d96c14803179160b3812653dc6ac2302cd569adff45adc`  
		Last Modified: Wed, 28 Jan 2026 02:52:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa1697e219e93d68a0b2e2e48f7e7a71e3a44d9a2c25293c04227ffc17857cd`  
		Last Modified: Wed, 28 Jan 2026 02:52:18 GMT  
		Size: 79.4 MB (79447142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d4cfe9bfc0841e25838a9ebd77f5b63ce3e9d38d9e864fb651731c504bc3ae`  
		Last Modified: Wed, 28 Jan 2026 02:52:17 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b384450d3146904060c25088e960109ce28286672fd0a1a3f291f388bbcb4e`  
		Last Modified: Wed, 28 Jan 2026 02:52:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138511b97f48220f4c0573f6ab4f6807e3f0bc5223bfc66ecb4c35748faff7ff`  
		Last Modified: Wed, 28 Jan 2026 02:52:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2264a102f9f434ae1cb9c529f247fef699e7560944502d40522f0cdee6efb1`  
		Last Modified: Wed, 28 Jan 2026 02:52:18 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c37bad1a41348990d6eb0bacd51ca5b637156141d4d5a382b852943d65a8bec`  
		Last Modified: Wed, 28 Jan 2026 02:52:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:4b0f9a058d6ec8fb938a9f01c205c39ab8af409fba51a02cb48279f91f5a38e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.3 KB (640265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392f06e0fb39552446408f177603ed12b21b924850e7b0c50348a5c06cfc73de`

```dockerfile
```

-	Layers:
	-	`sha256:c16cc314c787741ae625135056090c52deb22e3d7ac677493cc2b58cbd91e98a`  
		Last Modified: Wed, 28 Jan 2026 02:52:16 GMT  
		Size: 596.3 KB (596335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c87307320b80b6507dc7ac9491577e1566d69f7962b4a54fedcf40939076da68`  
		Last Modified: Wed, 28 Jan 2026 02:52:15 GMT  
		Size: 43.9 KB (43930 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:3a3a6268532121f79afb2ee4a21d53c520c18d9b559cc08e4c67cb2193dde7b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104646022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb41fb9870f1253258a5b0ac98f2b4d14d9ee2a94d7189b265c0f120fb87ead`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:34:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:34:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:34:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:34:26 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 02:34:26 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:34:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:34:26 GMT
ENV PG_MAJOR=15
# Wed, 28 Jan 2026 02:34:26 GMT
ENV PG_VERSION=15.15
# Wed, 28 Jan 2026 02:34:26 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Wed, 28 Jan 2026 02:34:26 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:36:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:36:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:36:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:36:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:36:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:36:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:36:57 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:36:57 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:36:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff50ab53c6bee0e5ba73b80a4920cfae3f77518329fd76913c9290dec63c641f`  
		Last Modified: Wed, 28 Jan 2026 02:37:11 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc6bc95e62943f057a6f0340ae4b9e2cc83ec298bd09ebb756b79b2ffa58cc0`  
		Last Modified: Wed, 28 Jan 2026 02:37:12 GMT  
		Size: 873.5 KB (873490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f615737c11ce359c08921f1ff6d817bfb41017da20a68dd813e8c586e5e9dd9`  
		Last Modified: Wed, 28 Jan 2026 02:37:11 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d2e104c96ae9b486d279bf9ba34f59a93f8c3ba8a0d8aa17cf8125106fa1cd`  
		Last Modified: Wed, 28 Jan 2026 02:37:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35d4cd190a559bae407d0c7128f0e14b5a6ef888e611e0866d1208c309305ac`  
		Last Modified: Wed, 28 Jan 2026 02:37:15 GMT  
		Size: 99.6 MB (99615988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c014775d5a0f237ced335ae304f70fc664f2da6088893b426a752528d8c6ea`  
		Last Modified: Wed, 28 Jan 2026 02:37:13 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e3027ef6c049e839ad9704812e23b67473f391fd8821668594b254657b5c53`  
		Last Modified: Wed, 28 Jan 2026 02:37:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766b3608ebfbe6708560baa8c3301c98d88a8289b69750dc04c85e77c8bb6ca1`  
		Last Modified: Wed, 28 Jan 2026 02:37:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59e6eed849ed7a375b4a47cbb6de50a76e6ade3aefd3eec9bc36131d3652af0`  
		Last Modified: Wed, 28 Jan 2026 02:37:14 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2af3e891cf05233049e8bfa149880435e631749c99aabf50c46bb8774a3b7d`  
		Last Modified: Wed, 28 Jan 2026 02:37:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:fc98206a41bc8feedcbdb5c049fa88e566cf854c1ad72e7e8c395108200c7864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.3 KB (640309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984b3f93f95fb8893b92a469140924c17f8b2ba2b1c50b626a949a883bd6fd14`

```dockerfile
```

-	Layers:
	-	`sha256:e499729bcf748f5fe7b7d77e2e9015a3d88baf6a8eb81c8fad46488a2b9372f5`  
		Last Modified: Wed, 28 Jan 2026 02:37:12 GMT  
		Size: 596.3 KB (596347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12783374ededde7761af03f2d2da25b690eac52b865a29693e6774f00fb95886`  
		Last Modified: Wed, 28 Jan 2026 02:37:12 GMT  
		Size: 44.0 KB (43962 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:eaba64dae5a52d4e47196d2779b0a08f340572f45ea27fdde6eceae7f8202a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114945268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1c5670a3b45dada65f2d9ddaed30aea292c4bc4d5f12897a0c266cfc5a94c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:27:53 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:27:56 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:27:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:27:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 02:27:56 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:27:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:27:56 GMT
ENV PG_MAJOR=15
# Wed, 28 Jan 2026 02:27:56 GMT
ENV PG_VERSION=15.15
# Wed, 28 Jan 2026 02:27:56 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Wed, 28 Jan 2026 02:27:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:30:04 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:30:04 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:30:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:30:04 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:30:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:30:04 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:30:04 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:30:04 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:30:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:30:04 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:30:04 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:30:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277c009459198dbdb5ab2cdb4a943df6164d9eadfc1bc24f0d825eac8b6868ae`  
		Last Modified: Wed, 28 Jan 2026 02:30:18 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d548e996725115b11c4acc18ae8966fbc6cda6218dca4cc1a6d6f2f51be388`  
		Last Modified: Wed, 28 Jan 2026 02:30:19 GMT  
		Size: 890.6 KB (890631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e7341ab9395fee371c0de719deb6f428c73b30c55b759f8167b1f3f03283c5`  
		Last Modified: Wed, 28 Jan 2026 02:30:18 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e12d6c70772e675275c9e1de8cf029a9ca62425c85d505f47fd2eea033a0de`  
		Last Modified: Wed, 28 Jan 2026 02:30:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c49ad4e1ad68c3c0b85883a556a7e502137400428e70019fbf51f28ff7cc9c`  
		Last Modified: Wed, 28 Jan 2026 02:30:23 GMT  
		Size: 110.4 MB (110416876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cd9db7ed0b303fc50b93793c6e964fe1f6b706c8930971c13142ff86534ebd`  
		Last Modified: Wed, 28 Jan 2026 02:30:20 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424031d99f5853a35d6e2e80fce0f0589a76f39ffe947def5fdec406e6baf176`  
		Last Modified: Wed, 28 Jan 2026 02:30:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8046238b313ca29f72e222ad1a05e93e2b2aab105e4d3d34c78aa035cd7b0764`  
		Last Modified: Wed, 28 Jan 2026 02:30:20 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949c54663b02a4e5666c6bd0759d8084492b76ea44352e15fbbada8f07d01a50`  
		Last Modified: Wed, 28 Jan 2026 02:30:21 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1e1ad02554d4e878851a8141e7c603fe78e327d201a416564f95fb4f8c7201`  
		Last Modified: Wed, 28 Jan 2026 02:30:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:3ccd1d1afedf77b9371e0701970e09b4eb0e0a6e1a2b4fb24942d1b6ec47a4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 KB (640029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4df79ad0d071525ca60b4a2c7b72bf2138cbb203d883f87328a679f4afd5a58`

```dockerfile
```

-	Layers:
	-	`sha256:024f72f5d9d4b5448e63ef52922b0e3c1bfbe9bedef0d42c40e745bcc7f9b977`  
		Last Modified: Wed, 28 Jan 2026 02:30:19 GMT  
		Size: 596.3 KB (596300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41a539977298ad708c56d9ad61c3257820e306aa5f48fd284abab1146f67b7eb`  
		Last Modified: Wed, 28 Jan 2026 02:30:18 GMT  
		Size: 43.7 KB (43729 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:5d20e6bf518d74d9206dfc7f535bfd4a34995039137fdf2b6c7fc575b1bace92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92419180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417342c1b6f659752aeead0725b6284f18d6abed9d500b14c8ee60fc9990b0ad`
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
# Wed, 28 Jan 2026 03:41:23 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 03:41:23 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 03:41:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 03:41:23 GMT
ENV PG_MAJOR=15
# Wed, 28 Jan 2026 03:41:23 GMT
ENV PG_VERSION=15.15
# Wed, 28 Jan 2026 03:41:23 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Wed, 28 Jan 2026 03:41:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 03:48:10 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 03:48:10 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 03:48:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 03:48:10 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 03:48:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 03:48:11 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 03:48:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:48:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 03:48:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:48:11 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 03:48:11 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 03:48:11 GMT
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
	-	`sha256:feb8caad2d394d40c900318205bb2a4fab84cb8a4174174889d0d3ba8cd34ec9`  
		Last Modified: Wed, 28 Jan 2026 03:44:43 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea567f655947b15a81f4906d157299d55233dbc5ed74ff062f795cda2c2b610c`  
		Last Modified: Wed, 28 Jan 2026 03:44:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e459c5f60023bdeb1173eb8fdc01ad080bf20074a3bfc4fa7f666985117f71`  
		Last Modified: Wed, 28 Jan 2026 03:48:55 GMT  
		Size: 87.8 MB (87788804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca94ba3de7106db93ac4269f8ed2eb77bf69b33039186826860fe6b2bf6cd2d`  
		Last Modified: Wed, 28 Jan 2026 03:48:53 GMT  
		Size: 9.5 KB (9456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b2d161f04ed3ba40aacb69b51c1e5f354c3de5be723d3dc15d0c7e464ad5b9`  
		Last Modified: Wed, 28 Jan 2026 03:48:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32288fe844c4c9c556117b72d4030d8512c6d9173f8db1a494ed48eca8e10f8d`  
		Last Modified: Wed, 28 Jan 2026 03:48:53 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75ee140cc94f56d06194e235fce5a82bebeb5ea9bb2edd07ad6086800cd5eb3`  
		Last Modified: Wed, 28 Jan 2026 03:48:54 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511face63cac81e03479cf8d6270c56ab14edffc1e6e66b9ac003c660fcfca61`  
		Last Modified: Wed, 28 Jan 2026 03:48:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:af12a3544a0eb5fcaa17566071e94d7e92b54aa27527b9abf487b1e88bae95c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.5 KB (636534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f6afb7e9c5ce6590f998e85c39832c8ac571b55f640d15720f21c6f4a0e804`

```dockerfile
```

-	Layers:
	-	`sha256:07f555a36ac811646d00069a35b01883d559bf014a700ccd261ab88e0e1f26df`  
		Last Modified: Wed, 28 Jan 2026 03:48:53 GMT  
		Size: 592.7 KB (592724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1503b5c50b40172c90f2f41bec015167f6b3a31c7e56a72c07d23e24eba0a7c`  
		Last Modified: Wed, 28 Jan 2026 03:48:53 GMT  
		Size: 43.8 KB (43810 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:fe6dcc02e55139ed00c4747cc73ea9432695b784ab87820e3eaf5a51a942f972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108615329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2de6efa4b8c42aa02db5af3ba8acf224e37356e0848dc5c5cc17217b18594c`
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
# Fri, 14 Nov 2025 07:42:02 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 07:42:02 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 07:42:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 07:42:02 GMT
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 07:42:02 GMT
ENV PG_VERSION=15.15
# Fri, 14 Nov 2025 07:42:02 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Fri, 14 Nov 2025 07:42:02 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 10:22:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 10:22:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 10:22:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 10:22:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 10:22:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 10:22:26 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 15 Nov 2025 09:51:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 15 Nov 2025 09:51:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 15 Nov 2025 09:51:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 15 Nov 2025 09:51:35 GMT
STOPSIGNAL SIGINT
# Sat, 15 Nov 2025 09:51:35 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 15 Nov 2025 09:51:35 GMT
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
	-	`sha256:b61568bffe09594f38a4358fa0027d359c02c9e9664c5e3da06f4814c0e9823a`  
		Last Modified: Fri, 14 Nov 2025 08:34:15 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f405327ef14efadeef909f0df17348553c8e2b5d4662f91456b23d19d7fe6218`  
		Last Modified: Fri, 14 Nov 2025 08:34:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44143512cbb42a1efd6b3dc7bac9cf5fecf4cdaba24f1ade01989b860c1d9bb7`  
		Last Modified: Fri, 14 Nov 2025 10:25:28 GMT  
		Size: 104.2 MB (104216408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b353d8c3b0f1de46dfadc792ead303ac82bafda1226113fe2d7fbdbafa45b99`  
		Last Modified: Fri, 14 Nov 2025 10:25:13 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f38d82832eaeec386f4e140842f516432df6e8e31d0a61b68c7ed8c6ba093ed`  
		Last Modified: Fri, 14 Nov 2025 10:25:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc7d62b936690497e08cb8acac7952029a6f5a16c3f2d558d4f3d40ee2b9b1a`  
		Last Modified: Fri, 14 Nov 2025 10:25:13 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e561d4d26263487a383a6cf103f1c2ea9c4c2d34f16b7d745d12a1b273d0a3`  
		Last Modified: Sat, 15 Nov 2025 09:52:49 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe6a5f71ce0835154937fa8355fea690c3dedefe1fd4a9b7c168361f5363776`  
		Last Modified: Sat, 15 Nov 2025 09:52:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:67c4e6309be8d93e0fea1fa9a05cbbf6d1c669c824d13cbeb596519f389dadd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.5 KB (639466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0c6f00b7487caf1cddeb2cde3859233cd11debdfa6dbb86b1517abe5631963`

```dockerfile
```

-	Layers:
	-	`sha256:f42e447fc1efa5d4c2a7cc285a5434c1edc6b004ecffb72734110992eb2c730a`  
		Last Modified: Sat, 15 Nov 2025 09:52:49 GMT  
		Size: 595.0 KB (595016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a66310147c1f422a1d95e47853679e796af931cbe35d125596d5c807cbbe68dd`  
		Last Modified: Sat, 15 Nov 2025 09:52:49 GMT  
		Size: 44.5 KB (44450 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:12afc4bdcd7724fffc21d97e68d32c775efb70044ff65514e0b4462371ffe9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 MB (117377584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b813f470ac3ed63ce6de2cd267cf77a5b13225f19e95c3b5127fbabffc5584c`
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
# Fri, 14 Nov 2025 01:24:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 01:24:12 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 01:24:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 01:24:12 GMT
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 01:24:12 GMT
ENV PG_VERSION=15.15
# Fri, 14 Nov 2025 01:24:12 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Fri, 14 Nov 2025 01:24:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 02:43:18 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 02:43:18 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 02:43:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 02:43:18 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 02:43:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 02:43:18 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:35:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:35:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:35:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:35:17 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:35:17 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:35:17 GMT
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
	-	`sha256:7d26e50aab688246007d981ec03ed0f2ba085e93831f3c2b4a5c41cedb4f6ab4`  
		Last Modified: Fri, 14 Nov 2025 01:27:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d3fda138bdb19608f3408a47a5ceb1f1e5a70ee029d664c864ace4ba7e8e7d`  
		Last Modified: Fri, 14 Nov 2025 01:27:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2730712dd33522d17e97b5701f3cc62f2050a31301ce02945319e7b2befce107`  
		Last Modified: Fri, 14 Nov 2025 02:43:44 GMT  
		Size: 112.8 MB (112816885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4e1e0681ba1ef3aa5eb57c8dc6a6c7cdb3872bebde0979aece2107d3219d0c`  
		Last Modified: Fri, 14 Nov 2025 02:43:41 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4192e5491af9c3809185888dd7ed36902589a54190290574fd1c90e41bc0ca`  
		Last Modified: Fri, 14 Nov 2025 02:43:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed7c969136a93b72a0b5ab9c06f21fb18e551bf6db5ed6e06204a81eb18931a`  
		Last Modified: Fri, 14 Nov 2025 02:43:41 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fb5b593fa9332505e7244506435b61e6f6c3108a3fd1156742361f80f2aae2`  
		Last Modified: Fri, 14 Nov 2025 19:35:29 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ea3dcff44523a78fa473eb03788fd3ed8a1c95086781e0787935938682c420`  
		Last Modified: Fri, 14 Nov 2025 19:35:28 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:203ada7223eff1a5f19bc143b4f1b788cab0e6ed5079849d0c27a807d38a8852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.4 KB (639376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a606b57c5f95241aca4d1c37affc44dea0066d4db053bc49761688ee3ba845e4`

```dockerfile
```

-	Layers:
	-	`sha256:6c143a0dc8aeeb3f1667cb8316a937864b670d2815554fb4b048acb199199a42`  
		Last Modified: Fri, 14 Nov 2025 19:35:29 GMT  
		Size: 595.0 KB (594986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2501129c72b1e03e66cf0f7355b67376709ca1364d17364e144ac2b92d8549dc`  
		Last Modified: Fri, 14 Nov 2025 19:35:28 GMT  
		Size: 44.4 KB (44390 bytes)  
		MIME: application/vnd.in-toto+json
