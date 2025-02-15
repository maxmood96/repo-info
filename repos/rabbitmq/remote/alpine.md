## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:fe198e696a90ced008ff5fb3fcfc5d19da18495908be203fbf060d1dab91cb1d
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
$ docker pull rabbitmq@sha256:74217638d18b3f1da912ceb85596d25a357478999d0dc72e27ff9762a98abc60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77620745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8a8b47bc3b8927908c90349c34bfc7b4cafdd9798f8985b9246a5b378c9da7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 11 Feb 2025 18:31:38 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 11 Feb 2025 18:31:38 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_VERSION=4.0.6
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 11 Feb 2025 18:31:38 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e24e41057b5d7f91beccc6a2655c19c7d4dbb3d725c93b7d95ec5fd238d206`  
		Last Modified: Fri, 14 Feb 2025 20:38:40 GMT  
		Size: 45.0 MB (44992377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ecc9605ad2af643cb9a9be4ab4919a54209bd450f09740884861930294b0d8`  
		Last Modified: Fri, 14 Feb 2025 20:38:38 GMT  
		Size: 8.3 MB (8311649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e282cdcf18a00ce31e7472d8c003951625c04f04d7d2e072bbd827baa3b6ea`  
		Last Modified: Fri, 14 Feb 2025 20:38:39 GMT  
		Size: 2.3 MB (2277698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f974cac6a1dd9847931bfe3886a30ce95ae1f14bfc56e3a2126f9a3f2a7daae`  
		Last Modified: Fri, 14 Feb 2025 20:38:39 GMT  
		Size: 18.4 MB (18395031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c6ae7723c430cb3695da035b5c18c46eeb306630ee7e21d80106fe8a72f22a`  
		Last Modified: Fri, 14 Feb 2025 20:38:36 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44846c63ee4b8b899061d6c831788a77742428d2cb9deff74e689e801c4f8c7e`  
		Last Modified: Fri, 14 Feb 2025 20:38:36 GMT  
		Size: 105.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9039f1b33edd529f4372cef62d4a597016cc6d2e328e9ac72f3df7c9f721a9a9`  
		Last Modified: Fri, 14 Feb 2025 20:38:36 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1742075626ee45cf5c20428c707f39bc768a7fb37ba8415a73e94635a8294ee8`  
		Last Modified: Fri, 14 Feb 2025 20:38:36 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d1804366d748c21760488d5a0d27e45eb229cd1f8c97e726872c4d7ef5d7f99a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6458442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68eaad14fcd3737f6f22edaa7e055ad9b0f1c6ff81919f75dc8af7b486301453`

```dockerfile
```

-	Layers:
	-	`sha256:028d99dac8001f76c32124b79e4525f92ae6bb6b02f8841ea759083a333251f6`  
		Last Modified: Fri, 14 Feb 2025 22:53:18 GMT  
		Size: 538.2 KB (538244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f372141bbee56ab886b4dbfcebf7fe4e0402feb76f39ac7e0130c06d7c967548`  
		Last Modified: Fri, 14 Feb 2025 22:53:19 GMT  
		Size: 2.9 MB (2932259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92a559a3cd80ba18170f669208397a4d08e17ad2da69b9b3205e4d70a11f4364`  
		Last Modified: Fri, 14 Feb 2025 22:53:19 GMT  
		Size: 2.9 MB (2928081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6a2ef29351c4623300f1e32de458b5863e36a6f5f3947eeb303793e0ff645c6`  
		Last Modified: Fri, 14 Feb 2025 22:53:19 GMT  
		Size: 59.9 KB (59858 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:79b7cb5902a2ad8a3c5155ce383dfe8f420511eea5675ef52bc47d9f09255b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65688673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823749719a4744bd3b05f0c8a0dd814c840ec3c7ef0324e2935964721ef5521e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 11 Feb 2025 18:31:38 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 11 Feb 2025 18:31:38 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_VERSION=4.0.6
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 11 Feb 2025 18:31:38 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3379e3ec68a2fca90b8a118fb0bd7384107c3c8d7dc45bbd8e8da582699df3ac`  
		Last Modified: Sat, 15 Feb 2025 09:09:02 GMT  
		Size: 35.6 MB (35604017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e6060aa0f3b1ef8772f87c58abb2f5a4a529db437cb5d530df89c2f49a1fb7`  
		Last Modified: Sat, 15 Feb 2025 09:09:07 GMT  
		Size: 7.1 MB (7097977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffe73773e52a42f3df67f2471061b907a563d0d32622407c898fb8113c8414c`  
		Last Modified: Sat, 15 Feb 2025 10:53:38 GMT  
		Size: 1.2 MB (1225229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1739dfed6762b51c0e2fbdabb8c11cbb1dfcebe01951bb4f38d31373da854fb4`  
		Last Modified: Sat, 15 Feb 2025 10:53:40 GMT  
		Size: 18.4 MB (18394966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cbfbb247c72eb96ebc521b48163ac4daeeae6f704a7a4f754422cebb75f05c`  
		Last Modified: Sat, 15 Feb 2025 10:53:38 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1b3f7e457cf120d129437ff69485d3b327ae0e82391ca0bc59f4e48034c6d6`  
		Last Modified: Sat, 15 Feb 2025 10:53:39 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670bd21bdfe8b31ab3499b1300ea699c1afa05aceb540bff67f913b901047b33`  
		Last Modified: Sat, 15 Feb 2025 10:53:39 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7759a760faa481035a943747814e087013329c8827b772ef075facd8659d33fb`  
		Last Modified: Sat, 15 Feb 2025 10:53:39 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7d64ddd2389ca30429c3941330da66222c428740d3cb68e53f991aced54d82c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 KB (59835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72baad49c708f64b072007e39df3ad98fb11d698e3372d6510fe96978f59b53`

```dockerfile
```

-	Layers:
	-	`sha256:4665007b48edf7490a8e7688078b2266c56f265f4c03a57aa7035a6d12bf7aad`  
		Last Modified: Sat, 15 Feb 2025 10:52:50 GMT  
		Size: 59.8 KB (59835 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:91cd684803b50a6ed2f0c93497993f52bd92875f52223439101a16002352118b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64890506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76e52404c1c7f9aac69829a6a136701ea627368f8838876b797988446d459ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 11 Feb 2025 18:31:38 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 11 Feb 2025 18:31:38 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_VERSION=4.0.6
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 11 Feb 2025 18:31:38 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71067497b007faf314b0e1a7ee3adcc57891b83d19974c4fbff6298cd1471893`  
		Last Modified: Sat, 15 Feb 2025 12:08:20 GMT  
		Size: 35.5 MB (35520138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db397b196c9712f226207d68853af8196f22f7e94a7fff35ca690e2e067365fd`  
		Last Modified: Sat, 15 Feb 2025 12:08:24 GMT  
		Size: 6.7 MB (6742213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c1aa308be711b6aff6cf24e79411cbcaf86eea785850090ebe3aa60e1ff6e0`  
		Last Modified: Sat, 15 Feb 2025 14:02:17 GMT  
		Size: 1.1 MB (1133021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04aac5fdc47f3af25172cc185c714ce1283ff2a4e927a465f7adcf8f01839a02`  
		Last Modified: Sat, 15 Feb 2025 14:02:19 GMT  
		Size: 18.4 MB (18395275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26770032d8cb521013293216722734fe6d9e4bc71b008cf1642a4206caee0a4f`  
		Last Modified: Sat, 15 Feb 2025 14:02:20 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76059ac46f865d8445cbf9dc81af75716e9a3457071c6da694ddf2ca795f9988`  
		Last Modified: Sat, 15 Feb 2025 14:02:21 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d97d95a962b319e16c2ba4999d574cd2eac47ae915b11637b1d757ebd041170`  
		Last Modified: Sat, 15 Feb 2025 14:02:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868a3691ae38dee7ee821fbb97431d26dac7a4407120d90cdd515e7d10282c2b`  
		Last Modified: Sat, 15 Feb 2025 14:02:22 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a33b7168478c4519110c5da5131e183f1cc494063b7eeaa62da954417ac6aebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6494343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271e5ce5de4c7839d513af9d6e6c6f8fa5ec6488a0a055cd3d2adb04225241d0`

```dockerfile
```

-	Layers:
	-	`sha256:8d53608fd00ddbb592d713e722ecab77730d4c81a7746c0c5dbc723641e52d6d`  
		Last Modified: Sat, 15 Feb 2025 13:52:51 GMT  
		Size: 653.9 KB (653939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3943ea2440e77af3e02c1793e2b3bded7ff0e8c494eebde74997a920b07ddad5`  
		Last Modified: Sat, 15 Feb 2025 13:52:52 GMT  
		Size: 3.0 MB (2967743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:032309b4e3d75d55333150b4dd340af52b8b4be3e0c2fd7fb5155fcbca6858dd`  
		Last Modified: Sat, 15 Feb 2025 13:52:52 GMT  
		Size: 2.8 MB (2812610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60bf9ce8dcd5cb70e14128c11890e90d089c9e7b5f7fef55dd3e6da94d0fb3f8`  
		Last Modified: Sat, 15 Feb 2025 13:52:53 GMT  
		Size: 60.1 KB (60051 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:9b8c2efefa87e12dd20e06ce7b8f54142339c950b188f3a56fe4d6d45b46be2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76748459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9748ca5f6157d77d7846329a3e477f6b5ffac8d269e7f60f00b9d302c69795a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 11 Feb 2025 18:31:38 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 11 Feb 2025 18:31:38 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_VERSION=4.0.6
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 11 Feb 2025 18:31:38 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab519e59bfdd97d55857db538d74eed89f176f1c2441f192abaf0e195e9a9419`  
		Last Modified: Sat, 15 Feb 2025 06:09:11 GMT  
		Size: 43.0 MB (43001332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce984f4d8ccc59852ce4571d7ad3bd60ffd7386d046563fad875a8d663125923`  
		Last Modified: Sat, 15 Feb 2025 06:09:15 GMT  
		Size: 9.0 MB (9034855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b16b7ed98669b27ed3384695adafb75b033b3eb0bae8f3d01012d03e4a3827`  
		Last Modified: Sat, 15 Feb 2025 07:56:57 GMT  
		Size: 2.3 MB (2322457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17298e2827f7f0ab284f475fd888e8ec0cac0f1d7331b0b9e953ea4cb937548`  
		Last Modified: Sat, 15 Feb 2025 07:57:00 GMT  
		Size: 18.4 MB (18395038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7033c0587ff797d05811a392e8b154db2d30d46f12f41dd9d960e93be240d255`  
		Last Modified: Sat, 15 Feb 2025 07:56:58 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bec0f72046546270eb04dd2bbf425daf28b0d51f83378946b8763e12835503`  
		Last Modified: Sat, 15 Feb 2025 07:57:01 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1e23f98bcad52cf7574d6f00cd22bcf1b18af849abf68736fa2ef9296e7c5e`  
		Last Modified: Sat, 15 Feb 2025 06:09:17 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c67c57f3e2ef77759608fc02dafaaf6ed96389eb0a6ccee37f7cb252aa27d88`  
		Last Modified: Sat, 15 Feb 2025 06:09:20 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fe3865bdc9e9b456ed68897f9335c20daef632463c39f59c562ea8c5acb8e816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6836951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e823dd1c4d68e3e448ae7480244b25c6e3235365c257731f0f1ab727b0fe34`

```dockerfile
```

-	Layers:
	-	`sha256:7fab661a3a8030030cefcaac98c9bd5d5778944bd26750ff6f329dc5ed685235`  
		Last Modified: Sat, 15 Feb 2025 07:53:01 GMT  
		Size: 658.6 KB (658585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9638fe5fa0f2caa7d612f78967a00b63a8fbfffabd88f236c31e93bb4115fc6`  
		Last Modified: Sat, 15 Feb 2025 07:53:02 GMT  
		Size: 3.1 MB (3136698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3eeaae646f9323b4ac3127449d94f342350e0705f120621b9623fecc8742548`  
		Last Modified: Sat, 15 Feb 2025 07:53:02 GMT  
		Size: 3.0 MB (2981571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40cf9def46ca56b843b4da4e2f38788d801d9738da3caf9a6f54747b26a6cef0`  
		Last Modified: Sat, 15 Feb 2025 07:53:02 GMT  
		Size: 60.1 KB (60097 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:dbe606ab9a4c356b20d191b07c68bb376b4710eb2d315cac9f24df16ceb4be19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67108046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b15cf6b72ccbe467ee619d61650f331b42d21b30c59fd5c253af1a61097e1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 11 Feb 2025 18:31:38 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 11 Feb 2025 18:31:38 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_VERSION=4.0.6
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 11 Feb 2025 18:31:38 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b18fc1fcc6358a00d94ea44bf59330e3684960a3d32af6f4c781ede74595ab9`  
		Last Modified: Fri, 14 Feb 2025 20:36:56 GMT  
		Size: 35.7 MB (35693296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0ade995e9bba17c4ca14f6dc4c3b3992f3c84275cdeed301c8af38dacba05d`  
		Last Modified: Fri, 14 Feb 2025 20:37:01 GMT  
		Size: 8.3 MB (8324861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18090257436a42357b55e2b6f56bcafa8e89c31c8ea4546716745d91f6150480`  
		Last Modified: Fri, 14 Feb 2025 20:36:55 GMT  
		Size: 1.2 MB (1229253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29ba90eb98023fe07c59e72abff8f9ef16bcfb8a946b7890483fed3cf64738d`  
		Last Modified: Fri, 14 Feb 2025 20:37:03 GMT  
		Size: 18.4 MB (18395261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df99e45bc276d3ebfbfa58c9a7f8a97f673033d9e8d07e30ff87c1673fd267e2`  
		Last Modified: Fri, 14 Feb 2025 20:36:54 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03466d40af99b35eb31ea153a188f1c803cef86774178fb6a1541190432ccc42`  
		Last Modified: Fri, 14 Feb 2025 20:36:54 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5874c15e6925eed1631d0595b06b2a508c59860c1bf5dbc32424d0b367f0ae32`  
		Last Modified: Fri, 14 Feb 2025 20:36:54 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886e39cca9bd9bed3fc93e5e30722a1a7433de5d6a9f6b74038c30ca72cbb25f`  
		Last Modified: Fri, 14 Feb 2025 20:36:54 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f0d2eb5bff1a851fb43ab8da7e800ffbf4c12371b284f09d7b34d455ea241042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6431637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74df4896626ee2af0ae9fd17d96c2467dcb0b3e543dab8f29f6cefeda193f703`

```dockerfile
```

-	Layers:
	-	`sha256:3c2d76962c02e0c5bf8716fc05cfa14847da22d7e2ed773ec0d40a3cdd6b57c3`  
		Last Modified: Fri, 14 Feb 2025 22:53:28 GMT  
		Size: 533.6 KB (533593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fa5cff1b985ca8b6ee79c94fe0fa145f7f83351e622ed0f9a6ecb8912678dad`  
		Last Modified: Fri, 14 Feb 2025 22:53:28 GMT  
		Size: 2.9 MB (2921205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c309cb780830a34df0707cda0f369657b7a218ccd6ce73d461330a12c17d0d5`  
		Last Modified: Fri, 14 Feb 2025 22:53:29 GMT  
		Size: 2.9 MB (2917031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68023771439d252e2219229b45540e8cc57f01892faf29c9229d8c7c1e6a4b45`  
		Last Modified: Fri, 14 Feb 2025 22:53:29 GMT  
		Size: 59.8 KB (59808 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:049ea131a9d67bc70bd0ed4ad7157ccf61ff113e4bbe1fe44a346f00e4de3762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68250921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e18db286e16eac4e39c244f1f4aac8353d232560aac0626540c3a6261d4692`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 11 Feb 2025 18:31:38 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 11 Feb 2025 18:31:38 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_VERSION=4.0.6
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 11 Feb 2025 18:31:38 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8baefa18f43b35df40134fecffbd37472cad655715971da91fe4d80dabb7d31b`  
		Last Modified: Sat, 15 Feb 2025 02:02:16 GMT  
		Size: 36.1 MB (36086204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f3106c014d890e6ab80d502ab12152b764a8f56d5864cbbd59446729d16362`  
		Last Modified: Sat, 15 Feb 2025 02:02:18 GMT  
		Size: 8.8 MB (8848303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a95591a1dfd58d48a73bda0dbe0bd0c0fa7b4bf90457b78c6821ff52c81205b`  
		Last Modified: Sat, 15 Feb 2025 02:02:19 GMT  
		Size: 1.3 MB (1344999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708a73afe1127cbd9f276c3edbf9b87404c68ba9b3f39832004d705c83658bab`  
		Last Modified: Sat, 15 Feb 2025 02:02:21 GMT  
		Size: 18.4 MB (18395319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f39bdf5fa5eee3312c37b839bca746e976fb13246646ffa94520fff19ce07d`  
		Last Modified: Sat, 15 Feb 2025 02:02:22 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f53405b27c3432e342d1f1f7877aad21dc45f952bf0df2c1df73dc3d38e5633`  
		Last Modified: Sat, 15 Feb 2025 02:02:22 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3ffd6e02ec8d7505f460b40879bfe6e857952e255bb9ce7b3f9ab1fbbb1fd7`  
		Last Modified: Sat, 15 Feb 2025 02:02:23 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc3a303e7e5b4c3217d99fd2a2f2967f7fb9d59bfae98c2785c4416fe693c1f`  
		Last Modified: Sat, 15 Feb 2025 02:02:24 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9e4745cd46d2f98c6b24edbe0658f65eaeb4fc92c3ef8794ca1fe7fec8437d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6732619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df303b6276b49cd79b33d8b146237ad1cfe153e38f3ec8393bfa27611867fd70`

```dockerfile
```

-	Layers:
	-	`sha256:e460e80a303808786239b2000fe13c53eab0602799fe01f8e9d971633193b69c`  
		Last Modified: Sat, 15 Feb 2025 01:52:54 GMT  
		Size: 652.0 KB (651986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e1c5024f4e4051a96bb01428861fee344a83f9be82e4c09b5d4fcedcc6d1d6d`  
		Last Modified: Sat, 15 Feb 2025 01:52:54 GMT  
		Size: 3.1 MB (3087927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f68fb812e0792e9a5be47398689b6224a948144057ca905752d8c656619f16d`  
		Last Modified: Sat, 15 Feb 2025 01:52:54 GMT  
		Size: 2.9 MB (2932788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:027afb48508179b85a92db6cb8649332af0fa6a58e112016ea6fea227ac1cc66`  
		Last Modified: Sat, 15 Feb 2025 01:52:55 GMT  
		Size: 59.9 KB (59918 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:bf799dc38082f19f9692c71d95ac1b7445198724634cc7e82ada0365893104c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69897734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496eddd5f7307a4e9c865eb3733f3ae68dc4b9e4810d4d0b96845529a2e7272c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 11 Feb 2025 18:31:38 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_VERSION=4.0.6
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 11 Feb 2025 18:31:38 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9886a7e03dbc5df22591eed48d7c458d6616776bce01ed2b07bb0a9dc308cf4c`  
		Last Modified: Wed, 12 Feb 2025 23:02:36 GMT  
		Size: 37.0 MB (37026812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494a13298ecc51fd839cd23cf61899b41202bcd732ff6020bcaf8d721a71a05a`  
		Last Modified: Wed, 12 Feb 2025 23:02:38 GMT  
		Size: 9.9 MB (9858956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fc48b995a0e5c674279d689b529fe1578f42a0527d2c74fb2199ece681cfdf`  
		Last Modified: Wed, 12 Feb 2025 23:02:40 GMT  
		Size: 1.3 MB (1265042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff83258439d5628dc78f915728e1e89ec69617fbabd0cd7b16210ecc4a8fe71`  
		Last Modified: Wed, 12 Feb 2025 23:02:42 GMT  
		Size: 18.4 MB (18394922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1464d3db17697d42217a3327d1d374c3d54b70bbe2f9008199a2ea6cb4bcceaa`  
		Last Modified: Wed, 12 Feb 2025 23:02:43 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcea1c7019b2d846df14e12eadd714ea95edac2ce591f77b444862e655a55223`  
		Last Modified: Wed, 12 Feb 2025 23:02:44 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2142470306af16ed217b866473ddc2440b9152aced9065ef561bcfa188db6fd`  
		Last Modified: Wed, 12 Feb 2025 23:02:44 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f4aa117899144b039b36d1f692e598d6a63fceba6d2f2aa0faf37662e6ebfd`  
		Last Modified: Wed, 12 Feb 2025 23:02:45 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6317bda03047f4ceda0b13dbe0c2899a891ff30316fa61693657567e217b7183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6810717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba60571c635fbb8e9668ea32005c09ee40d75fd790a6e65bcc2104091a4a012`

```dockerfile
```

-	Layers:
	-	`sha256:403504c0618018e18440e244ab9e7a0670fec88f876e2a9b95c9cb4887cebc28`  
		Last Modified: Wed, 12 Feb 2025 22:53:29 GMT  
		Size: 654.8 KB (654772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b4bd7164bde934a60cc4f3c398de9146e2dad22e298b3734abf274d841bb3cc`  
		Last Modified: Wed, 12 Feb 2025 22:53:30 GMT  
		Size: 3.1 MB (3125576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af4424cc54c44ed15dacb75d45f18204b7bfa3f78c3961288ba2b8b92798b49b`  
		Last Modified: Wed, 12 Feb 2025 22:53:30 GMT  
		Size: 3.0 MB (2970449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25d245c2546ce5a15c29f0a78a7df7f7353212b5e5270f8ca8989618fc91bde0`  
		Last Modified: Wed, 12 Feb 2025 22:53:30 GMT  
		Size: 59.9 KB (59920 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:b84e90ddf99a784062da82bcb9653bf5a3e87ab6eae5645061390d6a73f17fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66803318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bc04e87db5e9c4a472fed33d28586fa76e34fc453e37af0291e4ec4a1ebc56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 11 Feb 2025 18:31:38 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 11 Feb 2025 18:31:38 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_VERSION=4.0.6
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 11 Feb 2025 18:31:38 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bddb23bfaed48f0faebd996321e476f9a51d7f672968e0577a69759b6411951`  
		Last Modified: Sat, 15 Feb 2025 08:02:30 GMT  
		Size: 36.1 MB (36104538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b11c2ce2ae686d8e4e9fbd18e27e792644f8da9ac651b2febf0b9e8065d86d6`  
		Last Modified: Sat, 15 Feb 2025 08:02:33 GMT  
		Size: 7.5 MB (7510940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932fdf5a972c63955cdc88436f8bff61663a1b5b12181905cf4e3d1ad3c759a0`  
		Last Modified: Sat, 15 Feb 2025 08:02:35 GMT  
		Size: 1.3 MB (1323225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017c71c2e0ab6f8928b274205ab9f818cdbf37e7e7cf9252a39dc9258555b509`  
		Last Modified: Sat, 15 Feb 2025 08:02:37 GMT  
		Size: 18.4 MB (18395302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e393ce43c0e898e286f68821d752a5a8997e7fae69848ade842f1794a842b4cc`  
		Last Modified: Sat, 15 Feb 2025 08:02:38 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbb33a270664891215875e0a5251eb443894c8a77435ab874e50c24daa86f16`  
		Last Modified: Sat, 15 Feb 2025 08:02:38 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305bde3957cd69d1408d9b665ed656df4bd46a926996bb448563a567f351e4f5`  
		Last Modified: Sat, 15 Feb 2025 08:02:39 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69dc964e9ac67252c7596c930278e07bec88f5586a4130876553ea60139062b`  
		Last Modified: Sat, 15 Feb 2025 08:02:40 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:40a75c269a83e0d969ec4439807dafd606d039d6a81bb01069236f7f4f509000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6512489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b73b91f7925176a6f8b464436b9a763d8326dc0d07dc2f478d26d18bf2668baf`

```dockerfile
```

-	Layers:
	-	`sha256:76d6d426f0d6e1324906d184f07e3f33e817eff3d6549d122981692bd80f3847`  
		Last Modified: Sat, 15 Feb 2025 07:53:13 GMT  
		Size: 652.0 KB (651952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e7002619f831a48bb7b2ad2bfabbae73478c1c5a8e7a379be1ee63f3775660c`  
		Last Modified: Sat, 15 Feb 2025 07:53:13 GMT  
		Size: 3.0 MB (2977894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a6717bfba76207d9d0f4b23d2a508382af429651c38a85b8a4e78a7fe681c7`  
		Last Modified: Sat, 15 Feb 2025 07:53:14 GMT  
		Size: 2.8 MB (2822785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46bd4bd8bd7d2e6bf27a56e2d2f9dba89e5f98dabe8de7d48bff791204716f69`  
		Last Modified: Sat, 15 Feb 2025 07:53:14 GMT  
		Size: 59.9 KB (59858 bytes)  
		MIME: application/vnd.in-toto+json
