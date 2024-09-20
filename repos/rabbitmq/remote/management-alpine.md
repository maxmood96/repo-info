## `rabbitmq:management-alpine`

```console
$ docker pull rabbitmq@sha256:6772b7aa22d524a270d14c10704738aee6d41fbb8391d3f5031fe363583999f3
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

### `rabbitmq:management-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:f67497d4fb795d25044348beecccf4b584923ed76d2b8525a6a0790b3a728b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87691291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1353c3accdc961304a28d0f809189eee3d3b070b9092ae52434390dd610652d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 18 Sep 2024 16:57:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_VERSION=4.0.1
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 18 Sep 2024 16:57:52 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 18 Sep 2024 16:57:52 GMT
CMD ["rabbitmq-server"]
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610ce35de3807073d33c0a3521d39f303f34daf24b0f7ec36fc527e995d3af1a`  
		Last Modified: Thu, 19 Sep 2024 19:04:30 GMT  
		Size: 41.6 MB (41571108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9d58859c15847beee196ae291cc000aed0733d6319f07ee383c2f22f0ca07c`  
		Last Modified: Thu, 19 Sep 2024 19:04:29 GMT  
		Size: 8.3 MB (8284904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8623a068de6c7e6485cdeb31df2daf17857fa32341e6d45cf7a10676c9528a54`  
		Last Modified: Thu, 19 Sep 2024 19:04:29 GMT  
		Size: 2.2 MB (2234364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6946145c533149e293c095c94c697c61348242029a4e76719e36f650c9015d3`  
		Last Modified: Thu, 19 Sep 2024 19:04:29 GMT  
		Size: 18.3 MB (18309238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a855b31dc781bb3df488c8462db83a19ca60924714aaff4c9c3bcd744a73b108`  
		Last Modified: Thu, 19 Sep 2024 19:04:30 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f852642ae79944ba1250e7f29b633281409a6976f59eb9a60e97680448c983c3`  
		Last Modified: Thu, 19 Sep 2024 19:04:30 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef5b6b7c400707ee109225ac84f66bdcb2f92c0eece974784391dd5304a299d`  
		Last Modified: Thu, 19 Sep 2024 19:04:30 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6089e3c528abf28f95d9a086bbede000c4735c314c43bf271e7918ce5ab87de7`  
		Last Modified: Thu, 19 Sep 2024 19:04:31 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb4c2dd262024db1934730351b45dc4a63ef451de3c318f28abb5aebd404351`  
		Last Modified: Thu, 19 Sep 2024 20:01:12 GMT  
		Size: 13.7 MB (13666123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d08f796f2bc3be819ab3e147734b8eef750381f7366d73e2a08161071b5e98d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 KB (13551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e26cded1332e68106aa91a3ad02f75af69776563294deea4cfd31df67d08225`

```dockerfile
```

-	Layers:
	-	`sha256:830c9078665786c352c2475c74916313b31821ec9e1570fcb0c0331f0b96c5d0`  
		Last Modified: Thu, 19 Sep 2024 20:01:12 GMT  
		Size: 2.4 KB (2363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c55db10e3f84f82ff6edfddbcdb0ddeff105ac85123fb28063e89f92a0c9da00`  
		Last Modified: Thu, 19 Sep 2024 20:01:12 GMT  
		Size: 11.2 KB (11188 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:db0d9b6f37147d68b811156ace801cff91407a370ba02214ccecdb45cb449e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77655453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f2391292d7f091e6255704d50120f7675ccf4d2e66b050938dfba54aa1760f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 18 Sep 2024 16:57:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_VERSION=4.0.1
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 18 Sep 2024 16:57:52 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 18 Sep 2024 16:57:52 GMT
CMD ["rabbitmq-server"]
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc86c03e9da6b54d1acf7c43dbee9686494771dbd572357ebf468acd00875d`  
		Last Modified: Sat, 07 Sep 2024 12:04:52 GMT  
		Size: 33.2 MB (33185875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd269fb16bdae3e476ff0d39c0432228b661eb9e4202284f15ed23681039615`  
		Last Modified: Sat, 07 Sep 2024 12:04:52 GMT  
		Size: 7.1 MB (7079945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbb0559a74c8d168c21891fc520f8c60ea643b12725bbbbe46ca4ca1c5d68d5`  
		Last Modified: Sat, 07 Sep 2024 12:04:51 GMT  
		Size: 1.2 MB (1230004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc9d9bb22d7394f43ff0795ccd8a1885c1b155912415efd5d7734fc1bf9528f`  
		Last Modified: Thu, 19 Sep 2024 19:02:40 GMT  
		Size: 18.3 MB (18309249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d1102e9898fcab4a2821fabc0cd5cd27278363446bff1874f4c9d0a4292118`  
		Last Modified: Thu, 19 Sep 2024 19:02:39 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e2522e0b4b9a2055b0a3d461f93a99bf3e81a62957b68a28148484e66a8d28`  
		Last Modified: Thu, 19 Sep 2024 19:02:39 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d76441da7757e61bdec0dbb86508ea6602b7dd5174917f0df874108dc0a1e76`  
		Last Modified: Thu, 19 Sep 2024 19:02:39 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1112448062581efcf157494c50bf0b209a94f9227931e3eaf519f38c49283b`  
		Last Modified: Thu, 19 Sep 2024 19:02:40 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d5e0aee256d96fb88d5cb8a8b4e9e91522c3405ced29f0559bd3cd90dc567f`  
		Last Modified: Thu, 19 Sep 2024 20:00:41 GMT  
		Size: 14.5 MB (14482129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:409efd12e97c793b520133eb4b4cd810bf3b536e5694083c23189fa415479fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 KB (11056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2773ad05a06e5360cd85a873dfb26134ab9b10941157fc388d68d8a9fb6e46a5`

```dockerfile
```

-	Layers:
	-	`sha256:f7cf45f6d5694b1a0c0d0a322ff1514af44c0c800217dcf7651e90c8e16bd671`  
		Last Modified: Thu, 19 Sep 2024 20:00:40 GMT  
		Size: 11.1 KB (11056 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:110cc9d5563b47123891a30dcdb0b416e255ff6d7d353cf08233d640cc9af6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76447553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c884e19cbc526889b3f4759f67ceefe723f7596fe651aafc1ca37ca732aed1c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 18 Sep 2024 16:57:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_VERSION=4.0.1
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 18 Sep 2024 16:57:52 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 18 Sep 2024 16:57:52 GMT
CMD ["rabbitmq-server"]
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd9d453be4c080b9b86f2acb6b9dbd0ec34c17a1163757b6966259831cce69f`  
		Last Modified: Sat, 07 Sep 2024 12:26:04 GMT  
		Size: 33.1 MB (33087585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd729021b6dae860ba7a13249de85f7343adb05da25af22277cea034f3d84ba`  
		Last Modified: Sat, 07 Sep 2024 12:26:01 GMT  
		Size: 6.7 MB (6716593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b4185c167bc7761ccec13a8003dedb2855a78327479ef4585745da32adee48`  
		Last Modified: Sat, 07 Sep 2024 12:26:01 GMT  
		Size: 1.1 MB (1132942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4643d353ef8e750688c72c540a74e02a56552c4d0a452ef79f5f7e6b52322297`  
		Last Modified: Thu, 19 Sep 2024 19:11:08 GMT  
		Size: 18.3 MB (18309100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e3b291a37e031484afe5bafaf1634f3a36e59183cad9ca89cdc19a10ecc311`  
		Last Modified: Thu, 19 Sep 2024 19:11:07 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bbb7e3db97233e874d6436a231108778cd1602e4870db3633c632fab978cd9`  
		Last Modified: Thu, 19 Sep 2024 19:11:07 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef4cb82fcf6025662837fc4f9ff6ea5e90380df7154acb6577a9309572e7cb6`  
		Last Modified: Thu, 19 Sep 2024 19:11:07 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a907c4f3d9309039cdbad7ea05f307915aaeb1b9f373f205525d5cb5719a2`  
		Last Modified: Thu, 19 Sep 2024 19:11:08 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f41e8d6d78d8903e97892422f4826d5aae7149e8aaacc94aab2dbaa8dd9f584`  
		Last Modified: Thu, 19 Sep 2024 20:01:19 GMT  
		Size: 14.1 MB (14104087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4772acb13ac5f37299871bc5207e24ee4844d8b79a5971849c5870cbe5956783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1630975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bd760d244e2b77a36c7d4156fbb8162c643d37959dbd59c1a3c9ff4526b10d`

```dockerfile
```

-	Layers:
	-	`sha256:575edd7c52977b6098563764c97e5872ea2f86917a48259041d8f947cff45638`  
		Last Modified: Thu, 19 Sep 2024 20:01:18 GMT  
		Size: 1.6 MB (1619699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c32742fb4da29f99212cda64a03c55459e95e3043e9644b16456017f82ba66f`  
		Last Modified: Thu, 19 Sep 2024 20:01:18 GMT  
		Size: 11.3 KB (11276 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:0e6c9f6c5a240be8951849b0010784792a2ff934ecc0bbbde3088d7d0d88f6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87414321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5e4041a62c30682e28815225ff0b8e92bbc096e7fc469008927f31dccb3527`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 18 Sep 2024 16:57:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_VERSION=4.0.1
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 18 Sep 2024 16:57:52 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 18 Sep 2024 16:57:52 GMT
CMD ["rabbitmq-server"]
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3c99bf71fb3b6f073fc14ae9527292614744ea736f6351d9de7b1c6e787049`  
		Last Modified: Sat, 07 Sep 2024 11:21:55 GMT  
		Size: 39.7 MB (39690107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f601b017a968c1401d45c5107f6d079226f3a855bd3defe75fe86a114b6fc0`  
		Last Modified: Sat, 07 Sep 2024 11:21:54 GMT  
		Size: 9.0 MB (8995974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbba0bc4bfef30f4f115198675779fca456958eb4635fc517d242dc50ef70c3`  
		Last Modified: Sat, 07 Sep 2024 11:21:54 GMT  
		Size: 2.3 MB (2321274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce226389b8523b128f53a60df2bfeafa56e0aa83e9ca3c2f79f06927ca58da6c`  
		Last Modified: Thu, 19 Sep 2024 19:15:02 GMT  
		Size: 18.3 MB (18309265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c30e86659dae513f02e39448408ee0c8317106ab1dc72e5e1d1bfa748e7f9c`  
		Last Modified: Thu, 19 Sep 2024 19:15:01 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4832e0630cdd67860d1ca474afc576aa5ae40bf8ee549863f89d8571a374edab`  
		Last Modified: Thu, 19 Sep 2024 19:15:01 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75773fe26674026dbdac5b91daae3ce8e292ade10406541bffb5a3e894d5e2e`  
		Last Modified: Thu, 19 Sep 2024 19:15:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e9da285975a312b0a3dbe28e607c81202ec9b23508f0e6368e0c5cd3923b10`  
		Last Modified: Thu, 19 Sep 2024 19:15:02 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8055c21501f9f37c3a850d63a0ca977ea6572c0d9336eaf17743c718e8858e`  
		Last Modified: Thu, 19 Sep 2024 20:25:43 GMT  
		Size: 14.0 MB (14008312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ce1378f3b6af9ba515a7eb16fb138d86c36af9cc9d775b29382c28f37d7183d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1631132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e039032e19c4b9d215d80f05a6415d3367ac6cdbbdc10846df41f618a3cfbf`

```dockerfile
```

-	Layers:
	-	`sha256:f960bf1411995f1522a714a2452fd74c0227209bf62981aac362eba8301f4ba2`  
		Last Modified: Thu, 19 Sep 2024 20:25:42 GMT  
		Size: 1.6 MB (1619547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da210b4746fee9c72d7c50cd92db34eaa7a07beca1e1c27663d96c49dd1425d2`  
		Last Modified: Thu, 19 Sep 2024 20:25:42 GMT  
		Size: 11.6 KB (11585 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:f97c31d030828854557f372881e4303a26d3e8cd594b5223ca6ec293a3f5735f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79818606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf6d7d74e2f16c7a00aca11b6dbc97ec192b0b027dcf2c5f9cf93c84440b9b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 18 Sep 2024 16:57:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_VERSION=4.0.1
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 18 Sep 2024 16:57:52 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 18 Sep 2024 16:57:52 GMT
CMD ["rabbitmq-server"]
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75042aed74337952ec8c0bd888384b15c0850af4bedfaf467ee8c10d7d95202e`  
		Last Modified: Thu, 19 Sep 2024 19:04:20 GMT  
		Size: 33.4 MB (33357584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6487128c43e568484b25e44eab6d9cd1f1266d22ac7dcd27908ececd89a17ad6`  
		Last Modified: Thu, 19 Sep 2024 19:04:19 GMT  
		Size: 8.3 MB (8324914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bd9501b385fe0d8eb80c0b84f2443186ee083db2a1f9b4880a75478c7e6d4f`  
		Last Modified: Thu, 19 Sep 2024 19:04:19 GMT  
		Size: 1.2 MB (1231506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a13350580dbcd89a4675eea8a8b9263d2f2b57d5b9494fc0d148de93f87bd49`  
		Last Modified: Thu, 19 Sep 2024 19:04:20 GMT  
		Size: 18.3 MB (18309062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb38d82cb6de7287433ac691720a14d132f667f81526d08f529fe0b48954b32`  
		Last Modified: Thu, 19 Sep 2024 19:04:20 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e629851b1c6dcfdbbdd49a154b34e49d4bfbbaeb29feca4a1d10a662486081ec`  
		Last Modified: Thu, 19 Sep 2024 19:04:20 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670eac7f7538a923c2f81ce203767c2f49975a2c303ca96862d7e4f8b1b08abc`  
		Last Modified: Thu, 19 Sep 2024 19:04:21 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018c57577f7831a6d37fcf58be9d9693453fb90a317b9b7c1f01bf0062902ecc`  
		Last Modified: Thu, 19 Sep 2024 19:04:21 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7c3bf0d5b7776dbbbb0d2a2dee938fb8dcbe3826b3d297032839bc9a210332`  
		Last Modified: Thu, 19 Sep 2024 20:01:10 GMT  
		Size: 15.1 MB (15124629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:eda9c1fdce949066c06605315734a217e89734191bd2505e7e17d4fc295201b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf87021b5d0733c2c923656aecb6536fd1a2bc745ceb3d81e3d27e4e3f2b391`

```dockerfile
```

-	Layers:
	-	`sha256:93c84d20ff4bce61960ff53b901750262f12f22d9555bba073c4ae32466a6a29`  
		Last Modified: Thu, 19 Sep 2024 20:01:09 GMT  
		Size: 2.3 KB (2340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:079df8e010628642bae07f6474d6ba892434f0933926736112b1bed652532488`  
		Last Modified: Thu, 19 Sep 2024 20:01:09 GMT  
		Size: 11.2 KB (11155 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:7abf0c2528db56d5492667695162bcbcff5e54ef6a45a4b11d5935cbbfbfc5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81030451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45aa2900423e9dd7a32a96f7677bca93d03da191eefaec9533f5db7fd79758c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 18 Sep 2024 16:57:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_VERSION=4.0.1
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 18 Sep 2024 16:57:52 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 18 Sep 2024 16:57:52 GMT
CMD ["rabbitmq-server"]
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcb199bc4be6814c9d55db2fca0bb542fc5a767492af5adb4442ebffc5b31a9`  
		Last Modified: Sat, 07 Sep 2024 11:14:56 GMT  
		Size: 33.6 MB (33614675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cb8bdef0126f8e62c83419b737c1ee93fd719e3d6903e080179b8421f163fb`  
		Last Modified: Sat, 07 Sep 2024 11:14:55 GMT  
		Size: 8.8 MB (8834094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e71b4c9ed62eb3a7d96bff484d4203eae06a5c748a111ab80a1ffff3cd7d97`  
		Last Modified: Sat, 07 Sep 2024 11:14:55 GMT  
		Size: 1.3 MB (1346081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd1c9dbe958146c347a6e10dff5f229cf0ccdd0bfee8d28cd2f369741497fd8`  
		Last Modified: Thu, 19 Sep 2024 19:22:00 GMT  
		Size: 18.3 MB (18309011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b341bfdf8a5007351ed6c25ee6a4bd3a6e7c047c973d6f89e6f49d360f57c93c`  
		Last Modified: Thu, 19 Sep 2024 19:21:59 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f1c530664c6f0d49ee43509c0f42653ac5cd3c0f0caa4e52d4b18fe9ae64b7`  
		Last Modified: Thu, 19 Sep 2024 19:21:59 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3753abe20491e52b6c0a4a40817f2b7180d9c622f796f575e8578ebbc5bc7e`  
		Last Modified: Thu, 19 Sep 2024 19:21:59 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef7d3de8d6d7854ba2ece8f60e4bf4e1de4480c2022fe6e59cad369db3ac707`  
		Last Modified: Thu, 19 Sep 2024 19:22:00 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a2b85bf4254b6b36dedcd0ca5a1e42c45bcbf64dfd3a9da83ad45b1a5c6ab9`  
		Last Modified: Thu, 19 Sep 2024 20:33:09 GMT  
		Size: 15.4 MB (15352417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:35d6c45c87e2dd7d65f23890802c5bf1ac22e42e3b4d26894a207dfb6e0a4678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1629159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1012b1ac0504342e6ff022b4aeed908d66fe671e675a43ed1ae7154825cb55fe`

```dockerfile
```

-	Layers:
	-	`sha256:a2adb06b93730d36dd8045d61c62bc36777d968dc1d041ee0aeeafe6b084ae32`  
		Last Modified: Thu, 19 Sep 2024 20:33:08 GMT  
		Size: 1.6 MB (1617915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0106f961a52d2ffda76db77e3b11ea270c92a3b3e5354a0309ffa28866499381`  
		Last Modified: Thu, 19 Sep 2024 20:33:08 GMT  
		Size: 11.2 KB (11244 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:65a79b26f6d62e5c03a34bf615b0709356101453a8794ae9ca5bb1f879a159da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82289886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c46689a118d3d7b820b1c851e84cad449a7aee0ded9dac75f6a667383f3f2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 18 Sep 2024 16:57:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_VERSION=4.0.1
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 18 Sep 2024 16:57:52 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 18 Sep 2024 16:57:52 GMT
CMD ["rabbitmq-server"]
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d541526334938416ce86387328ea1389282f9c31e5f50b4a1f50b184b762df9c`  
		Last Modified: Sun, 08 Sep 2024 07:39:54 GMT  
		Size: 34.6 MB (34562240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f20314d91607af74d9b0bfea7a13585bccf5925d9297c73963560cee8f2c00`  
		Last Modified: Sun, 08 Sep 2024 07:39:51 GMT  
		Size: 9.9 MB (9866547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac183215d5cf0095068fdd0fedf851340a7c89f1a424b6a1c44cc48ba69fa61e`  
		Last Modified: Sun, 08 Sep 2024 07:39:49 GMT  
		Size: 1.3 MB (1270891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17deea9796fbc1fd7ec8ab951e253caf47058c4a4414e20fda56498ceeb0c4a7`  
		Last Modified: Thu, 19 Sep 2024 20:17:14 GMT  
		Size: 18.3 MB (18309238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef1bea08060e530ec12906412294dfa2038f7eecce810be34fb404b379f59cd`  
		Last Modified: Thu, 19 Sep 2024 20:17:11 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4161066860d9dabae2780d10d79609c8fc56d701e76c2614babe9c70bb9e1aa`  
		Last Modified: Thu, 19 Sep 2024 20:17:11 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e5804e43ae396cf410c73c8f68885e159adba8a6ec7525eccd3ee146513472`  
		Last Modified: Thu, 19 Sep 2024 20:17:11 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c80d7e02753bbe064eaccc8061c5f15961f3ee6acc97e425bfd2b0176ff9764`  
		Last Modified: Thu, 19 Sep 2024 20:17:12 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e384f357313c03a61dfa9f6ce4ed5a19734b84e18909ce714c60e1736a52101`  
		Last Modified: Thu, 19 Sep 2024 23:18:45 GMT  
		Size: 14.9 MB (14907771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4cd0b67755864e1f048330100370c4b15e394f2d090e5c8884ddc31f3aa28715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1630617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05b978271844bccff48fadebbd04035e6fc54df352a1f58783da826a48b9ec6`

```dockerfile
```

-	Layers:
	-	`sha256:f5f87b60e6007222f051e3fcf2cca5d6bfc13bfc9b431085a21dec5c8fa016b6`  
		Last Modified: Thu, 19 Sep 2024 23:18:43 GMT  
		Size: 1.6 MB (1619373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba733b0b715c89c858af2230870d7689eb5034179bd412917a50de1da5e5c814`  
		Last Modified: Thu, 19 Sep 2024 23:18:43 GMT  
		Size: 11.2 KB (11244 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:8771bad6eb84d73a9ef72570cd77d410ac682f84ca616ab3d499ee368e649a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79612991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b48e547ec070c177d5a07769ea110bb317831e9c406d7da816bd913b456e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 18 Sep 2024 16:57:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_VERSION=4.0.1
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 18 Sep 2024 16:57:52 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 18 Sep 2024 16:57:52 GMT
CMD ["rabbitmq-server"]
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b817b10a0c9729e45812971a59a7c7610314759cf9920828f966b2ccdb6831`  
		Last Modified: Sat, 07 Sep 2024 10:17:23 GMT  
		Size: 33.7 MB (33689699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8569e07ef45dc8559fda5855d29b0a8e020c14ec39d9dbe44037f4f005302c`  
		Last Modified: Sat, 07 Sep 2024 10:17:22 GMT  
		Size: 7.5 MB (7481813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86fd01dd71699fad1a630d604ea6bb31cd3a64ac5c268ce8ef06697cc87473b`  
		Last Modified: Sat, 07 Sep 2024 10:17:22 GMT  
		Size: 1.3 MB (1325141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de707d14dc0e8b398482053d065d6aa969fc7fcedb274e429317f8d1972104b`  
		Last Modified: Thu, 19 Sep 2024 19:21:54 GMT  
		Size: 18.3 MB (18309146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be08ecb58aefa294971c4fda2d3b1154f7b839fc337d755f00f456791a539571`  
		Last Modified: Thu, 19 Sep 2024 19:21:53 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8c015c3366498a6769d4532e76f942b836267a81a5b5bb3fa199cad379c5ad`  
		Last Modified: Thu, 19 Sep 2024 19:21:53 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdd68c8eef402f91ad3b8dbac362fada8d65ba7e8fbf0164358ba6cdfd2bd64`  
		Last Modified: Thu, 19 Sep 2024 19:21:53 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0fe473f9027fb2baae9396b8b0128c8e70287bac2027284154b985014fc10a`  
		Last Modified: Thu, 19 Sep 2024 19:21:54 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5a8bc5b03bf334d62e573896d1b42c8ed8cb22b5780f599c2206b707cf7719`  
		Last Modified: Thu, 19 Sep 2024 20:38:01 GMT  
		Size: 15.3 MB (15343848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:cc528cc0b8174a62c7a4d9edcb3859452fc32b0f44d4f6a6f250c407a41e8903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1628565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d50f9739e5354ea983914b669b74ff40f74ac45a612f5a50365b96b7e424179`

```dockerfile
```

-	Layers:
	-	`sha256:304a74b9416834fcf8d42e92566e4a805ec2e9d96627ecb14b1b2ceadf994e60`  
		Last Modified: Thu, 19 Sep 2024 20:38:00 GMT  
		Size: 1.6 MB (1617365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:512eb986c54599f0c0313b26cedb7067415fa541b88001eb1d05d4d06d8f3779`  
		Last Modified: Thu, 19 Sep 2024 20:38:00 GMT  
		Size: 11.2 KB (11200 bytes)  
		MIME: application/vnd.in-toto+json
