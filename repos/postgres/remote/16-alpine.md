## `postgres:16-alpine`

```console
$ docker pull postgres@sha256:23e88eb049fd5d54894d70100df61d38a49ed97909263f79d4ff4c30a5d5fca2
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

### `postgres:16-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:6dfa5b099f5fa9290aa16eb857abee8176e4d150156916745fed867335fa93fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109958567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97fe41a065781e884f8a23fd3dfd04c3348ce02d7a7c5cb2c0645317b4eb663`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:37:22 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 00:37:24 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 00:37:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 00:37:25 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 18 Dec 2025 00:37:25 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 00:37:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 00:37:25 GMT
ENV PG_MAJOR=16
# Thu, 18 Dec 2025 00:37:25 GMT
ENV PG_VERSION=16.11
# Thu, 18 Dec 2025 00:37:25 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Thu, 18 Dec 2025 00:37:25 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 00:39:38 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 00:39:38 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 00:39:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 00:39:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Dec 2025 00:39:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 18 Dec 2025 00:39:38 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Dec 2025 00:39:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:39:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 00:39:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:39:38 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 00:39:38 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 00:39:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e5feb410e895a1fd0e7a9121fe24ffca666de333d3cde8f9d18946014f97df`  
		Last Modified: Thu, 18 Dec 2025 00:39:54 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3048a283a43359eaef3a7a922cb39eb67377b94a7a35f45ac6bab59b3b724a89`  
		Last Modified: Thu, 18 Dec 2025 00:39:55 GMT  
		Size: 922.9 KB (922932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe79fe4410f2109f6d488a84a4450deb1b023cbec56a6cb56ddd501ca9948ea`  
		Last Modified: Thu, 18 Dec 2025 00:40:02 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137ed19c6b800208bcec468e732d4aecaaee30bfdc062b4fe3fe78cc17899630`  
		Last Modified: Thu, 18 Dec 2025 00:40:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b8e529965a96239f30cf08cecdb9003b7ac17ec468b7810de37b18d4dab47c`  
		Last Modified: Thu, 18 Dec 2025 00:40:27 GMT  
		Size: 105.2 MB (105158394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfb940eb8240471f343f971e55f53164dc9e560dd66834b48e5bb439b563c87`  
		Last Modified: Thu, 18 Dec 2025 00:40:02 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76f2995a422088f3088f8aaaa26dbbdf95383183150e11421480c1dce735cd2`  
		Last Modified: Thu, 18 Dec 2025 00:39:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9582264a43c03c8993ad34946a2b164d43724efec6b711abfa2b3ea136bcf2b3`  
		Last Modified: Thu, 18 Dec 2025 00:39:56 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a0dfeb7e380b372d3adf99e71b12cb6f2d15d6370f8ccd4f4953272ab71475`  
		Last Modified: Thu, 18 Dec 2025 00:39:56 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb143896d95aee25e2e04c3a42b50d0be54ff7628e03275719f7f458e60089e`  
		Last Modified: Thu, 18 Dec 2025 00:39:57 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:4e66820d50ec48920ec0c207958fd091991d9fb69c6f49430ab69081dd19ffc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.4 KB (642386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab3344fe5c700a54b3ac4535e3081db2ddc47dc8adda634c5e551e8aecc88a9`

```dockerfile
```

-	Layers:
	-	`sha256:fe7002a62779d1de0393842ebc84759038299fbfab8a79dc007f4d6a1c7111d9`  
		Last Modified: Thu, 18 Dec 2025 03:09:30 GMT  
		Size: 598.1 KB (598080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9bc753a885a2a46050f714e05dcaf9f66122b55097814c6077129c7d05bb335`  
		Last Modified: Thu, 18 Dec 2025 03:09:30 GMT  
		Size: 44.3 KB (44306 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:ddc332ae7bf83d199d88858df11c2907a7bfd86de9967882712d37a07481d5b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89373667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d74f339eac1bea42e5357949a0b73be07bab976ff3c798b579d217ad2107e63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:47:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 00:47:43 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 00:47:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 00:47:43 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 18 Dec 2025 00:47:43 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 00:47:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 00:47:43 GMT
ENV PG_MAJOR=16
# Thu, 18 Dec 2025 00:47:43 GMT
ENV PG_VERSION=16.11
# Thu, 18 Dec 2025 00:47:43 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Thu, 18 Dec 2025 00:47:43 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 00:50:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 00:50:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 00:50:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 00:50:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Dec 2025 00:50:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 18 Dec 2025 00:50:41 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Dec 2025 00:50:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:50:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 00:50:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:50:41 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 00:50:41 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 00:50:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc201af4387628eb008cccdeceeafd090ab6a6754f4eb6d71ccad24e925ad031`  
		Last Modified: Thu, 18 Dec 2025 00:50:59 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225a0bc2db896905cefa6f3935fe428e9b3254a064ccb5b28d58c258f4e857fd`  
		Last Modified: Thu, 18 Dec 2025 00:50:51 GMT  
		Size: 889.5 KB (889469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a14a3b823bc2f7cb45ce4f0552351874161079615436c98dcf7740c0733836e`  
		Last Modified: Thu, 18 Dec 2025 00:50:59 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f81b1d221d6f4a7608fba149d225e8771e7c563b63a1a84ee913f15ac2f161`  
		Last Modified: Thu, 18 Dec 2025 00:50:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ca1d123ac3c105aefef26034e1226a6d6b54dd11ba240d83e184e680b4d16`  
		Last Modified: Thu, 18 Dec 2025 00:50:54 GMT  
		Size: 84.9 MB (84898629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c371c97856a3ee918302f7565cc90ddea89749a383f2456f4f9a821a63038c95`  
		Last Modified: Thu, 18 Dec 2025 00:50:52 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7919a7be21961bfb6b9ff1d83727379d3c219fe1665def8c1fa1d96f68167e68`  
		Last Modified: Thu, 18 Dec 2025 00:50:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eaafd8b69165fc5b50c427c3ba1ed92f855de90804097ad4ef67c797a44c49d`  
		Last Modified: Thu, 18 Dec 2025 00:51:00 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d247a9068eb92459deffe8f90d3bb3be884c02c27ab775cdb04ab23c51894225`  
		Last Modified: Thu, 18 Dec 2025 00:50:53 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c5c0ba4fe6019b04d42aa2da735fdddd9febd9f8e321792d71c37610ca85df`  
		Last Modified: Thu, 18 Dec 2025 00:51:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:20bbdbf211c68508544792b293937ca45995370380fbb737af5fde978092f993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 KB (44268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6f17f4ffc5e3c0dc3f4f9b2535a20b0cae298d625e6d8933319e431010d099`

```dockerfile
```

-	Layers:
	-	`sha256:c888aa13a7add7332f4d1166023e02431dc73830f6c718711aa4e1b754ac4748`  
		Last Modified: Thu, 18 Dec 2025 03:09:34 GMT  
		Size: 44.3 KB (44268 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:a0e766af2ce024a4db8e1d2981ab926bbd8ab3b3d66939a120cc75eba34f6c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84609717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919f942034d1c073cce279a1e61685939d615e86c0ebc2eb8ad75869ea35b0cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:47:54 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 00:47:57 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 00:47:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 00:47:57 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 18 Dec 2025 00:47:57 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 00:47:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 00:47:57 GMT
ENV PG_MAJOR=16
# Thu, 18 Dec 2025 00:47:57 GMT
ENV PG_VERSION=16.11
# Thu, 18 Dec 2025 00:47:57 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Thu, 18 Dec 2025 00:47:57 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 00:50:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 00:50:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 00:50:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 00:50:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Dec 2025 00:50:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 18 Dec 2025 00:50:44 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Dec 2025 00:50:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:50:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 00:50:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:50:45 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 00:50:45 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 00:50:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d355e81a1fa0e7bdd5bbdd44def4dd9dc47919dbf2302226b52184d55f229a6`  
		Last Modified: Thu, 18 Dec 2025 00:51:06 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113b27d50258e53d9e7010ef7735b9902122dc1063140e544ad31886778c6669`  
		Last Modified: Thu, 18 Dec 2025 00:50:57 GMT  
		Size: 889.5 KB (889515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2507d9fdf567cdf2c6a72c3cf22cff66cb98399d3bf47886d51203acd03ac11f`  
		Last Modified: Thu, 18 Dec 2025 00:51:06 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0496b21367875838dd236ee373a228c81afd4fc77ea87bf2e35f808c789bffdb`  
		Last Modified: Thu, 18 Dec 2025 00:51:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097c231a77dc8f5008e971695b16a9c4e49a3c4fcf5f23c436eaad95ec41c7a3`  
		Last Modified: Thu, 18 Dec 2025 00:51:00 GMT  
		Size: 80.4 MB (80423679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c829b76cfe97c19490af4ffdd1053d1b1ae69381c3a21e79a6d1c1d98197f94e`  
		Last Modified: Thu, 18 Dec 2025 00:51:06 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fafdff694da31d1f1c7cba97b56b736ddcda8ebd417d45cd8784dae6d6eaaf`  
		Last Modified: Thu, 18 Dec 2025 00:51:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebefecc64fda27f0faf4017bd3c6abc9a9023c4e29932da1acebe12d170e36f`  
		Last Modified: Thu, 18 Dec 2025 00:51:06 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962ddc05942907239ddfd7e0a99d79ed89d36db828324c20558a065103de17e9`  
		Last Modified: Thu, 18 Dec 2025 00:50:59 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a9a073de0e411b1a23b2ae81f4651dc6e34b9751392912e6dac8fe7c937741`  
		Last Modified: Thu, 18 Dec 2025 00:50:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:8cf3f61cba9e3f5585cdc2bf3a4ed3d860c05abe745e657cbd923bd404731b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.0 KB (641950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e55c6b6079f5a84951a0a793cb2c208d1732e1f1e620157eff13f47f1cdf03`

```dockerfile
```

-	Layers:
	-	`sha256:f0237f1c29f31f54462416e041e1f5606d8b11402dbbeff48cba3b8774ad449d`  
		Last Modified: Thu, 18 Dec 2025 00:50:57 GMT  
		Size: 597.5 KB (597466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:325e3f8678bea911ca58e9d0c50668e54aab1c0e0f219c878bb6c730ef0bc74f`  
		Last Modified: Thu, 18 Dec 2025 03:09:38 GMT  
		Size: 44.5 KB (44484 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:a0e2f138c3483cb0c8a3dab36dce43eadf0224e93d0cf7115f24d8aa305ea33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108126298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d32048ee4d8d41201412687a485bf2da8b11aab309369cca3fbdf30f8ceab76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:37:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 00:37:23 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 00:37:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 00:37:23 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 18 Dec 2025 00:37:23 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 00:37:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 00:37:23 GMT
ENV PG_MAJOR=16
# Thu, 18 Dec 2025 00:37:23 GMT
ENV PG_VERSION=16.11
# Thu, 18 Dec 2025 00:37:23 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Thu, 18 Dec 2025 00:37:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 00:39:33 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 00:39:33 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 00:39:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 00:39:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Dec 2025 00:39:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 18 Dec 2025 00:39:33 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Dec 2025 00:39:33 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:39:33 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 00:39:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:39:33 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 00:39:33 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 00:39:33 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409f53b105a8e40dbecc9dde288087eea5dae3e80ef0b678c6ea184c3bf426a3`  
		Last Modified: Thu, 18 Dec 2025 00:39:57 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f73330ca75e6687bf1277b084686864ded4270d22b7315204267a8eace2330`  
		Last Modified: Thu, 18 Dec 2025 00:39:57 GMT  
		Size: 876.5 KB (876480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf4b6218dc37eceecedb3519cb0ac0f1a4ff0d5aed3c83231c808893ef13b2d`  
		Last Modified: Thu, 18 Dec 2025 00:39:57 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d26d6c343c295cdcd2b02db84b93fcd69baa3fd0612510418adf9c0d2be9f80`  
		Last Modified: Thu, 18 Dec 2025 00:39:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf4b0abe453ad2197dbc6db3cbb97873a649fccb1c3cee722da7b3660dd0edc`  
		Last Modified: Thu, 18 Dec 2025 00:40:09 GMT  
		Size: 103.0 MB (103036941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c795092f8ce9c9b1d6c285781bc62df6f6d61d21c1117eac513b3e90c5780e58`  
		Last Modified: Thu, 18 Dec 2025 00:39:49 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7215aa7d72dfa2915f33deef4277cdba2cd3b74e240caf73bb51b311ec0da12`  
		Last Modified: Thu, 18 Dec 2025 00:39:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302472f811f67bc71607bbbe20cb6aeb683cb3b98e9dc468eaf776d0c1f9098d`  
		Last Modified: Thu, 18 Dec 2025 00:39:50 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7318a68b4c9c217be51c5dd149068e03a2ffbcc6e7bc422326f6d3ccee9e2e`  
		Last Modified: Thu, 18 Dec 2025 00:39:57 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5ac8f25241c27ccc8e041a17f0ab1b09ef1454b38a2ca4e4ca0585745902cf`  
		Last Modified: Thu, 18 Dec 2025 00:39:51 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:b028ce48b4200bb859dc58bc1cc1ec75ad925dbc1643aa77134159076eda78b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.0 KB (642016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9acb8ec43f6b7ea91fac6d27d7e33947d47bca72af1ec1026dee5cc5eecd61d3`

```dockerfile
```

-	Layers:
	-	`sha256:cd55bbf26114b3130abc514f35a2b97123c44fbf3edbcbb5f04e4efebd12ed7e`  
		Last Modified: Thu, 18 Dec 2025 03:09:41 GMT  
		Size: 597.5 KB (597486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:743c87cb39d31bf809071baa9fd9355c12e81a67d611e38036166a3f8856c4a7`  
		Last Modified: Thu, 18 Dec 2025 03:09:42 GMT  
		Size: 44.5 KB (44530 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; 386

```console
$ docker pull postgres@sha256:0f255deafe99a450cc6e386d4401a7bf4a5c357e1bba4294d19ba91a49fb2ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115977075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148a14d32fe630c55ebff3920255ea3b9b227b92e61e02ba1abd1587b17b80ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:38:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 00:38:18 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 00:38:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 00:38:18 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 18 Dec 2025 00:38:18 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 00:38:18 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 00:38:18 GMT
ENV PG_MAJOR=16
# Thu, 18 Dec 2025 00:38:18 GMT
ENV PG_VERSION=16.11
# Thu, 18 Dec 2025 00:38:18 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Thu, 18 Dec 2025 00:38:18 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 00:40:49 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 00:40:49 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 00:40:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 00:40:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Dec 2025 00:40:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 18 Dec 2025 00:40:50 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Dec 2025 00:40:50 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:40:50 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 00:40:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:40:50 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 00:40:50 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 00:40:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f6c9c8d66c116e39decfa58ed236586308b7db6d99ef4c76c65da674db1079`  
		Last Modified: Thu, 18 Dec 2025 00:41:06 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea724e8cdf19547906c73e9214ff6e30eee285f91abb99eb73fe3b5c054f91a`  
		Last Modified: Thu, 18 Dec 2025 00:41:15 GMT  
		Size: 893.2 KB (893244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73328678d5d6328632ac6009836049009eacb2e77d145a799a00675a196332d6`  
		Last Modified: Thu, 18 Dec 2025 00:41:15 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb84ea0c0c13c2243a81002bf3cfb5070832595bce5e1a0bd268da1ea7b869d`  
		Last Modified: Thu, 18 Dec 2025 00:41:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a186b8327d516e1c9c47340cbc7c7430a9992acb419d5b7b2fd2556b64e575be`  
		Last Modified: Thu, 18 Dec 2025 00:41:23 GMT  
		Size: 111.4 MB (111380594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db689ab8ffde542053fd99c39625a6b5d9c1090adaa64110069cc9655b1694cd`  
		Last Modified: Thu, 18 Dec 2025 00:41:16 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8dd486ac04221a349aae91b030669be6d8d6899f865e3610f970a1272ca34f`  
		Last Modified: Thu, 18 Dec 2025 00:41:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e68222dc83fb29251b77a6641184d1aa53b2922b4f362b19d134cb198b6a3c3`  
		Last Modified: Thu, 18 Dec 2025 00:41:16 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e41e45df017d34975c78e4ec642a30b1d87e9ae0b160c80fb865e3f71ab451a`  
		Last Modified: Thu, 18 Dec 2025 00:41:16 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a109aa52ec5e21fd349b7eb6b0de6f3bb218a29eccbaff54a83b7cf5e86b0b5d`  
		Last Modified: Thu, 18 Dec 2025 00:41:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:99b663fd3349be16bf0e7e400657cd4e1c192093b4c152674affd8a00adc0bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.3 KB (642312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5e5b5598c075a8bdfaff00055fc7eedcd8b47170df382c1aca783afffd08ba`

```dockerfile
```

-	Layers:
	-	`sha256:e74fd1ad09db315983edd2293d21fdbc05b64029353cd9b6781140bcc6218e5b`  
		Last Modified: Thu, 18 Dec 2025 03:09:45 GMT  
		Size: 598.1 KB (598055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c55a068f59bdb2b6563f4ca340cee974495f9b7d6ef54a3309f1e89413ff3986`  
		Last Modified: Thu, 18 Dec 2025 03:09:46 GMT  
		Size: 44.3 KB (44257 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:d5757c9adfdb2fd5e5541fca603459be4af0e05d02e102c34244f93e5552e876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94863431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14a7d8dd6397806399314c150165bf5e7c353c72a349765c857ed80bb957162`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:23:31 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 01:23:37 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 01:23:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 01:27:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 18 Dec 2025 01:27:15 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 01:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 01:27:15 GMT
ENV PG_MAJOR=16
# Thu, 18 Dec 2025 01:27:15 GMT
ENV PG_VERSION=16.11
# Thu, 18 Dec 2025 01:27:15 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Thu, 18 Dec 2025 01:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 01:30:27 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 01:30:28 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 01:30:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 01:30:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Dec 2025 01:30:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 18 Dec 2025 01:30:30 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Dec 2025 01:30:31 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:30:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 01:30:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 01:30:32 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 01:30:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 01:30:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff80bfb816c7f5a841f48ccc8340de9f38d3ad53202d1114a5d309378c7e4c`  
		Last Modified: Thu, 18 Dec 2025 01:27:00 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a7bf1ce9f177344350a6b5de388d3492ef2eee83822d55eb5653a1e893a773`  
		Last Modified: Thu, 18 Dec 2025 01:27:00 GMT  
		Size: 881.5 KB (881524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef3774e02f66275039ec450631fe6e5b7c5de5ade853d0353cd9ea07ada7cf2`  
		Last Modified: Thu, 18 Dec 2025 01:31:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164435015427598747f1483897002e9036fe27b49b12766e70cb1efcdbff8e45`  
		Last Modified: Thu, 18 Dec 2025 01:31:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb3b5143919a3ee24cbf89579d27504ec47ef2571f6259c2e757ebe6b2234df`  
		Last Modified: Thu, 18 Dec 2025 01:31:38 GMT  
		Size: 90.1 MB (90137001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26355a2be33ecfc755a5c0866d4f06f7d6fb2c9c1fcc3232dde3b9ed31fa2ce0`  
		Last Modified: Thu, 18 Dec 2025 01:31:21 GMT  
		Size: 9.6 KB (9568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c38fd4520ce549719336508c73e8d972db112ec80bc3cdd5dfe7eeabfd7e404`  
		Last Modified: Thu, 18 Dec 2025 01:31:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e89293b6446f274a0f9ef34fdeb3fa3fed1726f20cbd105ae77c4978b876bfe`  
		Last Modified: Thu, 18 Dec 2025 01:31:21 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed98fb07206d352efcfafb11be44e748591598735ecf53e030f32e9e3bdefbc1`  
		Last Modified: Thu, 18 Dec 2025 01:31:11 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce64d97a2f2f2131ae5f255e75deb2a7bcbe790bbb9c7957c7eb693607aa50a`  
		Last Modified: Thu, 18 Dec 2025 01:31:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:00a191d8cd8b2705a631c80fa87a3b483f6efba2dcdf2b268a5fc0b2987ab16d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2ef8c406fd6197cec384755969bd9ec2f5cbfb7e33f28967e12692975c4a7e`

```dockerfile
```

-	Layers:
	-	`sha256:062434acc0bb23660a7f849a585a1f925e7714a6f2bb13e03b8de54a7abd7f4a`  
		Last Modified: Thu, 18 Dec 2025 01:31:09 GMT  
		Size: 595.8 KB (595801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2eac2b79ca97093825dc89caad771942083d020180ebb9c3a7251b27d74662c`  
		Last Modified: Thu, 18 Dec 2025 01:31:09 GMT  
		Size: 44.4 KB (44360 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:2a34d7b364f75b6100fff7e1cbea34578bd9462c35d18e26ff54ae0593d14baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (111002551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ca65ad5b05d0d56ea0afb14a5fd80da808d88767ddbda4aa0da90c9755815d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 22:58:49 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 22:59:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 22:59:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 19 Dec 2025 00:50:52 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 19 Dec 2025 00:50:52 GMT
ENV LANG=en_US.utf8
# Fri, 19 Dec 2025 00:50:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 19 Dec 2025 00:50:52 GMT
ENV PG_MAJOR=16
# Fri, 19 Dec 2025 00:50:52 GMT
ENV PG_VERSION=16.11
# Fri, 19 Dec 2025 00:50:52 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Fri, 19 Dec 2025 00:50:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Mon, 22 Dec 2025 04:38:59 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Dec 2025 04:39:00 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Dec 2025 04:39:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Dec 2025 04:39:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 22 Dec 2025 04:39:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 22 Dec 2025 04:39:01 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 22 Dec 2025 04:39:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Dec 2025 04:39:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Dec 2025 04:39:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Dec 2025 04:39:01 GMT
STOPSIGNAL SIGINT
# Mon, 22 Dec 2025 04:39:01 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Dec 2025 04:39:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e7504fb8b5ca902553810400e8ecf856a5984c36fb7dba7b9d1932f5432750`  
		Last Modified: Thu, 18 Dec 2025 23:52:28 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254154902548782aac7bbe74d12c713d81df39d8b697e905a7ada02053473207`  
		Last Modified: Thu, 18 Dec 2025 23:52:28 GMT  
		Size: 868.9 KB (868948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7363523f3adbe06817ea37caa9e4e6b3624d1fb0dbdee981cef69302f9c9c01`  
		Last Modified: Fri, 19 Dec 2025 04:43:55 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d460fd12a197206addf50ae676cb3647196c9d8d1bd09a30c6dcc460442fc4e`  
		Last Modified: Fri, 19 Dec 2025 04:43:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed116c5fb1e3fda9f909e41adaf6e727044fc05353dafdefb7d49e56e22b41a`  
		Last Modified: Mon, 22 Dec 2025 04:42:06 GMT  
		Size: 106.5 MB (106532507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b862a2f37c58512f304723eadd356f89e23bcba482a0881edef1d2937512fb`  
		Last Modified: Mon, 22 Dec 2025 04:41:51 GMT  
		Size: 9.6 KB (9568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84071209a200a5657a6cf2c77fac6b0dc2d5f293b1b9442c615d8d41a41bd1d7`  
		Last Modified: Mon, 22 Dec 2025 04:42:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8121113054efc730034458c75ff311ab74d04677c5d1a2671d901dbe26566c06`  
		Last Modified: Mon, 22 Dec 2025 04:42:13 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8ec959d01d32d2db22836ba2fdc0e4b419dccd15b297bf101574fcbe3bd36b`  
		Last Modified: Mon, 22 Dec 2025 04:42:13 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ee59768946ba65eba044d86de727e2791e7bc34f366f4be7e965f1751cd341`  
		Last Modified: Mon, 22 Dec 2025 04:42:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:d0a22ccc0a9ff199e81627afa5985019bfe27c7cec5a2b5d4350f6f9723b849f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.8 KB (641824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c144b650295cd692b53f639793c30654805de76d542f748985c13b2ae31d583e`

```dockerfile
```

-	Layers:
	-	`sha256:359cf5ea7cd52f35b0c79a7bffee58592c32f2078612abf332e70ec51ebad6d3`  
		Last Modified: Mon, 22 Dec 2025 04:41:51 GMT  
		Size: 597.5 KB (597459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dcae09e2225fa8b8ab08c5f6a8d51385681fd9a084b2704eb9534bcbcfbb4c8`  
		Last Modified: Mon, 22 Dec 2025 04:41:51 GMT  
		Size: 44.4 KB (44365 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:1941bbd1ee8faeb8c7fdb06dbe7dda2b7b62bc04c4cff44384f9f5ce61ae5a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118078898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c84f3d09a31a51a14263770ab86df47455ccb8c39b900ab273084fa51ff61e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:06:27 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 01:06:32 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 01:06:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 01:06:46 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 18 Dec 2025 01:06:46 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 01:06:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 01:06:46 GMT
ENV PG_MAJOR=16
# Thu, 18 Dec 2025 01:06:46 GMT
ENV PG_VERSION=16.11
# Thu, 18 Dec 2025 01:06:46 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Thu, 18 Dec 2025 01:06:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 01:11:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 01:11:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 01:11:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 01:11:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Dec 2025 01:11:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 18 Dec 2025 01:11:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Dec 2025 01:11:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:11:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 01:11:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 01:11:47 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 01:11:47 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 01:11:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69c5f2050f07a5cb01bb74eff322320d79ef052693ec1bf2e791c3e34ee9ad2`  
		Last Modified: Thu, 18 Dec 2025 01:12:14 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3d39d8e02436f0b019f16e16fc19ff6b779eae84772469808fc5da728fdd6f`  
		Last Modified: Thu, 18 Dec 2025 01:12:14 GMT  
		Size: 897.4 KB (897417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345d32fb76fdd114a113a2a6d5d89c0479e2dba33e3dc018691cfd7ade2a7b5b`  
		Last Modified: Thu, 18 Dec 2025 01:12:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a3fa7a77f2d74932180ee7684bbf4df82724880bef0a231173cc98ac9ac11e`  
		Last Modified: Thu, 18 Dec 2025 01:12:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2aa18b2d9edf8263e75f65bce7f05ac924b07173f5a9a5b41f8f12f1914816`  
		Last Modified: Thu, 18 Dec 2025 01:12:41 GMT  
		Size: 113.4 MB (113440027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e063ef4c90414bcf4615a57e651b7ca5ae35880ac959d3014b4bcf5c02d2a`  
		Last Modified: Thu, 18 Dec 2025 01:12:15 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094654859ac5a495c4dbecd58e138d66b5ec32793e949e221da2386c5d571fad`  
		Last Modified: Thu, 18 Dec 2025 01:12:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70078bce0b8da85b733133ee9e4a1dd2211bfac340328032bd8cde77d49bf9ab`  
		Last Modified: Thu, 18 Dec 2025 01:12:26 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b343f79c51e2b5779dbb09c5fa903f2435c6038d97315ee8369762e2ff88c6cb`  
		Last Modified: Thu, 18 Dec 2025 01:12:16 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09322945e0a4da183a70ada12c53dbdde846c8e85b032237d43ce05b2eaa4c7`  
		Last Modified: Thu, 18 Dec 2025 01:12:16 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:bab6381e306bfc76417d384e8f55ef70e6218e3b077ebe1d5517b201a7201dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.7 KB (641734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512f01cb7179926197a9e17556d786207fc71633d8b8fdb9d90b741a509a00a9`

```dockerfile
```

-	Layers:
	-	`sha256:6bcddd63bd0ededb8bc7b0f23444982504d3be13bf84f4cdab4a3177fbd5f62b`  
		Last Modified: Thu, 18 Dec 2025 03:09:57 GMT  
		Size: 597.4 KB (597429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f430677bc9f30e8eb7fd0c6a2af4ad7419d69a5c6a51a72539ddf2931aa20144`  
		Last Modified: Thu, 18 Dec 2025 03:09:58 GMT  
		Size: 44.3 KB (44305 bytes)  
		MIME: application/vnd.in-toto+json
