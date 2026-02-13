## `postgres:17-alpine3.22`

```console
$ docker pull postgres@sha256:782d30fb9e606675746ad2e743344f3b5e2db0e776c4d89fa97ce4f708fa2301
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
$ docker pull postgres@sha256:a9c2682506d47221b9b6fbe4d9970bc24fea3c6eb75776a1f9e22d4687fc4d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110637598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00adfa46251f5742d60878fb4a017cdc366245c8dc992426ae7193d91ea57798`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:04:17 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:20 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:04:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:04:20 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:04:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:04:20 GMT
ENV PG_MAJOR=17
# Thu, 12 Feb 2026 21:04:20 GMT
ENV PG_VERSION=17.8
# Thu, 12 Feb 2026 21:04:20 GMT
ENV PG_SHA256=a88d195dd93730452d0cfa1a11896720d6d1ba084bc2be7d7fc557fa4e4158a0
# Thu, 12 Feb 2026 21:04:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:06:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:06:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:06:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:06:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:06:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:06:55 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:06:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:06:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:06:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:06:55 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:06:55 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:06:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a443183e4b2fb5f1f02b3cbdf2949bd73da2010cab600d4e6eb136e30391ca91`  
		Last Modified: Thu, 12 Feb 2026 21:07:11 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923f56ee9cf326367a12dd213c93a250a8e2f469f9a9ee89956c7e064548ad42`  
		Last Modified: Thu, 12 Feb 2026 21:07:12 GMT  
		Size: 918.3 KB (918287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ba1a64d641014a265a3390776b3bd296e7d247ad188f3a8f9d9739b4c42937`  
		Last Modified: Thu, 12 Feb 2026 21:07:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d876ae877d7dbcaf62d4364bef909ae7a878073fcd257bfd41c4ae514aea5216`  
		Last Modified: Thu, 12 Feb 2026 21:07:14 GMT  
		Size: 105.9 MB (105897074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696d9aeafc0248be9ff00fd78d618c18142a8505a71fe0dcc51296afb8f2256f`  
		Last Modified: Thu, 12 Feb 2026 21:07:12 GMT  
		Size: 10.0 KB (9952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967f7cdfcd31905b32f8f63b123ba25438567d15c989e8d0c1b6a159ecb9a6b8`  
		Last Modified: Thu, 12 Feb 2026 21:07:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4490cfb67d819ed64d69218207c9555327f728a0757fd21ec75a7bf5d2bcb5c`  
		Last Modified: Thu, 12 Feb 2026 21:07:13 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cedc1aea34c2fc850982ae0645be4e9cb18e6a9708c607d7d0319bb728a1d64`  
		Last Modified: Thu, 12 Feb 2026 21:07:14 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c356c1e5e851333bb134656678f44dfbce2baa1911996e0ff11d2ecbacde1a0`  
		Last Modified: Thu, 12 Feb 2026 21:07:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:4fb9b8fa0e2f2375dbbb9ceed135f88ba17d2236adf0c7fcc4bd25cb472a783a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.4 KB (637369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64de490121653d2aea6c4dbfd5c538c167e2f5de17a297b0dd68346337a4d53f`

```dockerfile
```

-	Layers:
	-	`sha256:c7d992a1196d7b937063f383ec2e58a4317572b90b2d99c8f80690eb75c67810`  
		Last Modified: Thu, 12 Feb 2026 21:07:12 GMT  
		Size: 596.3 KB (596311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53c46cf801b7f5defaa0ae187192653f945ffef803b0be782863bf37ca861ef8`  
		Last Modified: Thu, 12 Feb 2026 21:07:11 GMT  
		Size: 41.1 KB (41058 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:7a755bcb34af6dfd34b1af6e80b94de0bf391463fb13d06844dd13f246a230b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90143378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e1be14f030e34729487095fcbc428e88f570ba8bbfe8d04186bfa9ce9ea213`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:21:07 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:21:11 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:21:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:21:11 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:21:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:21:11 GMT
ENV PG_MAJOR=17
# Thu, 12 Feb 2026 21:21:11 GMT
ENV PG_VERSION=17.8
# Thu, 12 Feb 2026 21:21:11 GMT
ENV PG_SHA256=a88d195dd93730452d0cfa1a11896720d6d1ba084bc2be7d7fc557fa4e4158a0
# Thu, 12 Feb 2026 21:21:11 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:24:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:24:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:24:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:24:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:24:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:24:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:24:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:24:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:24:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:24:14 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:24:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:24:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddf1d16d30699f039affc2ad9fcf43ae787daddc82f99e9c5d389f53cdebc09`  
		Last Modified: Thu, 12 Feb 2026 21:24:25 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4852dc38be81d3bb8ba65c26e01c46029cfdfadb837c98f2ab22c20c00fb0422`  
		Last Modified: Thu, 12 Feb 2026 21:24:25 GMT  
		Size: 886.1 KB (886133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88bb109baae3c2a29ca44039528260593f1f171f2cc4343840ed8ec3fd86d0bc`  
		Last Modified: Thu, 12 Feb 2026 21:24:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a0c7c733e36bebc61d03bd58e5445f55ba5a2335d61e78bab1a853bb1a1f69`  
		Last Modified: Thu, 12 Feb 2026 21:24:27 GMT  
		Size: 85.7 MB (85734841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b4ce1984c70580dc5d211e9b54e65d93383e65c370d56916e14a35a52e697f`  
		Last Modified: Thu, 12 Feb 2026 21:24:26 GMT  
		Size: 10.0 KB (9952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fb4b917a264736b905f39635f59a3d1e2784e96a5e24c5bb93098a28896220`  
		Last Modified: Thu, 12 Feb 2026 21:24:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d30deea788266aa97ede062721a75b7ca67f1df0c17aad4adce56fe1ae7e1c3`  
		Last Modified: Thu, 12 Feb 2026 21:24:26 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d06e78ddaa06c2457142979b1f4332ab3f7b86401e509831164acffec2dbef`  
		Last Modified: Thu, 12 Feb 2026 21:24:27 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e488151c90036b3aec6b54789ee2ccc6e7645458ee0b35b3a9c091653c8eb5c7`  
		Last Modified: Thu, 12 Feb 2026 21:24:27 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:87165ee0192d03b6514901603604072ec67915071fd75053880b1526831b18d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 KB (40992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a01d65d23718d32e6624cecdb23d95b8444903e4bce8471fb4c3a998a1db9f1`

```dockerfile
```

-	Layers:
	-	`sha256:7dbf115957a1ef5c44e3aa902eebf44b778cc5f63e561bfe54e845ab45dc3fa8`  
		Last Modified: Thu, 12 Feb 2026 21:24:25 GMT  
		Size: 41.0 KB (40992 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:ff6321252497fe06348a5e713e5238a10631d82cb5d9f3c000911da608b923ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85393155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c49543041c1dcc0002e5d697398b7fe8b270bbe5510e2f64598f0ca83d44dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:22:19 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:22:23 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:22:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:22:23 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:22:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:22:23 GMT
ENV PG_MAJOR=17
# Thu, 12 Feb 2026 21:22:23 GMT
ENV PG_VERSION=17.8
# Thu, 12 Feb 2026 21:22:23 GMT
ENV PG_SHA256=a88d195dd93730452d0cfa1a11896720d6d1ba084bc2be7d7fc557fa4e4158a0
# Thu, 12 Feb 2026 21:22:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:25:27 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:25:27 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:25:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:25:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:25:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:25:27 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:25:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:25:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:25:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:25:27 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:25:27 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:25:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544b2cfe58c6e37a8be5862cda197045c966ffaca210b0bced468b6475462b55`  
		Last Modified: Thu, 12 Feb 2026 21:25:39 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb35e1f8433756296cc8556b9d94ccb414bf24b249869ef192de1c276dbf791c`  
		Last Modified: Thu, 12 Feb 2026 21:25:39 GMT  
		Size: 886.1 KB (886136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6dcb90edc1eca532947f4f9c93005b3807635684b2ac9d47703b50958ead94`  
		Last Modified: Thu, 12 Feb 2026 21:25:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9e08de5c49a2c181d1c16e3b21e4d46f4fdddf3c0ea61a9dc8953a8d2d507c`  
		Last Modified: Thu, 12 Feb 2026 21:25:41 GMT  
		Size: 81.3 MB (81266026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e33c9c9a1079f9a37bc075d9a4542752055689104d09434745b7b67e79f049b`  
		Last Modified: Thu, 12 Feb 2026 21:25:40 GMT  
		Size: 10.0 KB (9952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329e7af0b30ae5aed0986f3fb09949480783a0677d6900bb56671f2b02807542`  
		Last Modified: Thu, 12 Feb 2026 21:25:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0a192c5a1d3c03046b19e2f64332ed7f9866f023c05ccd52b403e6e481ee6e`  
		Last Modified: Thu, 12 Feb 2026 21:25:40 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20690a0e1a895be2e4174c342081ae145d9a54316a1b4550b316c9acaab25c0`  
		Last Modified: Thu, 12 Feb 2026 21:25:41 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb7fc529616643d572daca11d8ab0db8f9971b76fa980b917cb6b61ee217851`  
		Last Modified: Thu, 12 Feb 2026 21:25:41 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:7abf4b6bc8f358897054f9a102cb9b32307850e42223d949ca06e3b19d38c353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.5 KB (637538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045c4563a3a585a67d2bf9efb41e3a3bb292e5ec90cc69af8736b252e323a038`

```dockerfile
```

-	Layers:
	-	`sha256:0c34b4dbc75b8f75278778739becd41514a7f19b12706bc48ebf3509c630fa61`  
		Last Modified: Thu, 12 Feb 2026 21:25:39 GMT  
		Size: 596.3 KB (596331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23db9ac80dac14dc4cbb6521c4dba734a522158540f9e5eb83db08abac44c935`  
		Last Modified: Thu, 12 Feb 2026 21:25:39 GMT  
		Size: 41.2 KB (41207 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:74d738e56f45555b09496531d2cb67a7fa1b60bb848a36e9e1203ae02534b082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106581063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a91333312598634c7a9d8bb895e6d7a77566ad4e836e3ea8bcfa820a73c12d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:04:22 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:04:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:04:25 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:04:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:04:26 GMT
ENV PG_MAJOR=17
# Thu, 12 Feb 2026 21:04:26 GMT
ENV PG_VERSION=17.8
# Thu, 12 Feb 2026 21:04:26 GMT
ENV PG_SHA256=a88d195dd93730452d0cfa1a11896720d6d1ba084bc2be7d7fc557fa4e4158a0
# Thu, 12 Feb 2026 21:04:26 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:07:11 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:07:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:07:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:07:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:07:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:07:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:07:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:07:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:07:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:07:11 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:07:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:07:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3990b1f3bcfa2411e2b3066a925ef4e9ccb48f3cffe71ba70dcaffdff1bb4604`  
		Last Modified: Thu, 12 Feb 2026 21:07:26 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59693c4dc7d0c2881bd87820dfe5c68cfc5f5dc6ddc6c7ce796f387a02650913`  
		Last Modified: Thu, 12 Feb 2026 21:07:26 GMT  
		Size: 873.5 KB (873483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daa55d920625364415c0b1c8fb59d925ea865b6288b336fc75f2dbf655af1fc`  
		Last Modified: Thu, 12 Feb 2026 21:07:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5613b6969245b3facb95f2e51fee4746d0e425dc1f9b867597d80c1aee965e14`  
		Last Modified: Thu, 12 Feb 2026 21:07:29 GMT  
		Size: 101.6 MB (101550708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17e808095714e43e69cf5a18d60dea72f8f3203b6d3cc38f5ebba595e450339`  
		Last Modified: Thu, 12 Feb 2026 21:07:27 GMT  
		Size: 9.9 KB (9950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba29a6539713e8c07bb264f958a566bf63e98d43dd7d2fe714e468fa2fffa4c0`  
		Last Modified: Thu, 12 Feb 2026 21:07:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0d11cefd2e06cc4e75082a61bf06b25b294d6f3f6213ae7f0eb6189399ccd6`  
		Last Modified: Thu, 12 Feb 2026 21:07:28 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1d80e48964f0ecb970bb92870319400e1d2b72399753cd7b2d98185931edfe`  
		Last Modified: Thu, 12 Feb 2026 21:07:28 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e3fdf56ce47cdec04e910150d2dfb3b6c3f68f756b7a312dbc0f4a8ed7d633`  
		Last Modified: Thu, 12 Feb 2026 21:07:28 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:e6aed31feba94ff34639b110353a20bab0acbbd3b6437359a36913fb62b98f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.6 KB (637583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36af842ec32a7839b591f21c2b2fcfbab24c39f0d30281e3fb626301c80d0e16`

```dockerfile
```

-	Layers:
	-	`sha256:bba1ff07b9fb008b020d4e73c14906c52dfe625bfa5d5631f7208424749712e4`  
		Last Modified: Thu, 12 Feb 2026 21:07:26 GMT  
		Size: 596.3 KB (596343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cfd779d3531aa58b7a2d981d9202ed7e529205428166f46d0f0e38af9cda0c6`  
		Last Modified: Thu, 12 Feb 2026 21:07:26 GMT  
		Size: 41.2 KB (41240 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:8de6d405eb3cb0d98fbd9fa161f1ad5ed2f16973b579d15d1edd7df9995f4171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116912447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01dc7363d59f8f1b28033c7a96d0239869ac187d9781cfc758292e5a1586f38a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:04:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:51 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:04:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:04:51 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:04:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:04:51 GMT
ENV PG_MAJOR=17
# Thu, 12 Feb 2026 21:04:51 GMT
ENV PG_VERSION=17.8
# Thu, 12 Feb 2026 21:04:51 GMT
ENV PG_SHA256=a88d195dd93730452d0cfa1a11896720d6d1ba084bc2be7d7fc557fa4e4158a0
# Thu, 12 Feb 2026 21:04:51 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:07:33 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:07:33 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:07:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:07:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:07:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:07:33 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:07:33 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:07:33 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:07:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:07:33 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:07:33 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:07:33 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cb2785331ceab96ffc69fbb63d69267360159dbcda2b82b2dc4778b4f83506`  
		Last Modified: Thu, 12 Feb 2026 21:07:49 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4786d552c9b9649928b333af0c9fc7e8e6cc239eee5e6d2fccaa391c5ef1c8`  
		Last Modified: Thu, 12 Feb 2026 21:07:49 GMT  
		Size: 890.6 KB (890635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e46e455d3b6e2afda6cdabd64609577eee48201d09db8fc9e2f90a3c341e5d`  
		Last Modified: Thu, 12 Feb 2026 21:07:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce725e172fd656abca0228add0bf8a289b6c3e830dd932077a22297ccdf19ed`  
		Last Modified: Thu, 12 Feb 2026 21:07:52 GMT  
		Size: 112.4 MB (112383720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a5182fae6e3e06eb5257407e5de6867582ab455b11a1bb75fd9bee1f39e13c`  
		Last Modified: Thu, 12 Feb 2026 21:07:50 GMT  
		Size: 10.0 KB (9952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e0110439913693a789643fe9cf54d9bbc0229f71a6e3ab0b9c13087ba3790e`  
		Last Modified: Thu, 12 Feb 2026 21:07:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab234997642d9397e4a54a757672ece71c303b84d65278c6830e43992a1e67ed`  
		Last Modified: Thu, 12 Feb 2026 21:07:51 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d760b307fe04ca5c09a50c6c06e1f47e7eba02396af67b194aaed195a92c931`  
		Last Modified: Thu, 12 Feb 2026 21:07:51 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd434b4b6e3be80c151fc187866dc302406eeddee3b6744fc82600076979eee3`  
		Last Modified: Thu, 12 Feb 2026 21:07:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:ca12e4288033248779289ffa0b1b112922613c7e9269f99477f481bf88549cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.3 KB (637318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071e65460fc24c33fac3793a0e93eda6e470f85b8a9077fe4cae459fc4ca4d84`

```dockerfile
```

-	Layers:
	-	`sha256:635afa52f998d026903876ce8702fab8cf635c672fddb9d06889ff689d129829`  
		Last Modified: Thu, 12 Feb 2026 21:07:49 GMT  
		Size: 596.3 KB (596296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6339407f8951ef34d82e88473ffff22e68f9dabcc521bc8085fe26f4a60f474`  
		Last Modified: Thu, 12 Feb 2026 21:07:49 GMT  
		Size: 41.0 KB (41022 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:cd7d70329508bf6b9fc049fd8fa2850a1f290c95dbeb4167a41fa34e71d27b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94474386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccca3ffbd5c7d77e28eab07aca7e4f4d7e9dbf3d8e738189b581e12a7b3eeff4`
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
# Thu, 12 Feb 2026 21:06:12 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:06:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:06:12 GMT
ENV PG_MAJOR=17
# Thu, 12 Feb 2026 21:06:12 GMT
ENV PG_VERSION=17.8
# Thu, 12 Feb 2026 21:06:12 GMT
ENV PG_SHA256=a88d195dd93730452d0cfa1a11896720d6d1ba084bc2be7d7fc557fa4e4158a0
# Thu, 12 Feb 2026 21:06:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:18:05 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:18:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:18:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:18:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:18:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:18:09 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:18:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:18:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:18:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:18:11 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:18:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:18:11 GMT
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
	-	`sha256:bb8773caba0cc71f1241c5d1fb6e8c3b7afa6a89200a7975c71ffbf3112756a3`  
		Last Modified: Thu, 12 Feb 2026 21:11:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767bb3efa7dbb61022f8fcf57f629ad533c642b821f27b2e34831f492f1db629`  
		Last Modified: Thu, 12 Feb 2026 21:18:49 GMT  
		Size: 89.8 MB (89843680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d096194525ac92b54a7c7e014d619c36a7e45212a984840a952da987c7c90658`  
		Last Modified: Thu, 12 Feb 2026 21:18:46 GMT  
		Size: 10.0 KB (9957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58175dd9f85bf7cab9f3a60a37bf85f17f2a2c8c4e90c68e1114ac7a65c462dd`  
		Last Modified: Thu, 12 Feb 2026 21:18:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b334b024ff73f8d8fe8334f1d7407bca7897a8e3cff89b8e16f2ffe2646a58`  
		Last Modified: Thu, 12 Feb 2026 21:18:46 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7372cb5c6eef14c589e5952ad1bfbc9360ad3796bf773c16402a718727892db`  
		Last Modified: Thu, 12 Feb 2026 21:18:47 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d7f2c7e6d1bfd6b45bd9efae9ec8e7b740dced7504fd8226b5e5e7c02b88ac`  
		Last Modified: Thu, 12 Feb 2026 21:18:48 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:258acf66c1ac5f1f6bd67f768fed818cd747ca26ffa1b76e689420a9a30e748a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.8 KB (633818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11341cb9d452bf462dc8f510fcd885805f9f282c128febf4242d2458736526a0`

```dockerfile
```

-	Layers:
	-	`sha256:0839b97c5ab56edce44170cb9935399bdefcf7491ca90b16c4eaabefbb7bd41f`  
		Last Modified: Thu, 12 Feb 2026 21:18:46 GMT  
		Size: 592.7 KB (592720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8399f3a59f91c2c82aac43d0095dcd51f9857a74a35df3b361076ae63429f73a`  
		Last Modified: Thu, 12 Feb 2026 21:18:46 GMT  
		Size: 41.1 KB (41098 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:2803a449ccc9b995ed1e9b77396e3fc776edfcab21f130972b603124823c00c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110717154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8feb106a4b07dd7341e34fe852ef43dcb60367d977b3bbc7496d017dd7e2bddc`
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
# Fri, 13 Feb 2026 00:03:22 GMT
ENV LANG=en_US.utf8
# Fri, 13 Feb 2026 00:03:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 13 Feb 2026 00:03:22 GMT
ENV PG_MAJOR=17
# Fri, 13 Feb 2026 00:03:22 GMT
ENV PG_VERSION=17.8
# Fri, 13 Feb 2026 00:03:22 GMT
ENV PG_SHA256=a88d195dd93730452d0cfa1a11896720d6d1ba084bc2be7d7fc557fa4e4158a0
# Fri, 13 Feb 2026 00:03:22 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 13 Feb 2026 04:57:18 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 13 Feb 2026 04:57:19 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 13 Feb 2026 04:57:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 13 Feb 2026 04:57:19 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 13 Feb 2026 04:57:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 13 Feb 2026 04:57:20 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 13 Feb 2026 04:57:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 04:57:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 13 Feb 2026 04:57:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Feb 2026 04:57:20 GMT
STOPSIGNAL SIGINT
# Fri, 13 Feb 2026 04:57:20 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 13 Feb 2026 04:57:20 GMT
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
	-	`sha256:778a0da493e5086a70feef9ef732427bd2c927a4c5e0b6cb88e9e6e2f5d4d72a`  
		Last Modified: Fri, 13 Feb 2026 00:55:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed882c52851ab20532dcb6729073cdd421ff7cc0b3abd6d79b94ab47a12810c`  
		Last Modified: Fri, 13 Feb 2026 05:00:27 GMT  
		Size: 106.3 MB (106315725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d07bc178fa1ccdf9e8479c83a467eca0d619128d56f3d840a1fe4c294465ab3`  
		Last Modified: Fri, 13 Feb 2026 05:00:12 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f282504bcbaadf97ec886e84736ece40e32de999ccb4e5c66f79dd8c6d705263`  
		Last Modified: Fri, 13 Feb 2026 05:00:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2851edae6a0b5bc8df32f3a69767f74c3174eeb95bbea61ca43d6a9fc9357`  
		Last Modified: Fri, 13 Feb 2026 05:00:12 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e165fee96f4c61014affff371da4b6b7439b60100384a8dbbf4ef0ecdaac9ce`  
		Last Modified: Fri, 13 Feb 2026 05:00:15 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03ed566975917249da73d94fb9ab9cc4f146c3c4e7385432e66827b66a5c586`  
		Last Modified: Fri, 13 Feb 2026 05:00:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:ad7202dcb4e37e7281f4b917bc7db4276790fb0c1bbba975389d24777c7c95b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.5 KB (635482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06622692c787ff9b4a88f4b7f710087e3d90431b9a4c2c146144d2e7bd1d57b`

```dockerfile
```

-	Layers:
	-	`sha256:936634f51a6280b34773cd2175b680bf7f5a8c1fedad4debcb430092b0018504`  
		Last Modified: Fri, 13 Feb 2026 05:00:12 GMT  
		Size: 594.4 KB (594378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f5d9f4eae494e1923162bb683b6524ea5e5abe792802b306e31ad661ce2952`  
		Last Modified: Fri, 13 Feb 2026 05:00:10 GMT  
		Size: 41.1 KB (41104 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:ba6e39b689fe8847c4aefcdf0a09cfed1c1483e746f6c3dbd85f2179758f94f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119354824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c1ff61e335b33f8a5a7b783edbcc22f0d09b7b2a7b087cf60cf953ef479851`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:02:33 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:02:37 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:02:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:02:37 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:02:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:02:38 GMT
ENV PG_MAJOR=17
# Thu, 12 Feb 2026 21:02:38 GMT
ENV PG_VERSION=17.8
# Thu, 12 Feb 2026 21:02:38 GMT
ENV PG_SHA256=a88d195dd93730452d0cfa1a11896720d6d1ba084bc2be7d7fc557fa4e4158a0
# Thu, 12 Feb 2026 21:02:38 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:20:59 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:20:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:20:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:20:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:20:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:20:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:20:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:20:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:20:59 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:20:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:20:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de5ab441dabb81e9ca143b33f430fcde023e7641b4434052405ebb7c2c0434e`  
		Last Modified: Thu, 12 Feb 2026 21:06:17 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a1da40c4ec0399caebc58e7630eee7f84ed9d37fc332bef6e8ad2882c4e04b`  
		Last Modified: Thu, 12 Feb 2026 21:06:17 GMT  
		Size: 894.4 KB (894409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17aa5adf39a06c5e976f41a2e570538eeee2fa378dc20c16fd22fd3debc2a26d`  
		Last Modified: Thu, 12 Feb 2026 21:06:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe2237a432cba06039b7117dab78568855f7e33924b6161b81cac4fe1057df4`  
		Last Modified: Thu, 12 Feb 2026 21:21:26 GMT  
		Size: 114.8 MB (114792622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16a3d902d8c89fd555051f2e459d368679bac7641eba4f1a151425857b96f20`  
		Last Modified: Thu, 12 Feb 2026 21:21:23 GMT  
		Size: 10.0 KB (9951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63090b48f2bae3d019871f453a8031445e8b654c0c45bba879f58c6da83fd443`  
		Last Modified: Thu, 12 Feb 2026 21:21:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c95b4f991527636755b12821bf11977aa23124f03edd7d72caa9c41e47b245`  
		Last Modified: Thu, 12 Feb 2026 21:21:23 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117cd9b753b143768888206ba396ab9a27c0317086ff3138e2d73bc24b4489d5`  
		Last Modified: Thu, 12 Feb 2026 21:21:24 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ed17e023693d8ab5876afe4e6b43227bbcfeb9df03f8b720b6de95ff268ee9`  
		Last Modified: Thu, 12 Feb 2026 21:21:24 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:93ff60178ae74c9ab8ec518778a28fa2f64c800233d81db3fb9fe2cd678b5062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.4 KB (635418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73bce3399215788852f00ce72f106c4bef463fe1a321d8ae2c6a50a391ff6e0d`

```dockerfile
```

-	Layers:
	-	`sha256:4d7c24dd4a450ff5665ee954c56729af4388dc61fae2da59c7920cb15bdd533b`  
		Last Modified: Thu, 12 Feb 2026 21:21:23 GMT  
		Size: 594.4 KB (594360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5040365e39aa5b2c283e9c713ed880cff5a6e757676a0d69b4df784c506ab47`  
		Last Modified: Thu, 12 Feb 2026 21:21:23 GMT  
		Size: 41.1 KB (41058 bytes)  
		MIME: application/vnd.in-toto+json
