## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:575de299f2c4f10006079e013987a5985b0cb8a6a450435fddfb7e60b248dcd1
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
$ docker pull rabbitmq@sha256:b706672b8cab1ba01d65750154dff008d3be516bccc942975a925b1097614e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77345561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391310bf614873bd2f6d7a6e89ea34cbeacee104c568ed735280d30b24a6337e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 12:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 11 Dec 2024 12:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 11 Dec 2024 12:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_VERSION=4.0.4
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 12:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 11 Dec 2024 12:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 11 Dec 2024 12:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 12:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 11 Dec 2024 12:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b54fc2ec9f671dad3389137578d2006a3b053acdb7b295b406608715c062d0`  
		Last Modified: Wed, 11 Dec 2024 22:36:31 GMT  
		Size: 44.9 MB (44864851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc6c0b52ffe61aa7ea7b910a2b1c5617f0dcc2537b97a1348b103ae0b7d9555`  
		Last Modified: Wed, 11 Dec 2024 22:36:30 GMT  
		Size: 8.3 MB (8284909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b864c9b719bccc76e830a47286aefee39a6b660b2877dc1b42a76d365638a`  
		Last Modified: Wed, 11 Dec 2024 22:36:30 GMT  
		Size: 2.2 MB (2234420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a87b772a7a11411a5378ce666c30c0613595a48332593dbea07d966c1689b6`  
		Last Modified: Wed, 11 Dec 2024 22:36:30 GMT  
		Size: 18.3 MB (18335735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac694565ffd9155ad780b59379297dd1ee235098ceeb535fcb36a196cc8baa6`  
		Last Modified: Wed, 11 Dec 2024 22:36:31 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352c8ddabb9519a66b9be9cb188d64a8b0842d3821256fd29980c6b4c2066086`  
		Last Modified: Wed, 11 Dec 2024 22:36:31 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd4ed56594dfddec814e842ed7c6bfb791013235e635a6e81a279a4870b9f5`  
		Last Modified: Wed, 11 Dec 2024 22:36:31 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ce51501734aea6e354697698893294b5f6cb2111a7a9c5e5257d69aeaca338`  
		Last Modified: Wed, 11 Dec 2024 22:36:32 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a0aab97d449b7a173b1dea8dc5c19192356f1fe669decfcdea4042f09ee1190c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6445992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae2f4d363a7698bd90b147b11af3def4f30e50603ed4cb4aed66c8190ea0c20`

```dockerfile
```

-	Layers:
	-	`sha256:ee4c996c402d4a03319cb6009b8d0ef2d0ab590b24f05f544109abdc143ea2a7`  
		Last Modified: Wed, 11 Dec 2024 22:36:30 GMT  
		Size: 652.8 KB (652848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f275a17e8708fce7adf166b818d38e2608d6db8ade6b2e96df7c97d8f80f844`  
		Last Modified: Wed, 11 Dec 2024 22:36:30 GMT  
		Size: 2.9 MB (2942987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f2b811b8ea980d0756a06fb78be1da2f83b77298997c96bbab042b301af4fa7`  
		Last Modified: Wed, 11 Dec 2024 22:36:30 GMT  
		Size: 2.8 MB (2790314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b000f2b801645e8a76b8a49e7c271f2ec08029a08ba89e670edb6ee665340e13`  
		Last Modified: Wed, 11 Dec 2024 22:36:30 GMT  
		Size: 59.8 KB (59843 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:48ae995018f9e26cdd81d2f48808423ae2369f2c1d43ffac08491684eaee85c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65517803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa889e25d73d7b68f751d36363a8717c438059115eb54cbd683a891e739c8cef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 12:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 11 Dec 2024 12:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 11 Dec 2024 12:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_VERSION=4.0.4
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 12:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 11 Dec 2024 12:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 11 Dec 2024 12:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 12:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 11 Dec 2024 12:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0078510b4b8c712d0d924707e9208f0601af66f99d63f1f63a8104f9af7ce0`  
		Last Modified: Wed, 11 Dec 2024 22:37:31 GMT  
		Size: 35.5 MB (35503760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908a404e76ca47a5e931f44da6a1b4f5399d516a827f39d71e8aed151172188f`  
		Last Modified: Wed, 11 Dec 2024 22:37:30 GMT  
		Size: 7.1 MB (7079916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51e669bc09dd1022bb32cf782b36f8868c3d2b9c2dd097f5a24fded80955c6c`  
		Last Modified: Wed, 11 Dec 2024 22:37:30 GMT  
		Size: 1.2 MB (1230010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620551c9bfc564804bb6d736c7801983f863a37407591c4d4cc33af73523848c`  
		Last Modified: Wed, 11 Dec 2024 22:38:01 GMT  
		Size: 18.3 MB (18335778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17818e85ec4b25499a1cc8c5de72ea07d0c998fef7ec839ed4d1bc818838af9`  
		Last Modified: Wed, 11 Dec 2024 22:38:01 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f12e4ce53fa317188158661489eb20e2d6e2e2006ef9920c73ae7478c42daba`  
		Last Modified: Wed, 11 Dec 2024 22:38:01 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2993fd7a1573bbfa2421e699ab27d8ff49509d2b3531f21936536b194d46a82`  
		Last Modified: Wed, 11 Dec 2024 22:38:01 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01f8fbfc3fde47de8a5ff25f8030075fa55255aadf2b59cfa92d5e5d72bfb87`  
		Last Modified: Wed, 11 Dec 2024 22:38:02 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4d789f2755e352c4acf13bf7633fc80795f08025abe5558d792093c10e7ada27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 KB (59822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4441aec0a4d9e816c1152737edd7a9c04aaeab3ed969dc432c1582ace7364d60`

```dockerfile
```

-	Layers:
	-	`sha256:5e78a29877b840af4e1de6bf56158e1a5dbb31cfe7c7151c37a8dc2ba15534fd`  
		Last Modified: Wed, 11 Dec 2024 22:38:00 GMT  
		Size: 59.8 KB (59822 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:38512d30538327e88cd33bd6705ffb2f28803158478d7f90ae3285ef275a3a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64707907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d468ea6293d00cff69b75126265fc2bf4d1066be8151901400df5c7737602f38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 12:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 11 Dec 2024 12:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 11 Dec 2024 12:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_VERSION=4.0.4
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 12:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 11 Dec 2024 12:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 11 Dec 2024 12:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 12:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 11 Dec 2024 12:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69e259e9ec24a361698f6bc8220be80fe3bf420e025114c4adb5c7239038b6d`  
		Last Modified: Wed, 11 Dec 2024 22:45:23 GMT  
		Size: 35.4 MB (35425148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa919152b6cad1944c2ce05a652125a9a89b0d1666dbfc7384fea586cb3708a`  
		Last Modified: Wed, 11 Dec 2024 22:45:22 GMT  
		Size: 6.7 MB (6716580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fc8bff7d8ac0de9e2f9dbdcbbcfe0da38009ee039fc0d4a646e5d371d98fd3`  
		Last Modified: Wed, 11 Dec 2024 22:45:22 GMT  
		Size: 1.1 MB (1132943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f41778be7212d13ad20ff0d96baf52f68bdfb9124019ed122b6dc385681a02`  
		Last Modified: Wed, 11 Dec 2024 22:47:31 GMT  
		Size: 18.3 MB (18336007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dc81389eb15e99aeaa0c814c0e51b911d40d70d07e755aae4443c46ba81bc9`  
		Last Modified: Wed, 11 Dec 2024 22:47:30 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772a25a10e7655a509124d838eec56848ca6b1c6599267f109a69fda16ff20e5`  
		Last Modified: Wed, 11 Dec 2024 22:47:30 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909b4187577c4d7fc232be0cde6efd9a08b989e3338b6270475848c3a7aa685e`  
		Last Modified: Wed, 11 Dec 2024 22:47:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16caa2a45992af4effdd6da2aecba601d47a4d9e61026cba9d96f4f8c938a7f`  
		Last Modified: Wed, 11 Dec 2024 22:47:31 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:618fc0aee8e7beb79aafd7c46368b7ff2f16019ea88daba7b5fd7c576c824528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6239994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb34c02f8573c9641fba53df7544add36be23085070c86288cd996ba68f8ac6a`

```dockerfile
```

-	Layers:
	-	`sha256:b931b7d023863e52d3820499229f35122080cd2302ad481c08bff52729d70c24`  
		Last Modified: Wed, 11 Dec 2024 22:47:30 GMT  
		Size: 648.9 KB (648915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2764a7272d97762053863636dfd823eab35d753ed896185e1ce59669cff4fd1a`  
		Last Modified: Wed, 11 Dec 2024 22:47:30 GMT  
		Size: 2.8 MB (2842519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45626580dc4d1c049d80f65906d7463a8de56fe9a63f1d64a525cd23e2b4cfa2`  
		Last Modified: Wed, 11 Dec 2024 22:47:30 GMT  
		Size: 2.7 MB (2688523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2cfbfce31fe8f2e44379604b34581cbc2f923e8df537582e6b274df6cde5f43`  
		Last Modified: Wed, 11 Dec 2024 22:47:30 GMT  
		Size: 60.0 KB (60037 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:296865db35980f5c5b1e30f964b70ab09e42b1c66bacbd4618b7d7d48b08cf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76501152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bca3d2b133a10745259dede1140f4ffa75b63db86263157b5f3c5f88385a44b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 12:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 11 Dec 2024 12:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 11 Dec 2024 12:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_VERSION=4.0.4
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 12:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 11 Dec 2024 12:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 11 Dec 2024 12:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 12:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 11 Dec 2024 12:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b5ab0caeddd1abaa37224d9a486339015337675a6e2b1df7fabe8bed782487`  
		Last Modified: Wed, 11 Dec 2024 22:41:08 GMT  
		Size: 42.8 MB (42758704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1edb38b954579ca6b7352009cc3cd4c186ff37994f3cf588639bf60622861a`  
		Last Modified: Wed, 11 Dec 2024 22:41:06 GMT  
		Size: 9.0 MB (8995922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b259f8553832c73ea1dfcd740f5c5d43feb0ef053b677771f7e3edc2c38f47c`  
		Last Modified: Wed, 11 Dec 2024 22:41:06 GMT  
		Size: 2.3 MB (2321289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c632fb46e36829297558b512b86045a8ef477726074c8c10d1f0c7646b54449`  
		Last Modified: Wed, 11 Dec 2024 22:42:44 GMT  
		Size: 18.3 MB (18335763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa61e2f4ce7145176ca69baadae5cc92c734f2a7f88d1ec809b5272a89e890bd`  
		Last Modified: Wed, 11 Dec 2024 22:42:44 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb82fc95b18a039f7837fa01526f094e75be0236c7017167cf814bc6392575b6`  
		Last Modified: Wed, 11 Dec 2024 22:42:44 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8058d5c4081eb724fe032c77a510a72166172e6a0bcb2cbb83d434e823a4c6bc`  
		Last Modified: Wed, 11 Dec 2024 22:42:44 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c1b592d1ce09ac6174ea72b0c24fc6f6f774302eb89543fb4729d80b75f21f`  
		Last Modified: Wed, 11 Dec 2024 22:42:45 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d941468b402a8aed4eb5b6f0b644b710a15e65cebb8c0d086446ab19b3f52517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6480623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6631ff59a868d81e1dde29bebb2289c145e34864460967f7f1db699da4ce208`

```dockerfile
```

-	Layers:
	-	`sha256:00d333c6ab9637a6634ace3344a48f049127373cb71e7899c152d8b5e530378c`  
		Last Modified: Wed, 11 Dec 2024 22:42:44 GMT  
		Size: 653.6 KB (653638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:816228e83d7d5226875164fbff94251190a2ce403f5b2480b74596886d123af6`  
		Last Modified: Wed, 11 Dec 2024 22:42:44 GMT  
		Size: 3.0 MB (2960446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e45fb8606e52de791a6383a68ac2e95d2839f428e4679d21a8c991c7344dbd24`  
		Last Modified: Wed, 11 Dec 2024 22:42:44 GMT  
		Size: 2.8 MB (2806456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cdeac1823849fef36d1a9b500822771cd1ab0690ba2a7f57d7f743fdd532200`  
		Last Modified: Wed, 11 Dec 2024 22:42:44 GMT  
		Size: 60.1 KB (60083 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:ef0486c701c97389a892f08f02360caaa0c862d8baef45a68f58b6a259a4e105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67049872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb747fa62c3138026191dab29fa80d093ccacdd06aae6e4a8b418ef238fcc55c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 12:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 11 Dec 2024 12:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 11 Dec 2024 12:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_VERSION=4.0.4
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 12:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 11 Dec 2024 12:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 11 Dec 2024 12:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 12:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 11 Dec 2024 12:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5738058383d2a7c1e927260b32abb6d6c84f2c20b2ec72c4d658b12d5f26e2e1`  
		Last Modified: Wed, 11 Dec 2024 22:36:17 GMT  
		Size: 35.7 MB (35686465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b8b7f7511dd6ca893fcc7eefc1152a1dacd629974d6d4678adae6fa5a65873`  
		Last Modified: Wed, 11 Dec 2024 22:36:16 GMT  
		Size: 8.3 MB (8324938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7320d5decbb91bbebc1a6f5cf1a87e9bc0733d435bf8fa9d7a1d4a5a81e95d`  
		Last Modified: Wed, 11 Dec 2024 22:36:15 GMT  
		Size: 1.2 MB (1231515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5c5a8c295a69d16047639a414856fc9d3bbc3a6002bdc71285e6a661748794`  
		Last Modified: Wed, 11 Dec 2024 22:36:16 GMT  
		Size: 18.3 MB (18335991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21daf1fc036cd24c96a66c5c602ff983a4f6fb822834def4c083e3b1a5da17e6`  
		Last Modified: Wed, 11 Dec 2024 22:36:16 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f17986629bae02da727bc4b4ca644cc90bd1ff71565f7d97e63c4b055aea0ed`  
		Last Modified: Wed, 11 Dec 2024 22:36:17 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebb9d12c65f6e2b56f3b10da984c333c68e94472951aae246aadd273638f56c`  
		Last Modified: Wed, 11 Dec 2024 22:36:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1a7a092018bbcaaa8f28865c294227ae56f118a421e6b5bc0cbd6da3266f7d`  
		Last Modified: Wed, 11 Dec 2024 22:36:17 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:37e56e4fed847f8f66d3176d20e10bda89cf3c865602d2689b4e3f84c93f3865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6421654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d135fce385a7b34c8e3324cf26072ebb2d1105495d46a4bb6972c6fe2c9910`

```dockerfile
```

-	Layers:
	-	`sha256:413cb5542abb63eb7a7dd06ee714a57bb9b89d065350a5399c975e156580deee`  
		Last Modified: Wed, 11 Dec 2024 22:36:16 GMT  
		Size: 648.1 KB (648120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a66709ff4ef3c8dfb7acb91518da96b5f7d64af52b701f6c5899eb4a4352dc1e`  
		Last Modified: Wed, 11 Dec 2024 22:36:16 GMT  
		Size: 2.9 MB (2933205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18547ac490302a4daaae60ce444d8e689110586df9890c7e70d5dc0070a2cae3`  
		Last Modified: Wed, 11 Dec 2024 22:36:16 GMT  
		Size: 2.8 MB (2780536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:253ea92fe73e95cc1d3f95050f99f68ce043f1c61868cccdc0054ff413c17f64`  
		Last Modified: Wed, 11 Dec 2024 22:36:15 GMT  
		Size: 59.8 KB (59793 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:2d372e572ee64f11d0ecd021821861fd42db89333735504e16ac2dce2c704567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68074519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712b45812c591af31a8d68bb3cac56e621ff8dda4886f6b52abb8dcecde0fec0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 12:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 11 Dec 2024 12:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 11 Dec 2024 12:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_VERSION=4.0.4
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 12:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 11 Dec 2024 12:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 11 Dec 2024 12:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 12:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 11 Dec 2024 12:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a9609dc78f262801654c1a2d3ee36d4f2a555c04ce2eb020a941d97f21106e`  
		Last Modified: Wed, 11 Dec 2024 22:42:19 GMT  
		Size: 36.0 MB (35984080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1499e5e29163ea3c2c3b6709d2e9b94f02b28834a1fade4f5d65f385f5282e`  
		Last Modified: Wed, 11 Dec 2024 22:42:18 GMT  
		Size: 8.8 MB (8834085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e660d230dbc95863451f27c2d70099436790c18298df7ac768d4e7caac71c48`  
		Last Modified: Wed, 11 Dec 2024 22:42:18 GMT  
		Size: 1.3 MB (1346116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21293ccd36740eba3223ee16fdff68619b35ac4ade401ec8a6e9efb995b4a7e`  
		Last Modified: Wed, 11 Dec 2024 22:45:00 GMT  
		Size: 18.3 MB (18336036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd09429308a00fbecf372d03e5a618bade536a6e5c3d3404d5ec730697c0b1e8`  
		Last Modified: Wed, 11 Dec 2024 22:45:00 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720462b8c5cccc42c262345802e4e221d142f21a03de80eb3796cf796c6bf484`  
		Last Modified: Wed, 11 Dec 2024 22:45:00 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1fe512318de5130a7ac5ed4e2b13abcdfa73decf222ec276943df61fa03d56`  
		Last Modified: Wed, 11 Dec 2024 22:45:00 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc456d67075a4919178324c9949cf40a82a539f88736be15854b62a6bf7381c`  
		Last Modified: Wed, 11 Dec 2024 22:45:01 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d588559e1fb244622cb21938ef3ae2deaca682d49402b305271a96514c56bf01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6418710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224bca0d5c3a4e7e9308acbd7fbd62cd67495261fcd2e61ccc9846208840ec1b`

```dockerfile
```

-	Layers:
	-	`sha256:73bd21aa80d44e35e9b21df61e994d3d3ca306b3c786d508292511cb0d605458`  
		Last Modified: Wed, 11 Dec 2024 22:45:00 GMT  
		Size: 647.0 KB (646959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e6ce5aa724f335e9270522f1d98adfa5b4898362827acda7d2bf3c4be7a3ed1`  
		Last Modified: Wed, 11 Dec 2024 22:45:00 GMT  
		Size: 2.9 MB (2932924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21c37b2a9d457d3e5edd03ea72ee03e350a9dea073b8d2eadf0c089c7b63a4ec`  
		Last Modified: Wed, 11 Dec 2024 22:45:00 GMT  
		Size: 2.8 MB (2778922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baaae08b5ea4df7e3e5c1f1d9dfd293fb2fca93c8a50b4407378e17f5b5dfdb0`  
		Last Modified: Wed, 11 Dec 2024 22:44:59 GMT  
		Size: 59.9 KB (59905 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:8b0387af6b39d8523eba8c23dd2424834add530bf80400092d50b9f2d3c37cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69771771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9235bd4f8228998bd52f382f48b39a079740179a14bb9ef556f7c59d25ba9c9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 12:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 11 Dec 2024 12:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 11 Dec 2024 12:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_VERSION=4.0.4
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 12:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 11 Dec 2024 12:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 11 Dec 2024 12:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 12:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 11 Dec 2024 12:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2231c990ab9dfd3e09731c8bbe461e5d14d40362c9f368f44c48cdec4eadac30`  
		Last Modified: Thu, 12 Dec 2024 01:16:35 GMT  
		Size: 36.9 MB (36925327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6620178b42b30361b1bef16c6634d12850c9d28e36162daa0666256f95526385`  
		Last Modified: Thu, 12 Dec 2024 01:16:32 GMT  
		Size: 9.9 MB (9866554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4da5dc2fc9691415e274425062528afd94cd00d072df70ab25719586b021356`  
		Last Modified: Thu, 12 Dec 2024 01:16:30 GMT  
		Size: 1.3 MB (1270925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926aeff2c32570f7823db319d92f5cf87c7c4ddd35ce3a01854f73adf04ff38d`  
		Last Modified: Thu, 12 Dec 2024 01:35:20 GMT  
		Size: 18.3 MB (18335740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a75587bc4707baa68544162913f235de40d163cecd49fab3a6f90f741bcd8b1`  
		Last Modified: Thu, 12 Dec 2024 01:35:11 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae6fa029e37ab707abc2ffeee12e32a55de5e105e8b3918cd309afa1b56c3ff`  
		Last Modified: Thu, 12 Dec 2024 01:35:11 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881a7abfddcfe856268b225a13b9dbb7cbce8f67c67e0aa7dbc87237f9d8fbe0`  
		Last Modified: Thu, 12 Dec 2024 01:35:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a4ee95c72a01340c8b076ce5afc58bd1704d206f828b212438c441b83b0583`  
		Last Modified: Thu, 12 Dec 2024 01:35:12 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fe678337c4808f1f3c93214292544ed8e388d5cae337dc0e2570305d19b3f906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6453811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6573289b5a48187db8c22f610d68d833ce416ce89b3d751dba5bb14b1b06bac9`

```dockerfile
```

-	Layers:
	-	`sha256:6c1b3183343299f3fec0aca6539dbcadf24e3687003c70de0b51a1bd366c8ed9`  
		Last Modified: Thu, 12 Dec 2024 01:35:11 GMT  
		Size: 649.8 KB (649802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561f399113216173808fff2a5559f0b263246b70ebe6fa5b3101ecc60d1cd4f3`  
		Last Modified: Thu, 12 Dec 2024 01:35:12 GMT  
		Size: 2.9 MB (2949047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5f7c57d281ad317e217eea15cc0de4cf963a8d6384ce7daccbb27c7720bc2cb`  
		Last Modified: Thu, 12 Dec 2024 01:35:17 GMT  
		Size: 2.8 MB (2795057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a4a83c272a4df41e836dafa8551019dc5f56ba6b13533d5f7bffa12357f6463`  
		Last Modified: Thu, 12 Dec 2024 01:35:11 GMT  
		Size: 59.9 KB (59905 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:b7457846ffe9cd7e09bba9c5af018495c0b0df15937aafd5969a46e4a99b7607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66649744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20828b83fc52d56e351f6afe518ee413ed05c3333274aa23d9128ebf296f5a79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 12:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 11 Dec 2024 12:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 11 Dec 2024 12:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_VERSION=4.0.4
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 11 Dec 2024 12:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 12:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 11 Dec 2024 12:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 11 Dec 2024 12:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 11 Dec 2024 12:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 12:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 12:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 11 Dec 2024 12:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb1750214f4f325fd8c98e417e41ac6c9c81252807e73de1631d0db4ae71a99`  
		Last Modified: Wed, 11 Dec 2024 22:52:00 GMT  
		Size: 36.0 MB (36043350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0213f86f1dd45733a95f625c82d999ec45abe621539e4850566b3459e81bad39`  
		Last Modified: Wed, 11 Dec 2024 22:52:00 GMT  
		Size: 7.5 MB (7481820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f033464d0e1684ac2a4be86cff65c3deb60892ac414969508236f7eeb3e4ef6`  
		Last Modified: Wed, 11 Dec 2024 22:52:00 GMT  
		Size: 1.3 MB (1325200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2858baac41b51af0d025b062460ce81850c399ad68b4ae0f640b8ca44c250f0`  
		Last Modified: Wed, 11 Dec 2024 23:03:08 GMT  
		Size: 18.3 MB (18336021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aa4807927c1985099b503f237f0bb895f42d396900b69394d35e6ba4c8e105`  
		Last Modified: Wed, 11 Dec 2024 23:03:08 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b963eee459f95654e431fef2ed9af238ed1f411006a39f5b49d75cfa2ed3f0`  
		Last Modified: Wed, 11 Dec 2024 23:03:08 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877d7ae073a5b810cf3d6c1f54b79f4d2d357adc54d50a5501a4624d8ad0bcad`  
		Last Modified: Wed, 11 Dec 2024 23:03:08 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198531f92a432ca4c78b0c85a01ac2c06112c077f3ec9fb9f5b19846d4d009a3`  
		Last Modified: Wed, 11 Dec 2024 23:03:09 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:090ab7c239be01d048ec567565e291888a11a6b94891886e20a108eeebb9c23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6252750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbeef7c0a427d33f2809141249eb4c51a51045e1d3e8440f300e376250d390b6`

```dockerfile
```

-	Layers:
	-	`sha256:253a7998d0b03a4e6aad4f85d0df6e2874229c1992ea43cfd385da573dcc2901`  
		Last Modified: Wed, 11 Dec 2024 23:03:07 GMT  
		Size: 646.9 KB (646925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:634445eddeb9bdb55b32220d9370ed7c32e1b5ab6284e18a9160cb6813e3c944`  
		Last Modified: Wed, 11 Dec 2024 23:03:07 GMT  
		Size: 2.8 MB (2849977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8aaad59713519aa134c365837ba6eac2d9e44a6f2776e693b08446aa3f1465fb`  
		Last Modified: Wed, 11 Dec 2024 23:03:07 GMT  
		Size: 2.7 MB (2696005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df494b09d6529fa830816e3795ac9fad3e5a509757cbba9fcdfb30101d2595c5`  
		Last Modified: Wed, 11 Dec 2024 23:03:07 GMT  
		Size: 59.8 KB (59843 bytes)  
		MIME: application/vnd.in-toto+json
