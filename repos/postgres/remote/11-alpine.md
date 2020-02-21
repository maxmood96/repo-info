## `postgres:11-alpine`

```console
$ docker pull postgres@sha256:b93192d25a80e1299955199f94b1be87304a821cb4e6be9caedc94a977f2bf09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `postgres:11-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:f1e48907613dd57c701e327f25e7f4f61443ff4ae2f5b90104d5c2b4cb3087ce
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59224749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9ed89bf55810ffc94d15c9e85c6d99b32123d801d6b8f7aa471e9fe9d28d25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2020 03:17:19 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 21 Feb 2020 03:17:19 GMT
ENV LANG=en_US.utf8
# Fri, 21 Feb 2020 03:17:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 03:25:09 GMT
ENV PG_MAJOR=11
# Fri, 21 Feb 2020 03:25:10 GMT
ENV PG_VERSION=11.7
# Fri, 21 Feb 2020 03:25:10 GMT
ENV PG_SHA256=324ae93a8846fbb6a25d562d271bc441ffa8794654c5b2839384834de220a313
# Fri, 21 Feb 2020 03:32:54 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Fri, 21 Feb 2020 03:32:56 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 21 Feb 2020 03:32:57 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 21 Feb 2020 03:32:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 21 Feb 2020 03:32:59 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 21 Feb 2020 03:32:59 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 21 Feb 2020 03:33:00 GMT
COPY file:fa1ca76844f23c5beb98bdf3620414d012eb44eabdb324f0cce0bd5b0b913477 in /usr/local/bin/ 
# Fri, 21 Feb 2020 03:33:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 03:33:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 03:33:02 GMT
EXPOSE 5432
# Fri, 21 Feb 2020 03:33:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f3047c2e42d3a597c27f75d70b769cd0eb2498e4133b2685bccedc3c1d3e53`  
		Last Modified: Fri, 21 Feb 2020 03:51:11 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e53fddf183a4ecee751c9a7a66a903e0a2711048e4820e57ca2dea7a580cfe`  
		Last Modified: Fri, 21 Feb 2020 03:51:11 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce3f27db71b290b3e76d872a94e2927ba77b187c24254eb04365f4b359216b2`  
		Last Modified: Fri, 21 Feb 2020 03:52:05 GMT  
		Size: 56.4 MB (56408232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d12af52e60e459fd46f7501e1a9f5802fa9f0b66dd76aee4f3fa0ce9439e76`  
		Last Modified: Fri, 21 Feb 2020 03:51:53 GMT  
		Size: 7.6 KB (7567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e664312e0a687bdd3efd474d7865c92b5b8ca257fd8d5ea79f53a49c33f539`  
		Last Modified: Fri, 21 Feb 2020 03:51:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0cfb72f4fea849eed06fde6e08f98af03b751a37c8df6af7860e35c5f3c58e`  
		Last Modified: Fri, 21 Feb 2020 03:51:53 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4e02d2a5830ae757efafebec333023de54ebdb230b339f2fd2f5c629fc3956`  
		Last Modified: Fri, 21 Feb 2020 03:51:54 GMT  
		Size: 4.2 KB (4215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c67a040d276c101a2e730d5cf756ea5483a59aa97937e0a20b3c33d1915781`  
		Last Modified: Fri, 21 Feb 2020 03:51:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:09dde11b47cbeb5463153a3c6ef53371b16198959a2457d345a5264de3c92514
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57585963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3f2556955ab5047435d6c4016b91fa47d1bea58ac2c0ff8ad44957e6f1001c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2020 00:42:27 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 21 Feb 2020 00:42:28 GMT
ENV LANG=en_US.utf8
# Fri, 21 Feb 2020 00:42:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 00:48:35 GMT
ENV PG_MAJOR=11
# Fri, 21 Feb 2020 00:48:39 GMT
ENV PG_VERSION=11.7
# Fri, 21 Feb 2020 00:48:48 GMT
ENV PG_SHA256=324ae93a8846fbb6a25d562d271bc441ffa8794654c5b2839384834de220a313
# Fri, 21 Feb 2020 00:55:06 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Fri, 21 Feb 2020 00:55:16 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 21 Feb 2020 00:55:25 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 21 Feb 2020 00:55:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 21 Feb 2020 00:55:34 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 21 Feb 2020 00:55:36 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 21 Feb 2020 00:55:37 GMT
COPY file:fa1ca76844f23c5beb98bdf3620414d012eb44eabdb324f0cce0bd5b0b913477 in /usr/local/bin/ 
# Fri, 21 Feb 2020 00:55:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 00:55:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 00:55:49 GMT
EXPOSE 5432
# Fri, 21 Feb 2020 00:55:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c288e93ef5b01ac6124357c0936a9a28b458e8b331cfb2234bba3d58a80b8c35`  
		Last Modified: Fri, 21 Feb 2020 01:07:27 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e9b75c81caf8fead15ad12a8b5a6104156da54990def5f42fab50a350445e5`  
		Last Modified: Fri, 21 Feb 2020 01:07:26 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26676086e198c81d43c953d792cbba38679793beaadd8e5727eec75689cfcb2`  
		Last Modified: Fri, 21 Feb 2020 01:08:19 GMT  
		Size: 55.0 MB (54954709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0b7e44020ed81138bdb8ff77db2288eec516fbea04f127ce15f90ad3108314`  
		Last Modified: Fri, 21 Feb 2020 01:08:00 GMT  
		Size: 7.6 KB (7572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f4f7d268fc2f54fff255411a593546560e2d7d2e6f0c2075e59400a841d80f`  
		Last Modified: Fri, 21 Feb 2020 01:08:00 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e8566cc4c9bc7e1d5ab370ae0bc98d0d4f82aed6da6c8c9d3c35de1cfe2a02`  
		Last Modified: Fri, 21 Feb 2020 01:08:00 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae73c649dedc462ed32bb9f7cee1074032b66e8bb0124a566fba6d47ba183c6`  
		Last Modified: Fri, 21 Feb 2020 01:08:00 GMT  
		Size: 4.2 KB (4219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f538b9284d54b5c79bb9a8463163dde4dc5326832a77898787f2af9a076879`  
		Last Modified: Fri, 21 Feb 2020 01:08:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:e1cb7ca6cb901cc31f0eefe7a02d06406b270bbd99ea9c96e5ec6221d43de988
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54877468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecea292842c3dcc555514fafee5f11ee107068120d00df63c4e406de8c25da0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2020 04:08:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 21 Feb 2020 04:08:15 GMT
ENV LANG=en_US.utf8
# Fri, 21 Feb 2020 04:08:18 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 04:33:02 GMT
ENV PG_MAJOR=11
# Fri, 21 Feb 2020 04:33:03 GMT
ENV PG_VERSION=11.7
# Fri, 21 Feb 2020 04:33:04 GMT
ENV PG_SHA256=324ae93a8846fbb6a25d562d271bc441ffa8794654c5b2839384834de220a313
# Fri, 21 Feb 2020 04:36:05 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Fri, 21 Feb 2020 04:36:10 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 21 Feb 2020 04:36:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 21 Feb 2020 04:36:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 21 Feb 2020 04:36:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 21 Feb 2020 04:36:16 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 21 Feb 2020 04:36:16 GMT
COPY file:fa1ca76844f23c5beb98bdf3620414d012eb44eabdb324f0cce0bd5b0b913477 in /usr/local/bin/ 
# Fri, 21 Feb 2020 04:36:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 04:36:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 04:36:20 GMT
EXPOSE 5432
# Fri, 21 Feb 2020 04:36:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d28556b9d27837eddbd1e9574ccb3d3113562cf38e657148ceb2be2f1f0d47d`  
		Last Modified: Fri, 21 Feb 2020 05:42:23 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ee7ca8e5f4189fcc45873d54ebf89e8fc3b16b65e2cb34543571f1ec96d09c`  
		Last Modified: Fri, 21 Feb 2020 05:42:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61aa8d6a3df1a775695d3a76e73887b78f99b1811c9e3c8c3dd80afbd756c234`  
		Last Modified: Fri, 21 Feb 2020 05:43:26 GMT  
		Size: 52.4 MB (52444226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96946dffe66f2b617eb11a40bac80b306ca5b1e8b3dcee6e6c79a728916717f6`  
		Last Modified: Fri, 21 Feb 2020 05:43:11 GMT  
		Size: 7.6 KB (7574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1fc12dd074578051861cc203e2571836fae913ce85f41aa93ae830f067acfe4`  
		Last Modified: Fri, 21 Feb 2020 05:43:10 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38e7bace2caa6087049083a549f7af8519170f9207651768a9bd1c55d0f6042`  
		Last Modified: Fri, 21 Feb 2020 05:43:10 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda40bfd075d9d44333c41c11a85deabef375deb3b55ad956a8837cd774b2a07`  
		Last Modified: Fri, 21 Feb 2020 05:43:10 GMT  
		Size: 4.2 KB (4215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be0926802ce7ca469ae806335dd7c445416989a4b4b369510948cc5c6f2aacd`  
		Last Modified: Fri, 21 Feb 2020 05:43:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:8a756d29e7ba1a245c4153d3ef2d04b3f1e8a41214de926099a80606a01347ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58823380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a5e7dc5eda7c73c57e74128668a92d2226b5e5be6b07f98faf6cf8b90ec9bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2020 02:05:58 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 21 Feb 2020 02:05:59 GMT
ENV LANG=en_US.utf8
# Fri, 21 Feb 2020 02:06:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 02:31:45 GMT
ENV PG_MAJOR=11
# Fri, 21 Feb 2020 02:31:46 GMT
ENV PG_VERSION=11.7
# Fri, 21 Feb 2020 02:31:47 GMT
ENV PG_SHA256=324ae93a8846fbb6a25d562d271bc441ffa8794654c5b2839384834de220a313
# Fri, 21 Feb 2020 02:35:26 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Fri, 21 Feb 2020 02:35:31 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 21 Feb 2020 02:35:34 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 21 Feb 2020 02:35:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 21 Feb 2020 02:35:36 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 21 Feb 2020 02:35:37 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 21 Feb 2020 02:35:38 GMT
COPY file:fa1ca76844f23c5beb98bdf3620414d012eb44eabdb324f0cce0bd5b0b913477 in /usr/local/bin/ 
# Fri, 21 Feb 2020 02:35:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 02:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 02:35:41 GMT
EXPOSE 5432
# Fri, 21 Feb 2020 02:35:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c14e5f935b8cb1b6d0db90a9204641c43e69320b1561ce983d21b11e0983be3`  
		Last Modified: Fri, 21 Feb 2020 03:47:40 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2632faa1250c2a583b0bce0117142113c1f1f855634f409608f981ec5762cf`  
		Last Modified: Fri, 21 Feb 2020 03:47:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ade26bc4872033bb2fe0d73c73bc2adb6a56924004f7fb95b71c93af407285`  
		Last Modified: Fri, 21 Feb 2020 03:48:40 GMT  
		Size: 56.1 MB (56086613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3385395b5491c75b380ee7aed9fb5c970b037e004306a5b7301d991bc1725dba`  
		Last Modified: Fri, 21 Feb 2020 03:48:24 GMT  
		Size: 7.6 KB (7573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d725a856454b2ded5b98206c6af391ab9312720f60f1df1153b66d497e3b36`  
		Last Modified: Fri, 21 Feb 2020 03:48:24 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f02b94572b9ba4b1afb72966b698da25d1d2fe7fa9fd89c90ec63d78e5ec79`  
		Last Modified: Fri, 21 Feb 2020 03:48:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a0a322a1448469b38d69993090b4f267dcc85abe01909015d284ac9cd3cc82`  
		Last Modified: Fri, 21 Feb 2020 03:48:24 GMT  
		Size: 4.2 KB (4217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d338789e1bac2a731f8431eee1aa7524abb08e672e3c33fa50a9ed4ba753e9c`  
		Last Modified: Fri, 21 Feb 2020 03:48:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; 386

```console
$ docker pull postgres@sha256:f68ad1683e78f53fff65bd1c0a080f7a07cf8c0a0bdb109f961c0b932e6a4be2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62422653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87815bcadfdfdddcab4762c311221f94442a0945c506c01f2031454d148639d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 18 Jan 2020 01:38:44 GMT
ADD file:381b617b92fe699ad4ef4f30e0d9599f89e43e252883348c420ebe2a0cccbd63 in / 
# Sat, 18 Jan 2020 01:38:45 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2020 03:30:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 21 Feb 2020 03:30:16 GMT
ENV LANG=en_US.utf8
# Fri, 21 Feb 2020 03:30:18 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 03:42:04 GMT
ENV PG_MAJOR=11
# Fri, 21 Feb 2020 03:42:05 GMT
ENV PG_VERSION=11.7
# Fri, 21 Feb 2020 03:42:05 GMT
ENV PG_SHA256=324ae93a8846fbb6a25d562d271bc441ffa8794654c5b2839384834de220a313
# Fri, 21 Feb 2020 03:51:44 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Fri, 21 Feb 2020 03:51:45 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 21 Feb 2020 03:51:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 21 Feb 2020 03:51:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 21 Feb 2020 03:51:47 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 21 Feb 2020 03:51:47 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 21 Feb 2020 03:51:47 GMT
COPY file:fa1ca76844f23c5beb98bdf3620414d012eb44eabdb324f0cce0bd5b0b913477 in /usr/local/bin/ 
# Fri, 21 Feb 2020 03:51:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 03:51:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 03:51:48 GMT
EXPOSE 5432
# Fri, 21 Feb 2020 03:51:49 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f024b1263dc58db07a458b73ae1a2dca02ca55bef1ccd1fa3fd50656551fadf2`  
		Last Modified: Sat, 18 Jan 2020 01:39:18 GMT  
		Size: 2.8 MB (2806560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959a23ad99210023932b0a65eae572206908695baed873ef3d83466df1b9ef9f`  
		Last Modified: Fri, 21 Feb 2020 04:13:10 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7b6dcfa29bbafa44252daa9ebfba486bf13fd4e291a15a1212477d86c8e69d`  
		Last Modified: Fri, 21 Feb 2020 04:13:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d2185a4381904a5c5e09c6843df3390b5fec2a929ffc012e750518d6296bce`  
		Last Modified: Fri, 21 Feb 2020 04:14:53 GMT  
		Size: 59.6 MB (59602528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0021b1f7245c8a3e493e9c02196951fc022a611b9d722cf90a62d686733ea616`  
		Last Modified: Fri, 21 Feb 2020 04:14:28 GMT  
		Size: 7.6 KB (7570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8048d71350e0e6baea0db7a9a9e9459188fa78ba9d95602312edca315a05c895`  
		Last Modified: Fri, 21 Feb 2020 04:14:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c7246d80ab289b648f1f78c1aae8ce865ef205df6ae1f9683a5d8ef22c8109`  
		Last Modified: Fri, 21 Feb 2020 04:14:28 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977f8296e2e6eb075ef1e58ec4172f932fa9a7bd00833a5b74153d1c0d3b5787`  
		Last Modified: Fri, 21 Feb 2020 04:14:28 GMT  
		Size: 4.2 KB (4216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1beea41223e42d47570964897ca4c15aeff33a32d1f8b9c614694c886185d26`  
		Last Modified: Fri, 21 Feb 2020 04:14:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:e4c4579f169ca8edb7642fd261c092df630c4e9a031e2010278704ed9285c359
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61457028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5594d31959e38f282b99d31b404e630a89cd5e6017b6c133a09295ba9d74c5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 18 Jan 2020 02:20:41 GMT
ADD file:32ddb3d5255071cca51573ceee2464dd5a87c8d1cce514ae965b6e824d9ef24b in / 
# Sat, 18 Jan 2020 02:20:45 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2020 02:55:02 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 21 Feb 2020 02:55:06 GMT
ENV LANG=en_US.utf8
# Fri, 21 Feb 2020 02:55:21 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 03:08:23 GMT
ENV PG_MAJOR=11
# Fri, 21 Feb 2020 03:08:26 GMT
ENV PG_VERSION=11.7
# Fri, 21 Feb 2020 03:08:30 GMT
ENV PG_SHA256=324ae93a8846fbb6a25d562d271bc441ffa8794654c5b2839384834de220a313
# Fri, 21 Feb 2020 03:13:11 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Fri, 21 Feb 2020 03:13:24 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 21 Feb 2020 03:13:33 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 21 Feb 2020 03:13:36 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 21 Feb 2020 03:13:49 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 21 Feb 2020 03:13:55 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 21 Feb 2020 03:14:00 GMT
COPY file:fa1ca76844f23c5beb98bdf3620414d012eb44eabdb324f0cce0bd5b0b913477 in /usr/local/bin/ 
# Fri, 21 Feb 2020 03:14:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 03:14:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 03:14:13 GMT
EXPOSE 5432
# Fri, 21 Feb 2020 03:14:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cd95c8a93e39dcaa0634a65d5b86a88bcd5c3092adb1f96504a7030faa165123`  
		Last Modified: Sat, 18 Jan 2020 02:21:25 GMT  
		Size: 2.8 MB (2822125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487dbfc4a657c93ce517fa99806761e43b8d02d8f87262b7d2bcdf1d03bc2a4d`  
		Last Modified: Fri, 21 Feb 2020 03:41:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6192d48972b2e6f74c26a885c0b2d2f1f9842f20efaf6e14a2fcb5baf7eb6672`  
		Last Modified: Fri, 21 Feb 2020 03:41:25 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4c143dc2c25f1ee9a205621255409aedca65407eb1ba471ed213a83831c05f`  
		Last Modified: Fri, 21 Feb 2020 03:42:34 GMT  
		Size: 58.6 MB (58621218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fe21285a1b1018504d1704e172e0b40eff886bb747d6c9bb797aab07a9e003`  
		Last Modified: Fri, 21 Feb 2020 03:42:18 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cde823c3b30f2ed40fbc16862dde38e3afd1f2a5103b9a1cb25dd0c7e06bd26`  
		Last Modified: Fri, 21 Feb 2020 03:42:18 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6697882af3e8afbbb6fbcc4344930cba641ebbd5f6ba74400e4039330dd73d25`  
		Last Modified: Fri, 21 Feb 2020 03:42:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521cf9bfbb09934aebe7361ac37f6a78cf2780d643eff8f4e5ee1d35da5cb88e`  
		Last Modified: Fri, 21 Feb 2020 03:42:18 GMT  
		Size: 4.2 KB (4216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199faed2b3fdd1d2593ee842948f36209c4c598792100b1e41592441fd89dfa4`  
		Last Modified: Fri, 21 Feb 2020 03:42:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:72ceac7f4688c868e413889fe9e77acbf75888837cb37637fe4577d954080264
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61181069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c373a80e3c023d2288854a69da089951c4372471f837880d786bea59e1b73b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 18 Jan 2020 01:41:33 GMT
ADD file:a6f8b7d4ba199527053ef1ac710b5e318135cb6903cb9ad6fae4fe42e6ad0bf7 in / 
# Sat, 18 Jan 2020 01:41:33 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2020 00:18:10 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 21 Feb 2020 00:18:10 GMT
ENV LANG=en_US.utf8
# Fri, 21 Feb 2020 00:18:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 00:36:43 GMT
ENV PG_MAJOR=11
# Fri, 21 Feb 2020 00:36:44 GMT
ENV PG_VERSION=11.7
# Fri, 21 Feb 2020 00:36:44 GMT
ENV PG_SHA256=324ae93a8846fbb6a25d562d271bc441ffa8794654c5b2839384834de220a313
# Fri, 21 Feb 2020 00:42:56 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Fri, 21 Feb 2020 00:43:05 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 21 Feb 2020 00:43:07 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 21 Feb 2020 00:43:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 21 Feb 2020 00:43:10 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 21 Feb 2020 00:43:11 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 21 Feb 2020 00:43:11 GMT
COPY file:fa1ca76844f23c5beb98bdf3620414d012eb44eabdb324f0cce0bd5b0b913477 in /usr/local/bin/ 
# Fri, 21 Feb 2020 00:43:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 21 Feb 2020 00:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 00:43:14 GMT
EXPOSE 5432
# Fri, 21 Feb 2020 00:43:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:176bad61a3a435da03ec603d2bd8f7a69286d92f21f447b17f21f0bc4e085bde`  
		Last Modified: Sat, 18 Jan 2020 01:41:59 GMT  
		Size: 2.6 MB (2582031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351827524ade65a9aeff2700d440f7f2bebfa06e09bfb97a7ac70bca2e59c9bd`  
		Last Modified: Fri, 21 Feb 2020 01:27:44 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb1c51f7255ecf03a8dff2b406f9fe7250980e67bb33cc0837625b64dff486b`  
		Last Modified: Fri, 21 Feb 2020 01:27:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02bf8abf682be7380e3e53a908475e9416577078cf04e594bfdd43b87c19181`  
		Last Modified: Fri, 21 Feb 2020 01:28:38 GMT  
		Size: 58.6 MB (58585368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c49f71d71bc67a87fb635686cbec5a20024ce2f769ced944c4643a2c5765d7`  
		Last Modified: Fri, 21 Feb 2020 01:28:27 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1724b145ebf5a2d15fbb30d01105aad5880d7abeb4a7e4d424d167759cb0b0c5`  
		Last Modified: Fri, 21 Feb 2020 01:28:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e611e96d794306aa53e19085c0b81278afb4f8af0f6b5b8812ddbb929c9dce`  
		Last Modified: Fri, 21 Feb 2020 01:28:43 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1231cf56feba0da40bdb65b95443ea8ba71cb52877368d0baf1eb76af531dc3b`  
		Last Modified: Fri, 21 Feb 2020 01:28:43 GMT  
		Size: 4.2 KB (4212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f62b5559ce4398bc23118fe76d74d36ff60d67252628c872f71cf685849065c`  
		Last Modified: Fri, 21 Feb 2020 01:28:43 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
