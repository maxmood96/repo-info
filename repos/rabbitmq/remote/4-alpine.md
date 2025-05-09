## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:a9d1c4f50eb1be66f33271d9eca0dd73858db32cfa25ad2c78bf094f24ee0a7a
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
$ docker pull rabbitmq@sha256:544547a6a1c9f855bff5d18537d018cb0b175ef584e5b4b5efc0f745a992d52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85518208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3e9d6f2cf7b532f96cc6e93785b8ba6b83e71bc14c14ad2efb2507a2fdebf4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 17:58:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 08 May 2025 17:58:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_VERSION=4.1.0
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 08 May 2025 17:58:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 08 May 2025 17:58:28 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:58:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 08 May 2025 17:58:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b329ee1fe301f072a5f4435395dd4e64507ee2692959a45ba3c6335736d52224`  
		Last Modified: Thu, 08 May 2025 18:59:08 GMT  
		Size: 42.8 MB (42831432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d22fe30486eae250b416fbd756eb32f3ce29c1b435701843532f75e79bc0fe5`  
		Last Modified: Thu, 08 May 2025 18:59:08 GMT  
		Size: 8.3 MB (8311601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088dca543f151f1db5bd7822ea138ddd76fad4e7649e973d29e79c9735ffeede`  
		Last Modified: Thu, 08 May 2025 18:59:07 GMT  
		Size: 2.3 MB (2279419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb0eb1b0cfcf5cfc16c2ca71a4d649806c2f93b39f9bbc455ecbdab1a7e71c4`  
		Last Modified: Thu, 08 May 2025 18:59:08 GMT  
		Size: 28.5 MB (28451762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee14e9a44a308e9c51e49816e27ea99427714205f7fbaf849f18ba482172a17`  
		Last Modified: Thu, 08 May 2025 18:59:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454cc4a699014837586bffd106c3c9b063f9175d55b206e37cf9744315c63a05`  
		Last Modified: Thu, 08 May 2025 18:59:09 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cb6722b50e2a1c4b75ef79e66a50bd630951a4ed5f4a0e1d0994d38f11862f`  
		Last Modified: Thu, 08 May 2025 18:59:09 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a758bff8c9f4c50527474c14f502c7e23f52fc1ecd71b06a7a662fb956f05f4`  
		Last Modified: Thu, 08 May 2025 18:59:09 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0c31d17a472bdc62115c58238e0e13e3d8e54ef1c8b0865835ee5fe4868d24e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6728949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f916a0857c2aa2ba354ca928a46b925302d3bbdd96b2562cb1556c7bf360993a`

```dockerfile
```

-	Layers:
	-	`sha256:ddc0cc79d1f0ac0968b57637d806a296dc64d9629174874e32689d9da24bc775`  
		Last Modified: Thu, 08 May 2025 18:59:07 GMT  
		Size: 659.6 KB (659640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc1d02e4546e523545b09872e2a439c022415e815db6ea787c67d2c36f7a865e`  
		Last Modified: Thu, 08 May 2025 18:59:07 GMT  
		Size: 3.1 MB (3081286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eebdfe198d3c13bb9591860e4ea3fbd9c1d3330f9ef62d387c61d9740585287d`  
		Last Modified: Thu, 08 May 2025 18:59:07 GMT  
		Size: 2.9 MB (2928081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cfbc3c1180bfecf0b6b7cc9e693a5e3b4b63d54a5e65318fbf4239a18410479`  
		Last Modified: Thu, 08 May 2025 18:59:07 GMT  
		Size: 59.9 KB (59942 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:38b903de3ed7a94301c16711c4ddfd572a1a27545381178f8f42f3843545f7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73574491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b89094950127018dd61c021bbee5ab8f720d8129eac818087ef2100706982f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 17:58:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 08 May 2025 17:58:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_VERSION=4.1.0
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 08 May 2025 17:58:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 08 May 2025 17:58:28 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:58:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 08 May 2025 17:58:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0b9575eb19eeb6c4284a60a7d97e8587a656a44e1c7f336faed4622f3ab3cd`  
		Last Modified: Thu, 08 May 2025 18:55:56 GMT  
		Size: 33.4 MB (33431371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591f1326078d8f955195d4931a4bdd014c301b9a962d3ba8a400ae07af12ac0d`  
		Last Modified: Thu, 08 May 2025 18:55:55 GMT  
		Size: 7.1 MB (7097976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39642c906c217917e6c7f8a75aa131eb06af38fe1b9f64453bc9faa3c83b86b`  
		Last Modified: Thu, 08 May 2025 18:55:55 GMT  
		Size: 1.2 MB (1227001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb786cb033d95fa6dd308ed90dc0121df63c648f38cf656783c4626f47cd3cf`  
		Last Modified: Thu, 08 May 2025 18:55:56 GMT  
		Size: 28.5 MB (28451665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0b8f98165336dcb6a85f9f8728fae1636f91e703d3520989930bb1c340a958`  
		Last Modified: Thu, 08 May 2025 18:55:56 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f51ee61d82cb37e1b663b59b6bd9b9126b91d343829b8440f7511d107dad6e`  
		Last Modified: Thu, 08 May 2025 18:55:56 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edf7efa26def5d960f4c7616e02f71088914e0fd40f6b7626cd203f82579156`  
		Last Modified: Thu, 08 May 2025 18:55:57 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee210eed0fd8081728f6015145f3b8a79cbddd5ae065101a553e36e851921a84`  
		Last Modified: Thu, 08 May 2025 18:55:57 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:de02a5b64983677dea1e4eae67cc79ff724e899b94a070f05eb0cc431c99fc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 KB (59921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ee08ec3c99f4c46446bf199bd3c609e9c88d5aa38a2d89a39338193c0543a0`

```dockerfile
```

-	Layers:
	-	`sha256:315e1aee0ab1b43e79e373bc58bc47c1c4ab0faa2566a379690362491293d7b3`  
		Last Modified: Thu, 08 May 2025 18:55:54 GMT  
		Size: 59.9 KB (59921 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:e0eb6f70e11cdb14f2f48883e45573b7bf8c8ace62079fb6ac7ae21db55359cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72799910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82dd6227f9cf4a100866678f9df4fd2d3f7746b7843a6e71b620261aa3ee0e58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 17:58:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 08 May 2025 17:58:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_VERSION=4.1.0
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 08 May 2025 17:58:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 08 May 2025 17:58:28 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:58:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 08 May 2025 17:58:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c7890eb4484bbaf493a3c5bdc16f65a76dc34eec4e8eb3b284e45d4b300c49`  
		Last Modified: Thu, 08 May 2025 19:02:00 GMT  
		Size: 33.4 MB (33371635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cc32af2422bc4d6e9aeaa43c71c4c1dc9637b069795158faac38d298b4baee`  
		Last Modified: Thu, 08 May 2025 19:02:00 GMT  
		Size: 6.7 MB (6742177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2f41c8719599ff716a80f4bc890c9d4da8058eb2b9967663238a49c46aebe9`  
		Last Modified: Thu, 08 May 2025 19:01:59 GMT  
		Size: 1.1 MB (1134786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dd033633d8b6555a540aa2e7ac3d4d91db90affab97b40e89f29c394758b7a`  
		Last Modified: Thu, 08 May 2025 19:02:00 GMT  
		Size: 28.5 MB (28451445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57021372dc8ac326ae4572080f002683e3b2104e80fa24d136ec4af80285031`  
		Last Modified: Thu, 08 May 2025 19:02:01 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1653b7d9da1d8eacc84513626c5bd52ed97bec53d8382f6d3ddaf7a44ff5d739`  
		Last Modified: Thu, 08 May 2025 19:02:01 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61239dfea5677b36b0e1c9c8e0d48e415dd078ea60bf594b8f6c703aab245e1e`  
		Last Modified: Thu, 08 May 2025 19:02:02 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ec63555185fad01b8825d5bd5b788d6becc2fb03d0bd866731b2bea57a2d78`  
		Last Modified: Thu, 08 May 2025 19:02:02 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:99d39f8940616c0b6b5ecec7e237fd100840bce9965ab2152581198f86f380a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6495671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca82a918461751463129f3115e9d154ea8e22a0658feb1b34180c4601114d44`

```dockerfile
```

-	Layers:
	-	`sha256:8f6c8353e4cc005baf7b9927353263e12f134f6017463a2686f9cdaa32cfa46f`  
		Last Modified: Thu, 08 May 2025 19:01:59 GMT  
		Size: 655.8 KB (655785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16ff991793f5edad6458d9598854a93c1b70ede7c66087bd6232553c961a1495`  
		Last Modified: Thu, 08 May 2025 19:01:59 GMT  
		Size: 3.0 MB (2967140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ee0d7b1315eadaa45ee56f4370e27db4320e2d52667ced3773b7beaab434ee`  
		Last Modified: Thu, 08 May 2025 19:01:59 GMT  
		Size: 2.8 MB (2812610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:906cb18b06d4eeac3d5fac055a0bc52a82b844da25b905bc06b88ea0728847fb`  
		Last Modified: Thu, 08 May 2025 19:01:59 GMT  
		Size: 60.1 KB (60136 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:f798c3b888731c929c52b5091d61c468c8c093c015143d92fef5fec07aa5e71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84642201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23457d7055aecdf1ed36f1bd35360617c326bf5207349e7ed2deac9c62b81a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 17:58:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 08 May 2025 17:58:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_VERSION=4.1.0
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 08 May 2025 17:58:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 08 May 2025 17:58:28 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:58:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 08 May 2025 17:58:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348a3b4f3433a92f55c163f741f1255474a388f50279fd414febe63e7e76b10b`  
		Last Modified: Thu, 08 May 2025 19:00:21 GMT  
		Size: 40.8 MB (40836979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843c3ef8b41ecb68de15dd27dfe4e11ca2430cb3275b07f46c79b70027311114`  
		Last Modified: Thu, 08 May 2025 19:00:20 GMT  
		Size: 9.0 MB (9034848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8b66f34d8ab9510ee2d06e80b1ae8ead0466fe189805b1859b336594d9508c`  
		Last Modified: Thu, 08 May 2025 19:00:20 GMT  
		Size: 2.3 MB (2323942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f27b94122b120b5f9d3f83cb75ece8eb09d32baf3b7d3c51685ed9dfade971`  
		Last Modified: Thu, 08 May 2025 19:00:21 GMT  
		Size: 28.5 MB (28451657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4978fc36a60885906866eaac847a6a17798879c3ed7eb35a08e0c1bca4e885df`  
		Last Modified: Thu, 08 May 2025 19:00:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f446ae4541e9e8d60b231c8185e1e47b158e100e5f6aacf8dfe3692157b779ef`  
		Last Modified: Thu, 08 May 2025 19:00:21 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fadfea1126f4e52649ee715e048c3dc08095268b6440c1dde7dcd3f9f248887`  
		Last Modified: Thu, 08 May 2025 19:00:22 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12973550c49a1e60f396394a49083a7a3fc4a48c6c4cf44591b82cf64e80483e`  
		Last Modified: Thu, 08 May 2025 19:00:22 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2799cd362d7f43ab267dcfa57acaf88b65a98d2a8b62f94267fe2c76b3b04016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d68ef675827984f1d27e40c65a1a6ab75885d6f63a2a6276c2c9d58cd15560`

```dockerfile
```

-	Layers:
	-	`sha256:22dcef661a905692299707a6fa4523276feffe80132061d71e0fc9cd8cbd0e1f`  
		Last Modified: Thu, 08 May 2025 19:00:19 GMT  
		Size: 660.4 KB (660431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9523c9c15c6e80dbd117c35a424963d81a8be1d7f2d23d7fbabffbef086f8f4e`  
		Last Modified: Thu, 08 May 2025 19:00:20 GMT  
		Size: 3.1 MB (3136095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72ade3b0fdbb3203088ead5321179b5029c5025d6d61614aa8e9ac42c582156f`  
		Last Modified: Thu, 08 May 2025 19:00:20 GMT  
		Size: 3.0 MB (2981571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6f332e5210d351836a4225a1b5acd4121b6f6df028f9605bc3c03d5f7b873f0`  
		Last Modified: Thu, 08 May 2025 19:00:19 GMT  
		Size: 60.2 KB (60182 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:9811a6e53ce1a915e6fec88c952d6740388bd17088d24fe424623b49760d1d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74990639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58afd462be11e12541621172798b19d4a6c928c2fc287e5e36e02d6c9da8e13b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 17:58:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 08 May 2025 17:58:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_VERSION=4.1.0
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 08 May 2025 17:58:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 08 May 2025 17:58:28 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:58:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 08 May 2025 17:58:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3a69ef150323c83a3e0b8ed367a01bbd48b3c7712ccb48989e64e9e08560e6`  
		Last Modified: Thu, 08 May 2025 18:59:05 GMT  
		Size: 33.5 MB (33518420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1e98cfd8b908c5377c8a1a6ed00cc0574bcb51d56ebeb30c244eaebe397fce`  
		Last Modified: Thu, 08 May 2025 18:59:04 GMT  
		Size: 8.3 MB (8324817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8863fba5cfe31bcec645159c4e7fa307104fdbf80f6b0b3550d26b0b6e967bd`  
		Last Modified: Thu, 08 May 2025 18:59:04 GMT  
		Size: 1.2 MB (1230664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e026a516122b961bef3888aca0af4610831041a9190fa1374436ed244ad2b25b`  
		Last Modified: Thu, 08 May 2025 18:59:05 GMT  
		Size: 28.5 MB (28451366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68a064caa2e2328051ea3486b203c4eed00275a087ca7c2b04edc285ffc8c72`  
		Last Modified: Thu, 08 May 2025 18:59:05 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3428745c98f3502810162f426b82d941dd240a69d8f32362ba6773df4997568`  
		Last Modified: Thu, 08 May 2025 18:59:06 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33701c8c782df013a3ecef0bf95c1647b2ac5c8f71c46b183752a82cb38169e`  
		Last Modified: Thu, 08 May 2025 18:59:06 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c5f723dab962ea9549def90f2826ae25bafb4f1f01ce7b47750349faac124`  
		Last Modified: Thu, 08 May 2025 18:59:06 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4282e393256cdf400629c463678e52e4e6d4e116c7b19eaf07721a8c6a9312a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6702145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709966b44a8f609540937e866ae14ace04e0b80f91e4653d4d79f6e465f2816e`

```dockerfile
```

-	Layers:
	-	`sha256:c5118d080f4f8dfbf925eed0c729a59175dae73bac743f560528de6c36f1fc6d`  
		Last Modified: Thu, 08 May 2025 18:59:04 GMT  
		Size: 655.0 KB (654989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0029164556382db8fdfb17730be6f5e4e76c50aa77e600c29022bdd53c6e6b73`  
		Last Modified: Thu, 08 May 2025 18:59:04 GMT  
		Size: 3.1 MB (3070232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fd68d9d2b7a41c050b85a23a209c17b93e4aa2b21579586bcd44535322ab685`  
		Last Modified: Thu, 08 May 2025 18:59:04 GMT  
		Size: 2.9 MB (2917031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e208eda8e236e1430dc812dfd687d7af381d366db1ba96599e96b2a0e57dc213`  
		Last Modified: Thu, 08 May 2025 18:59:04 GMT  
		Size: 59.9 KB (59893 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:5da306356e85355dc094572a7c22bbe7193acebb0c4ca1da3664450075890e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76126038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5817d48ce13f85184e2073f383c7c7d83dd80bd5befbf05c1cbe54a37e0905`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 17:58:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 08 May 2025 17:58:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_VERSION=4.1.0
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 08 May 2025 17:58:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 08 May 2025 17:58:28 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:58:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 08 May 2025 17:58:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c8aeb0e70db5ef5b210ff2d0544da65f6f518919b49cfb722b3319dda873fa`  
		Last Modified: Thu, 08 May 2025 19:01:23 GMT  
		Size: 33.9 MB (33903577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bd4a8ec53808110a83a0faad5237007d8551cb819e31a6c69c0ae1cdd106e9`  
		Last Modified: Thu, 08 May 2025 19:01:22 GMT  
		Size: 8.8 MB (8848322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827e01e89edcb906aee2a8ac7c965bc35d3bb74297ab118d7557036471922880`  
		Last Modified: Thu, 08 May 2025 19:01:21 GMT  
		Size: 1.3 MB (1346577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d84b17a6d847f63d06e77ccb2538705d5bc4e54938ebe4f0c985d42b4dadd1`  
		Last Modified: Thu, 08 May 2025 19:01:23 GMT  
		Size: 28.5 MB (28451471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f2a2cea99f9a2104d05359a9bd4c9cbfb45e107bc4d6ae5f408ed52f3baefa`  
		Last Modified: Thu, 08 May 2025 19:01:22 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea13d7c0da4f9fa649341c2c4d82b81b3fc11e5a77960db11fe2330c2824204`  
		Last Modified: Thu, 08 May 2025 19:01:23 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040dfb85ab94ed00c1693d3066043087395bad8eedb1a7b3e899988fab537bce`  
		Last Modified: Thu, 08 May 2025 19:01:23 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8490576d0911417858ffa8568b23ac965f5368eaa2d8ae9819872f1d9f8f4990`  
		Last Modified: Thu, 08 May 2025 19:01:24 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9e374364016a9c956d9a8b3a7e010600277cc77f5d618ee094f75dd0e2c89bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6733949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f27ce66995bbb7a6b78789fbcbe54ec78429e9f3936c440ac1a5bae61bb4fc7`

```dockerfile
```

-	Layers:
	-	`sha256:2b5d2315cc17af52b3575f0fec2bfeb9cbb72f51f020868d1e1459eae07e923f`  
		Last Modified: Thu, 08 May 2025 19:01:21 GMT  
		Size: 653.8 KB (653832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19d9c7047326f8691062cd58bb9d50ffbb95713f701181c5af8797bd13dba36`  
		Last Modified: Thu, 08 May 2025 19:01:21 GMT  
		Size: 3.1 MB (3087324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:622d386034f85b58fbeb4767187ee72f58444057c66639443a87e334b8b186c1`  
		Last Modified: Thu, 08 May 2025 19:01:21 GMT  
		Size: 2.9 MB (2932788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2c5b68fffa5ba358bcecdd67e22e2a2c988df6e76ceae7345eccff856fbbd7e`  
		Last Modified: Thu, 08 May 2025 19:01:21 GMT  
		Size: 60.0 KB (60005 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:e746c763cacb325fc27f0cec48eea1a3b1d4e5f6fb45b28a4b37c0ac18d5a04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77807444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c287fd38078dec01a1bd58f83998e2306933b4bb5e9371ba3a6e4b3a1f23ef5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 17:58:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 08 May 2025 17:58:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_VERSION=4.1.0
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 08 May 2025 17:58:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 08 May 2025 17:58:28 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:58:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 08 May 2025 17:58:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe28f8f3876979617093feef5c0ee596ad1ff84285e1b98f46dac5ef222bc402`  
		Last Modified: Thu, 08 May 2025 21:26:57 GMT  
		Size: 34.9 MB (34877235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6f004d1d41c868c3e71c3c0c8fae81b9afd4a41f11b528ab9f700090837ddd`  
		Last Modified: Thu, 08 May 2025 21:26:53 GMT  
		Size: 9.9 MB (9858971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b9d7244a99c2107b6002e41575a6a80a628d1dcf46538dfc182c73121b52c6`  
		Last Modified: Thu, 08 May 2025 21:26:52 GMT  
		Size: 1.3 MB (1266438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fa56e7889cb34e96bf2d3224a172bd33d570da8266d6af13699388238c3e8d`  
		Last Modified: Thu, 08 May 2025 21:26:56 GMT  
		Size: 28.5 MB (28451610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3caa7c6cae6d653777058ec6ddda8131afbc0cf5273c660ad26bb8faa2ca1e57`  
		Last Modified: Thu, 08 May 2025 21:26:53 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc260d31d47674f516584b1673599f2546d469cf916212127b8a68d8041b4c7c`  
		Last Modified: Thu, 08 May 2025 21:26:54 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10b44a42e2b541998143b9661688b21c303238e65e70e7e20656e5f3b5ee210`  
		Last Modified: Thu, 08 May 2025 21:26:55 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9511bea89fbe4330e1ad1137c954732b48ea0864bbd88053d98cf4882c093a4c`  
		Last Modified: Thu, 08 May 2025 21:26:55 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:353892e8aeee8e12946f5b29bb0010a6803b01d6e437b955e71137ddff261266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6812063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45a89b39cc480a0553bc63b2ffb998eb65451c49a0c3a3259b1f4e4241f655b`

```dockerfile
```

-	Layers:
	-	`sha256:13eca6fb3f5aac1a926a0ba5829ac41134b5cf532b58bcad09cd69a50e425535`  
		Last Modified: Thu, 08 May 2025 21:26:51 GMT  
		Size: 656.6 KB (656624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f29df667ccdab925c091d10875e3d362589fc8cd31c172bfbba5251b75a23330`  
		Last Modified: Thu, 08 May 2025 21:26:52 GMT  
		Size: 3.1 MB (3124979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e340c03f18f760c9ee9289f7a0f9a3b524cf23178ed8b786ef97e675d2daa14d`  
		Last Modified: Thu, 08 May 2025 21:26:52 GMT  
		Size: 3.0 MB (2970455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f92bfcfc78dd73d0c9f699a3c0f9c02b336592c8149f3ec1d4350893581cd8b`  
		Last Modified: Thu, 08 May 2025 21:26:51 GMT  
		Size: 60.0 KB (60005 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:ba519523fe8b15ed2229a91bf11b1ac0410b361ecd50036943f8a61fb87557cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74700541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c211ded2bf992a584a066ba012836d612eb03339c749a7af210e4afbeefdbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 17:58:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 08 May 2025 17:58:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_VERSION=4.1.0
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 08 May 2025 17:58:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 17:58:28 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 08 May 2025 17:58:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 08 May 2025 17:58:28 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 08 May 2025 17:58:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 08 May 2025 17:58:28 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:58:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:58:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 08 May 2025 17:58:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbbc66f6aa8e6c4db285673a861c6e70cdfda2d8cd2339883ba53f895ace20d`  
		Last Modified: Thu, 08 May 2025 19:01:54 GMT  
		Size: 33.9 MB (33943995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a75e8bef0da4f4ecd2e1c4dedf70ecfa0f44c294cb8302c9d5422745ae05e9`  
		Last Modified: Thu, 08 May 2025 19:01:54 GMT  
		Size: 7.5 MB (7510994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f928c2c8909ee73bbf3fc1b5aac4fecb66a13e8035de7da9e54ecfcbe56caba`  
		Last Modified: Thu, 08 May 2025 19:01:53 GMT  
		Size: 1.3 MB (1324702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2a58a36a4d4a13fb2330ecb8b25ba70440784cd119b4864e87e790c85fec2d`  
		Last Modified: Thu, 08 May 2025 19:01:55 GMT  
		Size: 28.5 MB (28451533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6952d4c2cc938aaa8841bc486d90c07348ff912443c81dec07d4b9c6543371e`  
		Last Modified: Thu, 08 May 2025 19:01:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0abc773156f02734a823bf937ea6777b6add6f93517952ecaeace584d51243d`  
		Last Modified: Thu, 08 May 2025 19:01:55 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121dbb66c1cdb79b6ebbb098df1c741b7551507f0f3e1db5f134884265119d83`  
		Last Modified: Thu, 08 May 2025 19:01:55 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af2877d7acab91475e8e73e4a1c0bac6bb06b6193e680acf69c4e6f3bba5bd7`  
		Last Modified: Thu, 08 May 2025 19:01:56 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:317f912a0982e218254338afe2cf08f8bb0aac5419bc024d115bc1a90aae2b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6513817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10030c4f95fcbea5a80b5efc36061fc3509ad324d7be553ebd192ba1efeeb487`

```dockerfile
```

-	Layers:
	-	`sha256:2ced4b744192c8c6ebc4b02afc0f3e33de979773292314f8b30190bf50963ff8`  
		Last Modified: Thu, 08 May 2025 19:01:54 GMT  
		Size: 653.8 KB (653798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e26987fc86ca879dff18b314d8996e02190651869501176cc75bc892e58e61da`  
		Last Modified: Thu, 08 May 2025 19:01:54 GMT  
		Size: 3.0 MB (2977291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:763d37fc4e86c2fff91ae5322f5dd292787cd2b082a1a7d423f42581ffbe8d87`  
		Last Modified: Thu, 08 May 2025 19:01:53 GMT  
		Size: 2.8 MB (2822785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dda29c3575a49b6ffa432f37356876b444fc258bdae96d3d87f47990d83468a`  
		Last Modified: Thu, 08 May 2025 19:01:53 GMT  
		Size: 59.9 KB (59943 bytes)  
		MIME: application/vnd.in-toto+json
