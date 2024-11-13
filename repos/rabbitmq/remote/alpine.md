## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:255821383e64045f7a5b9b8b8b9ce40b30a0c29d1b2e3945bc3be2145bb6d212
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

### `rabbitmq:alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:b5df9f18d50f4ffc93ccc51d71f5d284b033777bc82d1da74da8d8fdfbcd1d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74058051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab43ea5d853c5fa0013dbc38dfbacdcbfe2e2ecc291697edd4b5d37c7c225c97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 01 Nov 2024 11:35:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_VERSION=4.0.3
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 Nov 2024 11:35:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 01 Nov 2024 11:35:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd82a57152b59e0791647543abc462720fce7105538550b193aedc3372bf2b9`  
		Last Modified: Tue, 12 Nov 2024 02:52:15 GMT  
		Size: 41.6 MB (41580221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d24b5752befad192e0a6b54420cb12919adbac10033d235379a9fd5e5c2973`  
		Last Modified: Tue, 12 Nov 2024 02:52:15 GMT  
		Size: 8.3 MB (8284915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07e2496e9ffae65715973e78237328f853754064feeeda021fbedfbb125d833`  
		Last Modified: Tue, 12 Nov 2024 02:52:14 GMT  
		Size: 2.2 MB (2234377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e483f8e8c2e908c3cc90b6634330dd57106d12b5aaf863235871a342a4bbde4`  
		Last Modified: Tue, 12 Nov 2024 02:52:15 GMT  
		Size: 18.3 MB (18332878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a625059df2edd40cf7f1fb35994c167afff72a5430d9053762d9913569d96372`  
		Last Modified: Tue, 12 Nov 2024 02:52:15 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2554c791be32632846084943e4a9337131a668edd1f783b2e1f2bac965372139`  
		Last Modified: Tue, 12 Nov 2024 02:52:15 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4aebe32ec5a9489df5bd940f49e04f5b92962ac6e145c775e1133e59ef9d75`  
		Last Modified: Tue, 12 Nov 2024 02:52:16 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e61a52191ba974462cdcab55a17fb6b7467dedc5e8fedb8698e60be9f564944`  
		Last Modified: Tue, 12 Nov 2024 02:52:16 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3f69be1267094208465d2c1d0dcfb34c6ac16486141c30ead2c29247006657e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6456082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76131a9a701b8ea4c11ad1441a20ea8e8a67cfb49d0ab3bc3cecad99699f341e`

```dockerfile
```

-	Layers:
	-	`sha256:d4b27f098ff4d420c1b12a0fde4b0131e1223532a38f0a256a91e168253884a6`  
		Last Modified: Tue, 12 Nov 2024 02:52:15 GMT  
		Size: 652.9 KB (652933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0326abe557265e94e17a5a8cec9782a24d6fc3f74b5e1a372ae7f69a3331e62e`  
		Last Modified: Tue, 12 Nov 2024 02:52:15 GMT  
		Size: 2.9 MB (2948875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e543716b9268621a7b32d7e31bd02dc3e4147fe5054afc6dc9dcf48453fa2109`  
		Last Modified: Tue, 12 Nov 2024 02:52:15 GMT  
		Size: 2.8 MB (2794406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afce077665ccdeaa3406111b85c7749d382ed0f6a9bbc7b61703739dadcc98fe`  
		Last Modified: Tue, 12 Nov 2024 02:52:14 GMT  
		Size: 59.9 KB (59868 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:0aa699a1e49e50be813d0745f08abd0f8326a8b737f1bb119eaf0d7160b6a5c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63208419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e006a53971c6ff929f9b0934285467c37b8c8afdb772351c4994fee78b0e4b46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 01 Nov 2024 11:35:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_VERSION=4.0.3
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 Nov 2024 11:35:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 01 Nov 2024 11:35:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4f3e24d539bccf31287b62a8c5348587f00ffc6d065454e5fbbc53a840d396`  
		Last Modified: Tue, 12 Nov 2024 14:59:34 GMT  
		Size: 33.2 MB (33197329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7410dac0bfdccdf53ac9145a9265710d118abee43f159f213fe25951e74433d3`  
		Last Modified: Tue, 12 Nov 2024 14:59:33 GMT  
		Size: 7.1 MB (7079929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad47d4555beef6a9a77ad80b956cb2542ce77e777de46ad7c7c7dd9ddd17ce43`  
		Last Modified: Tue, 12 Nov 2024 14:59:33 GMT  
		Size: 1.2 MB (1230024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a521677fad02ad48357cca2480d1664d694eac04b3961338292026388df7df`  
		Last Modified: Tue, 12 Nov 2024 14:59:33 GMT  
		Size: 18.3 MB (18332791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7beca7e166d7fb0b0754028a7663df418fb0b68bf2454f0dda61a58ac8a5ca14`  
		Last Modified: Tue, 12 Nov 2024 14:59:34 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b519b8afba7b25743d660fdba3dd67dc47d373f7ba2b5c1a6a57c437779783d4`  
		Last Modified: Tue, 12 Nov 2024 14:59:34 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d48f00e41aaca76102ff82b0883fed0920219de63149e9e1979c9b1caa51732`  
		Last Modified: Tue, 12 Nov 2024 14:59:35 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62847df814863eee360dc112d25d6a4959f777d81940e3796f9de3d1e33ed9e`  
		Last Modified: Tue, 12 Nov 2024 14:59:35 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f1c76eb1b221409ca02d14efce534c0e277e731f214b16848ce9fc0d70b251cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 KB (59846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489aa6665f523eae23d786858967113bb32b3bb0b5b66f4912ca19d4f096fc2b`

```dockerfile
```

-	Layers:
	-	`sha256:0ef76320b5b0f59e1c8e192688a92b63efb75510b520c9e52969ea509f52e62e`  
		Last Modified: Tue, 12 Nov 2024 14:59:32 GMT  
		Size: 59.8 KB (59846 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:063fa991942e6ecc5c814644a03e5b9dd43689032c1b6fab0f3f32028447b9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62372165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5892a3a33afc8b8c4232aa2a61d656c4d755d5845cee8ba47e76fb55df0f61ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 01 Nov 2024 11:35:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_VERSION=4.0.3
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 Nov 2024 11:35:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 01 Nov 2024 11:35:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f72133e5f4dd0d86d51c7cc51030e0643442cc3b0f31b010b841ec64373171a`  
		Last Modified: Mon, 04 Nov 2024 23:25:59 GMT  
		Size: 33.1 MB (33092993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dcecece5bb15530976c94289dd888ba5b0aa00dbc67a585c842d9c2db5d159`  
		Last Modified: Mon, 04 Nov 2024 23:25:59 GMT  
		Size: 6.7 MB (6716576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c32467725ad48a2d6907d87659998dbba86891f33fb8372efd269dbd12969bf`  
		Last Modified: Mon, 04 Nov 2024 23:25:58 GMT  
		Size: 1.1 MB (1132944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9545b06b1d795e0aebfa84e5f8e7afb9a30492761928ff153c1611563118302`  
		Last Modified: Mon, 04 Nov 2024 23:25:59 GMT  
		Size: 18.3 MB (18332403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb52634f2b780a8d428cce0d9605ccaad9c9751fe98da6473a32d4eeb06ca4e0`  
		Last Modified: Mon, 04 Nov 2024 23:25:59 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e97af29f73f3c1513a55e8084b1411c1ee45428e2e827ee998992d8395c8f95`  
		Last Modified: Mon, 04 Nov 2024 23:26:00 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a39772252eabcf82ac57008eeb4b4970c2a5ab53c5280cc4d9552d70bf1fe8`  
		Last Modified: Mon, 04 Nov 2024 23:26:00 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86635ca04d48aa7df8aeb773e048bf0596662a737e957f049de3abfc10772e1`  
		Last Modified: Mon, 04 Nov 2024 23:26:00 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:74646c0a9474c1466d2e0a4786fe24e482de77cfe4012df0a261034877b02629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6249920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de47ff76152cb84a2b609da40746ee1d9af38924bee6b63a849d70bc8b4d54de`

```dockerfile
```

-	Layers:
	-	`sha256:43470e1c802052a15140ec3b0572a13f3a807dfbc1fb1ae31a354275bc0d19cd`  
		Last Modified: Mon, 04 Nov 2024 23:25:58 GMT  
		Size: 649.0 KB (649004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ede80689bcfdeac4b6a18fc9ccb562bde8a779d3e292cfef689b0c6fc3a74052`  
		Last Modified: Mon, 04 Nov 2024 23:25:58 GMT  
		Size: 2.8 MB (2848415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f086a7363d15b4e85a74f2759a5837dfb271b29cfb46f00d69e809fc418edabc`  
		Last Modified: Mon, 04 Nov 2024 23:25:58 GMT  
		Size: 2.7 MB (2692615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23fad6b3642def2be48a1844132dbde82a319fe13e4cb4378691f2cfef3d8de9`  
		Last Modified: Mon, 04 Nov 2024 23:25:58 GMT  
		Size: 59.9 KB (59886 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:f2d1d632e53629b7c218317437b4c94a8be778faf96945df6c000f7509665bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73433117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433a4b39bb5473d6490608d5bc66727d76d94208de0f4d0b0077215dca480793`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 01 Nov 2024 11:35:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_VERSION=4.0.3
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 Nov 2024 11:35:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 01 Nov 2024 11:35:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b1382f054c61b7a19eb69a48f6b865f6a481932aa1dc6f95fde11de51e2f45`  
		Last Modified: Tue, 12 Nov 2024 23:28:53 GMT  
		Size: 39.7 MB (39693612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30952eec162b109ece354466298b6b3eb05decfdc81b0d729a94b2b305138f4`  
		Last Modified: Tue, 12 Nov 2024 23:28:52 GMT  
		Size: 9.0 MB (8995932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806f29ec6e04675d4a6c3a613f1fa7876d29dc5e52f6f33e30a9caf50ea3da6d`  
		Last Modified: Tue, 12 Nov 2024 23:28:52 GMT  
		Size: 2.3 MB (2321271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229f8a80a80d89fd746b18f1bb7a5eef056cbdfd6eb8c41270cd9e9bab4a576a`  
		Last Modified: Tue, 12 Nov 2024 23:28:52 GMT  
		Size: 18.3 MB (18332828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7cfb8505c0d8728517eb444797c0773365bb0d7dd3bbdf60c9cb4c12d3a173`  
		Last Modified: Tue, 12 Nov 2024 23:28:53 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12facdf69193ec1176ded409cbaa75a2c29254179659568e1cce533f1a647655`  
		Last Modified: Tue, 12 Nov 2024 23:28:53 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7091fb4a4c11491278732e1badb642e971ad7837263904b7146f8c905d4df2de`  
		Last Modified: Tue, 12 Nov 2024 23:28:54 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2377293a01e24107b98811189f875a29f17d843d86cb865bb5f7cb350ed302f`  
		Last Modified: Tue, 12 Nov 2024 23:28:54 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c670a5c5bdf471efb65d6158e4d5654268b8e03eb9044b0522b096a705838ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6490724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3128ec97df74c534f455f2bb26eabea151ab541cd784e13d2c6cce9e5cc2880`

```dockerfile
```

-	Layers:
	-	`sha256:03f38f14b58c3639bc8cae7a0649f0f35e3f583ebafe792b76677091a9521742`  
		Last Modified: Tue, 12 Nov 2024 23:28:52 GMT  
		Size: 653.7 KB (653727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:885667d3e91196d1b85a28f143bc91811cb12f469e14823428a348910a444989`  
		Last Modified: Tue, 12 Nov 2024 23:28:52 GMT  
		Size: 3.0 MB (2966342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d1e5de60e996e2d79578fa0bbf502d7026ab7dcf7b6e0e52456420b60eeb139`  
		Last Modified: Tue, 12 Nov 2024 23:28:52 GMT  
		Size: 2.8 MB (2810548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c77128d87d9b256371b7ff822f7310c0e4b05fc5ec45382d240d144237bde0f6`  
		Last Modified: Tue, 12 Nov 2024 23:28:52 GMT  
		Size: 60.1 KB (60107 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:6c39b2eaa4619a213440f21ea22021f6005f8024d286ba4bef674a6e54eb9b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64720865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e50eddebd93e0ccf979b1046fcd3094837e663b0f4105ed172efcab1d8fa98a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 01 Nov 2024 11:35:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_VERSION=4.0.3
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 Nov 2024 11:35:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 01 Nov 2024 11:35:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a9d543b1cce496e9110cd00c720cdfc0f3499a066ce6bd0e406efb7872c3d3`  
		Last Modified: Tue, 12 Nov 2024 02:52:29 GMT  
		Size: 33.4 MB (33360817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df41813501d8adb1d54c51b47dea7d0bf63d09b05ebe1d4b40c36175f8453c6`  
		Last Modified: Tue, 12 Nov 2024 02:52:28 GMT  
		Size: 8.3 MB (8324923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65537d7ce5f18fbb215f92f36210f5852ae9cc6a6dc3b2ac6236ebf6e404baa1`  
		Last Modified: Tue, 12 Nov 2024 02:52:28 GMT  
		Size: 1.2 MB (1231509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa885f10e9e4abe5febd5bc04b7abff66674c1a454dac58f2b61e1ca5978c09`  
		Last Modified: Tue, 12 Nov 2024 02:52:29 GMT  
		Size: 18.3 MB (18332651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5024e5a0d89f53e6d8c243e816b6a25dce6aa64d936954ee4555ab9e766cafb9`  
		Last Modified: Tue, 12 Nov 2024 02:52:29 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3223f098951bac40ccd87817357c244275e7ebf041476a4d4d55f2bd520868`  
		Last Modified: Tue, 12 Nov 2024 02:52:29 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b82e1a948fdbd2f9838506c58fcb9c60cc47f90905d36b39f21e274a84822a`  
		Last Modified: Tue, 12 Nov 2024 02:52:30 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8e9947bfc9d8d95048054356b67b58b92c914b7a6801f2fd08b818ce059bee`  
		Last Modified: Tue, 12 Nov 2024 02:52:30 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a9d0726089fb1905fa59fe13917d1a97c90246723f30b75d6199e53eb3e39e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6431743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf027480e28d8cf9e8f2f4e603dbb5ad6d8cf32f9b4a32fa06268fdd7ea7a29`

```dockerfile
```

-	Layers:
	-	`sha256:0e062c11cba48ccc5486ff77fe162e6e890ec17026b3e5cc624c96d17007ffb8`  
		Last Modified: Tue, 12 Nov 2024 02:52:28 GMT  
		Size: 648.2 KB (648205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1ae9b736a85415ba70bd431342ddcd5ac634ae32f5af9854796912898d58844`  
		Last Modified: Tue, 12 Nov 2024 02:52:28 GMT  
		Size: 2.9 MB (2939093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:677f4edc17172af7c7904c78cb8cf59701e8139df5ae3ef724bffa036198ee34`  
		Last Modified: Tue, 12 Nov 2024 02:52:28 GMT  
		Size: 2.8 MB (2784628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88c65b3ad55757eda7795438991bfb7be06356aedf9427ebc3ac769b251cab5c`  
		Last Modified: Tue, 12 Nov 2024 02:52:28 GMT  
		Size: 59.8 KB (59817 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:6e7c4b80bc6cf2f681d9c89d663f871213562857e14ccf490feaf6acfa29f1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65707048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7ba6ec220ae84bc47e86b27ca6ee403181a6d47aa142250200c752861fe0d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 01 Nov 2024 11:35:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_VERSION=4.0.3
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 Nov 2024 11:35:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 01 Nov 2024 11:35:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f5ad3e97e9bfa3f4d5f47fc7131e93eab67354bae82c70f8b50e230d36a330`  
		Last Modified: Tue, 12 Nov 2024 14:02:31 GMT  
		Size: 33.6 MB (33620000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63928be000e86045eb82e1fb21732c02325ecf74bcee65534b8592364be39e5b`  
		Last Modified: Tue, 12 Nov 2024 14:02:30 GMT  
		Size: 8.8 MB (8834116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46437d58f20212a6202d945fe84cf3c607cac336ab4ae7661f8f39f629d60d92`  
		Last Modified: Tue, 12 Nov 2024 14:02:30 GMT  
		Size: 1.3 MB (1346113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666bb3566112bc371276bf1c1a149f54d52547310a8cd3c01b6fc8b636d051e6`  
		Last Modified: Tue, 12 Nov 2024 14:02:31 GMT  
		Size: 18.3 MB (18332614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efedd4d22b91fe58015c33770fbcf5b01c5e145e628b7b383eb7eac095b381dd`  
		Last Modified: Tue, 12 Nov 2024 14:02:31 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4756996532c7f2f547d62653459b6839ec68ec909198c52f8f7e73b7db331221`  
		Last Modified: Tue, 12 Nov 2024 14:02:32 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6483801ea84ee951a4a91c362f75646482325bb181b29e295a978ba2ce56b25b`  
		Last Modified: Tue, 12 Nov 2024 14:02:32 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af96ce5a0fd4bd8488bd05bc80fe32982229647fddd7a3180973fb5eae99b7d`  
		Last Modified: Tue, 12 Nov 2024 14:02:32 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2ab76759c0765495ef324305bd64901272066c568688e648a727477a6c150ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6428812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3cefa23a0dc5eb29f6446d99ce099936cda7cba7d89809d4a6f4ac7286ae2c`

```dockerfile
```

-	Layers:
	-	`sha256:e2cc4b75f732255d6d687a956c0e95f6861f4ba29173c956704cf3f742b43c2d`  
		Last Modified: Tue, 12 Nov 2024 14:02:30 GMT  
		Size: 647.0 KB (647048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c982ce70b32b004f221c5c48d9ca7102d2100c7c6c67d62a05d2e375aaf282c`  
		Last Modified: Tue, 12 Nov 2024 14:02:30 GMT  
		Size: 2.9 MB (2938820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c66613f15e751fa911b6678842f04492b1a2625eb7be7c26e4ed281fe8964829`  
		Last Modified: Tue, 12 Nov 2024 14:02:30 GMT  
		Size: 2.8 MB (2783014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8005531111b64ec41c8be2946140381df5c7b9c8a5af42105ae15857d9e9ddfa`  
		Last Modified: Tue, 12 Nov 2024 14:02:30 GMT  
		Size: 59.9 KB (59930 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:fc1d95e163ecfd5c53029ed9b80c7746dcb19aff73edd3d643001609c6ff7e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67421414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a272621ac68dffc0ab16ac71e1d79cae9a88d918f24828d80e1da5caaaef3a9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 01 Nov 2024 11:35:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_VERSION=4.0.3
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 Nov 2024 11:35:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 01 Nov 2024 11:35:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231d316d714595ab60188c35e3b60375cbc5fd414b2b09da936fce41dd04ae38`  
		Last Modified: Tue, 05 Nov 2024 02:14:40 GMT  
		Size: 34.6 MB (34577921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a0650eef7070e4a6481044074d94e9b556b5bea3da2f4bcda6feea9f586fd1`  
		Last Modified: Tue, 05 Nov 2024 02:14:40 GMT  
		Size: 9.9 MB (9866553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ea38c37d2c62fbcf0bb479680843f19bd4dcab4364b0f0abc56eee5a07b034`  
		Last Modified: Tue, 05 Nov 2024 02:14:35 GMT  
		Size: 1.3 MB (1270921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5f49f177f3b94f6097251f4e286e71eb9884c8288cccef205b0dc79002451c`  
		Last Modified: Tue, 05 Nov 2024 02:14:38 GMT  
		Size: 18.3 MB (18332814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825b02eb4262d035f6149d8da4e2c0892dd3e9e126251601a9f38aad87e8dafd`  
		Last Modified: Tue, 05 Nov 2024 02:14:36 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50799c5c017decc2eea4b660901d0dc8d21a84ddb6276a83fd22649c9482480`  
		Last Modified: Tue, 05 Nov 2024 02:14:37 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86a6b568d6ae3f256eac24fa092f67ac630aa411406ee0b85c57d7522e47552`  
		Last Modified: Tue, 05 Nov 2024 02:14:38 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721d59d2bc2069b1ab64c740d6439230a70f24b8759b6611d258f296f1d6591d`  
		Last Modified: Tue, 05 Nov 2024 02:14:39 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:eab891efd9aabe6c873b4254bba082c2d9e03e7f445cc65e364ed355a526fbe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6463738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e116cf91024f0850e0ad9db6c7e77d0607e9b3eb61cd999b19607b90566d0199`

```dockerfile
```

-	Layers:
	-	`sha256:efa070ab92540a3537053420e4fdc163f2feb79b71e6ac32613c864c11b59fdb`  
		Last Modified: Tue, 05 Nov 2024 02:14:35 GMT  
		Size: 649.9 KB (649891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b58ea1fb26f5de31000c0a9f3eaec5c87756c5afc4bed5d60efb87e01458f546`  
		Last Modified: Tue, 05 Nov 2024 02:14:36 GMT  
		Size: 3.0 MB (2954943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ad8138a5459645b4900416f345308d02b3aef9baa35bfa1c0df0d8e6d7f4828`  
		Last Modified: Tue, 05 Nov 2024 02:14:36 GMT  
		Size: 2.8 MB (2799149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcebda419e1d149b44f8f162ada04ca8691739a4c0dafb2d770a4e846419193`  
		Last Modified: Tue, 05 Nov 2024 02:14:34 GMT  
		Size: 59.8 KB (59755 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:3630511780b733873d9d9c8bd7e276785a914f778a3ae85667be71c0a9764cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64294103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b042df98bc04c6e92ef65e6770f9d4efa897799bc8f31159afb478866466319`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 01 Nov 2024 11:35:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_VERSION=4.0.3
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 01 Nov 2024 11:35:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:35:30 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:35:30 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 01 Nov 2024 11:35:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 Nov 2024 11:35:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Nov 2024 11:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2024 11:35:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 01 Nov 2024 11:35:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2e644be2dce127c9fcfc43e4fd49d151aaa4cc7d89694d9888ed435e676517`  
		Last Modified: Tue, 12 Nov 2024 21:19:04 GMT  
		Size: 33.7 MB (33691048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e67f572d430d1571ac953f6550546cad4f3d62c9d3a777d1a44e6431a6f5bfd`  
		Last Modified: Tue, 12 Nov 2024 21:19:02 GMT  
		Size: 7.5 MB (7481838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e844abd1c984f822b833e2e90834aa23a5fc7a96478de98e323a30c25b341d14`  
		Last Modified: Tue, 12 Nov 2024 21:19:02 GMT  
		Size: 1.3 MB (1325213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2236c1a48f8867d114b4a1ef33468e8735945abe06650b57e2dcfee0ac40feb`  
		Last Modified: Tue, 12 Nov 2024 21:19:03 GMT  
		Size: 18.3 MB (18332649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1fb4893b8ddf1691605962ecf0cbf94487e59676d0d411add5be6fbb9d4acb`  
		Last Modified: Tue, 12 Nov 2024 21:19:03 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce560fe9fc196157dbdd93a2b796bc6afd9d7a23557cbba39a4ce5107f624d0`  
		Last Modified: Tue, 12 Nov 2024 21:19:04 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1db66a6f849d99d2bb4935c539946d65673cb17d513a556964258b79be520d2`  
		Last Modified: Tue, 12 Nov 2024 21:19:04 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666c3356150f5514d7a64dea192a110e9ae01b7b3d88f12c891b45d94ea97a71`  
		Last Modified: Tue, 12 Nov 2024 21:19:04 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a783fa94fc596da9eea14b6ba2650b987842cc145fdcdeff6cf64d569f53514c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6262852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ad080d203fcf01b08bb92add5d1ec3211648e9be91444c4902a16ab9093ea7`

```dockerfile
```

-	Layers:
	-	`sha256:b6c669b756cbc8bf9fb777f370f4dc994128bf84ba8196de4276c60212a7e28f`  
		Last Modified: Tue, 12 Nov 2024 21:19:02 GMT  
		Size: 647.0 KB (647014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a15f57d671e0196f345d2784bf0e2928dc0e0dd612da04ef82a99d09e0846215`  
		Last Modified: Tue, 12 Nov 2024 21:19:03 GMT  
		Size: 2.9 MB (2855873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dc118621d211f4e712cdaebffe38ec0f2c42941b9ae2ba3f79484a271da270d`  
		Last Modified: Tue, 12 Nov 2024 21:19:02 GMT  
		Size: 2.7 MB (2700097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e525fdaf5639ea366a5b46cbdb3b3b0127d12daa7933a146160143fa2efe774`  
		Last Modified: Tue, 12 Nov 2024 21:19:02 GMT  
		Size: 59.9 KB (59868 bytes)  
		MIME: application/vnd.in-toto+json
