## `rabbitmq:3-alpine`

```console
$ docker pull rabbitmq@sha256:34a3110294e75a5df5e038922ab18c11b9a34b0a49b9edcdad824c981688dc06
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

### `rabbitmq:3-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:3c1889c72ccc5bf22cc9ebfe3542073889b00374b27405190681bf50f29fbb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72009914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86545e84f1064eba607bdf3d7d3632d34d53d93462a6187c645c4d75a47d4582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:12:40 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 01 Apr 2025 23:12:40 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 01 Apr 2025 23:12:40 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_VERSION=3.13.7
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 23:12:40 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 01 Apr 2025 23:12:40 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 01 Apr 2025 23:12:40 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:12:40 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 01 Apr 2025 23:12:40 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46b1991ea487a5f030991e6987e69b29438256b1666fac290ba8d00989026b0`  
		Last Modified: Wed, 02 Apr 2025 00:01:06 GMT  
		Size: 39.7 MB (39730254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5efb25eaed0382c746a0b8ab1c4d07ad7d0faf6154b616dbf22976047a0e265`  
		Last Modified: Wed, 02 Apr 2025 00:01:06 GMT  
		Size: 7.6 MB (7600312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4feb5b45476ca2f9e079f0e53df245163799e0dcbd248aab5a43596aff73b8`  
		Last Modified: Wed, 02 Apr 2025 00:01:05 GMT  
		Size: 2.3 MB (2279278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323c17c9f3d665d3029f9556d525426c12226a4dbe5c0521e0129c83287be6a2`  
		Last Modified: Wed, 02 Apr 2025 00:01:06 GMT  
		Size: 18.8 MB (18756077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ba1c02c5997bd297d0b192f93f7f7e07b7b42e13ccb9d2c713cb70348ce4bf`  
		Last Modified: Wed, 02 Apr 2025 00:01:06 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d503848003fd0298e288e8f073feb7878093f2e2189e8a0c5584937ea09cef`  
		Last Modified: Wed, 02 Apr 2025 00:01:07 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99370772f7be27f839d4687c33fd25bd46cb3e2b598b82f5d204f31d46798db7`  
		Last Modified: Wed, 02 Apr 2025 00:01:07 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a558f2d252a1cdc1dab297febadc5f04aeb9464e8600a709a84959a0ae00794`  
		Last Modified: Wed, 02 Apr 2025 00:01:07 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c6f86fdcf9f297660416dfed6db253085cea1ecc090b3862a96fcba3476d5935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6724554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5dcf67e6d5dc86bc7a0efc551dbf1e450175d5d11456fa7e1ab23921fee33e`

```dockerfile
```

-	Layers:
	-	`sha256:426aa00bd59a63695aeb7f1750bce1c0f26bddbb44e27a0491b626deffeabbfa`  
		Last Modified: Wed, 02 Apr 2025 00:01:05 GMT  
		Size: 654.5 KB (654481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e4bf677368a316ff03f2ef3cb6c6f09f4a03c9197af4c91eff936dfe2ed8a19`  
		Last Modified: Wed, 02 Apr 2025 00:01:05 GMT  
		Size: 3.1 MB (3082616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18141a6eefb901a0d6ac62747a14889b608bbb6d740a8e58f60934ee175ec35d`  
		Last Modified: Wed, 02 Apr 2025 00:01:06 GMT  
		Size: 2.9 MB (2927783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50972af1c809dda434fa8876d48139023e29850ce88ee24925281bfd6ae9d388`  
		Last Modified: Wed, 02 Apr 2025 00:01:05 GMT  
		Size: 59.7 KB (59674 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:eca5c19bea0ca5d1fff8451e70f6eccbaf3e4f991cfec965371bbed1dce3b8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61064620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6901ba66179c36058c379bde51075f3776d17f726d720d1d4826774a435de59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:12:40 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 01 Apr 2025 23:12:40 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 01 Apr 2025 23:12:40 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_VERSION=3.13.7
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 23:12:40 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 01 Apr 2025 23:12:40 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 01 Apr 2025 23:12:40 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:12:40 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 01 Apr 2025 23:12:40 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a38c70220c01a12cd4918341d36b7d546b4c9d1a34fc85f88da321a27ce9b22`  
		Last Modified: Tue, 01 Apr 2025 23:59:16 GMT  
		Size: 31.3 MB (31289449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eccc728d7edd96bc88fa00a6caa5829a135f49df4502ae0475d2394f1d9248a`  
		Last Modified: Tue, 01 Apr 2025 23:59:16 GMT  
		Size: 6.4 MB (6425551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacd49d42da9545b893959f095104723e96d3cabcab09b29dc1f426d13549da9`  
		Last Modified: Tue, 01 Apr 2025 23:59:15 GMT  
		Size: 1.2 MB (1226987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8ada23146a8c2150ede931692e07a7bd88eb6dba7a6ae5cd49905bfd30beb6`  
		Last Modified: Tue, 01 Apr 2025 23:59:16 GMT  
		Size: 18.8 MB (18756154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35028dd68a844a1392c286635fba000327d93740881087aa5ea582700a5d78b`  
		Last Modified: Tue, 01 Apr 2025 23:59:16 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b456e267fab5182d3b0a09d928f5a59cac4c09a8cc39b19fdcb3d6c6c1a80989`  
		Last Modified: Tue, 01 Apr 2025 23:59:17 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534b53ce1e46449435a547f7b8a07162838da679bcd87d9b05860c9402192405`  
		Last Modified: Tue, 01 Apr 2025 23:59:18 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4a122455ad263a89d3268ab4254bbe615a2c87d77619bf4264a3f2c5b7cb47`  
		Last Modified: Tue, 01 Apr 2025 23:59:18 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b0a01892e8de50d6c893368745f00a3fd617572eedfb20130218e504f2a74edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 KB (59644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da59c80c68ab53fbf6bfd0c61d5a6cb2e1c8ae53ebf22bc22d5212f76f8ce71`

```dockerfile
```

-	Layers:
	-	`sha256:a1ab2ab82fb599d2b80fca431a0215f36a65302ee2a2a3f3a9e44734fbe531be`  
		Last Modified: Tue, 01 Apr 2025 23:59:16 GMT  
		Size: 59.6 KB (59644 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:8b30a4b654cad3dcca51ad43887d8dae90f1fc4049b82c51a86a0b20dc559103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62332531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df35f4d5a065df2abe21af0ee45b0f67327bdb77e898d586a01d12ed112b3545`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Mar 2025 17:05:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 28 Mar 2025 17:05:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 28 Mar 2025 17:05:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:05:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:05:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 28 Mar 2025 17:05:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 28 Mar 2025 17:05:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 28 Mar 2025 17:05:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:05:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:05:14 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 28 Mar 2025 17:05:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 28 Mar 2025 17:05:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Mar 2025 17:05:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 28 Mar 2025 17:05:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2587ca0c65c428fed2af7f81cf070229dbf0fe5aef67d2837e831e487037b064`  
		Last Modified: Mon, 31 Mar 2025 17:57:51 GMT  
		Size: 33.2 MB (33216386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c93f46e63be017fed9efddba5fddd24ed8790dfd4ec7a533cfef3fd965851e`  
		Last Modified: Mon, 31 Mar 2025 17:57:50 GMT  
		Size: 6.1 MB (6125523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2673a99d5c7ebe6039ed3b8a99e7f4eec2681c804260aaf1d61d9cad13a39f08`  
		Last Modified: Mon, 31 Mar 2025 17:57:55 GMT  
		Size: 1.1 MB (1134763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b27e9e9ca22ec3c40789880699b455c27bd5480a59dc63cea86d0d1d6dbf180`  
		Last Modified: Mon, 31 Mar 2025 17:57:51 GMT  
		Size: 18.8 MB (18755987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c6b63e415a73924399b9e491e5189188db7662d8a77fb04bf44157c4c81375`  
		Last Modified: Mon, 31 Mar 2025 17:57:51 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400a9c51f8a3fa3e0cfdac3e1a65c688457871e97ee0eba45d16c66dfbef77a6`  
		Last Modified: Mon, 31 Mar 2025 17:57:52 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc4d05dc70983c1f41db25d0cef44f1547d4504825fbf414d8cae330fc86798`  
		Last Modified: Mon, 31 Mar 2025 17:57:52 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb68e9edf0c28278c7e5bede249127bd450827db899e274ca9dbbb19770ebfc6`  
		Last Modified: Mon, 31 Mar 2025 17:57:52 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7abb4a286659dfbfc8fa97433cb5c556391a3c4118654e8ec6f4c8475f934fe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6493008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df1205d230b3d2e9accc66a77198f823262e9e85d3e988264167a09d2e5ada1`

```dockerfile
```

-	Layers:
	-	`sha256:45a5486d3fc3e530bde010963eeb259b6c2a7ec6fbb1a815da841550110cf6b7`  
		Last Modified: Mon, 31 Mar 2025 17:57:50 GMT  
		Size: 651.8 KB (651837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41887d2a96ef666d6438fb56365b67ac02385ae55a418242ad92175dcd296ea3`  
		Last Modified: Mon, 31 Mar 2025 17:57:50 GMT  
		Size: 3.0 MB (2969093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12c7f6dd7c6f6b13b5d72950535ad9e0d5150b869189e7672fea378d4f795cf`  
		Last Modified: Mon, 31 Mar 2025 17:57:50 GMT  
		Size: 2.8 MB (2812304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46b36814e624dd459199d15755f62b6a607d1abb3ebd7cb6c2290fa584b49e1d`  
		Last Modified: Mon, 31 Mar 2025 17:57:50 GMT  
		Size: 59.8 KB (59774 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:3377caef2bbc2e6544347a1d41d10f2478f64d301a1a58359ce44f487bf0df80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72235853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b63267b824c80d6cae5b5e89e81efeff2737c0850bdcf8d0986ed7fcd1a07e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Mar 2025 17:05:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 28 Mar 2025 17:05:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 28 Mar 2025 17:05:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:05:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:05:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 28 Mar 2025 17:05:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 28 Mar 2025 17:05:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 28 Mar 2025 17:05:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:05:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:05:14 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 28 Mar 2025 17:05:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 28 Mar 2025 17:05:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Mar 2025 17:05:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 28 Mar 2025 17:05:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4a0bccbbe155bd3d1c605927271e978d3bf9d829d32ba20d594b35050ca219`  
		Last Modified: Mon, 31 Mar 2025 17:48:21 GMT  
		Size: 39.9 MB (39920392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59177eaea4906bad7750d9427cedada4278f33a27e0eca05c90ec552727a95d`  
		Last Modified: Mon, 31 Mar 2025 17:48:20 GMT  
		Size: 7.2 MB (7240551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1ba9c99bb4c508c60b57bfd98f2bd0507201b6eff92f21b40abf651e8cc429`  
		Last Modified: Mon, 31 Mar 2025 17:48:20 GMT  
		Size: 2.3 MB (2323896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ac1c98aa56434a63614b4e5888245c0969799a08c0a7f9bdede1d941d70cc7`  
		Last Modified: Mon, 31 Mar 2025 17:48:21 GMT  
		Size: 18.8 MB (18756236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6786b6e4d6ed8b412d64f7ab0edbd8502237e364e186206e9c4c4c47e3de315f`  
		Last Modified: Mon, 31 Mar 2025 17:48:21 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1620cd32fb598710d6a3748fd6eb02aabf4a82f6d49a9f871fe5d2edc8ee231`  
		Last Modified: Mon, 31 Mar 2025 17:48:21 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f9f3179971214c83e8469152b17fd7f6a3eda1282bc858fc97cee775700e93`  
		Last Modified: Mon, 31 Mar 2025 17:48:22 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0c9148c58edc7b6059e5ff39a1aef43b17136bc3ef88c70ef82e4e81eb46ee`  
		Last Modified: Mon, 31 Mar 2025 17:48:22 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:40db9c210f53f5e9c40fe23903b49ce72424771c6421a4b89205329625c7f3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6835600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a1648fc0f20c58d3a7751757798db528fcaf726ea4feb04e2ab674f8b3966d`

```dockerfile
```

-	Layers:
	-	`sha256:3567c8c78a20bcf57ab9d8c0d6a74cb1fff8feeacfe072981374aff1e7305b08`  
		Last Modified: Mon, 31 Mar 2025 17:48:20 GMT  
		Size: 656.5 KB (656479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb46b310b7d29f92643ac1123ca41e391d98ccf846a43f62c4d2ba931482ee10`  
		Last Modified: Mon, 31 Mar 2025 17:48:20 GMT  
		Size: 3.1 MB (3138044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60f0aa1a005ea38cb804337ca91696cac014ecdb0d5b3911a58f2e7d5e5dd3e7`  
		Last Modified: Mon, 31 Mar 2025 17:48:20 GMT  
		Size: 3.0 MB (2981261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d5fe0d78da24937f99175bd6e38d740275f5710cb03ba2dd403c3ea723d7700`  
		Last Modified: Mon, 31 Mar 2025 17:48:20 GMT  
		Size: 59.8 KB (59816 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:0f4fc6b430fe629d352899e33bc426d20e3fb409c8e5b72bef8614130db9760f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62337333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8824040ba51da5d3148b2d7b4236016e64e93e31e831adb1cb90408000a03ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:12:40 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 01 Apr 2025 23:12:40 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 01 Apr 2025 23:12:40 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_VERSION=3.13.7
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 01 Apr 2025 23:12:40 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 23:12:40 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 01 Apr 2025 23:12:40 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 01 Apr 2025 23:12:40 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 01 Apr 2025 23:12:40 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:12:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:12:40 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 01 Apr 2025 23:12:40 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6092a40f6a1c033da5136700ebeb5c75d6e1fd8ac0024d58b8af2145a0d1567`  
		Last Modified: Wed, 02 Apr 2025 00:01:11 GMT  
		Size: 31.4 MB (31376147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105c7596d9f8399982d6e6d2d45401cd86e05ff0d90f63d057e06b534d877cfc`  
		Last Modified: Wed, 02 Apr 2025 00:01:11 GMT  
		Size: 7.5 MB (7509158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6df443ee5ad644dbea7308d9f6a8d73a9b83c5b14228f2afbcdd883e90a5afb`  
		Last Modified: Wed, 02 Apr 2025 00:01:11 GMT  
		Size: 1.2 MB (1230643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4986b1845ebc6adccdf89a4e62b3a3f527e2a0100b0869335c25a3a153a5e7`  
		Last Modified: Wed, 02 Apr 2025 00:01:11 GMT  
		Size: 18.8 MB (18756017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4d80a003a1019be8fe8b287f4dd8c1c80f8f7ab788908cee88106b68e23882`  
		Last Modified: Wed, 02 Apr 2025 00:01:11 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e89c5812297c61fe99bc9b30d3be8c2b7e232cf9a3d44516900f5b4e8802496`  
		Last Modified: Wed, 02 Apr 2025 00:01:12 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e2e44d82b7011468a01e8b83e2d0fa13baa08277d973f53d1eb203abf77ed0`  
		Last Modified: Wed, 02 Apr 2025 00:01:12 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169d797e02bd9c746d597f7c96f23c97e6373196558552dd34902eb56a6d7aff`  
		Last Modified: Wed, 02 Apr 2025 00:01:12 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f907f062908a74e4a026305717e9b5fdbb7a7998051a3e3c5a2174b8318825a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6697768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed5b12dcaa5998810ced7dc0f6b9cb55beac86ad10e565886b0e79667d3ac58`

```dockerfile
```

-	Layers:
	-	`sha256:2f106340cace104d29349bc57707f95ad1f47907041f739b52de1dbe5868a9e3`  
		Last Modified: Wed, 02 Apr 2025 00:01:11 GMT  
		Size: 649.8 KB (649835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f4ba5d9bde87a28ecbb872e4f0b72cf12285f91d0f0de6872220fec8ce7ab14`  
		Last Modified: Wed, 02 Apr 2025 00:01:11 GMT  
		Size: 3.1 MB (3071567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04f3ac6f502e246c5994884bce8ce2acd46fa2271554a29eceacb6ffaa78784a`  
		Last Modified: Wed, 02 Apr 2025 00:01:11 GMT  
		Size: 2.9 MB (2916738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:830a412f3aaa5280fab468fa967cf4bb30acc0644d171d75de0f7d6f8499e53c`  
		Last Modified: Wed, 02 Apr 2025 00:01:11 GMT  
		Size: 59.6 KB (59628 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:14166a0a4b9c5b64ad950fef2b8da7536e19b5dbb0993ceacb774b5e61deb3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65436439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f809a0316af0333dfa1361d31d803d91ba288105bd75f4a1f245c0d40c726f94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Mar 2025 17:05:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 28 Mar 2025 17:05:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 28 Mar 2025 17:05:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:05:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:05:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 28 Mar 2025 17:05:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 28 Mar 2025 17:05:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 28 Mar 2025 17:05:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:05:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:05:14 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 28 Mar 2025 17:05:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 28 Mar 2025 17:05:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Mar 2025 17:05:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 28 Mar 2025 17:05:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabe201fbc7ce49930d5e6c1cbc90b750052755afcccd96ee14da99cf2ce51bb`  
		Last Modified: Mon, 31 Mar 2025 17:57:20 GMT  
		Size: 33.8 MB (33753902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac20f7dad8081982c16c678881214cd174eec5535db64eee7c9cdb2a809a59a8`  
		Last Modified: Mon, 31 Mar 2025 17:57:19 GMT  
		Size: 8.0 MB (8003853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84580b04a4dc093326e23e7410dcaf0a7df1d94dcb8374228636a7e79e85a0a1`  
		Last Modified: Mon, 31 Mar 2025 17:57:19 GMT  
		Size: 1.3 MB (1346522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f35703a472d5d711b205e9ab5f082de6f39ce92ac1ca9d3a916cf8e99c17d66`  
		Last Modified: Mon, 31 Mar 2025 17:57:20 GMT  
		Size: 18.8 MB (18756070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a1d58ded66d97abed666696f15a94c23e5a8d7a9a26fcfb740016a1c1e6d89`  
		Last Modified: Mon, 31 Mar 2025 17:57:20 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558a274b973341b5b48549c1222b63f2cbc556c1d211cef711ff213011cacf79`  
		Last Modified: Mon, 31 Mar 2025 17:57:20 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53d1a28c28bb4dfdaadb2a63aa8f4789fe2ab1286e92ed7617ddf0c0c242c3a`  
		Last Modified: Mon, 31 Mar 2025 17:57:21 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0b4b73523a35bf32035bd12390b3278c82cf65e5c6c02d6b563b14f9cceb09`  
		Last Modified: Mon, 31 Mar 2025 17:57:21 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:610b105a0015bc12c43965d026f45f378b3a311e88b097e2199ee09d6e73b08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6731294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3125f68ff921e67fcbd3e2b2ccdd7bb91edca708996dd5d43256e0b1595c06ec`

```dockerfile
```

-	Layers:
	-	`sha256:c6adacc564f7041c4eb5da8a1bf288cd62a4bf55468a738dcabf564c77d9990a`  
		Last Modified: Mon, 31 Mar 2025 17:57:19 GMT  
		Size: 649.9 KB (649886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:253571f24bdfef885bb38931f0a96d001845873bf6c8401ec708c35a80cf8094`  
		Last Modified: Mon, 31 Mar 2025 17:57:19 GMT  
		Size: 3.1 MB (3089279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c55df78cdbf77b9d12e4545e0b046e9fa7ae11b609bac2a5bee2f47866bc111`  
		Last Modified: Mon, 31 Mar 2025 17:57:19 GMT  
		Size: 2.9 MB (2932484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27674cf0fc888a18b21ead7e36dd922a3e9324466444b2014ef82e5a03838fe7`  
		Last Modified: Mon, 31 Mar 2025 17:57:19 GMT  
		Size: 59.6 KB (59645 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:beb18dca9f2f9ec3b181475760fb42bfaf8f2399ad05db4d5b070b64569431e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66849862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade4c06d20c953cd66dad6d36355dabc88e798f5ef13a969a4e0d5c01274d6b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Mar 2025 17:05:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 28 Mar 2025 17:05:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 28 Mar 2025 17:05:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:05:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:05:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 28 Mar 2025 17:05:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 28 Mar 2025 17:05:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 28 Mar 2025 17:05:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:05:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:05:14 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 28 Mar 2025 17:05:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 28 Mar 2025 17:05:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Mar 2025 17:05:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 28 Mar 2025 17:05:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8681c773da94d13e7ece169368f8268be8b4d03c5e3cb07aec5b245e47daf23`  
		Last Modified: Tue, 01 Apr 2025 00:27:41 GMT  
		Size: 34.7 MB (34713609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d355642687c04ec3540709e405d41482a256e89073d5798c749c93d26f107f`  
		Last Modified: Tue, 01 Apr 2025 00:27:37 GMT  
		Size: 8.8 MB (8760518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8bec5877c6b4953826ed9c24f8111306c25e120857c6195e24bc5273fb0ffa`  
		Last Modified: Tue, 01 Apr 2025 00:27:35 GMT  
		Size: 1.3 MB (1266437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861316c007c059d33d28e6e7bd1540fdc2935696ddbb8d20e54f7cbd8862626d`  
		Last Modified: Tue, 01 Apr 2025 00:27:39 GMT  
		Size: 18.8 MB (18756108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d88f6396a9fa1e1d836ffd4948ccdb1648354ebfee5254d90dd1b2c6d706e8`  
		Last Modified: Tue, 01 Apr 2025 00:27:36 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89574be8627c593fa735bcc7666362fa8458e767035a57bcaad4d93ea7137d40`  
		Last Modified: Tue, 01 Apr 2025 00:27:38 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a568052be162e0a034d95b3db5fc043b62d7216e51b7354864c44c5f26c8fa00`  
		Last Modified: Tue, 01 Apr 2025 00:27:38 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd23e098eb4710775d32962c071df0985fe7b5a402140fca3b4694adcccd522`  
		Last Modified: Tue, 01 Apr 2025 00:27:38 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1586a048a2d0f6ed58ca2eaf2bc6a0b74436126f27c95da55f8356e0f2c4d558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6809408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0fb1840512d8d41fcf6e0b241af1fe0cf274a6e533a9d71d89737e25696c17`

```dockerfile
```

-	Layers:
	-	`sha256:4571a02bf26e7c70a15a6bba42f5b7975336cf3873f7a256f2ecdb10cedf3c78`  
		Last Modified: Tue, 01 Apr 2025 00:27:35 GMT  
		Size: 652.7 KB (652678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56259fd65ece81297e08e7ca213e8bdede4780922016248bde1730eabbf3f9ee`  
		Last Modified: Tue, 01 Apr 2025 00:27:36 GMT  
		Size: 3.1 MB (3126934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f348e246f75c4b762002c651a7aa7b88d06494625713adebff295a174013768`  
		Last Modified: Tue, 01 Apr 2025 00:27:36 GMT  
		Size: 3.0 MB (2970151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd5fa0fac94c0193bb9ba85c70d64e8986342c35726e47a15cc2571ab5267837`  
		Last Modified: Tue, 01 Apr 2025 00:27:35 GMT  
		Size: 59.6 KB (59645 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:10e029c15784514e2c6c4ea7c8b5e9915d0eb860f10018453f12e9862f8ce07b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64084457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:692dbcc36eeb5f4d3fb3166886609cdf257836f343bbd93b544cb5c32d792b80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Mar 2025 17:05:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 28 Mar 2025 17:05:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 28 Mar 2025 17:05:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:05:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:05:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 28 Mar 2025 17:05:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 28 Mar 2025 17:05:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 28 Mar 2025 17:05:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Mar 2025 17:05:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 28 Mar 2025 17:05:14 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 28 Mar 2025 17:05:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 28 Mar 2025 17:05:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 28 Mar 2025 17:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Mar 2025 17:05:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 28 Mar 2025 17:05:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0c5c8b2f3e39b35551933474e73d269c8f3aa007179a55eff92ed7bd097c84`  
		Last Modified: Mon, 31 Mar 2025 17:50:50 GMT  
		Size: 33.8 MB (33789054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611cb134b8cd20c4032c4e3fb56aded0d3b262cf0e4145d8be04ff259b6873e2`  
		Last Modified: Mon, 31 Mar 2025 17:50:50 GMT  
		Size: 6.7 MB (6745390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7195e4b99c4bb8690ab8e62df9f808aced5c0363d8ce91889953819e12b21ccf`  
		Last Modified: Mon, 31 Mar 2025 17:50:50 GMT  
		Size: 1.3 MB (1324686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3f4d3e5de701e3813d52a21c8c68769ad7b58700af64d0fba64a69b63cf44b`  
		Last Modified: Mon, 31 Mar 2025 17:50:51 GMT  
		Size: 18.8 MB (18756012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4fddd1cee20aa068af74a962aaa640d041db626a4e0caf7fe2b28dde6b82b0`  
		Last Modified: Mon, 31 Mar 2025 17:50:51 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50084df34240965679ad5063dd54de6619e68e94492ada850c429ca208badbce`  
		Last Modified: Mon, 31 Mar 2025 17:50:51 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110a76a8c593fea688b89b6f2f264531a5f434bb3b237766cec4ae27f495ca96`  
		Last Modified: Mon, 31 Mar 2025 17:50:51 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c15704631168c85c4d654a94b663b63a306bdb60099d7065202753117ad921`  
		Last Modified: Mon, 31 Mar 2025 17:50:52 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f225eb05fccc1f602d1076c46e9f88e78d5afda1711165b003e8ab49fdd05c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6511186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998ac103c11897a5b4e27237557808f1707f14421571f60868d15ac5760f1a12`

```dockerfile
```

-	Layers:
	-	`sha256:7b6e0cc5b5c0383369deedb12753d5de729e18871224178f8499f61329a4404f`  
		Last Modified: Mon, 31 Mar 2025 17:50:50 GMT  
		Size: 649.9 KB (649858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a656a1003a965e981099ee1e80210082bd8ba72471b523ac685d7179a5a660c1`  
		Last Modified: Mon, 31 Mar 2025 17:50:50 GMT  
		Size: 3.0 MB (2979252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da33997691f39b9344533234497d1ea6f0cd6190ff543937cda9d801b0dcc1f9`  
		Last Modified: Mon, 31 Mar 2025 17:50:50 GMT  
		Size: 2.8 MB (2822487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d28defbcf4263d096103cf9462760cfe7ccb0a4837c00a56d3d63b23ea002eea`  
		Last Modified: Mon, 31 Mar 2025 17:50:49 GMT  
		Size: 59.6 KB (59589 bytes)  
		MIME: application/vnd.in-toto+json
