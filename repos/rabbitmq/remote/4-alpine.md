## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:ba8f1a68a00cd7cc141c01de752bdb598ded669f247c16f5f031e5a351564754
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
$ docker pull rabbitmq@sha256:f177c529c6fb98cfe6b956940f7ca8b1efeac3e5ac1f4bbe45a0429391f470f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77669030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b284280daa45c0efb5b1c1134a4d4a94867c4e44688469b59bf8408fda08c9af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Mar 2025 17:31:53 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 28 Mar 2025 17:31:53 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 28 Mar 2025 17:31:53 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_VERSION=4.0.7
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:31:53 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 28 Mar 2025 17:31:53 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 28 Mar 2025 17:31:53 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Mar 2025 17:31:53 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 28 Mar 2025 17:31:53 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d89e1cfcea0fb59104d0f516c23a167e0eb8ffda7a2fc8f517747392b75bf6`  
		Last Modified: Mon, 31 Mar 2025 17:25:57 GMT  
		Size: 45.0 MB (45036018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709a3cdd9a5137339c8da8962b0678262bada5ebc2160ffe918e3e32f3c60931`  
		Last Modified: Mon, 31 Mar 2025 17:25:56 GMT  
		Size: 8.3 MB (8311609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db17c3aeb292f57e58b9e355bf53dc283c068a869e33352ea8840f1e2c97dd17`  
		Last Modified: Mon, 31 Mar 2025 17:25:56 GMT  
		Size: 2.3 MB (2279262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8538f196db8350a44737d7ce97d46de88aec529437737b9484525ea05d175985`  
		Last Modified: Mon, 31 Mar 2025 17:25:57 GMT  
		Size: 18.4 MB (18398145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab70eea500d59ff51979fea7cd38fbc958753e8d8d4365614196ccdf89d8b122`  
		Last Modified: Mon, 31 Mar 2025 17:25:57 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5734869102e0693f9636548e55bc4de394fcb68aefa9754220134dfe79380bc8`  
		Last Modified: Mon, 31 Mar 2025 17:25:57 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81ab59f262254f2b08345f9c0101467b7f28b33a551fb6bad32b70d133d05e5`  
		Last Modified: Mon, 31 Mar 2025 17:25:58 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77382dfcc92c852b7cd9603c8de3daa2f05682bd7e3b99e790ef328f80c71274`  
		Last Modified: Mon, 31 Mar 2025 17:25:58 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:288a0538dc2926f5dac2c65b171b82bcf63b78308453a6fd33e1fa63a499bf5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6728274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674d80530351e35919ec15da320af1ed86e3c7b7e611ab53e8e7ae365d10b788`

```dockerfile
```

-	Layers:
	-	`sha256:c24be1ebb239b42ccefd3ac33d7b5e7a82e7b84799dd907b1c19e639f61f4c79`  
		Last Modified: Mon, 31 Mar 2025 17:25:56 GMT  
		Size: 658.4 KB (658431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7d0e4fd8a49fc39940d592ba5f0a5f4e253435e8223107b7bc6203fce9d05f`  
		Last Modified: Mon, 31 Mar 2025 17:25:56 GMT  
		Size: 3.1 MB (3081904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b899f768bb2b0bca7709cc7d576ef7406dbbe797c0f16002527bd4e4ecf7d9`  
		Last Modified: Mon, 31 Mar 2025 17:25:56 GMT  
		Size: 2.9 MB (2928081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c0a84f5360d69d4ac59f27df3794a4228baca1edd5638439cb00b78bf6b7652`  
		Last Modified: Mon, 31 Mar 2025 17:25:56 GMT  
		Size: 59.9 KB (59858 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:7139031ece9dc2e94181319fca8e1b3df0256d0c3572c31d76d11667ff7742e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65708235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b724b300927c77872ad62b5b6b612241302f6728a3479a079da7971e6ceb912e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Mar 2025 17:31:53 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 28 Mar 2025 17:31:53 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 28 Mar 2025 17:31:53 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_VERSION=4.0.7
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:31:53 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 28 Mar 2025 17:31:53 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 28 Mar 2025 17:31:53 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Mar 2025 17:31:53 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 28 Mar 2025 17:31:53 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87dd3ee0ee65e4e973add0ee75b61a132e1d52b4114baf1d3361dd474b2d788`  
		Last Modified: Mon, 31 Mar 2025 17:22:25 GMT  
		Size: 35.6 MB (35618739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acb96660a2d6927bf96bf8e451c23001b5b7d453b626a3a578d869edd3e70f8`  
		Last Modified: Mon, 31 Mar 2025 17:22:25 GMT  
		Size: 7.1 MB (7097969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f27f68769c3eadcce43eb00a8c0e17179c25963542355180e0b56ecb338bdb`  
		Last Modified: Mon, 31 Mar 2025 17:22:24 GMT  
		Size: 1.2 MB (1226964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aac98e37d0841ce5444a25f306874af9869044542509c04fe92ddb647b2806e`  
		Last Modified: Mon, 31 Mar 2025 17:22:52 GMT  
		Size: 18.4 MB (18398093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb85cb66b15578cb9381102f41d27b25ba8361179d02e471f5fd62be571d6876`  
		Last Modified: Mon, 31 Mar 2025 17:22:52 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1903aab8f104dcca3d721e9042d3f215684f6aaa06592c86773efd68074825`  
		Last Modified: Mon, 31 Mar 2025 17:22:52 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d43d106fc1e27ae1e7e6ef46deb00b8d44db3005f51e3dc0cc74b02d72f337`  
		Last Modified: Mon, 31 Mar 2025 17:22:52 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e79e61203f794d3fd27aaab22ecec643d9d8cd28dd86ebaadb85dda019b9fb7`  
		Last Modified: Mon, 31 Mar 2025 17:22:52 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:62b01ba9c6607c0acaa927c4a8dc0f106393760c409ed936600baa0e0ffa6606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 KB (59835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378fbbf4482b44abf65aafc84afda541b68275ad39541e387f3e622267c64cd8`

```dockerfile
```

-	Layers:
	-	`sha256:dd501246870d94514e2af71807a280c2c98ed0c2079c70ff353770cbccbbb841`  
		Last Modified: Mon, 31 Mar 2025 17:22:51 GMT  
		Size: 59.8 KB (59835 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:ce46bb7ae1546c7944af2944bdd943dbdda76531103a8050a17e0801a1260144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64946068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984d63f3c9a31d3606931878eec69cf80f35d4265dc36532f994b68f4efed998`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Mar 2025 17:31:53 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 28 Mar 2025 17:31:53 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 28 Mar 2025 17:31:53 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_VERSION=4.0.7
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:31:53 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 28 Mar 2025 17:31:53 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 28 Mar 2025 17:31:53 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Mar 2025 17:31:53 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 28 Mar 2025 17:31:53 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025c962907b70de9628060e54e50b6e558af6aa6d1d89a52366a4edfae0ddeed`  
		Last Modified: Mon, 31 Mar 2025 17:44:54 GMT  
		Size: 35.6 MB (35571441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69f9de5ef51b8358dda89fdd2ca1642c8fce25eb33170b3d28bdf2a2f988cb4`  
		Last Modified: Mon, 31 Mar 2025 17:44:53 GMT  
		Size: 6.7 MB (6742168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a704e20a9252586f45b715b22e7fee088f01f9d457e9237004bdf00585d19fd4`  
		Last Modified: Mon, 31 Mar 2025 17:44:53 GMT  
		Size: 1.1 MB (1134778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d769a2f2f20a3f19b587e606c1d9bf8298ad23cf0755079913217804a36d1a`  
		Last Modified: Mon, 31 Mar 2025 17:47:21 GMT  
		Size: 18.4 MB (18397810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c91baead544e4f0e108698d25004d2c6ebc7da6fc94f15cef3cb82c668c5feb`  
		Last Modified: Mon, 31 Mar 2025 17:47:20 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfc54a2f5a53ee054b7966faef1f76e5c78a4b717071cf9d65c511ed28d25e5`  
		Last Modified: Mon, 31 Mar 2025 17:47:20 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6bc4ffdcd36dca9a95025d691b1e8dd156c3733a316cec2ddf15a19db9e094`  
		Last Modified: Mon, 31 Mar 2025 17:47:20 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fc416283cd1e390a7d3c87203548d8826b0629d4502f598ea3c5d3f0bd42b3`  
		Last Modified: Mon, 31 Mar 2025 17:47:21 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7d4d6ad28f29e66903d673a393fce2d69ed5557f87322d284ba1a55edf71a966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6494995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0003471c72fef767009987fb31ac3b068e812607234df2c999dde857b6617861`

```dockerfile
```

-	Layers:
	-	`sha256:1b02c3c48bb9435f92c88d30c8e9c9222714cfef0bd85841eff92f5533b49ab9`  
		Last Modified: Mon, 31 Mar 2025 17:47:20 GMT  
		Size: 654.6 KB (654576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6093319a7e70cea40e99e35d27f146cc65512fbc0e19bd0a97bce2f2f8b93b81`  
		Last Modified: Mon, 31 Mar 2025 17:47:20 GMT  
		Size: 3.0 MB (2967758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbde0e835ad7a38a3a691ea93363f328f3cc91044c95c466b964825694400517`  
		Last Modified: Mon, 31 Mar 2025 17:47:20 GMT  
		Size: 2.8 MB (2812610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2cb6ef29d43301851a62ed22ade14a8c3f338029f67b7578d7589ce3e780d95`  
		Last Modified: Mon, 31 Mar 2025 17:47:20 GMT  
		Size: 60.1 KB (60051 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:406709d42c50a2755e7cf3ab215a9f755ab287088123a6affa935defef5d51a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76771603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017aa816d683c671589fb4878506f0d8ca849ba237064ae66d5d0c93030710d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Mar 2025 17:31:53 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 28 Mar 2025 17:31:53 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 28 Mar 2025 17:31:53 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_VERSION=4.0.7
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:31:53 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 28 Mar 2025 17:31:53 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 28 Mar 2025 17:31:53 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Mar 2025 17:31:53 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 28 Mar 2025 17:31:53 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f861f0253bcb0eb423d7acb19b2b2ead088ed94f4fc9831f2cfa527869852e`  
		Last Modified: Mon, 31 Mar 2025 17:31:56 GMT  
		Size: 43.0 MB (43019903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebe219fd6773af38a6c34084edbdfa2c286639a52cc598c12c3bd52031c46c3`  
		Last Modified: Mon, 31 Mar 2025 17:31:53 GMT  
		Size: 9.0 MB (9034853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262580c9961eb107c1a3131c26872e58b07719637b4240591afbd9aea698d5e3`  
		Last Modified: Mon, 31 Mar 2025 17:31:52 GMT  
		Size: 2.3 MB (2323904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450b296cc211162b4bca15b430258357351622853744f692652f830f8c965a89`  
		Last Modified: Mon, 31 Mar 2025 17:40:21 GMT  
		Size: 18.4 MB (18398169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e5fa503faed17e3a7ec7beecdf5094a5cc81b5eebb74552f0a08fbf82e33ef`  
		Last Modified: Mon, 31 Mar 2025 17:40:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed358c07c89ae90af9adf6bfe2f5a638bf4f1a497473fa8921bc6cb5f0ee81e`  
		Last Modified: Mon, 31 Mar 2025 17:40:20 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb3ee0b0f785a66b9f4be79462b4f80360879906aa28039f6876d73fb0e4e24`  
		Last Modified: Mon, 31 Mar 2025 17:40:20 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e15bcc275e34e4f6dae3f423fb11cac922fe2d61b9ca11cbcb3a10a6ac0e7c`  
		Last Modified: Mon, 31 Mar 2025 17:40:21 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b0080d0a61212eaaa03a646e8e1e8705ca67f2592a9953d1a6d37faaab95beb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6837603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd4224c5b1567bfc9c558acc3ef47d242abdeb82b735f2ea309bfb34c02c53e`

```dockerfile
```

-	Layers:
	-	`sha256:527749dfc0bd60da3ed6b7c7628da1c48fa2ffa35fa4334e75fd8d8a13eef019`  
		Last Modified: Mon, 31 Mar 2025 17:40:20 GMT  
		Size: 659.2 KB (659222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f3515b6146b0481009c641fd0e2777222f5aa113cea088a21830cf89d174fd5`  
		Last Modified: Mon, 31 Mar 2025 17:40:20 GMT  
		Size: 3.1 MB (3136713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2f51c36ee10c176214e48a4556dc9609d6fbb4f827f194ed9ef669e19dd6791`  
		Last Modified: Mon, 31 Mar 2025 17:40:21 GMT  
		Size: 3.0 MB (2981571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8072bc1bf1b7a23eb0ff9da44e99e034c03c9323d9d20fd7739a66ae70d433a1`  
		Last Modified: Mon, 31 Mar 2025 17:40:20 GMT  
		Size: 60.1 KB (60097 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:ede81a9e88e5b2e08795fef6ad6efca77e7f7cf17ade99fa0e6364c955d27a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67137897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d606f4cd7150fcd1d3253a78d6b957d0cb9f237a2ecd70365fc93b33bb557669`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Mar 2025 17:31:53 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 28 Mar 2025 17:31:53 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 28 Mar 2025 17:31:53 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_VERSION=4.0.7
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:31:53 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 28 Mar 2025 17:31:53 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 28 Mar 2025 17:31:53 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Mar 2025 17:31:53 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 28 Mar 2025 17:31:53 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27262710456652014796f43f19c401a5a475a4996310fd4e497040f3aaf47736`  
		Last Modified: Mon, 31 Mar 2025 17:26:03 GMT  
		Size: 35.7 MB (35719237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabaaeab6a3e08594f94cd55875749ff8661dede32531ddba0f6ae5ff40643dc`  
		Last Modified: Mon, 31 Mar 2025 17:26:02 GMT  
		Size: 8.3 MB (8324832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1c328ebc358ae52bf4805db89770c3f6153a0f504000c54bbeb35b35ede5e7`  
		Last Modified: Mon, 31 Mar 2025 17:26:02 GMT  
		Size: 1.2 MB (1230639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed59486ded323cb891cd7b3f767dc5468665552a3220373e5a86806e0911fa0b`  
		Last Modified: Mon, 31 Mar 2025 17:26:02 GMT  
		Size: 18.4 MB (18397816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ac922607949f1474a111016567f305165ad0b818a9a8437e94e66647c084b8`  
		Last Modified: Mon, 31 Mar 2025 17:26:03 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3272e455bb3e94e6bac9d4acd22486b3c7da7d767b27c04c689895b56901d4`  
		Last Modified: Mon, 31 Mar 2025 17:26:03 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97d62f7d3132951c6a6883badd65a46b1fb5a9881b08015a10e1e932b711f33`  
		Last Modified: Mon, 31 Mar 2025 17:26:04 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e3c45984e553e830ba949b8d7b0fb933ae64f7389a315df038d12b09cb64d8`  
		Last Modified: Mon, 31 Mar 2025 17:26:04 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:69ef4d165e66fee66297df90ee78f8f3ac5e554b65472ad7a085ed460c1ecbef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6701467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471f92982d6c94498f6bf1006d78f8ea902f975cd5f1e570fe90ec3c36b64780`

```dockerfile
```

-	Layers:
	-	`sha256:c62b098d0a7708168973e809282043539e9371dc216788518af50037b57f61f2`  
		Last Modified: Mon, 31 Mar 2025 17:26:02 GMT  
		Size: 653.8 KB (653780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:067469418e4396f1e4c45b7108873215c15082329f9c59a4a2b84d9f035a0ffa`  
		Last Modified: Mon, 31 Mar 2025 17:26:02 GMT  
		Size: 3.1 MB (3070850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23873f89569749ebc6e71ebb129f144cec0d218257573b697d3b2938b923b844`  
		Last Modified: Mon, 31 Mar 2025 17:26:02 GMT  
		Size: 2.9 MB (2917031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc9745731ba2f8eda503506c3d72236f23368dda6d586c1da6287cb2b9f18b8`  
		Last Modified: Mon, 31 Mar 2025 17:26:01 GMT  
		Size: 59.8 KB (59806 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:013595c24fd89ad986da1dc334751a9b84ee0f14bc3caf12e0ceafea0bf68003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68267805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c030683a2e9d6d736335800654609915c6bc3ba68de2f38edbb239885142a784`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Mar 2025 17:31:53 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 28 Mar 2025 17:31:53 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 28 Mar 2025 17:31:53 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_VERSION=4.0.7
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:31:53 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 28 Mar 2025 17:31:53 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 28 Mar 2025 17:31:53 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Mar 2025 17:31:53 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 28 Mar 2025 17:31:53 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5aa7d7f84a52cbd85f3246d33187103136e71ce2d49665dc0bd50ed97f5fa2f`  
		Last Modified: Mon, 31 Mar 2025 17:37:11 GMT  
		Size: 36.1 MB (36099090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d043ff8cb4736416d68a98932005fc9d702dccf8661da45bd7848681437848`  
		Last Modified: Mon, 31 Mar 2025 17:37:10 GMT  
		Size: 8.8 MB (8848299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9159be78c264822e25a3743b1e9d4de0141a016c8500560f58367b9466004776`  
		Last Modified: Mon, 31 Mar 2025 17:37:10 GMT  
		Size: 1.3 MB (1346545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8079098ff14ec3b726e37b601cf1b204820e4c8d0b0fa8ff73805184de61f67`  
		Last Modified: Mon, 31 Mar 2025 17:47:25 GMT  
		Size: 18.4 MB (18397780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7918b26f79ed55f6ddb83206548612a755feeb08e9b9449e1f58b17153e6cf`  
		Last Modified: Mon, 31 Mar 2025 17:47:25 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be6391312ed02d77c6cd002b2f73b2cb2b685e25b017639f6bdf505e8954abd`  
		Last Modified: Mon, 31 Mar 2025 17:47:25 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7eb068f19e632f65e30fae51336ce9b7cce6f3082131bb1d12544382fa0eaa`  
		Last Modified: Mon, 31 Mar 2025 17:47:25 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c330b5fa585b59f4ef5846cec3c1b08a66cb8e4a50f041577ceb89ba5cd643`  
		Last Modified: Mon, 31 Mar 2025 17:47:26 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:08e1de560cbdb227f3efcac157e8ae02bced321b27ba8530fc59253558bd2bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6733272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e69b3a88976ad042c417e1983c950496640847374dae9ff838f83c4c5b8d1dc`

```dockerfile
```

-	Layers:
	-	`sha256:210bc9aeb3e74ff7e40b495469b0d4d86d0915c0b61530a74b41334b2bf4f34a`  
		Last Modified: Mon, 31 Mar 2025 17:47:24 GMT  
		Size: 652.6 KB (652623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a9c94e52416b3b862d3d81b13ff2120667d551cbeb52f35dd02635274027cfc`  
		Last Modified: Mon, 31 Mar 2025 17:47:25 GMT  
		Size: 3.1 MB (3087942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db3178ff0dbf1c554a1b144acf6f02921804a2f80eff2737454a893938ddd91`  
		Last Modified: Mon, 31 Mar 2025 17:47:25 GMT  
		Size: 2.9 MB (2932788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:060d803f7bf8f5f8b366aefcea50d95555bd0cb9e6ec6d2466c9a4960295c4fb`  
		Last Modified: Mon, 31 Mar 2025 17:47:24 GMT  
		Size: 59.9 KB (59919 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:3c2d1265fc02e134f45ff517f4f30abb7b76cd2f18b1ded161f9c783a7eea888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69934610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6cab28eef174dc6bf85bfd07bd327fbb724e3f716f1c5f4fbd3071b797cfc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 05 Mar 2025 12:05:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 05 Mar 2025 12:05:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 05 Mar 2025 12:05:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 05 Mar 2025 12:05:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 05 Mar 2025 12:05:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Mar 2025 12:05:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 05 Mar 2025 12:05:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 05 Mar 2025 12:05:21 GMT
ENV RABBITMQ_VERSION=4.0.7
# Wed, 05 Mar 2025 12:05:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 05 Mar 2025 12:05:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 05 Mar 2025 12:05:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Mar 2025 12:05:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 05 Mar 2025 12:05:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 05 Mar 2025 12:05:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 05 Mar 2025 12:05:21 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 05 Mar 2025 12:05:21 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 05 Mar 2025 12:05:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 05 Mar 2025 12:05:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 05 Mar 2025 12:05:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 12:05:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Mar 2025 12:05:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 05 Mar 2025 12:05:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8feb8d671f818cb573474650cce5a8c5acc7104c81d28622a4ee4ca96bb4e3c`  
		Last Modified: Wed, 05 Mar 2025 22:41:51 GMT  
		Size: 37.1 MB (37059624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2989f682c4a736e8a9e146c3ce952e64e8e7219c83a84d999ad3eb329620b68d`  
		Last Modified: Wed, 05 Mar 2025 22:41:47 GMT  
		Size: 9.9 MB (9858935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a7604bba453807e1ec7932a70a095250682e93083e8d83085f9c5232e31613`  
		Last Modified: Wed, 05 Mar 2025 22:41:45 GMT  
		Size: 1.3 MB (1264922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c12b4d7ebe03f201c9b5d558d0f114140569a67d748ed329c872fdc49fa19a`  
		Last Modified: Wed, 05 Mar 2025 22:59:44 GMT  
		Size: 18.4 MB (18397941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9356f5c84f4dd0bbaeefbaa802554e93d797611a7def88b41df1957bebda5d9c`  
		Last Modified: Wed, 05 Mar 2025 22:59:41 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806726fb18de2e15f97090e7e88763ba78ffc21da7b87fac2f875ada5709c106`  
		Last Modified: Wed, 05 Mar 2025 22:59:41 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48228c17c624d579142885656056d79efb427f130bf61e6334bf41c5241d62d0`  
		Last Modified: Wed, 05 Mar 2025 22:59:41 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced07597332057263450d2bcd3916310704993d99b43514c58b7e6bf778308f6`  
		Last Modified: Wed, 05 Mar 2025 22:59:42 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:5df190a96c909ef8266e3eda87d1bdc58f9dea676f1fdbaafc88edbbab41d8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6810461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0b5238adaa6cf27be16f6ad97172495498b5e1be36e6086d08c43a9ca6b21b`

```dockerfile
```

-	Layers:
	-	`sha256:20f64e647ea62bfa27c903b8569c8c1fcf96b2dffc9b09da6a7b9805810dec0d`  
		Last Modified: Wed, 05 Mar 2025 22:59:41 GMT  
		Size: 654.8 KB (654786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dae392c9f1c742432ae3ffd3c7fb59cfa7148c85fdd3b4c5f9993842aed6c357`  
		Last Modified: Wed, 05 Mar 2025 22:59:42 GMT  
		Size: 3.1 MB (3125314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3adc0d37ffd475bea995984735c226bacba1e3daa88f59dfa2ced6558e7f4319`  
		Last Modified: Wed, 05 Mar 2025 22:59:42 GMT  
		Size: 3.0 MB (2970455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90fc545fe08018dab0b449ab1e6715a81abc6a41aa9624fbdbca3f996e3d9b8c`  
		Last Modified: Wed, 05 Mar 2025 22:59:41 GMT  
		Size: 59.9 KB (59906 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:71601f7a82e002256e9afb270b7d39d7347d72a17e18b9ad934fb1f78521ab29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66853702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7d5d32bcb6d4cceed36a6e762621b62044a6aa364a739e5336c6a1cf4e99b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Mar 2025 17:31:53 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 28 Mar 2025 17:31:53 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 28 Mar 2025 17:31:53 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_VERSION=4.0.7
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 28 Mar 2025 17:31:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:31:53 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:31:53 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 28 Mar 2025 17:31:53 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 28 Mar 2025 17:31:53 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 28 Mar 2025 17:31:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Mar 2025 17:31:53 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 28 Mar 2025 17:31:53 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8334131954c00b30a96f6fc2e5f9501952aff42cbda6df6eb09cf9c5454450e9`  
		Last Modified: Mon, 31 Mar 2025 17:29:20 GMT  
		Size: 36.2 MB (36150995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a706d054255a254f1e2075a7d9c7d78db0e3aa58653216a74a1c9a69c12d883`  
		Last Modified: Mon, 31 Mar 2025 17:29:20 GMT  
		Size: 7.5 MB (7510920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07fcd234c0bc7fe9474fcdef1e70aca0dd0f5bf3053a82eabadfaa6d1d5eb5ab`  
		Last Modified: Mon, 31 Mar 2025 17:29:20 GMT  
		Size: 1.3 MB (1324692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902338f4c9c777bda153b8901c5ce6f4f9c1dacd714e62273046967bb35e04c1`  
		Last Modified: Mon, 31 Mar 2025 17:40:10 GMT  
		Size: 18.4 MB (18397781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5620112aef94553106bca1c33e2ded0fe274adc98dad3e4470ca0419b72b2274`  
		Last Modified: Mon, 31 Mar 2025 17:40:10 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af271c43f4811aa81023f14513a1a260da9fe8fe83736faeff57625835b81ef`  
		Last Modified: Mon, 31 Mar 2025 17:40:10 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6fb140661f0a71661e77382703d9ba225ed844e0d0ac99c6eb94b6a8783644`  
		Last Modified: Mon, 31 Mar 2025 17:40:10 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44c23c8f986b56813483564ffa050b8faad4b2ad3b1eef2f43bdda1673029e7`  
		Last Modified: Mon, 31 Mar 2025 17:40:11 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:200a1a36d86eff24fe9ff6e921789b718444e0b0762268be7c0368d532099596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6513141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce3a7b9c453fd289ba5c7dbe03958a64ce498f0654e4fd88e60741cdca99dfd`

```dockerfile
```

-	Layers:
	-	`sha256:0b8538aeda1f2429738dbc251db54897f95a38bdada661638cd88a4dcdf3b960`  
		Last Modified: Mon, 31 Mar 2025 17:40:10 GMT  
		Size: 652.6 KB (652589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3ac13ba3e5077058a0cc3ff50bed5dc4b629048ce98a4b899a89aef382827d8`  
		Last Modified: Mon, 31 Mar 2025 17:40:10 GMT  
		Size: 3.0 MB (2977909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f8981c51e2c52d2cd2ef9cee6b9806ca1cb199b5b533fdf4d715717bfab8653`  
		Last Modified: Mon, 31 Mar 2025 17:40:10 GMT  
		Size: 2.8 MB (2822785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b18e96fecd4601818d076ae1d4e205de9f16677db7b47488281cfe25ec755b0c`  
		Last Modified: Mon, 31 Mar 2025 17:40:10 GMT  
		Size: 59.9 KB (59858 bytes)  
		MIME: application/vnd.in-toto+json
