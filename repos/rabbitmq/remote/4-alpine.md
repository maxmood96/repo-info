## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:4cf7da74143b4f7824330a9a1bc7d3af99e46988fb75b74b6976ba67de579c48
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

### `rabbitmq:4-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:927df0139a019c5bca56247f0f0f80d4a93cf9e2adb2c046b5a42a0e15efb5e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83448429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2245bf19e5ed4fa2d4d50559d619fb73faa22e8d28c6e5051ca71ffb3cef2132`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 19:35:07 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 10 Nov 2025 19:35:07 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 10 Nov 2025 19:35:07 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 10 Nov 2025 19:35:07 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 10 Nov 2025 19:35:07 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:35:07 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:35:10 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 10 Nov 2025 19:35:10 GMT
ENV RABBITMQ_VERSION=4.2.0
# Mon, 10 Nov 2025 19:35:10 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 10 Nov 2025 19:35:10 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 10 Nov 2025 19:35:10 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:35:15 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 10 Nov 2025 19:35:16 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 10 Nov 2025 19:35:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 10 Nov 2025 19:35:16 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:35:16 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 10 Nov 2025 19:35:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 10 Nov 2025 19:35:17 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 10 Nov 2025 19:35:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:35:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:35:17 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 10 Nov 2025 19:35:17 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3012a2d976b930d69516db0afd4de797ec9f071adf363a415b30b69749cb3fe`  
		Last Modified: Mon, 10 Nov 2025 19:35:45 GMT  
		Size: 42.9 MB (42859528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267116ec47e58a13f09633083fc442d7a2006db9229bcd286edc6b7b988041db`  
		Last Modified: Mon, 10 Nov 2025 19:35:40 GMT  
		Size: 9.1 MB (9143894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41479b48910ba3d80b291883c5c7dc3b9b2dcc831cf1d19bbd392b6902657e19`  
		Last Modified: Mon, 10 Nov 2025 19:35:39 GMT  
		Size: 2.4 MB (2374378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2839f550be6e8b7b5f8d5288d0497092feeb9ec555c6473c3383def406723799`  
		Last Modified: Mon, 10 Nov 2025 19:35:42 GMT  
		Size: 25.3 MB (25266431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941d3bb3d96645e432c07ecef08eec444d6a91d2e47e1ac95c923a87a8b5952c`  
		Last Modified: Mon, 10 Nov 2025 19:35:39 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c53d059cf2f31e95624ff16eb04df7c46b1175fb019e4d43b9e15c3401291d2`  
		Last Modified: Mon, 10 Nov 2025 19:35:39 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f111dc27ba219a98480863dd9298c1c0b950981f072436ac785ed5dfe4e16963`  
		Last Modified: Mon, 10 Nov 2025 19:35:39 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a9d220bc7248b982a93e93c4b932bb5b593986fb1f12db5941c718cefa75c5`  
		Last Modified: Mon, 10 Nov 2025 19:35:39 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c46b5a8b796b209058d6441225bf4e629999d41070b0c80dc55ab1c3316285a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6787006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3f924c613c0d624d8f5abe1356f7fa1d73aa93f88e7fa25c879c12e53bd63e`

```dockerfile
```

-	Layers:
	-	`sha256:cb7c66e94f2fb565bf8e3a89a3b3645fa99c0621f8bbca0c09d043352a469e2b`  
		Last Modified: Mon, 10 Nov 2025 19:54:02 GMT  
		Size: 675.3 KB (675257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:508ba71d2701505b9ed7e433ef71e28461640aca0dbedcd61df3de820873417a`  
		Last Modified: Mon, 10 Nov 2025 19:54:03 GMT  
		Size: 3.1 MB (3102698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:788aa6ed849b087ed018f7c5c87cd8e1876433d7458f1301953d185dc7228ceb`  
		Last Modified: Mon, 10 Nov 2025 19:54:05 GMT  
		Size: 2.9 MB (2949137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc0f9b219e09e5e35cde7968e3f43c7c7ad035d3c68f63a195f0efb247de102e`  
		Last Modified: Mon, 10 Nov 2025 19:54:06 GMT  
		Size: 59.9 KB (59914 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:2ce900958dc605f18ff1c4c20239b9b45bb079fe739c729a3c6ba7765551e1c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71333867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0038cdac3734b96974fc230cf3f07f2b4b86a80d3917a0156b6ae77f249509af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 19:31:42 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 10 Nov 2025 19:31:42 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 10 Nov 2025 19:31:42 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 10 Nov 2025 19:31:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 10 Nov 2025 19:31:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:31:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:31:45 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 10 Nov 2025 19:31:45 GMT
ENV RABBITMQ_VERSION=4.2.0
# Mon, 10 Nov 2025 19:31:45 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 10 Nov 2025 19:31:45 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 10 Nov 2025 19:31:45 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:31:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 10 Nov 2025 19:31:56 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 10 Nov 2025 19:31:56 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 10 Nov 2025 19:31:56 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:31:56 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 10 Nov 2025 19:31:56 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 10 Nov 2025 19:31:56 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 10 Nov 2025 19:31:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:31:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:31:56 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 10 Nov 2025 19:31:56 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a1b0da0f5a2ab4e4f48ea5669675637dcaed2cdd272e0a3edce34e266d78ca`  
		Last Modified: Mon, 10 Nov 2025 19:32:25 GMT  
		Size: 33.4 MB (33443049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6694d8d48bd4fdcd6d818d9e3d555ab69fb4336d78b4a6a7ff8337dfcdbf1b5b`  
		Last Modified: Mon, 10 Nov 2025 19:32:23 GMT  
		Size: 7.8 MB (7788809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e320c1a42de1854f52695bd834665df9fe149d454346edf81072121446f37520`  
		Last Modified: Mon, 10 Nov 2025 19:32:23 GMT  
		Size: 1.3 MB (1330055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f04113fb29b4d40d36ea2a056980802ade70f59409b9842298b344b981ac950`  
		Last Modified: Mon, 10 Nov 2025 19:32:25 GMT  
		Size: 25.3 MB (25266123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e528163eacfe3829af19e3e5d17d0af65c05a80ac53d464cc889fcfd7f047f`  
		Last Modified: Mon, 10 Nov 2025 19:32:23 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce7bb2e9f85da2b215ca42a0b694d7ab38a71bfbdd1ab615932588a6d31be82`  
		Last Modified: Mon, 10 Nov 2025 19:32:23 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5653e151ff6b42ff1c1271b29846bd7a9d6ac0ca2e577142757a57a083eeaad7`  
		Last Modified: Mon, 10 Nov 2025 19:32:23 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa25fdac0fd2483afded2e09bca9c3573b9b8017d23614f92d0c0aa2a0c8909d`  
		Last Modified: Mon, 10 Nov 2025 19:32:24 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:851710c517a1107f643c18ee01f57be3babe8639fd89a6be6c701b45b57e9276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 KB (59896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ac558a5cfdcab0d99f2295139a8aa898cf5aa8537acad6d9ef40ddb943bd66`

```dockerfile
```

-	Layers:
	-	`sha256:464acdaae442bf4cc9c53714d15ea08170d68d2cbe62923ec9e9ca49a5cd7bd6`  
		Last Modified: Mon, 10 Nov 2025 19:54:11 GMT  
		Size: 59.9 KB (59896 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:26a78a790d44db725c10790b5162d08f8533bc7b8c7d81c5e3e8dc462171b9e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70497678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6adaaac59fba4ed199baa99e8af90dc7c7c098bf970af9047722bb19df2070`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 19:36:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 10 Nov 2025 19:36:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 10 Nov 2025 19:36:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 10 Nov 2025 19:36:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 10 Nov 2025 19:36:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:36:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:36:18 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 10 Nov 2025 19:36:18 GMT
ENV RABBITMQ_VERSION=4.2.0
# Mon, 10 Nov 2025 19:36:18 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 10 Nov 2025 19:36:18 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 10 Nov 2025 19:36:18 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:36:25 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 10 Nov 2025 19:36:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 10 Nov 2025 19:36:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 10 Nov 2025 19:36:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:36:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 10 Nov 2025 19:36:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 10 Nov 2025 19:36:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 10 Nov 2025 19:36:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:36:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:36:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 10 Nov 2025 19:36:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2145bb904e2f36808053923ef793c5ddd8cae15eb443fe1687c1bbae87c88f2`  
		Last Modified: Mon, 10 Nov 2025 19:36:52 GMT  
		Size: 33.4 MB (33390738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a738cb474996344e2d103149ca7d1f2f4731d0178498c6fe4c29b181125b31`  
		Last Modified: Mon, 10 Nov 2025 19:36:50 GMT  
		Size: 7.4 MB (7390608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df510e0dc0c65e55577d9d181f6405d55ac9273e2454e162ecafe19949030b5f`  
		Last Modified: Mon, 10 Nov 2025 19:36:49 GMT  
		Size: 1.2 MB (1227058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962c64cc736693c2b11d73c672f42946f8f13464d0d1ecc15f723261153e7fda`  
		Last Modified: Mon, 10 Nov 2025 19:36:52 GMT  
		Size: 25.3 MB (25265970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2f60aae8ded304ce806a89fcf0669613620b673842ed359449ceacbad7a83f`  
		Last Modified: Mon, 10 Nov 2025 19:36:49 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93d630eac6d97af50133999f7224eae3dad576653620db9d6164bb1902d9a48`  
		Last Modified: Mon, 10 Nov 2025 19:36:49 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66113de745b256eb243bc345f10acd82879f6bc2304e3bdf1f55391944b4bad`  
		Last Modified: Mon, 10 Nov 2025 19:36:49 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5245ea4f5d9d55fc3bd0b4c10ae3e389c4da7deb3e516d6f126bd34f315c5e2f`  
		Last Modified: Mon, 10 Nov 2025 19:36:49 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c6240927a30c62a0845ccfe52c772c373359469ad1093ab947ce5df35e31fc07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6551313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c251556b1f4aa99070aaf203fc897c27b2bd00a222715f5d359694651306991`

```dockerfile
```

-	Layers:
	-	`sha256:5ebe38d8d0da02ba33df58c3fecdb613d42e0d0514c726e2c19c8723624062da`  
		Last Modified: Mon, 10 Nov 2025 19:54:14 GMT  
		Size: 671.0 KB (671050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b30b77988e92159855750873593e9ec875e029646cb3463a314db304d720ebf2`  
		Last Modified: Mon, 10 Nov 2025 19:54:15 GMT  
		Size: 3.0 MB (2987521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5af4963e091b12bfaac39d94b9b9de0e39552ac9c38ac44d27b0b0dda0e356e2`  
		Last Modified: Mon, 10 Nov 2025 19:54:16 GMT  
		Size: 2.8 MB (2832631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba1379d3cb3e66124212ebbf20c809157df816a8e2c29fde48cbc6d6d84bbefe`  
		Last Modified: Mon, 10 Nov 2025 19:54:17 GMT  
		Size: 60.1 KB (60111 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:b1e93dd26228737ef43c06545195a636195d1bdef726c28f1ebee81ee3661cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82507225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf56ca0a7a2b60d3264f21f6ac497e56d556efcc9683ec627995ac2fd08be740`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 19:36:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 10 Nov 2025 19:36:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 10 Nov 2025 19:36:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 10 Nov 2025 19:36:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 10 Nov 2025 19:36:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:36:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:36:33 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 10 Nov 2025 19:36:33 GMT
ENV RABBITMQ_VERSION=4.2.0
# Mon, 10 Nov 2025 19:36:33 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 10 Nov 2025 19:36:33 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 10 Nov 2025 19:36:33 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:36:39 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 10 Nov 2025 19:36:40 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 10 Nov 2025 19:36:40 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 10 Nov 2025 19:36:40 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:36:40 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 10 Nov 2025 19:36:40 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 10 Nov 2025 19:36:40 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 10 Nov 2025 19:36:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:36:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:36:40 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 10 Nov 2025 19:36:40 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fc6b02c537f0a2f405aebe6279d6d60839369e9221d740765902d626853c01`  
		Last Modified: Mon, 10 Nov 2025 19:37:09 GMT  
		Size: 40.9 MB (40851966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8c52e6922467c7899eb34b927289333fe3a5e01f1b402164abcb89456389c8`  
		Last Modified: Mon, 10 Nov 2025 19:37:07 GMT  
		Size: 9.8 MB (9824256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342c15c690ee0055ffcbac2887c50d3bdf2bd0ec80ca6a092020b884c0be88d4`  
		Last Modified: Mon, 10 Nov 2025 19:37:05 GMT  
		Size: 2.4 MB (2424789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317391af7d1b45562ea31717e9f59c3d3783805fbf23059f965d627ed4d66d88`  
		Last Modified: Mon, 10 Nov 2025 19:37:07 GMT  
		Size: 25.3 MB (25266400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bd1a655fcde870a254a46417ea8b7fe387167405371c4f06d39494953edec9`  
		Last Modified: Mon, 10 Nov 2025 19:37:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d621a11574d0dab62351418472d375a12842abadbd831d3f0d4dd6d2936ec8`  
		Last Modified: Mon, 10 Nov 2025 19:37:05 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc852dd305128ccfa84b967fc0db2606a5c56128ada49d23f306251981ac9573`  
		Last Modified: Mon, 10 Nov 2025 19:37:05 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e45325f39f479c8a0c15bab13f3860fd564026e1a700f5e952b540d14a3ea5e`  
		Last Modified: Mon, 10 Nov 2025 19:37:05 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f632f6d50d57d2f997eba3212c9c4070c9b52324fc59a7b8de75b479d82c5c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6895311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ad551fbe854ff6544d833d2f978a406c2f61d06575b475d551401974a2c031`

```dockerfile
```

-	Layers:
	-	`sha256:9bdf6c69e62996afbc4e562808e36c0d725335533a1935055480d1ab79831361`  
		Last Modified: Mon, 10 Nov 2025 19:54:22 GMT  
		Size: 676.0 KB (676050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19afcfa4ffae30b1b33abb5ae87abcb4dfa9c8bc39ded52411535910b949f76c`  
		Last Modified: Mon, 10 Nov 2025 19:54:23 GMT  
		Size: 3.2 MB (3156996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42e018d5184b257ea3eeb1b0b973016d3cfe78242b05c23f15e754577bc1ff73`  
		Last Modified: Mon, 10 Nov 2025 19:54:24 GMT  
		Size: 3.0 MB (3002112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:690759b212606f84402d214cb853d66a59f3d8c9d839b15793ea54eb78fd7aa8`  
		Last Modified: Mon, 10 Nov 2025 19:54:25 GMT  
		Size: 60.2 KB (60153 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:a04ac8cd452e809d6b15e1622eed0c3f0a7f4b9ddf41e94da3a39520df9e7d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72920716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a71a215bb862aaf786249be61c34e51bbdb408be9625a99d4e15c0b8b9da51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 19:31:08 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 10 Nov 2025 19:31:08 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 10 Nov 2025 19:31:08 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 10 Nov 2025 19:31:08 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 10 Nov 2025 19:31:08 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:31:08 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:31:11 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 10 Nov 2025 19:31:11 GMT
ENV RABBITMQ_VERSION=4.2.0
# Mon, 10 Nov 2025 19:31:11 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 10 Nov 2025 19:31:11 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 10 Nov 2025 19:31:11 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:31:17 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 10 Nov 2025 19:31:18 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 10 Nov 2025 19:31:18 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 10 Nov 2025 19:31:18 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:31:18 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 10 Nov 2025 19:31:18 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 10 Nov 2025 19:31:18 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 10 Nov 2025 19:31:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:31:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:31:18 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 10 Nov 2025 19:31:18 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f86a5601938e3e7f71fa015d146d97fd8d777f0291a431bd0e4974032eba25f`  
		Last Modified: Mon, 10 Nov 2025 19:31:44 GMT  
		Size: 33.5 MB (33542609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a0deed474ab3cd5b7cdc9462fd5961fb23a7c89a67c44e27d2fedd55bb3ae6`  
		Last Modified: Mon, 10 Nov 2025 19:31:41 GMT  
		Size: 9.2 MB (9159101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bc679fe3c961cbba98ad1eb1cba44f6020cb83af16437f2140054c6b935936`  
		Last Modified: Mon, 10 Nov 2025 19:31:40 GMT  
		Size: 1.3 MB (1332474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689e6318b79fd6813f3992f88d4f03ff422077a773791fe46fb7c88893ff3ccc`  
		Last Modified: Mon, 10 Nov 2025 19:31:45 GMT  
		Size: 25.3 MB (25265852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074a58d58a1aec510c3fb5603fe76914ee9778f79632c20bec8b982fc4e6282`  
		Last Modified: Mon, 10 Nov 2025 19:31:39 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b52f7c376ed6379ea032e9e13b9e195cf6f327c050883cba82b24e563fbaa5`  
		Last Modified: Mon, 10 Nov 2025 19:31:40 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79619c73cc376abc26ce9b828696afbd7a4447bfa7888d2aefea5708fcef802`  
		Last Modified: Mon, 10 Nov 2025 19:31:39 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8b57259b53f8c1f17ecc09ba6177d9afd01b67591c45ec4d6082f2919b846f`  
		Last Modified: Mon, 10 Nov 2025 19:31:39 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a200513efb802900bce866d1ab2712c0267d9a522f10c8dbb84241b9cf42b997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6759847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1019dc19ad225a88db3c450837729d9ac95fa3da02a6e76b45b96baf47cc010c`

```dockerfile
```

-	Layers:
	-	`sha256:920e95d926891571c9a1979e9246618cda0a14440b4e311f9cb223229e490d6d`  
		Last Modified: Mon, 10 Nov 2025 19:54:31 GMT  
		Size: 670.3 KB (670252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c33b546d5b72164a23d931a3e2c410d6ce857ec894e574476cc1fe58580ab624`  
		Last Modified: Mon, 10 Nov 2025 19:54:32 GMT  
		Size: 3.1 MB (3091644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acc477169cd4b00b01917697315d347b1ba62829f9e0e3c1af4aab156b73336f`  
		Last Modified: Mon, 10 Nov 2025 19:54:34 GMT  
		Size: 2.9 MB (2938087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c15a811b3eb7f7e96431e2c4a96979f4ec6c2784493404b622709a0785ceb32`  
		Last Modified: Mon, 10 Nov 2025 19:54:34 GMT  
		Size: 59.9 KB (59864 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:7692d289e1729d46436b7cce030f9252e72d0b5c016733a816e1d9c96278234f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74152639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17865a0a373e967b816949354e4c82dfbbabaa4b96a0a2c6002257929e0e0acc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 20:55:03 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 10 Nov 2025 20:55:03 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 10 Nov 2025 20:55:03 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 10 Nov 2025 20:55:04 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 10 Nov 2025 20:55:04 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 20:55:04 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 10 Nov 2025 20:55:08 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 10 Nov 2025 20:55:08 GMT
ENV RABBITMQ_VERSION=4.2.0
# Mon, 10 Nov 2025 20:55:08 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 10 Nov 2025 20:55:08 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 10 Nov 2025 20:55:08 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 20:55:18 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 10 Nov 2025 20:55:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 10 Nov 2025 20:55:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 10 Nov 2025 20:55:20 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 10 Nov 2025 20:55:20 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 10 Nov 2025 20:55:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 10 Nov 2025 20:55:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 10 Nov 2025 20:55:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 20:55:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 20:55:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 10 Nov 2025 20:55:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a4d51105d3283cdfb3e09808fac27b38049b3e1cd2441cc917b13dc3e640e1`  
		Last Modified: Mon, 10 Nov 2025 20:56:07 GMT  
		Size: 33.9 MB (33926026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d492b14e3466805135c77f32a688360c0dd16d159bf66501f6d06efa5b44b3ae`  
		Last Modified: Mon, 10 Nov 2025 20:56:03 GMT  
		Size: 9.8 MB (9774075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a818e67009e350d81fb7796849db74cfcc64b7dd8b69b78c71e65f291bb3a4f`  
		Last Modified: Mon, 10 Nov 2025 20:56:02 GMT  
		Size: 1.5 MB (1452624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e89527ae760546c2ccfc2d64f00f953dab04d837824cdc1b6cde143a3c2881f`  
		Last Modified: Mon, 10 Nov 2025 20:56:06 GMT  
		Size: 25.3 MB (25265930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0988a6a7eeb97a29069d51c556ce69abf392d98d11e14972f46ad244b23f3397`  
		Last Modified: Mon, 10 Nov 2025 20:56:03 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0485a9609327ccf0f20a788b0825742fe244bc8b6905f243d9317fb75b8617`  
		Last Modified: Mon, 10 Nov 2025 20:56:05 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf463e1e76ed670b04283fe8e504d362c4022036366fce13669d04257336350`  
		Last Modified: Mon, 10 Nov 2025 20:56:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6b10384dc1662b11cc8788a2e53ced481d6330f613444c939a58b9c99c509d`  
		Last Modified: Mon, 10 Nov 2025 20:56:04 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8230daec15e6e9f178a7f340d83035d8c9fde228b4b6878990ff81337fecff23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6791677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ed6f1d67e7d5909f600798498b84d30330d6f05756f8e75c90415a372e2749`

```dockerfile
```

-	Layers:
	-	`sha256:1f759d8d73e2589f0db794749a23c937336d7be8fb3102440786e93f160bc2ea`  
		Last Modified: Mon, 10 Nov 2025 22:53:57 GMT  
		Size: 669.1 KB (669097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2df14e20c7428eba68f11044cf70aa5417a0d66f2138746f00f03b41f052c95`  
		Last Modified: Mon, 10 Nov 2025 22:53:59 GMT  
		Size: 3.1 MB (3108750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:705c33a50dfefb88e41cdcfe0f671f3bd7ee8e04869237237115d3365bd6410b`  
		Last Modified: Mon, 10 Nov 2025 22:54:00 GMT  
		Size: 3.0 MB (2953854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4f7a9b9c247efb49539406322b2bfce7f63efefa222d291d3bb99a364948cc6`  
		Last Modified: Mon, 10 Nov 2025 22:54:01 GMT  
		Size: 60.0 KB (59976 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:29fbd3596046b0e686c0e8f9635249842ecfbe0f69f3c71c52eb2742f0098565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75949637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7d71d9341c86a4559a3a8ff8d2ebf2907717acc735197b79f778dc6d4ef66f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 23:00:41 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 23:00:41 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 23:00:41 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 23:00:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 23:00:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:00:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 23:00:55 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 Oct 2025 23:00:55 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 23:00:55 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 23:00:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 23:00:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:01:34 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 23:01:43 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 23:01:44 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 23:01:44 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 23:01:44 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 23:01:44 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 23:01:44 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 23:01:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 23:01:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 23:01:45 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 23:01:45 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10134cdd10881c5b8872bd6a22cdee3d4f7947cf07d56bcfcb67b233a15d9c12`  
		Last Modified: Fri, 31 Oct 2025 23:07:28 GMT  
		Size: 34.9 MB (34893302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc84479dee5ea17251ec65d2bf63013f46012984d82cfc0dacc6fa4e7eb030c5`  
		Last Modified: Fri, 31 Oct 2025 23:07:26 GMT  
		Size: 10.9 MB (10906600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdf1244b1015e4f3abc2025a38925d773a84d3d23c8714af5da707a897f52e2`  
		Last Modified: Fri, 31 Oct 2025 23:07:25 GMT  
		Size: 1.4 MB (1366493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f4fc003ebbc648006e42a148cf719e3feedb9f149b92374c03280473701263`  
		Last Modified: Fri, 31 Oct 2025 23:07:26 GMT  
		Size: 25.3 MB (25266245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d2996778974410b330bf379c00903a3c4ce56446833a9a35bc6536e6a847ac`  
		Last Modified: Fri, 31 Oct 2025 23:07:24 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f45fce4291972f5f7b9e2062982b27b38e93f4c4fdd45f7295fc1b4a5754c1`  
		Last Modified: Fri, 31 Oct 2025 23:07:24 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b03d9a6ea73b622b2b8f9cc00a18a440a39bfa753b3e610d5d4c090005e4e5`  
		Last Modified: Fri, 31 Oct 2025 23:07:24 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbca45694e03cab13dfd5bd528aeb3d3f90eb8147368710ebbb3ab1902a19ae`  
		Last Modified: Fri, 31 Oct 2025 23:07:25 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fbf07b92850ce400d83f880962e1b8d343301f36ea68bba87b78973221f9a038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6871011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecaa7a6df131017e13bf0e3f95de3df4e3cd4d57cb13786eda4157a514cbfaf4`

```dockerfile
```

-	Layers:
	-	`sha256:1844e427f98a577250e430d47734ec3f0f6edef866be4ea9cd2353aaa707fae1`  
		Last Modified: Sat, 01 Nov 2025 00:53:08 GMT  
		Size: 672.1 KB (672066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1f305f135df43cb74bfd1fce35a62f4a563c2927a5d8a4b71aa6829d4d55135`  
		Last Modified: Sat, 01 Nov 2025 00:53:10 GMT  
		Size: 3.1 MB (3146923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a70ade8edf2072bb55796cd7fc6af504ade025aaa6596dde1fd11bb014100a6c`  
		Last Modified: Sat, 01 Nov 2025 00:53:11 GMT  
		Size: 3.0 MB (2992039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e21df8177fd0c945efe406ad7163dc584f75544ff3c96c366d4967d7318592`  
		Last Modified: Sat, 01 Nov 2025 00:53:12 GMT  
		Size: 60.0 KB (59983 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:422bc078c76a5838464ca23b92814728edcf07452cd62a4bb0a119b0068e0f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72663100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b632095d80fdca481654041a8e7130041aa166b449620cb76778858dbc9f804`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 20:23:57 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 20:23:57 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 20:23:57 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 20:23:58 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 20:23:58 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:23:58 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:24:02 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 Oct 2025 20:24:02 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 20:24:02 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 20:24:02 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 20:24:02 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:24:16 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 20:24:17 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 20:24:17 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 20:24:17 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:24:17 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 20:24:17 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 20:24:18 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 20:24:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 20:24:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 20:24:18 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 20:24:18 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151f10fe2d5970a93b2c09548b23918d27bebe3e729d40d18d105c927642f22e`  
		Last Modified: Fri, 31 Oct 2025 20:25:04 GMT  
		Size: 34.0 MB (33968406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbcef3ee149023b862d4a5c01ed000b7fe1681669f9d8c804eef402cca769ab`  
		Last Modified: Fri, 31 Oct 2025 20:25:02 GMT  
		Size: 8.3 MB (8347157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc7a38ee1fe3901818cf81de72c1870a6b79011fef3b3611a15bf1da29e0956`  
		Last Modified: Fri, 31 Oct 2025 20:25:02 GMT  
		Size: 1.4 MB (1430649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735665edefcf2aad4d55873503deef537e0b49d462265a8b17fc79f095b37578`  
		Last Modified: Fri, 31 Oct 2025 20:25:04 GMT  
		Size: 25.3 MB (25265893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742e635b9f74cfb089d934abae9fdfe3b17ce487a6dfee24efaf182551ae3167`  
		Last Modified: Fri, 31 Oct 2025 20:25:02 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2986382df115e6dc31f54750e52b580a296073f3a0dd12ce90362757849e340b`  
		Last Modified: Fri, 31 Oct 2025 20:25:02 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b932a6beae64243460533130ac7459630af3d0d44a748cb7d6c9be9f8ebe42c8`  
		Last Modified: Fri, 31 Oct 2025 20:25:02 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c0e48355b01996594567359c479d344d831f665c938466c42aca4ad450b5ed`  
		Last Modified: Fri, 31 Oct 2025 20:25:02 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2b60b7da3f682c6362516d0360a1276df6732a742f151555b88c4de3b6194f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6570485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17705e50c22fb192a593fad926b46b1a726ae2accd953c8e40fc01f5665fa0b`

```dockerfile
```

-	Layers:
	-	`sha256:511186739443ea61e2ee0ff7d2ef23c269c1e43d8ccd128f6735bcea62df5149`  
		Last Modified: Fri, 31 Oct 2025 21:54:21 GMT  
		Size: 669.1 KB (669063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd1f64fbf52761f93c864ab31b923c435c4912315b0860a99e6a4b2cf4c986af`  
		Last Modified: Fri, 31 Oct 2025 21:54:22 GMT  
		Size: 3.0 MB (2998187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:021d277d901e2cb689b57977ea65b6cb59cc8b0e36ea42db35bb5d794b74b69b`  
		Last Modified: Fri, 31 Oct 2025 21:54:24 GMT  
		Size: 2.8 MB (2843321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82f43c66b8e16b108c3431016c584a0de92f4e0fc8bc4b3e259646605bc2594b`  
		Last Modified: Fri, 31 Oct 2025 21:54:24 GMT  
		Size: 59.9 KB (59914 bytes)  
		MIME: application/vnd.in-toto+json
