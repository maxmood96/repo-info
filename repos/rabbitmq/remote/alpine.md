## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:ae39273718413123950b4611438c49b9cc5290951c9224f4c9bce4c6347fe8ab
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
$ docker pull rabbitmq@sha256:ff224f2bdf34ccfd82ba39a15757ddfb63a8a7d0aa0b5ce6add50431885c3688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83504628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d8d234f070fd7dacc38e0210988bbe1aeea84f3fa9be6c8bcc740ad565a814`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:45:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 28 Jan 2026 03:45:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 28 Jan 2026 03:45:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 28 Jan 2026 03:45:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 28 Jan 2026 03:45:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:45:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 28 Jan 2026 03:45:23 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 28 Jan 2026 03:45:23 GMT
ENV RABBITMQ_VERSION=4.2.3
# Wed, 28 Jan 2026 03:45:23 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 28 Jan 2026 03:45:23 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 28 Jan 2026 03:45:23 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:45:29 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 28 Jan 2026 03:45:30 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 28 Jan 2026 03:45:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 28 Jan 2026 03:45:30 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 28 Jan 2026 03:45:30 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 28 Jan 2026 03:45:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 28 Jan 2026 03:45:30 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Wed, 28 Jan 2026 03:45:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 28 Jan 2026 03:45:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:45:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:45:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 28 Jan 2026 03:45:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c03c8cb72abfea7d2f029f025726abe9a481f482ff1e1f58323d46b46d0b274`  
		Last Modified: Wed, 28 Jan 2026 03:45:49 GMT  
		Size: 42.6 MB (42598772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ee09aa22c105fd519d1af849c9df70ff2db0a45312dcaee5bb944ef4f4a837`  
		Last Modified: Wed, 28 Jan 2026 03:45:47 GMT  
		Size: 9.2 MB (9198226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b317c244c31673a1d526dc3b102829b67ec442bc560c5684335fc4b6ff815f8`  
		Last Modified: Wed, 28 Jan 2026 03:45:47 GMT  
		Size: 2.5 MB (2465552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33144c1ddd05e8ba40d5f358d26dced066e71846457a1009d343e0b1b9c95550`  
		Last Modified: Wed, 28 Jan 2026 03:45:48 GMT  
		Size: 25.4 MB (25378508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8686245d4b190ed55d82e0ec162e50ddf3c8aaa9088392fd064fa0c9473509`  
		Last Modified: Wed, 28 Jan 2026 03:45:48 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8434cd8d5903949bff8900cf7bdd1a0b93bbaa922c4e10f52a87892eedfdbc6e`  
		Last Modified: Wed, 28 Jan 2026 03:45:49 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c28cd67ebccd8b77f40bdb255619840330b977e3c7757198e63093fdca43d94`  
		Last Modified: Wed, 28 Jan 2026 03:45:50 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f60c635098106c8add7adbfbd90a7d95f88ca635bf8bccf465a44e3928ab30`  
		Last Modified: Wed, 28 Jan 2026 03:45:50 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:844847ae33d4ff51ec6345a05b1fc6aca7f325e3d4aca3e8f1fba63e9e03175f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6963072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048de7642d709c082459b7989cc611d7e15418dfe6224fcbb9157b0424e787a0`

```dockerfile
```

-	Layers:
	-	`sha256:40477cc04c222eb3e9fb923459296668168b77d0cc42dead998b3e8d169eda23`  
		Last Modified: Wed, 28 Jan 2026 03:45:47 GMT  
		Size: 675.7 KB (675697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02a65adb0f2e1c1b9a1165e68c36aa7445b02dc9738d22f7ef454056cce061d5`  
		Last Modified: Wed, 28 Jan 2026 03:45:47 GMT  
		Size: 3.2 MB (3190316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d6d7de0abc6a28e364ae5af1290f6d065aed5e5298fa2abd0e1ab3f1ba0c092`  
		Last Modified: Wed, 28 Jan 2026 03:45:47 GMT  
		Size: 3.0 MB (3036751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4423055db8b8bab90666332afe126350251329f23de92cfda4012ec73bd06ad3`  
		Last Modified: Wed, 28 Jan 2026 03:45:46 GMT  
		Size: 60.3 KB (60308 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:82ff8da5cdf0ee7d28f5beb9946e33644b992d139fcf9aeb2eaad4960abc1c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71712138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b267af761237f17eec183cb5ab652a6f5e6cf0fa0edf5ad5bc5454d59b1dac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Tue, 27 Jan 2026 21:26:41 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 27 Jan 2026 21:26:41 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 27 Jan 2026 21:26:41 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 27 Jan 2026 21:26:41 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 27 Jan 2026 21:26:41 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 21:26:41 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 27 Jan 2026 21:26:43 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 27 Jan 2026 21:26:43 GMT
ENV RABBITMQ_VERSION=4.2.3
# Tue, 27 Jan 2026 21:26:43 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 27 Jan 2026 21:26:43 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 27 Jan 2026 21:26:43 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 21:26:52 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 27 Jan 2026 21:26:54 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 27 Jan 2026 21:26:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 27 Jan 2026 21:26:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 27 Jan 2026 21:26:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 27 Jan 2026 21:26:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 27 Jan 2026 21:26:54 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 27 Jan 2026 21:26:54 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 27 Jan 2026 21:26:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Jan 2026 21:26:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Jan 2026 21:26:55 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 27 Jan 2026 21:26:55 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d16be1243dbc76852752e8cc0fd2b9ff14d99ee1cff70c25d49a7ea5f63a59e`  
		Last Modified: Tue, 27 Jan 2026 21:27:02 GMT  
		Size: 33.5 MB (33504503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02f8a97c38b6e8c60ed7dd5ae822a71d40f15230948d2540123000d3feb72c1`  
		Last Modified: Tue, 27 Jan 2026 21:27:01 GMT  
		Size: 7.9 MB (7854408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457adb0c767c107fb81f029b9a78d7666866e405edf1f0e0836de9bbffeb98f4`  
		Last Modified: Tue, 27 Jan 2026 21:27:01 GMT  
		Size: 1.4 MB (1404596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb0fd55d4912f18b7061cb0df743a1ef8e5f3c6bd22af7650b823938c7ce5bc`  
		Last Modified: Tue, 27 Jan 2026 21:27:02 GMT  
		Size: 25.4 MB (25378453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9571a3a00969a94b894f4a8b7ed31195f26d17bdeffb306f230d822d8cbf40d1`  
		Last Modified: Tue, 27 Jan 2026 21:27:02 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3011cf60ea2a6e166082c1ef20e0b5c9939d919ef6e1c1e07794ef78e11d95f1`  
		Last Modified: Tue, 27 Jan 2026 21:27:03 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8376c55ac817a04a26b7fd9ab5bfd65d88a65b91bf1f336bc9a0fc39a8a2893e`  
		Last Modified: Tue, 27 Jan 2026 21:27:04 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e799599ef4cad47e092c2ee4fc7b4db1bc13f8527d9e60c180ba6d319e610a`  
		Last Modified: Tue, 27 Jan 2026 21:27:04 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c925e6985baadbe8c950b2124baa0fcb5d5ec44df7ca523546c7892cad763345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 KB (60289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde4ba45f38c52af75f6595b2fd2529548302c5ea600b2a0f89bbc708455b35e`

```dockerfile
```

-	Layers:
	-	`sha256:79da5048d9e7d0f49120cf36da6d539ed877fc43626efff66a58d60a32ef78b2`  
		Last Modified: Tue, 27 Jan 2026 21:27:01 GMT  
		Size: 60.3 KB (60289 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:59f7d2cc245bcdaa88756efdb3c21a5014f03eb36adb0582e95723511de88fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70803019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221066c094cce305293541d29a7c1537a40d56c083195519842a252792f378c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:43:18 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 28 Jan 2026 03:43:18 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 28 Jan 2026 03:43:18 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 28 Jan 2026 03:43:18 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 28 Jan 2026 03:43:18 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:43:18 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 28 Jan 2026 03:43:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 28 Jan 2026 03:43:20 GMT
ENV RABBITMQ_VERSION=4.2.3
# Wed, 28 Jan 2026 03:43:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 28 Jan 2026 03:43:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 28 Jan 2026 03:43:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:43:27 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 28 Jan 2026 03:43:28 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 28 Jan 2026 03:43:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 28 Jan 2026 03:43:28 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 28 Jan 2026 03:43:28 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 28 Jan 2026 03:43:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 28 Jan 2026 03:43:28 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Wed, 28 Jan 2026 03:43:28 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 28 Jan 2026 03:43:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:43:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:43:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 28 Jan 2026 03:43:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3be0934b1fcd2bffc8f22748108cdcdf2f6dba9084b3e8a74214ca660eb00a2`  
		Last Modified: Wed, 28 Jan 2026 03:43:44 GMT  
		Size: 33.4 MB (33409926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d8a98a38c5f38975e8ec30204db16463a23bef55ab526708d5e80629becb90`  
		Last Modified: Wed, 28 Jan 2026 03:43:43 GMT  
		Size: 7.4 MB (7435298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcafadb861aed09ee351612c044de2ab2bd7ec24b9e6fc7706f2ebb5e0b715e1`  
		Last Modified: Wed, 28 Jan 2026 03:43:42 GMT  
		Size: 1.3 MB (1295849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91079439587f0666f42fc3e2e94c8f06c30e45ce77b9088e2865792186c3b24`  
		Last Modified: Wed, 28 Jan 2026 03:43:44 GMT  
		Size: 25.4 MB (25378475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11c55cb75622dd2a1169a5eaedf2d62875d67556e55eb216183f01a0a1ede98`  
		Last Modified: Wed, 28 Jan 2026 03:43:44 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c890becdcc6c8b3ff4158ed0f082f722c2bf4f4db233040c8828a670b6756c`  
		Last Modified: Wed, 28 Jan 2026 03:43:44 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a77cc9712a969a77f633b8b50d6d2132b48dc6dcc449ffe02bab5fab5052f6e`  
		Last Modified: Wed, 28 Jan 2026 03:43:45 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773d7e862617727c9af9d58fbf1e672a4062077af742e57a9f81520a36db295a`  
		Last Modified: Wed, 28 Jan 2026 03:43:45 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a2a1627ba650cbb3732116e968345d4b37c037295dac46adb06e5bee9989d072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8cb316955dee03f2fa8a19d39ac5ab7f5dd0f2cdee1c83255b748f69776e48`

```dockerfile
```

-	Layers:
	-	`sha256:5fe4dedbe39862e0ffda4118cc8441b90b3c35a4f72c8e0a048ef7b6304f1db5`  
		Last Modified: Wed, 28 Jan 2026 03:43:42 GMT  
		Size: 670.8 KB (670840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba80c054932696057dabeec80bef94bbdd7d8bf90941094f22a59e8484814a94`  
		Last Modified: Wed, 28 Jan 2026 03:43:42 GMT  
		Size: 3.1 MB (3056807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e27274da7c9015ae00a5716a6bd88447b488a792ddb4a39ad801b0d8c544a093`  
		Last Modified: Wed, 28 Jan 2026 03:43:42 GMT  
		Size: 2.9 MB (2901913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bd1e91ac8e05e798348b7e6e9bea69d635470a9b39038b09b47a833024065a3`  
		Last Modified: Wed, 28 Jan 2026 03:43:42 GMT  
		Size: 60.5 KB (60505 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:f0adde5e43303c01a1acf881f398712ead72e7f6123d1e69bb7baa06a660feff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82524576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a84a13738903b40fb02911196b978397b7b7fba00a2de199b36594fd24df19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Tue, 27 Jan 2026 21:32:37 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 27 Jan 2026 21:32:37 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 27 Jan 2026 21:32:37 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 27 Jan 2026 21:32:37 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 27 Jan 2026 21:32:37 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 21:32:37 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 27 Jan 2026 21:32:39 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 27 Jan 2026 21:32:39 GMT
ENV RABBITMQ_VERSION=4.2.3
# Tue, 27 Jan 2026 21:32:39 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 27 Jan 2026 21:32:39 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 27 Jan 2026 21:32:39 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 21:32:45 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 27 Jan 2026 21:32:46 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 27 Jan 2026 21:32:46 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 27 Jan 2026 21:32:46 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 27 Jan 2026 21:32:46 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 27 Jan 2026 21:32:46 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 27 Jan 2026 21:32:46 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 27 Jan 2026 21:32:46 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 27 Jan 2026 21:32:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Jan 2026 21:32:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Jan 2026 21:32:46 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 27 Jan 2026 21:32:46 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b840f8b7b2c612506ac27612e01cbc76a0ec309ba7bf3cb14b397d9f9d7dc67f`  
		Last Modified: Tue, 27 Jan 2026 21:33:04 GMT  
		Size: 40.5 MB (40454930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6caf8b87ebb3cb95c028ada2b87f25eeec833049c57a9b1d982ba3f50f7b2ef`  
		Last Modified: Tue, 27 Jan 2026 21:33:03 GMT  
		Size: 10.0 MB (9979261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6993f25e4ea2aca76110b5f2e0747112f0287b1e4b9db58b6bc847ea6d79c47f`  
		Last Modified: Tue, 27 Jan 2026 21:33:02 GMT  
		Size: 2.5 MB (2514390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c4422557c3ed173ba2825ce3d36fd563ab9b849733a48ad2067928572b5ac1`  
		Last Modified: Tue, 27 Jan 2026 21:33:07 GMT  
		Size: 25.4 MB (25378510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1ac3ef1206a1f229c640f917ec48acbb6d4036eeab449f08274a8432db4121`  
		Last Modified: Tue, 27 Jan 2026 21:33:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a824824a1170e07f3f1a4b7cb9f4b007facc9dd313ac73ce5b0eb6ac3bbac576`  
		Last Modified: Tue, 27 Jan 2026 21:33:04 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d90bdfae6094f7618cd1726baf0eac83b3f126f0800ee9ef36e540aef7bc69`  
		Last Modified: Tue, 27 Jan 2026 21:33:05 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e89c67cd9109dae648685c57bb6a8aa08a8e1faa4186f2deaeeef03b25a7e9`  
		Last Modified: Tue, 27 Jan 2026 21:33:05 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3bdb0cb05cd7361636f8bc26fd83350002344b737bfc494213a6baf7355c8f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7036049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe0556402c62f1d3705499da83e309cd3f331ed75996da08eef20adf04ff5eb`

```dockerfile
```

-	Layers:
	-	`sha256:c613a06019ce2a82e2248a83237f435463cd59283e7bedd4ded1fb35b8913bee`  
		Last Modified: Tue, 27 Jan 2026 21:33:03 GMT  
		Size: 675.8 KB (675840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a59260aac6a862f6098d6f18236857672f7f18626c0d413805c71606b83db183`  
		Last Modified: Tue, 27 Jan 2026 21:33:03 GMT  
		Size: 3.2 MB (3227275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d45cf05f8ef6be06b0bb08bbb6bcfe2c2de478376676822566f5850cf578deb4`  
		Last Modified: Tue, 27 Jan 2026 21:33:03 GMT  
		Size: 3.1 MB (3072387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14328c9ea7293d963c8f45f2caf9f702b2749496c29a6c8a2bfc62a9abb87eb1`  
		Last Modified: Tue, 27 Jan 2026 21:33:02 GMT  
		Size: 60.5 KB (60547 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:24d24635213e3c49887e7e0a1ebc69cbd90e4cc8aa92fe6511ec37a3cb5b6227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73126583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d59fe9bd58184f0dfba7d1e27e93d33209cf7c1bb62a7c21b66fad12f8a0694`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:47:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 28 Jan 2026 02:47:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 28 Jan 2026 02:47:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 28 Jan 2026 02:47:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 28 Jan 2026 02:47:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:47:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 28 Jan 2026 02:47:55 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 28 Jan 2026 02:47:55 GMT
ENV RABBITMQ_VERSION=4.2.3
# Wed, 28 Jan 2026 02:47:55 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 28 Jan 2026 02:47:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 28 Jan 2026 02:47:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:48:01 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 28 Jan 2026 02:48:01 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 28 Jan 2026 02:48:01 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 28 Jan 2026 02:48:01 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 28 Jan 2026 02:48:01 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 28 Jan 2026 02:48:01 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 28 Jan 2026 02:48:01 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Wed, 28 Jan 2026 02:48:01 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 28 Jan 2026 02:48:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:48:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:48:01 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 28 Jan 2026 02:48:01 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0a2bff71f2ed86bdad8b80228007348d093454752574f48408fdd403b7043`  
		Last Modified: Wed, 28 Jan 2026 02:48:16 GMT  
		Size: 33.5 MB (33459063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4345a99b957702cd25dbf789fbe6f16797c8483f355336d0745fdd32d8c80b7f`  
		Last Modified: Wed, 28 Jan 2026 02:48:15 GMT  
		Size: 9.2 MB (9191404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bc59b218a265b272443d8d7427cd20c8fbf704056b8fe6936c90ffda46f753`  
		Last Modified: Wed, 28 Jan 2026 02:48:14 GMT  
		Size: 1.4 MB (1408993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82aead96781ccd4bdc2a70678bcad440c7a52d42bd876c2cc7202f3ddcf09fa4`  
		Last Modified: Wed, 28 Jan 2026 02:48:16 GMT  
		Size: 25.4 MB (25378381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c088ed02fa376870687edf1e7cbef77cecc032b485e91370b3900949da2aa238`  
		Last Modified: Wed, 28 Jan 2026 02:48:16 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16d98fcb2296c91125838f46475b091944a6e7821d7433e1c957da01c023409`  
		Last Modified: Wed, 28 Jan 2026 02:48:16 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5b8299bb6676aa71002a44694a05b9814f87ad09b6a67592353df6cb2b3a3a`  
		Last Modified: Wed, 28 Jan 2026 02:48:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496fa4a4c000fcc36a48aead12e413982592a5b761b183e05eb5f855de17c7cf`  
		Last Modified: Wed, 28 Jan 2026 02:48:17 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:703861f0712368f8e4ad5815041584abb8444611d3d4711d3492d6cad299963f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6914527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961ea9c89dc507bb1e7bbbbb489016d593142c252238827eabe3f9468a1a060f`

```dockerfile
```

-	Layers:
	-	`sha256:572ed6d4dd5f6ffc948c4e8dbd8039ccad12b0312afcb54340cfd8b61dedb0b5`  
		Last Modified: Wed, 28 Jan 2026 02:48:14 GMT  
		Size: 670.7 KB (670692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f629d1c9652f6356e74a2f112b1c297fa695c9d49403305b8a454262af6f3a1`  
		Last Modified: Wed, 28 Jan 2026 02:48:14 GMT  
		Size: 3.2 MB (3168569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fcfb8cd988bc0b2290e70ffb39f47ad4a6cb9780a1f9f83168c2959d958305f`  
		Last Modified: Wed, 28 Jan 2026 02:48:15 GMT  
		Size: 3.0 MB (3015008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5639179fbd5896d614a6ca80904f93824d9cd750278fa912f81ed6d5c946db85`  
		Last Modified: Wed, 28 Jan 2026 02:48:14 GMT  
		Size: 60.3 KB (60258 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:0b8d8d2dc69ac5a235edee91139cdf4da68816efd501a2caa4ab44c9cb34fd60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74770467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b301fcf29e9b09e50b09e6fd737967900f8269e03d218742a70ee5b7b985909`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Tue, 27 Jan 2026 21:39:07 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 27 Jan 2026 21:39:07 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 27 Jan 2026 21:39:07 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 27 Jan 2026 21:39:08 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 27 Jan 2026 21:39:08 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 21:39:08 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 27 Jan 2026 21:39:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 27 Jan 2026 21:39:13 GMT
ENV RABBITMQ_VERSION=4.2.3
# Tue, 27 Jan 2026 21:39:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 27 Jan 2026 21:39:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 27 Jan 2026 21:39:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 21:39:24 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 27 Jan 2026 21:39:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 27 Jan 2026 21:39:27 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 27 Jan 2026 21:39:27 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 27 Jan 2026 21:39:27 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 27 Jan 2026 21:39:27 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 27 Jan 2026 21:39:27 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 27 Jan 2026 21:39:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 27 Jan 2026 21:39:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Jan 2026 21:39:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Jan 2026 21:39:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 27 Jan 2026 21:39:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:42 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e7d0bb318a203d75f2cdfa5a018e7dfd6acb5d59d495f8b8eaf042a694ebe6`  
		Last Modified: Tue, 27 Jan 2026 21:40:04 GMT  
		Size: 34.1 MB (34067284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4287cef0a03e800d06a366426c6aa7edccfaba6207953376e39f66d28620fa15`  
		Last Modified: Tue, 27 Jan 2026 21:40:03 GMT  
		Size: 10.0 MB (9952633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33f7a02254e00c5492916316f1cd52ed602b78f033fbb99d908df79ba703c1e`  
		Last Modified: Tue, 27 Jan 2026 21:40:02 GMT  
		Size: 1.5 MB (1542620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1c74fd687eaae0d8ff7a299ce3e2fcea2b0325235f072d0e55774eaf2946c1`  
		Last Modified: Tue, 27 Jan 2026 21:40:04 GMT  
		Size: 25.4 MB (25378415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04dc30faefb3276e14636ad2d7219ffadee8368b54cadc27b3e98a7b03a5392`  
		Last Modified: Tue, 27 Jan 2026 21:40:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8a4e1772184fe5edfca6df7c567a61caca8c38a85d75d534bf7b272e981b6d`  
		Last Modified: Tue, 27 Jan 2026 21:40:04 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed4f519a2e4e8f9884a25c3450dd6f1b0a4274796a939cd92d209c711a5d6df`  
		Last Modified: Tue, 27 Jan 2026 21:40:05 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a72fa4ed1d9cf257d42a2596b06ee9b2feebc48cc64d8f926c971507ed7dee5`  
		Last Modified: Tue, 27 Jan 2026 21:40:05 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b42f473de4a51ad6791e766d580bae0f7bba6674fc4a7426c1786064bf97e6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6937727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13653b1cf15ff46dba1d69920fd2745ee45b51a8ef8607323ab1a8a50ba2179e`

```dockerfile
```

-	Layers:
	-	`sha256:2492592d3f3955b8b2a86d7a2eacb008b253416f6040eca1129524a8beb5c8f3`  
		Last Modified: Tue, 27 Jan 2026 21:40:02 GMT  
		Size: 670.8 KB (670837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:787b208942af7cd2046ead99bea372c47e200c2823014f8f5de4452db006cb30`  
		Last Modified: Tue, 27 Jan 2026 21:40:02 GMT  
		Size: 3.2 MB (3180710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15da7fff3ab6ff0b2054eeb76ace9d255e2662a1eca7f45dc706574db897afe4`  
		Last Modified: Tue, 27 Jan 2026 21:40:02 GMT  
		Size: 3.0 MB (3025810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde7599c517f433b1cb3689881604d423fcdd7138b554a10d518c59423bb016d`  
		Last Modified: Tue, 27 Jan 2026 21:40:02 GMT  
		Size: 60.4 KB (60370 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:119ea0d7149fe8c19f586a3baf891ce889a8aa698e2c86f772b17969e35a81e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78694306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd151401663158e3c2e531bbe44c0b2ec71f2925bc265e310c09e1ca2f52adf4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Tue, 27 Jan 2026 23:47:38 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 27 Jan 2026 23:47:38 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 27 Jan 2026 23:47:38 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 27 Jan 2026 23:47:39 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 27 Jan 2026 23:47:39 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 23:47:39 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 27 Jan 2026 23:47:51 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 27 Jan 2026 23:47:51 GMT
ENV RABBITMQ_VERSION=4.2.3
# Tue, 27 Jan 2026 23:47:51 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 27 Jan 2026 23:47:51 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 27 Jan 2026 23:47:51 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 23:48:30 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 27 Jan 2026 23:48:39 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 27 Jan 2026 23:48:39 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 27 Jan 2026 23:48:39 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 27 Jan 2026 23:48:39 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 27 Jan 2026 23:48:39 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 27 Jan 2026 23:48:39 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 27 Jan 2026 23:48:39 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 27 Jan 2026 23:48:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Jan 2026 23:48:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Jan 2026 23:48:39 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 27 Jan 2026 23:48:39 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b3cd4e86f865afe2d26dc136ea90a2e2babb45b5dd5fb2a043fcef8f61e5e3`  
		Last Modified: Tue, 27 Jan 2026 23:54:22 GMT  
		Size: 37.5 MB (37499736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c4144ce3a6795fd95f878d4964694f4898cc3545b8d86cd559234a9181ea25`  
		Last Modified: Tue, 27 Jan 2026 23:54:16 GMT  
		Size: 10.8 MB (10780478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0979c6b88c3276af8028f0f1ee98f591b12f56156a169ffa481b8059e7f74e`  
		Last Modified: Tue, 27 Jan 2026 23:54:12 GMT  
		Size: 1.4 MB (1449951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c6eafd569c4342cb7a009c92dab788baf4375c63db1c97df04f76e1f7719ca`  
		Last Modified: Tue, 27 Jan 2026 23:54:21 GMT  
		Size: 25.4 MB (25378445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4928d9dd96630654c516017f7743828c7692ba245932f4f5db781ae09870393`  
		Last Modified: Tue, 27 Jan 2026 23:54:15 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56fb8563b23644560df03c995df0c1d5397b7b21e2909801b05d9c3cbaf114a`  
		Last Modified: Tue, 27 Jan 2026 23:54:17 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8db543c623f15fa4ab29f3be88e94d17eefec41d014cc9fbc1a21b6698ec146`  
		Last Modified: Tue, 27 Jan 2026 23:54:18 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d104d206bd8a552a97916338c5466a11ab3bee9d71d9325e513fefd7297e2962`  
		Last Modified: Tue, 27 Jan 2026 23:54:19 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ef126ccdcc0d37d2cf7e1680e6bae57bfe073789c6e01076efbe62027b1c3bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7016945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8005462bfe4f54a3110dc39f902b0b82baa7aeafbebe787e459b57c290ff93e2`

```dockerfile
```

-	Layers:
	-	`sha256:02c47b6cc35f36a1b100ab6e3abac62bde2c7846e3c7bb0fd7649ab53ac1227d`  
		Last Modified: Tue, 27 Jan 2026 23:54:11 GMT  
		Size: 673.8 KB (673806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a9786c9a8d436a434b55f05e0e2bea670486f9cc6bd61c9c5da2dd49f7dbeee`  
		Last Modified: Tue, 27 Jan 2026 23:54:12 GMT  
		Size: 3.2 MB (3218825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca48a8f379c4a91fb33897e8a4552370f0296bf2f532308c499896fee041c87a`  
		Last Modified: Tue, 27 Jan 2026 23:54:12 GMT  
		Size: 3.1 MB (3063937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31053c98ecc24deb2fc9f8d48ee635d6aa319d12c4afb127df28d187f164c962`  
		Last Modified: Tue, 27 Jan 2026 23:54:11 GMT  
		Size: 60.4 KB (60377 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:3eed660ae49cc856e97948afa5997c9a679318b3fbfc01f834e33bf75c79adde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72879627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d81f114839b84d807d8db886c5a45d57053202c8efd4b6e73df0a2d603afe7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Tue, 27 Jan 2026 21:28:42 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 27 Jan 2026 21:28:42 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 27 Jan 2026 21:28:42 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 27 Jan 2026 21:28:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 27 Jan 2026 21:28:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 21:28:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 27 Jan 2026 21:28:45 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 27 Jan 2026 21:28:45 GMT
ENV RABBITMQ_VERSION=4.2.3
# Tue, 27 Jan 2026 21:28:45 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 27 Jan 2026 21:28:45 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 27 Jan 2026 21:28:45 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 21:28:52 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 27 Jan 2026 21:28:52 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 27 Jan 2026 21:28:52 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 27 Jan 2026 21:28:52 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 27 Jan 2026 21:28:52 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 27 Jan 2026 21:28:52 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 27 Jan 2026 21:28:52 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 27 Jan 2026 21:28:53 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 27 Jan 2026 21:28:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Jan 2026 21:28:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Jan 2026 21:28:53 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 27 Jan 2026 21:28:53 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:04 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f679dccc6361b2ca293ee675fe33ec30ecc14358cfae0a9ec3e4deb0806e005e`  
		Last Modified: Tue, 27 Jan 2026 21:29:15 GMT  
		Size: 33.9 MB (33919379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3502e259e1342eb4bccbb97016d80ff1621eb7d80bd513b46ae32099aed9f2d3`  
		Last Modified: Tue, 27 Jan 2026 21:29:15 GMT  
		Size: 8.3 MB (8339871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a44960ca728397e086e92c8fbad242b1d1d8460edffb20f9a5ad79a79b8c96`  
		Last Modified: Tue, 27 Jan 2026 21:29:14 GMT  
		Size: 1.5 MB (1515887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541c411db02aad9e0ba804ddea44a846e69d33ebe63b3ab4d2c7b6e7bbf025b8`  
		Last Modified: Tue, 27 Jan 2026 21:29:15 GMT  
		Size: 25.4 MB (25378430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c564fe75ee1f85f26992b086f003e4652f77579d47cb67c059059652cc02f9`  
		Last Modified: Tue, 27 Jan 2026 21:29:15 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9196c683bc2e97b3b64974e71cb4de5ff69663ec7c13eea40bb52343b92e131`  
		Last Modified: Tue, 27 Jan 2026 21:29:16 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaf389dbac363abb8c43414d235729012c397a6699401fd739669b0557a6b5c`  
		Last Modified: Tue, 27 Jan 2026 21:29:16 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b03ac672032f6acd1a086211ad740159984c28f4cb8f4dd5e9798f1efa78d9`  
		Last Modified: Tue, 27 Jan 2026 21:29:16 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:45f333a19439d5c746371f55b843cfeb108a779f0aea6ca3a85145d59e310c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6714109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7879e6449064c7b3b0d5d3c644a3fbc7bd0c8a23b0042e86186b6e4ebd04e9`

```dockerfile
```

-	Layers:
	-	`sha256:a421048dcb02385d42217f20f523e1f7f4fa849f35c633707a7369f1127de2bf`  
		Last Modified: Tue, 27 Jan 2026 21:29:14 GMT  
		Size: 670.8 KB (670803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc0327890ebe86a9ce3090be37b5c7111c281020c9d62b2b2f31409926b1284`  
		Last Modified: Tue, 27 Jan 2026 21:29:14 GMT  
		Size: 3.1 MB (3068934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0985709710222d7e5d844e12fdd707c5284a668b507b88039c16ccee7198d9d4`  
		Last Modified: Tue, 27 Jan 2026 21:29:14 GMT  
		Size: 2.9 MB (2914064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e846fcf34fb20fa68edd3977c4bcc2376e6497e469b5756bea35ccbceac26be1`  
		Last Modified: Tue, 27 Jan 2026 21:29:14 GMT  
		Size: 60.3 KB (60308 bytes)  
		MIME: application/vnd.in-toto+json
