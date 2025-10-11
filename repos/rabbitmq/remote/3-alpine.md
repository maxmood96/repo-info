## `rabbitmq:3-alpine`

```console
$ docker pull rabbitmq@sha256:0361eb9d64b9a416cdf86c585e1cf566819ea0e60cf5c6ce7e3b691aa997335e
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
$ docker pull rabbitmq@sha256:0d81dab17a8e7fb43955d3247ec52b7a82bdd3744aebf6aee91c06affca7590c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72273338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c83585eb6b67566b9ed5219433cc23e0be585bbd492d62cb70bb9b128ceecb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 10 Sep 2025 17:05:14 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["/bin/sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Sep 2025 17:05:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Sep 2025 17:05:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145a908b23a36b8f6479ba553b24b85c110f29a43948fa8dee7d661e6ed30535`  
		Last Modified: Wed, 08 Oct 2025 23:19:38 GMT  
		Size: 39.7 MB (39739203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2faa32a814a8946cba07df4099b75422abc5d1d53c4c21bb1527b44de8b2f9`  
		Last Modified: Wed, 08 Oct 2025 23:19:34 GMT  
		Size: 7.6 MB (7599164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99baa691242bdaea2ce867170b5eac9e16b16a3732ec38458dfa575559719b42`  
		Last Modified: Wed, 08 Oct 2025 23:19:33 GMT  
		Size: 2.4 MB (2374072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511a07cd0e3b36d27939beee46472abdbcee252f40e91b03c002247d2e618e23`  
		Last Modified: Wed, 08 Oct 2025 23:19:34 GMT  
		Size: 18.8 MB (18756706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e4457fe933e22851e4e92b80d12dea48c605c9b55512afb9a49e11b003bab0`  
		Last Modified: Wed, 08 Oct 2025 23:19:33 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164fc4fdd620ac82ea9a17d914c57d68fff604b3acd7e95fbedd04c9e943a336`  
		Last Modified: Wed, 08 Oct 2025 23:19:33 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a970c33d8f7fc682e223f695abc5f1e35e440833e35cebd946569f24cc6cda`  
		Last Modified: Wed, 08 Oct 2025 23:19:33 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17209073a16daa38306db51f949ce870ca5d5ceebf3a56d98915995fe6910df2`  
		Last Modified: Wed, 08 Oct 2025 23:19:33 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f7a0ec84dc7f31effce354ec5089b87bcbe58d44f708ddab29df377c9fa7b761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6776972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ec573597c011d26c6f83a5b44946de1395cb35d4def77321838089723c79b2`

```dockerfile
```

-	Layers:
	-	`sha256:17262e0a399e611e365a4a5901094bb5b3de030d74559dcd8b11bf2a5a9d5dde`  
		Last Modified: Thu, 09 Oct 2025 00:52:37 GMT  
		Size: 664.8 KB (664773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fba2918b0c7758def763f8da8ef997a80b3736abe1d138b41d7f23c5385676ef`  
		Last Modified: Thu, 09 Oct 2025 00:52:38 GMT  
		Size: 3.1 MB (3103686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6c87dee316ce7dcf7a8af0d49658ab5832cc4e1d32ee7f1c5c1fe48365c77a5`  
		Last Modified: Thu, 09 Oct 2025 00:52:39 GMT  
		Size: 2.9 MB (2948839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:904cd12dfa25931f4414c3fe784960ebab443ba04bfc0ee3f70e5bfac3ecc0e4`  
		Last Modified: Thu, 09 Oct 2025 00:52:40 GMT  
		Size: 59.7 KB (59674 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:4a0540ebb5a37fbd68d88da558525b800c0f09ff8eefeacdecc1bd0af1946c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61314629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f5056e332c873cd13828676cce542a912f6624d9fc76b41a94df0ae4003ebe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 10 Sep 2025 17:05:14 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["/bin/sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Sep 2025 17:05:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Sep 2025 17:05:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ff6b96b1fe3ea1b2b54f06f8d3f42ff087a832453605c0fcd57f7dcdb7db37`  
		Last Modified: Wed, 08 Oct 2025 22:22:29 GMT  
		Size: 31.3 MB (31297024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86dbe86d9866e89f76bda0855cf98e13dab156cbd61642919d3ca0e0eba95d5`  
		Last Modified: Wed, 08 Oct 2025 22:22:27 GMT  
		Size: 6.4 MB (6425284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1ea2a871d41ab3e415bb3086d31eb3e25af3a9cfcd7011f6be9f884a1b4e6b`  
		Last Modified: Wed, 08 Oct 2025 22:22:27 GMT  
		Size: 1.3 MB (1329794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b7ce6222976677378f301442a008e1bdca1ae32cb1d865845f8c19a0ac3ece`  
		Last Modified: Wed, 08 Oct 2025 22:22:28 GMT  
		Size: 18.8 MB (18756701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a6b7f40c42ed128767db046d833c54fd0571b63fc1c33ae9f1a7d6f730a907`  
		Last Modified: Wed, 08 Oct 2025 22:22:27 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c2290e0b94ec3363cf6589d37ac644c638abf0c89a4e0eab41092bc1814d73`  
		Last Modified: Wed, 08 Oct 2025 22:22:27 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7b44480c0e3dbfafef44f8e110c0f7585d96a915778711ce554f505d936860`  
		Last Modified: Wed, 08 Oct 2025 22:22:27 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac9e1269d06c7c92eb829b8db6833a9c777b8454d171d8a51e6bda25b0e719a`  
		Last Modified: Wed, 08 Oct 2025 22:22:27 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d893814cb77e2a1f5674007a4eef79e7ec2213f2e6652c95f6a9b6ccf14b5a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 KB (59648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607e50e79226325f048c60b0ae24c6ac8f693b8056603bf41e03b22954d67e9c`

```dockerfile
```

-	Layers:
	-	`sha256:d68b7fc96b67ab3e54c3ad1c7ae0386d8a28d7480e3600ce87538cf5501ff1da`  
		Last Modified: Thu, 09 Oct 2025 00:52:44 GMT  
		Size: 59.6 KB (59648 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:50fb0e8c55bfa38321c924380eb726ba607d44282c99df9887f5fa52bcd18302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60559919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87931e6a19363102a4748468e0ee7c6acc9f7a5accfe8b1d3d9894840548e59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 10 Sep 2025 17:05:14 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["/bin/sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Sep 2025 17:05:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Sep 2025 17:05:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d701d49f0bd9e38516bed86562d4f1305d4778104dc210d5322a0afa90debf4`  
		Last Modified: Wed, 08 Oct 2025 22:37:07 GMT  
		Size: 31.2 MB (31228161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9c0a289131fc57ee8dc9ef1ce06650e475f9cd1ff9d787a99f998612b59311`  
		Last Modified: Wed, 08 Oct 2025 22:37:06 GMT  
		Size: 6.1 MB (6125189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc85d4ec8bdf99375296a61468b05262f9711787e666ec032d5b4cb9ed9cd4f4`  
		Last Modified: Wed, 08 Oct 2025 22:37:06 GMT  
		Size: 1.2 MB (1226724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936099ea35106f8579353912386ca25b5d4c37e89244c374332eff968f3b8fe4`  
		Last Modified: Wed, 08 Oct 2025 22:37:07 GMT  
		Size: 18.8 MB (18756545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f4004e29ba20357ba7f17ef5ed83d584b39985d38a16a11f9f3581c3def319`  
		Last Modified: Wed, 08 Oct 2025 22:37:06 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21437382cc2f634a8e4156858fb65b2e668b02fa22441da4be65c98ce4c9e135`  
		Last Modified: Wed, 08 Oct 2025 22:37:06 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19f78d723ef80af852faf683b2e6187e6132de1b7519cb5d34de08cb925aeee`  
		Last Modified: Wed, 08 Oct 2025 22:37:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82454c3556ab04a6e30d860b89cc416b86f6bb00429b5357efa16f6bea430c1a`  
		Last Modified: Wed, 08 Oct 2025 22:37:06 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2a80962e8361e38981a0e7dc659eca2a98d60b97ef62fa7b155d0a941d7076bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6541250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7457e597a0636ac5b15660f56dc0a4e161097e12972b38feab8c3ef7746f712d`

```dockerfile
```

-	Layers:
	-	`sha256:931cf4a9c06ccc069782ecc8d2dd2189262353c52e74a687fbf14b9660e4afa0`  
		Last Modified: Thu, 09 Oct 2025 00:52:47 GMT  
		Size: 660.6 KB (660559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:052268f2ac325c9a7a8e32a7322ad168ec8d5b44efa96ab8770092a3909e946a`  
		Last Modified: Thu, 09 Oct 2025 00:52:48 GMT  
		Size: 3.0 MB (2988503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13b887dbadd6efc27f424c219b20d8032acee9c358bf3fc2e8b681b934e32247`  
		Last Modified: Thu, 09 Oct 2025 00:52:49 GMT  
		Size: 2.8 MB (2832325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dff992a156234aef26d0b8f663395c95f965063beed68c30fdded893fafaec9`  
		Last Modified: Thu, 09 Oct 2025 00:52:50 GMT  
		Size: 59.9 KB (59863 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:52156b4c38a534c8e5b7c5670ab920822a52c8ce309324240e4e70fa2e1e6659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70484405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23d07649b3d7ffb13d774a787d6980ea09e3379d3553edd0b9263cfda5a0e2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 10 Sep 2025 17:05:14 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["/bin/sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Sep 2025 17:05:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Sep 2025 17:05:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88075c6d0de9d97f1ec50f742c73d60b613711d084d46555c442e420cd95ee4`  
		Last Modified: Wed, 08 Oct 2025 22:02:17 GMT  
		Size: 37.9 MB (37922668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248e17d5a8c42cec73e6d204518c1954bebe9492b88ea1b9c00b60e596dab16c`  
		Last Modified: Wed, 08 Oct 2025 22:02:05 GMT  
		Size: 7.2 MB (7240453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c700f60ac800e64d3c15a0ef27f7575423eaf6e206d5e3bf98a65659dd49512`  
		Last Modified: Wed, 08 Oct 2025 22:02:05 GMT  
		Size: 2.4 MB (2424767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea393aa27df07c226d86193a63ee753b896831c8bad0f9686653ec95004be8a`  
		Last Modified: Wed, 08 Oct 2025 22:02:08 GMT  
		Size: 18.8 MB (18756708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de56ec04cb98008c26a3e4c7cf7e48aba456ff834b0bda5fa7929d80d35cc57`  
		Last Modified: Wed, 08 Oct 2025 22:02:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56966657e2387844972d3523f144812fbc74096b87ef5b75683998c90b3f6ac9`  
		Last Modified: Wed, 08 Oct 2025 22:02:04 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c05e7fae72ccc21d382fb6d9ea790c9fd61c599ca146e0f0b866ffb50306abb`  
		Last Modified: Wed, 08 Oct 2025 22:02:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f063d99b5c7927640db601217109604f530a9af2d629486f7cdc3fecf7cbb8b2`  
		Last Modified: Wed, 08 Oct 2025 22:02:04 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:517679b5c459a9ec38174c4590a65665bb991cd03f8c4b40a5e993af6178e6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6885232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a018c34636dcdd2523b780a6f338b814bd768cb9e6471ed357feb1980f0d23e7`

```dockerfile
```

-	Layers:
	-	`sha256:1697bdfd365ce4097e86cf15f7310870b2d783428a6fb1b55154a145d97a76a4`  
		Last Modified: Thu, 09 Oct 2025 00:52:54 GMT  
		Size: 665.6 KB (665555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0c7ae48b9a969053fd847a055a3e1604d4a4b419f1eb59ae6d183ac9fa9560e`  
		Last Modified: Thu, 09 Oct 2025 00:52:55 GMT  
		Size: 3.2 MB (3157974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd01b001e025b887230b763b99f0cc19ec3fbfb75a4782f3acaf8c008bd9b192`  
		Last Modified: Thu, 09 Oct 2025 00:52:56 GMT  
		Size: 3.0 MB (3001802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa07799183fe9848687063ce4cb923f3dadf6a443fe636d326074fc089a503d7`  
		Last Modified: Thu, 09 Oct 2025 00:52:57 GMT  
		Size: 59.9 KB (59901 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:dd8c6736643a3acdf54a155413da3bc00f3945d78946f7c520b5eb16db9da7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62597697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b117fddc6b6324242caf32d465c71d097b14c8e9bf1bd7a864eb54b46fe8d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 10 Sep 2025 17:05:14 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["/bin/sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Sep 2025 17:05:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Sep 2025 17:05:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01da0ce1f447f967674ad87fc0cc8d4a39b3bfcdeb22039126c4677b3e1ad9d8`  
		Last Modified: Wed, 08 Oct 2025 21:44:54 GMT  
		Size: 31.4 MB (31380961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1328578bec337f1e5077de25ca7a24504c46b7e0d538f998edd3aa824080fec`  
		Last Modified: Wed, 08 Oct 2025 21:44:34 GMT  
		Size: 7.5 MB (7507431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc17346a225af5103c320275e8baf3ac384acc404322f455a93f5f67bcd2b9c`  
		Last Modified: Wed, 08 Oct 2025 21:44:33 GMT  
		Size: 1.3 MB (1332247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cba29a0c2ce1fba305d0c7bd796ef4a5443f2f9adf8778144f4567cef5024b1`  
		Last Modified: Wed, 08 Oct 2025 21:44:35 GMT  
		Size: 18.8 MB (18756384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800c4578e46d83c1053c4de4df3dc3a35cff9b9a31323754aee2f33701705c14`  
		Last Modified: Wed, 08 Oct 2025 21:44:33 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483961ea1fe41d39a312ef29d79747e8bf8bb7b996b24d43189173dbe6f93487`  
		Last Modified: Wed, 08 Oct 2025 21:44:33 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155962081cb1dd9aabe45a5608029d605b0064ce5b334f3fc026bb88802d5c0c`  
		Last Modified: Wed, 08 Oct 2025 21:44:33 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e6ab41c49398b1159a66a67180400fc5969b3eef525a97b698c4e635c2c4c0`  
		Last Modified: Wed, 08 Oct 2025 21:44:33 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6807f18a2a313e751460991fbfcdfa898f1a02a2b621b2954614697e85619f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6749833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db17472745a3ade474c4e4c7b9b294374442c43f8e65d7a9387dae7a36e98ba9`

```dockerfile
```

-	Layers:
	-	`sha256:ac724b21075b0d8fbcc2a134a8d0d927cbba7080863129b16f88852e4b315d33`  
		Last Modified: Thu, 09 Oct 2025 00:53:02 GMT  
		Size: 659.8 KB (659773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c713c1319767a5d916d2494b2f6a2794d26c384e8d3ae095402ed1186ced712`  
		Last Modified: Thu, 09 Oct 2025 00:53:03 GMT  
		Size: 3.1 MB (3092637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42c7eaca9d6f24b35ba689491160210029797f3123f16c544a9bcfc5146e48a3`  
		Last Modified: Thu, 09 Oct 2025 00:53:04 GMT  
		Size: 2.9 MB (2937794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f0c97416fc2eef7b5a89ba8b3aa37ce269f0e71b329ca61c089b0fde5cddbe`  
		Last Modified: Thu, 09 Oct 2025 00:53:05 GMT  
		Size: 59.6 KB (59629 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:5c38fed1c33c97a1030877e290224468000a884087cef257e3393b4224d06d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63704389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f52d919939935caf90877375e75ea9e0e78d3ece5d04430bec781e11317bd90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 10 Sep 2025 17:05:14 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["/bin/sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Sep 2025 17:05:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Sep 2025 17:05:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fbe02f7142944c11945100c30256fa8eb07b848eae08686126d860bd034227`  
		Last Modified: Thu, 09 Oct 2025 04:44:07 GMT  
		Size: 31.8 MB (31757765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80da9339b403b650cf0a574f6a216c3252958a19a28eba23589992e6e1a6dcd`  
		Last Modified: Thu, 09 Oct 2025 04:44:05 GMT  
		Size: 8.0 MB (8003752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca40105941490833178b9bb90c3f6b15e502cd3d23e2c699d1a8723bf08474e`  
		Last Modified: Thu, 09 Oct 2025 04:44:07 GMT  
		Size: 1.5 MB (1452386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bac2e291d0ecc59ed306c822ece8a5b62c8d0ccdf9c80008529027258057d9`  
		Last Modified: Thu, 09 Oct 2025 04:44:07 GMT  
		Size: 18.8 MB (18756492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b015ffd1fd1fd265fa0b587f665e3b03e87a766003d6a25d0400c523fdfe74e2`  
		Last Modified: Thu, 09 Oct 2025 04:44:06 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069200d1c0941b72d573291c8c6e7f5c303ed507e05f6acb90b779821a4aa020`  
		Last Modified: Thu, 09 Oct 2025 04:44:06 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae2355c7c4af91956dcbcd8dde8379d95f0ea1bdb2b5ee687c09dd4ead6b2fe`  
		Last Modified: Thu, 09 Oct 2025 04:44:06 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f8959531cb2227e1681946fe42b5b24b5f493b3071dfef3d1bec7a0b9068bb`  
		Last Modified: Thu, 09 Oct 2025 04:44:06 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bc44d2ffa4724dd48205864e5dd95b7838497d5feeef25bb2be0be0549ae576b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6781621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7782061cefd505045da800b41fed35d3e9ec6f9c7f50ab0e8e1b45978e080112`

```dockerfile
```

-	Layers:
	-	`sha256:12314553a33b196aef11ee0133ceb1f56d5118276d876c65c1139a0617a134a7`  
		Last Modified: Thu, 09 Oct 2025 06:52:47 GMT  
		Size: 658.6 KB (658608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd3b7bca3e76b4161c37831d02deea573b4991c752a02d6e3bea0b4856f361c`  
		Last Modified: Thu, 09 Oct 2025 06:52:48 GMT  
		Size: 3.1 MB (3109734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6048fe421e5a2b3e06d66b58485201834f509f07c12f5d7f7d2fe1dcb87f642e`  
		Last Modified: Thu, 09 Oct 2025 06:52:49 GMT  
		Size: 3.0 MB (2953550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a68ae0c79d5f0ae2ea5a56c225a92c8edf220485d2e52fe1ee1c03c034a549af`  
		Last Modified: Thu, 09 Oct 2025 06:52:50 GMT  
		Size: 59.7 KB (59729 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:53ebc01b1c4e8faf2d9dc3a0377aa54e2e62c9a1f155795e172ede5658a43ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65119415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41be39cedb42b96a90fbd75e8ee877e11d2331c8453e66eb27faf31232d6a87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 10 Sep 2025 17:05:14 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["/bin/sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Sep 2025 17:05:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Sep 2025 17:05:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad0224f649315544d4e08e8189ded5db0f6bf43b74f59091e159061527f5e84`  
		Last Modified: Sat, 11 Oct 2025 06:00:09 GMT  
		Size: 32.7 MB (32720600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbdc314e901180c38c06a7e7a6cf0b9d243b28bb8480750ff33ebefe340a015`  
		Last Modified: Sat, 11 Oct 2025 06:00:05 GMT  
		Size: 8.8 MB (8758903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2244c383c290cf2e42fed7aa044d3f301855b042a93ce267fd0261b680a480ee`  
		Last Modified: Sat, 11 Oct 2025 06:00:06 GMT  
		Size: 1.4 MB (1366264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c507712bcb6cadbe613f9cb9616b2cbe47084276737bff124dadc927d703df0`  
		Last Modified: Sat, 11 Oct 2025 06:00:06 GMT  
		Size: 18.8 MB (18756656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bd4216f19dbe7db3fb3fa314f43d21e86381476040b67097051d9a7b1034f6`  
		Last Modified: Sat, 11 Oct 2025 06:00:05 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffe6540d56d1e420701d5be7a5c806d333d060ba06ae4b1fba88443572c143d`  
		Last Modified: Sat, 11 Oct 2025 06:00:06 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc7de05327349a90ff9c9e2c4c3bec4117324fd809eb4803939fd352faba681`  
		Last Modified: Sat, 11 Oct 2025 06:00:05 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8a578c4d59bcc0aae4a0d896ee7db1e285639c91139b7dbbe7b35f2f162c7a`  
		Last Modified: Sat, 11 Oct 2025 06:00:05 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:cb0c32b266773ec8f631f38acd96dc7252abdde9f9178312584f8556d2693b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6860949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41db90340fe7a652774bd595443c488fa05cf66bc88b3d2c9d2ae5a7e100252`

```dockerfile
```

-	Layers:
	-	`sha256:9c90a27ccd12605535d326cd446acb5b24ed78e561ebcadd37e26fe74dbac405`  
		Last Modified: Sat, 11 Oct 2025 06:52:44 GMT  
		Size: 661.6 KB (661577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:338367073330ec16ba41bb00b270312b6e9d9208cebc7e414dacd7290b1090d3`  
		Last Modified: Sat, 11 Oct 2025 06:52:45 GMT  
		Size: 3.1 MB (3147907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f122c1cbf2f88f786b6ad56ae258ab98e3e0dbd6cd217b6f920219e65acee16`  
		Last Modified: Sat, 11 Oct 2025 06:52:46 GMT  
		Size: 3.0 MB (2991735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20cfc401df6f253baa80f76ace2880e6357fddfc764657f116ba7c3105bb763`  
		Last Modified: Sat, 11 Oct 2025 06:52:46 GMT  
		Size: 59.7 KB (59730 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:78098f6cdf660b7dd0b3a32599f69724585b430972b5883ed51cddef95b5f026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62376713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9850706dfffb5d003c0bfb8bc88d72cd10216fd973f1f6c57d3acd575c8c3f82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 10 Sep 2025 17:05:14 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["/bin/sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Sep 2025 17:05:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Sep 2025 17:05:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926f89a58cae75a6beeed52cf7d40038b6c29de6e639330005db22da68e120ec`  
		Last Modified: Thu, 09 Oct 2025 06:04:26 GMT  
		Size: 31.8 MB (31793412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7910bbc6fe9517ee80da996d6d66228c441e675063d577c4508cc84baf11c4ef`  
		Last Modified: Thu, 09 Oct 2025 06:04:25 GMT  
		Size: 6.7 MB (6745368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ee2cc6651934c97cbfb4e5af6b4ee9ae257ede4a6ca44bce3bdb92b717af76`  
		Last Modified: Thu, 09 Oct 2025 06:04:25 GMT  
		Size: 1.4 MB (1430453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58515942d7c2f564a7b22499b2094c342f25585c665d400a86e03773142f0818`  
		Last Modified: Thu, 09 Oct 2025 06:04:26 GMT  
		Size: 18.8 MB (18756487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571a9304370ae366b5055100370e4f739f68cb75e07ecb38a3a884f2c407b02b`  
		Last Modified: Thu, 09 Oct 2025 06:04:24 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c4b50c7b670702d39df058d6adcbed0c18e3b93195684c298bba35fb1d210`  
		Last Modified: Thu, 09 Oct 2025 06:04:24 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d71903d1097b505b8c2915fcdeb18719af8616b378a7ff920f4d13b9f8c545`  
		Last Modified: Thu, 09 Oct 2025 06:04:24 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b922a2ef5025ed3cd9f56c34fb64b20396bd97277bf1afc1260c2031fe765f56`  
		Last Modified: Thu, 09 Oct 2025 06:04:24 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:63653e4b96328947a9e0d5c09767cc56eb43f48da9286bd23e89d542bbb97d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6560453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05f5a6aa3171d9cd9c04c3d86bddcc0da4e60d326b869c5e25c2f78bdff1105`

```dockerfile
```

-	Layers:
	-	`sha256:f4d43b5a17bae1a72db8f5d202232d353bc09f5f4afdbc80ebd6adc10b5f86a9`  
		Last Modified: Thu, 09 Oct 2025 06:52:59 GMT  
		Size: 658.6 KB (658580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e9842ad5932d8bb96a04d66735602ddf69f611888f0349d5e03fbb33af2a0a1`  
		Last Modified: Thu, 09 Oct 2025 06:53:00 GMT  
		Size: 3.0 MB (2999177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5496057f4d01ea912d104b46542c9d9e46e405fff0e04278d2435bdc19faa53`  
		Last Modified: Thu, 09 Oct 2025 06:53:01 GMT  
		Size: 2.8 MB (2843023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9676aa43534ea3ab511e206de667009f8480d45afbf29725b77786bc868c8bb`  
		Last Modified: Thu, 09 Oct 2025 06:53:02 GMT  
		Size: 59.7 KB (59673 bytes)  
		MIME: application/vnd.in-toto+json
