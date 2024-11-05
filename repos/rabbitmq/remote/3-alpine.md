## `rabbitmq:3-alpine`

```console
$ docker pull rabbitmq@sha256:d56385c116be5abd85cc512d4f75748b35aa913c5e69be6a97d0c5f9cc31e301
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
$ docker pull rabbitmq@sha256:e479cb7caf0cd7d66bc2232235e409fdb8b4beb9d0edd9e3e734f4385748267d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73776016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b37c618d2e19c4a8ebccfc3dc7a5eaa620993c4936b4f3733949ddb135c1e80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 01 Nov 2024 11:05:12 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 01 Nov 2024 11:05:12 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 01 Nov 2024 11:05:12 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:05:12 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:05:12 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 01 Nov 2024 11:05:12 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 01 Nov 2024 11:05:12 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 01 Nov 2024 11:05:12 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:05:12 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:05:12 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 01 Nov 2024 11:05:12 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 Nov 2024 11:05:12 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2024 11:05:12 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 01 Nov 2024 11:05:12 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abcfbb81743e72051c8d3e441c9009d639b602efe9ae22f7de0e49463f8fe47`  
		Last Modified: Mon, 04 Nov 2024 23:13:53 GMT  
		Size: 41.6 MB (41580237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966e49ee6928ce770d00684a0901b22b1aaf3bef6bb465db6c14cfe0e0ca7138`  
		Last Modified: Mon, 04 Nov 2024 23:13:52 GMT  
		Size: 7.6 MB (7579798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2ec197aeab1eaeece060209bf9770186c523d4a216c0290ca90263ff6562c4`  
		Last Modified: Mon, 04 Nov 2024 23:13:52 GMT  
		Size: 2.2 MB (2234383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3ff1bf4674808ee53a55a29144ac65947b65da98f78c474f45aeab0a99aef5`  
		Last Modified: Mon, 04 Nov 2024 23:13:53 GMT  
		Size: 18.8 MB (18756044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384511b937364282e10316a61f8c444c3bfb542ad2628b587a74ffc9c08e35db`  
		Last Modified: Mon, 04 Nov 2024 23:13:53 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae34883adb1ec3d3d429c9c984652e4e9c3738734aafe3f3d1e058cea1834ad1`  
		Last Modified: Mon, 04 Nov 2024 23:13:53 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0b4c685aaeef1bb69a5c770fe72e4fa835a2780df53247202ff6ba5075e251`  
		Last Modified: Mon, 04 Nov 2024 23:13:54 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd0a709cfdd0616a2e629ab49533d67b013918e1941e8985611e249f8f60f4f`  
		Last Modified: Mon, 04 Nov 2024 23:13:54 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:dbcc4b32f1d8d5c01a817a9f0fedecb84f0ab926a4e196cd52b84988b9982bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6452262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a438d3e8697878113946ac0d5ec61eef1a900010d09801413e4d2dceb05d048`

```dockerfile
```

-	Layers:
	-	`sha256:a38c37c2d7405e12c81d84ff66a1b2faa5becf7cf12601bbc3df527bc9439309`  
		Last Modified: Mon, 04 Nov 2024 23:13:52 GMT  
		Size: 650.2 KB (650166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfcd0ed9d363759eaa5725be5a1c1156edb4c697fcf036aeda3079ce4d3bf9d6`  
		Last Modified: Mon, 04 Nov 2024 23:13:52 GMT  
		Size: 2.9 MB (2948577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0509d4f68fa7844cb2dcb99d3b92c6b8a3f65dda4fcd79a7798bbb7059a3017`  
		Last Modified: Mon, 04 Nov 2024 23:13:52 GMT  
		Size: 2.8 MB (2794108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10612a2fac57762d27cddb5116fa5d3edcd78d1bbc1ccf7c5c0897f56aef9bf3`  
		Last Modified: Mon, 04 Nov 2024 23:13:52 GMT  
		Size: 59.4 KB (59411 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:39136d626ed054ed5c7d6940cef0614926d03cbef5ac8d18333ba54f38256bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62958210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad0c04e70ecb093e2a3048da7e0b02ed9f2e203a0c7b5818cab0e3187d610a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 01 Nov 2024 11:05:12 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 01 Nov 2024 11:05:12 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 01 Nov 2024 11:05:12 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:05:12 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:05:12 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 01 Nov 2024 11:05:12 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 01 Nov 2024 11:05:12 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 01 Nov 2024 11:05:12 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:05:12 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:05:12 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 01 Nov 2024 11:05:12 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 Nov 2024 11:05:12 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2024 11:05:12 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 01 Nov 2024 11:05:12 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf81b9554d9c318fd3038474b2153176094646fb95097fc997bd094454a84a7f`  
		Last Modified: Mon, 04 Nov 2024 23:16:38 GMT  
		Size: 33.2 MB (33197352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6684d497f8ad13af357673581ccdf55d860da51f085696ea3e77f202ddfe45`  
		Last Modified: Mon, 04 Nov 2024 23:16:37 GMT  
		Size: 6.4 MB (6406537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e77bc6fef51d1d0f419a9c502a7ee7362f6c5556d4f7e798a99a0783444aad`  
		Last Modified: Mon, 04 Nov 2024 23:16:37 GMT  
		Size: 1.2 MB (1230042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdccd43e630e29f004b46555d5ce9100f9cc10dad27d317a751f43d41a17f7bb`  
		Last Modified: Mon, 04 Nov 2024 23:16:38 GMT  
		Size: 18.8 MB (18756027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cebe72bf93eda21e8726bd55ec5f303ce55512109dea30031ba79facda856e`  
		Last Modified: Mon, 04 Nov 2024 23:16:38 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15508d38692f51fc750d6d661ee19b6c01a4eb67e96cb27af8d57689e32803d6`  
		Last Modified: Mon, 04 Nov 2024 23:16:38 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2037c3f07def77d24c816f68a153e03b5c3d1a6e084326bafdd745114b7ea776`  
		Last Modified: Mon, 04 Nov 2024 23:16:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7d63072da7086b807dff12cad2d4fa8dab03240a8af87a42eb67ec71020acc`  
		Last Modified: Mon, 04 Nov 2024 23:16:39 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a4139940227140dd7b27d4ec987c3a80452178ef501ec5feb391b1219a016f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 KB (59375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3927ed00790ac99876f1e37fffe6a7b9e84d8c44aa1754a3562a5393c511ed4`

```dockerfile
```

-	Layers:
	-	`sha256:6bde7207f777345787934ce3a2fb2b428fe8522208377af82bc97004b2e691ab`  
		Last Modified: Mon, 04 Nov 2024 23:16:37 GMT  
		Size: 59.4 KB (59375 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:f28928a9e96d3bcca63f2957e504e1d31ec173478813909a50efb85cbb8d2b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62186706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b3ce32c48bc5c3a38a8a4d6398541f96e25a53186b2094f667f0d51ea4c888`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 01 Nov 2024 11:05:12 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 01 Nov 2024 11:05:12 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 01 Nov 2024 11:05:12 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:05:12 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:05:12 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 01 Nov 2024 11:05:12 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 01 Nov 2024 11:05:12 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 01 Nov 2024 11:05:12 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:05:12 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:05:12 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 01 Nov 2024 11:05:12 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 Nov 2024 11:05:12 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2024 11:05:12 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 01 Nov 2024 11:05:12 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711c2a0f37f9986c8c6954c4ca09f3d32ae0abbc1c18ad00fa24e598f6cb9e99`  
		Last Modified: Mon, 04 Nov 2024 23:35:04 GMT  
		Size: 33.1 MB (33093093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0ad2e16b5dbd90cbd70f2746c2cdf9a3054d31bdf422944f9199eaf5145dfb`  
		Last Modified: Mon, 04 Nov 2024 23:35:03 GMT  
		Size: 6.1 MB (6107673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a97f217ce620a0afadeb223b8c77e6948d713b487fcec8bb8e5be5caf30146b`  
		Last Modified: Mon, 04 Nov 2024 23:35:03 GMT  
		Size: 1.1 MB (1132944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b835fbe1a3f38df2477fb9c73f29b5c408bdd34e864f6396957592d1267d9f3a`  
		Last Modified: Mon, 04 Nov 2024 23:35:04 GMT  
		Size: 18.8 MB (18755749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a1bf564ed54ca5a679a9e48217b65b7caffa8e3d9cb8bf58532c501c0b8255`  
		Last Modified: Mon, 04 Nov 2024 23:35:04 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97397043415eb0326daa65c25c8fe075260557f3083aca10adb7880fcb58d039`  
		Last Modified: Mon, 04 Nov 2024 23:35:04 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c31e2d8877ecf2c76a4d0893cbb1cf0f2e653e86c472720d548e25551f8fbe`  
		Last Modified: Mon, 04 Nov 2024 23:35:05 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c37e25b19156341ebba2ba2171ed8c6f0d55ef35da49fd624221878175e36`  
		Last Modified: Mon, 04 Nov 2024 23:35:05 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fc5813018af9201c5eea37c02c5be7f435313f3d751c746cc6ba87e6e4bf4f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6246237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b026f4a263c0de390f1efa48ce96e774637a108fd41dd8323a1dabf3a5438e3f`

```dockerfile
```

-	Layers:
	-	`sha256:279c65f50ec81212666881edd92c7ded7566231851c87cb98b624d265f02b9d9`  
		Last Modified: Mon, 04 Nov 2024 23:35:03 GMT  
		Size: 646.2 KB (646229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96f04483e0e3e302dbd7bdfc99efb7225e338f0de3928357264fc6f2b8cb2102`  
		Last Modified: Mon, 04 Nov 2024 23:35:03 GMT  
		Size: 2.8 MB (2848109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9f3327d4a7bab98421c2282ce8b00fdbde628d7d0b5e2b0a646062372a509cb`  
		Last Modified: Mon, 04 Nov 2024 23:35:03 GMT  
		Size: 2.7 MB (2692309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78cc2c17f981372abc5d1511f26ddb29ab1a9864453704b7cd3ddff30a51e398`  
		Last Modified: Mon, 04 Nov 2024 23:35:03 GMT  
		Size: 59.6 KB (59590 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:efeabe6cb525f77f3b63a57b40cefbb6a96eac273b85420689189b22e43db6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72062115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe5eeab959e0c255588ba6bbb0524cce4ea3c475b1bc51fe9a476908429136e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 09 Oct 2024 11:05:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 09 Oct 2024 11:05:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 09 Oct 2024 11:05:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:05:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:05:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 09 Oct 2024 11:05:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 09 Oct 2024 11:05:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 09 Oct 2024 11:05:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:05:20 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:05:20 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 09 Oct 2024 11:05:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 09 Oct 2024 11:05:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Oct 2024 11:05:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 09 Oct 2024 11:05:20 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3317d49661c32e47014b627d452dc2543f351f4c2f3d0d9a519b05452037e0`  
		Last Modified: Wed, 09 Oct 2024 23:22:41 GMT  
		Size: 39.7 MB (39693702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b857d778509b7634bb57ef97a843dd287a60b7e1423bd777f33c137bd7b53b13`  
		Last Modified: Wed, 09 Oct 2024 23:22:40 GMT  
		Size: 7.2 MB (7201635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be40d28e85d0eda9e6a9486d74369bd7afbd0cc68e7113ee66d06d4b66e99e5f`  
		Last Modified: Wed, 09 Oct 2024 23:22:40 GMT  
		Size: 2.3 MB (2321282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df1eb93bd114c7578955645d7c2a21900b86024bd044c36b485fc54bc8ef8bb`  
		Last Modified: Wed, 09 Oct 2024 23:22:41 GMT  
		Size: 18.8 MB (18756105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c3e9c4f56292c5928789e69f7eb3e9a29bea8b0973ce996d538a8282106463`  
		Last Modified: Wed, 09 Oct 2024 23:22:41 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc66f2963547fadf78703b371a0e6918cba0622ab6b19e7a20a1d7704319413`  
		Last Modified: Wed, 09 Oct 2024 23:22:41 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87422fef4b295b1fc89cc33984084908038bf9cd637876db3958be12faa8aedf`  
		Last Modified: Wed, 09 Oct 2024 23:22:42 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feed4c7773f09ea5e35f2b5935f5915e177e3ceb12f03a9706d7fa272affe98`  
		Last Modified: Wed, 09 Oct 2024 23:22:42 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0b8aef7749e3ae0a7fff8f48435d5455e9a54778a01327b667e9a51948140461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6458664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b440f8c77666890aa5798997a5cc4cfdfcba02ddc8942142739b6d0c3605c0`

```dockerfile
```

-	Layers:
	-	`sha256:3fad75a657e32c1d08825d4db4ffe461817bca417d1952a14d9291bda629b045`  
		Last Modified: Wed, 09 Oct 2024 23:22:40 GMT  
		Size: 640.6 KB (640573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e3c1f18eecb4b65f4f9e20b72d260bbd57f1a059781cce6b9076dee10dad250`  
		Last Modified: Wed, 09 Oct 2024 23:22:40 GMT  
		Size: 2.9 MB (2948555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:883c33b04ac10e3a7ee3baa94f76462ad08efb8488978a6613487ec74f575a31`  
		Last Modified: Wed, 09 Oct 2024 23:22:40 GMT  
		Size: 2.8 MB (2809933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:442e1510351661bdd327d056d707b79a25ea33553f78b1eb7e395b7ad3fb6c4c`  
		Last Modified: Wed, 09 Oct 2024 23:22:40 GMT  
		Size: 59.6 KB (59603 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:891946589bf6142be45cf9b5b5d16fda0e30c49bd49f5928359a8ef5890f366a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64325164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aacb7393fe8914bc02c59eabe833858d8a5f5c3e4ebb81ce954bdca96903b311`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Fri, 01 Nov 2024 11:05:12 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 01 Nov 2024 11:05:12 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 01 Nov 2024 11:05:12 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:05:12 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:05:12 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 01 Nov 2024 11:05:12 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 01 Nov 2024 11:05:12 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 01 Nov 2024 11:05:12 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:05:12 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:05:12 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 01 Nov 2024 11:05:12 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 Nov 2024 11:05:12 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2024 11:05:12 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 01 Nov 2024 11:05:12 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c47bfff96d11c7222fbc77b5850eb5b528089f184089a3738b1845f0cc6733b`  
		Last Modified: Mon, 04 Nov 2024 23:14:18 GMT  
		Size: 33.4 MB (33360688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae4d51b28966f94660964597b154bcb088cbcd22a87ffca32532211e5a8a9a7`  
		Last Modified: Mon, 04 Nov 2024 23:14:17 GMT  
		Size: 7.5 MB (7506287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dce9c1f58cf5a03fa264d9b2fbccae5095d5a6fb00f263912b854df7ff71e34`  
		Last Modified: Mon, 04 Nov 2024 23:14:17 GMT  
		Size: 1.2 MB (1231513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ca42e3265e9428cb7041e02e36b00b5c2e692076a6ce474292481dd3717970`  
		Last Modified: Mon, 04 Nov 2024 23:14:17 GMT  
		Size: 18.8 MB (18755759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e442faa7257c92a4af60617e1848ce46d61f340acaf489ecb581b995f88da414`  
		Last Modified: Mon, 04 Nov 2024 23:14:17 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6d19cb7b0bd89ddbb1ffa0d8511e0e4cf3ea061f6e2aacf2fbed6776348621`  
		Last Modified: Mon, 04 Nov 2024 23:14:18 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21854b92bf43b25d34683893b48f1704c75bd325a4e8cbf421defc22a9ddacbb`  
		Last Modified: Mon, 04 Nov 2024 23:14:18 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696cd4e304ac9dab7ca97097e7003cedff266867f69b30dc8c708680d97eede2`  
		Last Modified: Mon, 04 Nov 2024 23:14:18 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:45e2045aa943463cfe8ec1d51fd8ac5016be299d086d58ce761f1bf6cb9d9bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6427947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a89335a00ea6c86107b846ec3724a51eace2d678f238736a991d8278a27d16`

```dockerfile
```

-	Layers:
	-	`sha256:7b4c8147833550e1a413d187bc164f38cf0be06852992911aed61f904e40aa97`  
		Last Modified: Mon, 04 Nov 2024 23:14:17 GMT  
		Size: 645.4 KB (645443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8dd61a53c8f34e795cfa34337e28768e57e4a9416f7f77b4623b086cf4c5e4b`  
		Last Modified: Mon, 04 Nov 2024 23:14:17 GMT  
		Size: 2.9 MB (2938800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f38e4d2d3743421f8609d9a059f0d71e21e42dd34add209a394e11c6be8ac467`  
		Last Modified: Mon, 04 Nov 2024 23:14:17 GMT  
		Size: 2.8 MB (2784335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24837c4fec3fbc19bee76ce7f94341bda302a98179c6cb26781e08304b1abbf5`  
		Last Modified: Mon, 04 Nov 2024 23:14:17 GMT  
		Size: 59.4 KB (59369 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:b85b2e9eafa2a00d9dcb3c0d95af3d9d27391a9f720692d665473fbd858068ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65291166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bac44197df4ec70a84b052c9246db4a4f2cd0d3e0d284cc23efac9e4b07daee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Wed, 09 Oct 2024 11:05:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 09 Oct 2024 11:05:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 09 Oct 2024 11:05:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:05:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:05:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 09 Oct 2024 11:05:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 09 Oct 2024 11:05:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 09 Oct 2024 11:05:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:05:20 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:05:20 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 09 Oct 2024 11:05:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 09 Oct 2024 11:05:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Oct 2024 11:05:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 09 Oct 2024 11:05:20 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981c4efbfb12480ce0b022a175058e236ae4eef836926592bc0c3548dac1651c`  
		Last Modified: Wed, 09 Oct 2024 23:18:43 GMT  
		Size: 33.6 MB (33619172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cf199e90ad21e72aa0d38599b7be2ca482d2ac9df37e213a01367db0832891`  
		Last Modified: Wed, 09 Oct 2024 23:18:41 GMT  
		Size: 8.0 MB (7996031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a48c3c35006df55540796badb7c3db8622181b5c27bf86ae3ab2d4f626391ab`  
		Last Modified: Wed, 09 Oct 2024 23:18:39 GMT  
		Size: 1.3 MB (1346105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83097a1dd714af2563541df1afb12b0429d89b2d0fb2038057d00bff2cef210`  
		Last Modified: Wed, 09 Oct 2024 23:18:40 GMT  
		Size: 18.8 MB (18755687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4799191ed3a43c2d64faf02aaf51caabda790dd9f87768469c2feac6f9a0c0a2`  
		Last Modified: Wed, 09 Oct 2024 23:18:40 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c96aed7d122080cc62bbeb78b7eedac9f6fe1f662e792b10087667220ca8e0b`  
		Last Modified: Wed, 09 Oct 2024 23:18:41 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f627a8dbb711b5ed919c437efe99ae77e471b85068dbe602a8c5ab0f6e046ed`  
		Last Modified: Wed, 09 Oct 2024 23:18:41 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fdbe872b727acb77c255696ebb1348ece74d5113fe2a7e3d65fd328b9552b2`  
		Last Modified: Wed, 09 Oct 2024 23:18:42 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a87a853c79cd01cbc6209713dbed8d9c80b7c8bf186ca8a2121726250b408643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6396774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cb7d89d44c992bb747b2366546464f69ef5669d244a85a8ce11697ca43dd29`

```dockerfile
```

-	Layers:
	-	`sha256:770cbd02c6e90022dbf1b637ac4b438f3f2a2918d09764249a0885655ca240d0`  
		Last Modified: Wed, 09 Oct 2024 23:18:39 GMT  
		Size: 633.9 KB (633900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:690e0d30585f0e6cb106962b616387a00fee2a1a20dfd8095a092cc288024844`  
		Last Modified: Wed, 09 Oct 2024 23:18:40 GMT  
		Size: 2.9 MB (2921039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3868e623f94cf86e78126bdc5ddaba8e5b6b9b5e216c917ce46954d966902354`  
		Last Modified: Wed, 09 Oct 2024 23:18:40 GMT  
		Size: 2.8 MB (2782405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0585d91102197e2ffbd452a88785cfb9533a8a667813f6be240f0620375a402`  
		Last Modified: Wed, 09 Oct 2024 23:18:39 GMT  
		Size: 59.4 KB (59430 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:1106f67c8418356bb787d0d62dd973758c73f662ee99163a020f8e4a828cd70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66746133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5601cac263ca19840cb0e4c7373067d895d97d114bf3dd8b947b33feeb47011a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Wed, 09 Oct 2024 11:05:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 09 Oct 2024 11:05:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 09 Oct 2024 11:05:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:05:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:05:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 09 Oct 2024 11:05:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 09 Oct 2024 11:05:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 09 Oct 2024 11:05:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:05:20 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:05:20 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 09 Oct 2024 11:05:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 09 Oct 2024 11:05:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Oct 2024 11:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Oct 2024 11:05:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 09 Oct 2024 11:05:20 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b8bda8191e14fef9256075f26695319aeb41b34e0921092084b004d93eb3c4`  
		Last Modified: Thu, 10 Oct 2024 07:44:06 GMT  
		Size: 34.6 MB (34576233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22d64f119656689a60bf3f8381c688740b52a9c13105a845ffbf990f320d3d0`  
		Last Modified: Thu, 10 Oct 2024 07:44:02 GMT  
		Size: 8.8 MB (8769753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfcbdf604d1022c06db689284f96fe467d7c1f97e038932516016f9356c539f8`  
		Last Modified: Thu, 10 Oct 2024 07:44:00 GMT  
		Size: 1.3 MB (1270900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d82f37030b966ac697563208ff020bd4378876eee381caaf9e06f66b56aaf5`  
		Last Modified: Thu, 10 Oct 2024 07:44:04 GMT  
		Size: 18.8 MB (18756041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9c299574b2da7272708c157be2dcfb825f171cb1bb574bc55692317d7ce91c`  
		Last Modified: Thu, 10 Oct 2024 07:44:02 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bccbf1c6e84a8a1ab68fb69dcbc8308c344104796f366a5c3bcb668b173b70cd`  
		Last Modified: Thu, 10 Oct 2024 07:44:03 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25724013322c0377a20ee230115caef8121c2e3386eb59ac238c8f748f23ffa0`  
		Last Modified: Thu, 10 Oct 2024 07:44:03 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31235c94876b0b16701d3b7fc6078b49465e288860563c9341fd6ce4ccb516f2`  
		Last Modified: Thu, 10 Oct 2024 07:44:04 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2a9ec57ccdd05b8eb99cbc7170665cd2fd73d2fb63bcbc23732c53fcd3fb1bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6431877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54dc339d4430f0263d6a5f946dd66d85d2c76f16fb584597746a9871a83a01da`

```dockerfile
```

-	Layers:
	-	`sha256:05149fc9a22181c73cef21e4d999bf59c912df29fa978afc666e9b39da7f6add`  
		Last Modified: Thu, 10 Oct 2024 07:44:00 GMT  
		Size: 636.7 KB (636743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3acbd41ae5a4fd35f3aedc9acce1a9972719775afdcc0cbafad86027d3b01b97`  
		Last Modified: Thu, 10 Oct 2024 07:44:01 GMT  
		Size: 2.9 MB (2937162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f46d36cbb32e5ad86044f7d91f64b77b8385de0a400e864c49b7a926e320986`  
		Last Modified: Thu, 10 Oct 2024 07:44:01 GMT  
		Size: 2.8 MB (2798540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d42691467a0af5933f6070b4bedf91ab724a6fb23f7ae060dc089d298a8c4289`  
		Last Modified: Thu, 10 Oct 2024 07:44:00 GMT  
		Size: 59.4 KB (59432 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:dae770615ed86ebf410cb440421a446adbd8848cc9966fac1326e90bf950114a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63958379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a9391026f301b0ca64b6c49948e4b9c8b97111ca5c2b98247b461e4ace752f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 01 Nov 2024 11:05:12 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 01 Nov 2024 11:05:12 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 01 Nov 2024 11:05:12 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:05:12 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:05:12 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 01 Nov 2024 11:05:12 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 01 Nov 2024 11:05:12 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 01 Nov 2024 11:05:12 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 11:05:12 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 01 Nov 2024 11:05:12 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 01 Nov 2024 11:05:12 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 Nov 2024 11:05:12 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Nov 2024 11:05:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2024 11:05:12 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 01 Nov 2024 11:05:12 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df02e2c704fcafbfb4fc6c4aa688d7e909359c19fc1f4e820fb56412abba550b`  
		Last Modified: Tue, 05 Nov 2024 00:15:50 GMT  
		Size: 33.7 MB (33691057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa6525bc8c7dc287ff74c4b10ca6bf1d1b2e6c195e422c25280d6c35c38eaa1`  
		Last Modified: Tue, 05 Nov 2024 00:15:49 GMT  
		Size: 6.7 MB (6723047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d19f5a0e4d01c8d780ed54e5f6fa804f08a0c0eaf0eb4634b14d9517c5d2960`  
		Last Modified: Tue, 05 Nov 2024 00:15:49 GMT  
		Size: 1.3 MB (1325194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3568663b14531d26d504761dc4ae5bfd1c0e8eb4eba4c9dfbc7a8f48d46f938`  
		Last Modified: Tue, 05 Nov 2024 00:15:50 GMT  
		Size: 18.8 MB (18755740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7412351c79c46b137cbebcd440f7c3e34aff328caebd4e5c8324a5223502d2`  
		Last Modified: Tue, 05 Nov 2024 00:15:50 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daece774d9ddd5807648d49c351b7f44821f35942f6301972b88ebfdcd7cefe`  
		Last Modified: Tue, 05 Nov 2024 00:15:50 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563049f67a05c94f4105f66d1f88a760ac511032a5a03bc1c43f535fec1aa91d`  
		Last Modified: Tue, 05 Nov 2024 00:15:51 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548ae81021855b951921da7abc413d25ddd1480e0e7c6ec05e2a82eaa4927343`  
		Last Modified: Tue, 05 Nov 2024 00:15:51 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9d688f71d4dd64498035c831bea96455777d880a1736b82acf8e2dbfa8f84b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6259032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5410912ae0a6bcc03a66c07b6e2011abfdea6c3c8ef24dcb3c9e4cf73164b1c2`

```dockerfile
```

-	Layers:
	-	`sha256:48487ebfcc7422cfd3008a1720fb7e357cedef59fe7f482c26a9f23a34d11a7e`  
		Last Modified: Tue, 05 Nov 2024 00:15:49 GMT  
		Size: 644.2 KB (644247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:622404825b5bbb077745fa7b8d40539af4b318448970944fffb91b88962cf3f7`  
		Last Modified: Tue, 05 Nov 2024 00:15:49 GMT  
		Size: 2.9 MB (2855575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:392614184c25bb14ba52098e266652b5ea5928264611cfd76fa9980cdf789e4c`  
		Last Modified: Tue, 05 Nov 2024 00:15:49 GMT  
		Size: 2.7 MB (2699799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b02cf810164b4e3ad66b7b39265361d5ec75d2b88b736f82169906bd4eeb5bf`  
		Last Modified: Tue, 05 Nov 2024 00:15:49 GMT  
		Size: 59.4 KB (59411 bytes)  
		MIME: application/vnd.in-toto+json
