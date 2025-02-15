## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:c651b2ce81489449a11ed89c4de9045be91f22f805395a594c8ef7e94a70671d
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

### `rabbitmq:4-alpine` - unknown; unknown

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

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:df648ddf12a3137c298b198ebba2f4f852c2093a98982e1971849ec4a631d6ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65688157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b1f990b014b3b6707101eff42a44a63c2cafc73953dff1f57e7ad366ffda3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b976bbc82ee5ea001e17a95ea52cc52e04e53b5c55633e2541d239430e944532`  
		Last Modified: Wed, 12 Feb 2025 18:52:34 GMT  
		Size: 35.6 MB (35604128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240521bf547a593904dc3bdd837378f26e5471f29e78e98218d69156e72f020f`  
		Last Modified: Wed, 12 Feb 2025 18:52:42 GMT  
		Size: 7.1 MB (7097952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3950e22a9c8b8c5b7eda96513b7ebf8bbd02818d4031004dca870b6bae74928`  
		Last Modified: Wed, 12 Feb 2025 20:03:38 GMT  
		Size: 1.2 MB (1225392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d5489acce0cc56a2ae1ea02be0141d9c5d66b2e7254bd1c8732fe76e31d819`  
		Last Modified: Thu, 13 Feb 2025 00:27:42 GMT  
		Size: 18.4 MB (18395055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e350684f7b4c78199498a0c3cba9aaf43f43220aea81cfba652d77ae1ffca4d`  
		Last Modified: Thu, 13 Feb 2025 00:27:43 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c9e22e42148958bba924c11059ea22a1c35306faf36abaa551037f96912a4b`  
		Last Modified: Thu, 13 Feb 2025 00:27:43 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecad1233dda98ae3f36c29ff83842e9f20859c07f2eb8fc66e0965ead316d00d`  
		Last Modified: Wed, 12 Feb 2025 18:52:45 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae39938d77d0aa298aa49937dff4cb170549aefaf66d4c7436ad60741e33257`  
		Last Modified: Wed, 12 Feb 2025 20:03:42 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9987f6b51999a3a9dbf2e25b906fa1082b1171862e037c1aff8e1deb21ad8dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 KB (59836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0702fe3e21cd84835b9b2bec3178c7e3fd45a5373673e9504a8607504c7978`

```dockerfile
```

-	Layers:
	-	`sha256:c39d4ed27772a5f781fc9fb3947181c6d293c208699cdea28c936ee8e4b6fac8`  
		Last Modified: Wed, 12 Feb 2025 20:03:43 GMT  
		Size: 59.8 KB (59836 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:686a60583fec2fbee2ba87fde6e62507590e4e0e99de6974927b83324abe22c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64889722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79c292d1fad11dbb34f865839703670374822a9e6e449c1f2a184984b37e459`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c52ae3a3e5eb5fda9dd4b433947369cefff8544d3f25d441646508cd515ddab`  
		Last Modified: Wed, 12 Feb 2025 20:03:48 GMT  
		Size: 35.5 MB (35520179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2075462fbbff37c06f72c948a68fdb293bf6207205ee59b6bdef6bf2fcecd7`  
		Last Modified: Wed, 12 Feb 2025 20:28:53 GMT  
		Size: 6.7 MB (6742202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c258f4352e6afdec543b21b67ba9a10425aae39a6e735d02fb31c1e19cc48f7`  
		Last Modified: Thu, 13 Feb 2025 00:27:43 GMT  
		Size: 1.1 MB (1133190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5007d157d71f017d24275bf890cdf11e3955505951c62f3288315f53f1a1b4`  
		Last Modified: Thu, 13 Feb 2025 00:27:50 GMT  
		Size: 18.4 MB (18395295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28551afbfff68e6ac1d1599438dc808f7d23370272ab5a526b34791bbc36ac1`  
		Last Modified: Thu, 13 Feb 2025 00:27:44 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10397df66437b47b9dac564595d495187163cfd0725eab841d62b68596a80f7`  
		Last Modified: Thu, 13 Feb 2025 00:27:44 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b579502c050e80a1d5b8755038ff3868b8d2922f860cfc63461412404568bf0`  
		Last Modified: Wed, 12 Feb 2025 20:03:52 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9231c1daf5f00c728ed39b28f8e8a0453d1f499856625ed866b027b626cb112b`  
		Last Modified: Wed, 12 Feb 2025 20:03:53 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f8326f97a73c1b88793add3959c96846d8d4df02e8bb6bf2b31a603093f910b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6494325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027d8b756bc8da98ca5f4ad4d53f4e09808e5a3753eb81f7d7513e6e0908c3d5`

```dockerfile
```

-	Layers:
	-	`sha256:23dd36f1d24a1c8c8ba6e2255f62b0f0c615d636a9c48f496f37ff8b7771c6fb`  
		Last Modified: Wed, 12 Feb 2025 20:03:55 GMT  
		Size: 653.9 KB (653933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fa09990737587bcbb12ad942ef557881c301c01765ce0244c20570fa48605ae`  
		Last Modified: Wed, 12 Feb 2025 20:03:56 GMT  
		Size: 3.0 MB (2967737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0460eef266eabb036718dd93c8e3e86208462eb02c6d9e048a5a0536b9816515`  
		Last Modified: Wed, 12 Feb 2025 20:03:57 GMT  
		Size: 2.8 MB (2812604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e66e8a17028f907481718e70206b6ef6fff4086426252fd3a2931f36283d44`  
		Last Modified: Wed, 12 Feb 2025 20:03:58 GMT  
		Size: 60.1 KB (60051 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:7437693f807c72904d60666df9571cd3b34cc7ea3f0c8503a244a9c86e5a1f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76747662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb63f510d71e102c7d6f8b61c9c0ddde3a578aa23e21903dd370920189aa1308`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324f06bb94a36cf7619c9350f754e5b39d50f4d65bb9ceded483bc311a5beeb7`  
		Last Modified: Wed, 12 Feb 2025 20:04:02 GMT  
		Size: 43.0 MB (43001066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982bfd2bb11a59a26dec89cfe125eab2792c6065407c91e69dada25bd945db19`  
		Last Modified: Wed, 12 Feb 2025 20:04:03 GMT  
		Size: 9.0 MB (9034864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f727cc928a164645e47cc2d6bae91a779b41f4668ff9f8b0116b80e8fbd1c366`  
		Last Modified: Wed, 12 Feb 2025 20:12:19 GMT  
		Size: 2.3 MB (2322590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de893231489b9cb41ae796d632c0e83e3fae651ea5e0abc7e2e6dbed900fbeb`  
		Last Modified: Wed, 12 Feb 2025 20:04:33 GMT  
		Size: 18.4 MB (18395042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a26a99da8a67cbc4053fa0466bdbc7387d74bce1a9899b470d6caa6c417de`  
		Last Modified: Wed, 12 Feb 2025 20:27:28 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa970f8e5850eb7cb48a96b4f00d0f819a54d814c004283dcf039214df710e3b`  
		Last Modified: Wed, 12 Feb 2025 20:04:32 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6839ec47be9794a3730dddd255a08f9ac627a268e031632060f1f81dd408a542`  
		Last Modified: Wed, 12 Feb 2025 20:04:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c8f146a558490234fe60bde80dafa278db0d385ddc7dd1f1c81ba495993317`  
		Last Modified: Wed, 12 Feb 2025 20:04:34 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:78aa3244eca7bef6597b05b56bedb5a20ba83d81a19808d1f8f51d5c67c3ef42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6836933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743cae0d5a3232502a2b9b23ce6d2dda6b83e988c39231ca818f2aa4b3ddd30c`

```dockerfile
```

-	Layers:
	-	`sha256:74dc58b848f31859c1e9ae02bd39490d32b2ea506c21ed28a8fdf5bfb659d1bc`  
		Last Modified: Wed, 12 Feb 2025 20:04:09 GMT  
		Size: 658.6 KB (658579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50440ddaa1800096884adedef7221aca2c05c248ae6982a140be8f494aa0c012`  
		Last Modified: Wed, 12 Feb 2025 22:53:19 GMT  
		Size: 3.1 MB (3136692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:836e3f04c7dc87fad91e04693e88518ffaa8dc691e61182095b3febdaa719cd7`  
		Last Modified: Wed, 12 Feb 2025 20:04:11 GMT  
		Size: 3.0 MB (2981565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:329b2a946d780274772681642d38e872c903c753b0cf7695ab2659718f3588eb`  
		Last Modified: Wed, 12 Feb 2025 20:04:12 GMT  
		Size: 60.1 KB (60097 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; 386

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

### `rabbitmq:4-alpine` - unknown; unknown

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

### `rabbitmq:4-alpine` - linux; ppc64le

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

### `rabbitmq:4-alpine` - unknown; unknown

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

### `rabbitmq:4-alpine` - linux; riscv64

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

### `rabbitmq:4-alpine` - unknown; unknown

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

### `rabbitmq:4-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:6af561edf5cb0696f10875adf62fcb63add6e3d81b60e287820efbe1e98562a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66802817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcd4ec590a4b8cffcebe44b1c85d1171daf9083712e08251cc5f1d3206379a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a53a23f97b0d934ecc30a13dd3ad6c763f6156bf2e963521116b7c40d9871e6`  
		Last Modified: Wed, 12 Feb 2025 20:04:49 GMT  
		Size: 36.1 MB (36104648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9fd957d31eb916c02d92d8bf3469c2b57f7a263c8749ee08e4405cf2eb321c`  
		Last Modified: Wed, 12 Feb 2025 21:34:23 GMT  
		Size: 7.5 MB (7510912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b0531c9bae0a239fff1e62aded8eca81c92cc822843eead07b19564aad4e47`  
		Last Modified: Wed, 12 Feb 2025 20:04:51 GMT  
		Size: 1.3 MB (1323349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606294f6619f44e7b9f2140f21c8f427529ecca5696ca46b2f25f6dcd9067add`  
		Last Modified: Wed, 12 Feb 2025 20:04:53 GMT  
		Size: 18.4 MB (18395289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e018a770f0517726a77b4de966544c498559a4b2df03ad46fdf837020741ada`  
		Last Modified: Thu, 13 Feb 2025 00:27:53 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d100e7267af6901d82955a698e6a48fb8cefb6f9b96b4e59ee5d1c7ef1e3b707`  
		Last Modified: Thu, 13 Feb 2025 00:27:53 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a00c64ac1c88bfd118f6fc2085bef2f5d615eee2c8ddc7d0985b46329e2b3f`  
		Last Modified: Wed, 12 Feb 2025 20:04:56 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d72335ef8365ebdf12e463e811bb4b2fdc31b8d13c25951aadbe897f2cf065b`  
		Last Modified: Wed, 12 Feb 2025 20:04:56 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:5cc167be8c08f6fd16cd0417526e52c52c849f3bb488c0c4be81aea3e29a3f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6512470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e308443a5493aa9f3a1d884c13ea12bc8af15374951f07fd6bc7f679ee2c1ed1`

```dockerfile
```

-	Layers:
	-	`sha256:6d4c87c6fb513ec191e69482fd7cd51dd262b6e80c8a6b38df01c9d9c57aa62a`  
		Last Modified: Wed, 12 Feb 2025 22:53:33 GMT  
		Size: 651.9 KB (651946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e80915f9d718d3926d6ce226b00f6082f5e4bc23dea2dd95a51baf8aa326c48`  
		Last Modified: Wed, 12 Feb 2025 22:53:33 GMT  
		Size: 3.0 MB (2977888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4733e7d6e8d7cef2fd388e4c7b236dde34719576e58967b5e1483cd8b8959685`  
		Last Modified: Wed, 12 Feb 2025 20:05:00 GMT  
		Size: 2.8 MB (2822779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c23b3908df08c1319de6959b3d71d9f80cc3a749caedad1f39972ea8f9206a8c`  
		Last Modified: Wed, 12 Feb 2025 22:53:34 GMT  
		Size: 59.9 KB (59857 bytes)  
		MIME: application/vnd.in-toto+json
