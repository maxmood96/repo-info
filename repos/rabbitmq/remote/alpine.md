## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:3f147ae36fdfc4eaf5c24ca64d6118adc4b4e0484ec7f830a5969f6d080f435c
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
$ docker pull rabbitmq@sha256:6c30406d68690072a3b5bdcf7e0fed84a77df7d342dbd05c9efd5a44bcf02041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73765115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2262fa9f479affb5ea6a0cde9bde7852b86ee0f6ca1d4e16cad010fbacd86d14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Mon, 26 Aug 2024 05:05:19 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 26 Aug 2024 05:05:19 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 26 Aug 2024 05:05:19 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_VERSION=3.13.7
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Aug 2024 05:05:19 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 26 Aug 2024 05:05:19 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 26 Aug 2024 05:05:19 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Aug 2024 05:05:19 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 26 Aug 2024 05:05:19 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6868476460225d403165667fd6adea3e37803782ffa1e987aa27f51a49aa54`  
		Last Modified: Mon, 26 Aug 2024 23:02:32 GMT  
		Size: 41.6 MB (41564948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209fb49f926feaf5b3b5dcbbbd9d0ce1bba0ecebbdf74c57673bc3f4f0aae794`  
		Last Modified: Mon, 26 Aug 2024 23:02:31 GMT  
		Size: 7.6 MB (7578135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d6d4f6377bf136f69f75ddc614534d9ba464a96875ebe7a1cfc194e79124df`  
		Last Modified: Mon, 26 Aug 2024 23:02:31 GMT  
		Size: 2.2 MB (2241461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c2c2dabc25657d283f3cbe2c9432c8a8407827a8d36a6465317d534ed4ae8b`  
		Last Modified: Mon, 26 Aug 2024 23:02:33 GMT  
		Size: 18.8 MB (18755930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fe2049c0a218b3d612a9ceff6b27f97aee36731f9b42081edc271489f84c26`  
		Last Modified: Mon, 26 Aug 2024 23:02:32 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ebf3a68a71a206ddfb733c78abe7ff09d51ba89221cf5b1ac66220c9ca1799`  
		Last Modified: Mon, 26 Aug 2024 23:02:32 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064efbfc920bc2d7c979829f865f4bf39badf291690f68b4039c157644814295`  
		Last Modified: Mon, 26 Aug 2024 23:02:33 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9b9c64065024995809bafe0aaa9b328821dccb4b2700d8e32c185a13d1cee9`  
		Last Modified: Mon, 26 Aug 2024 23:02:33 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:03885fa1547957d6c1597ab674fee592a090c8295cba831b86b9e5ea646e7ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6427468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ef43d51c90f87c3ddefe271415e15e33d4e5c153680b73912b5232129d1da6`

```dockerfile
```

-	Layers:
	-	`sha256:d4444d50f8f30dbec9d6ef8249e49323bf0f2652efed1846b4a7e2816c1b3dbf`  
		Last Modified: Mon, 26 Aug 2024 23:02:31 GMT  
		Size: 640.2 KB (640162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dcd5b802289d92612f076b17f8dd299089497279dd2aaec3b6c5d41166d8c76`  
		Last Modified: Mon, 26 Aug 2024 23:02:31 GMT  
		Size: 2.9 MB (2931565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bfd24a6ea802fdf8ab2d2faae1f9af0e1d77e1466d2bf53b4923ceb24f2eb12`  
		Last Modified: Mon, 26 Aug 2024 23:02:31 GMT  
		Size: 2.8 MB (2794092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3adb33f8c318d9866c9e50a99bde50c05fc87ca52b1b84d8f2471113414f3cc`  
		Last Modified: Mon, 26 Aug 2024 23:02:31 GMT  
		Size: 61.6 KB (61649 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:0f4b2f5557e5f6cca1c3de046081d139f24552f2f06f8ebc95926f2b044b1cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62945267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bab1e9ad1fa5982c4cd32bcf7fc8e52f667862c08e223761a55090dda0a8a6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 23:00:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 05 Sep 2024 23:00:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 05 Sep 2024 23:00:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_VERSION=3.13.7
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 23:00:29 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 05 Sep 2024 23:00:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Sep 2024 23:00:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 23:00:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 05 Sep 2024 23:00:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff4940fa77e3dacc1cb1a9bedc817566c6cffdfa38d0d48618c197e405f11f5`  
		Last Modified: Fri, 06 Sep 2024 22:08:34 GMT  
		Size: 33.2 MB (33185971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a92decc8227d07b7f95f206ddad41ad0edbf5d89d361de17e712edeb1bdefc`  
		Last Modified: Fri, 06 Sep 2024 22:08:33 GMT  
		Size: 6.4 MB (6406535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ff1db3cafe5cc67fc633ec91e8588aff2d5ecdeb7608874945441305041d86`  
		Last Modified: Fri, 06 Sep 2024 22:08:33 GMT  
		Size: 1.2 MB (1230001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cd621e47a016f3bc37b364ed821a658b919e7349229e745b9c0c6c1b4def18`  
		Last Modified: Fri, 06 Sep 2024 22:08:33 GMT  
		Size: 18.8 MB (18755824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0981cf3ce31d4d214f361b3174ab11f225ca9cb71dbeaee020e4dde417d49eb6`  
		Last Modified: Fri, 06 Sep 2024 22:08:34 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f2152e6dfa2d3a30f76312e481b05da3a4ae70d3133435d8c90a34b7d8e152`  
		Last Modified: Fri, 06 Sep 2024 22:08:34 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e8cd6eb6a192a67f6d671f68f0a84f8551cb2924a1af5d81feaf48f626eae2`  
		Last Modified: Fri, 06 Sep 2024 22:08:34 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956c9d747bd1c831aec8653bc079baca3dfeb7394a0747cc5edf179fe55677ce`  
		Last Modified: Fri, 06 Sep 2024 22:08:35 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:be52c6acfa39a32cebd4d6435a85a351a51c2032bcf157f4796ed09a027cc698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 KB (59647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1113672659c3083348dc45fa5eb80123ff99510d59b3d75b5af0209b1665e6`

```dockerfile
```

-	Layers:
	-	`sha256:69c44dec405e2229d56c151c660d153cf6cc3218de0f801d2a52e884d92d5b8a`  
		Last Modified: Fri, 06 Sep 2024 22:08:32 GMT  
		Size: 59.6 KB (59647 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:a09eb88889e99d143f3da001f9d7aaebab55d1528cec5ed56fb3bc66a473a077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62186815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf570d658d9f898880702df27e59036d2de2127e13e2488c59e6d058444339e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Mon, 26 Aug 2024 05:05:19 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 26 Aug 2024 05:05:19 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 26 Aug 2024 05:05:19 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_VERSION=3.13.7
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Aug 2024 05:05:19 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 26 Aug 2024 05:05:19 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 26 Aug 2024 05:05:19 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Aug 2024 05:05:19 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 26 Aug 2024 05:05:19 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a982534696144ceb7d200537d306396b09f6637e6757b2a9de2f1dab8708d3ec`  
		Last Modified: Sat, 17 Aug 2024 00:54:29 GMT  
		Size: 33.1 MB (33087010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6c5f6bf838b2f2d43d5fad5daa6fdd20957bb236949a0921ac9a5a37be47bf`  
		Last Modified: Sat, 17 Aug 2024 00:54:28 GMT  
		Size: 6.1 MB (6106894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab49839e095324037fecaf8073095462d04abcf8ef94a3d9dd6b642053b1fa6f`  
		Last Modified: Sat, 17 Aug 2024 00:54:28 GMT  
		Size: 1.1 MB (1140442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb51454f1ae74db66cafc4ad41328eb70670d3fedf739a5b3670a8503f7fbab`  
		Last Modified: Mon, 26 Aug 2024 23:04:05 GMT  
		Size: 18.8 MB (18755760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6399a3de37ef553ea32d69f0caf4fd1a3bd7c4e3a417482c93593b9c3a1d7a`  
		Last Modified: Mon, 26 Aug 2024 23:04:04 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263bed7361f59871ebd0465ab985eca1e6b9b41a8c81cb10b384a2e0ae16380b`  
		Last Modified: Mon, 26 Aug 2024 23:04:04 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c752f1c60829f29cea00b1b9de704e0103e2c20620f0ef048f1abdeedf83c009`  
		Last Modified: Mon, 26 Aug 2024 23:04:04 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ff0e17f109638b7d7cd81bc5421735725e73161d139230f580b380f4a67462`  
		Last Modified: Mon, 26 Aug 2024 23:04:05 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:df82dafccf262461ddb172e178f94b8da438913312d7b60b8a3b637cd0e11aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6221158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1603eb759e92ad3ce986da7b8cf3e3e8c2a402caf9edf72eba5911fd1fbc55`

```dockerfile
```

-	Layers:
	-	`sha256:e727f660da9835415439c12582917de54500f27a66c04e92ca4dff63b90aae51`  
		Last Modified: Mon, 26 Aug 2024 23:04:04 GMT  
		Size: 636.1 KB (636127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81957e3f3ee027d6adbc321f2271e5a3f0dbd6fe4a9bdf5281c7095b91fa2e3c`  
		Last Modified: Mon, 26 Aug 2024 23:04:05 GMT  
		Size: 2.8 MB (2830893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6594ee99f3495108d7bb535e2a239fd779bda893dfcddb4c00b4b2e55bfef7a`  
		Last Modified: Mon, 26 Aug 2024 23:04:05 GMT  
		Size: 2.7 MB (2692301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee969f49595e2ae7b37a1fea1b19df06fa15ace0c7bf8a08900855c5e804766`  
		Last Modified: Mon, 26 Aug 2024 23:04:04 GMT  
		Size: 61.8 KB (61837 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:41e0fa4245015d89013922be6bf740b166d4fb76035444203d1fff78c92d4a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72058175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9a000f40c08244bf031c27f76e363222926100815f533d75ae9fcfe07e2721`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 26 Aug 2024 05:05:19 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 26 Aug 2024 05:05:19 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 26 Aug 2024 05:05:19 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_VERSION=3.13.7
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Aug 2024 05:05:19 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 26 Aug 2024 05:05:19 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 26 Aug 2024 05:05:19 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Aug 2024 05:05:19 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 26 Aug 2024 05:05:19 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ebcf3fc865f7b70630f40a496af3e4f5e8899252513db86d9ed6898a6502f3`  
		Last Modified: Sat, 17 Aug 2024 00:40:49 GMT  
		Size: 39.7 MB (39685252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943739027bc55d6480260d07dffa2e33c88464e97042fdbb05125bc2b44e7727`  
		Last Modified: Sat, 17 Aug 2024 00:40:49 GMT  
		Size: 7.2 MB (7200490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e68d00f43ae338a7a382fd8f3e6e9f5e5f500bef4b4cf55695f4ef0fc4a61b`  
		Last Modified: Sat, 17 Aug 2024 00:40:48 GMT  
		Size: 2.3 MB (2327824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab1be8eb3b0e88f34081c103091fd6275d533910b8d17a0078f86a7083e5c0d`  
		Last Modified: Mon, 26 Aug 2024 23:23:15 GMT  
		Size: 18.8 MB (18755925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47104d95eb9400adee78909240dd80052b003bc20b95f100ce44617ba457381`  
		Last Modified: Mon, 26 Aug 2024 23:23:14 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e552ed084c11733fb7e6b95833ea1974c9fd4e863101eca38b861cf219b9b0`  
		Last Modified: Mon, 26 Aug 2024 23:23:14 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4ce4b67c42c91d3a20aa8559c4c94471c920be6566b35b96f8895aaaf609fe`  
		Last Modified: Mon, 26 Aug 2024 23:23:14 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ece47ef38ab60a5c3a7f29b9f640ac732672405fa8cce1306e2cad08b8fd3c`  
		Last Modified: Mon, 26 Aug 2024 23:23:15 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f68a4b7b28f13baa310902d537071f522738d46fe48257a62c00b96d44cfe8ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4933e4e12b5926bcc496b6aa800828cbf850d4c8e4135ad735c50e0d419cb9c5`

```dockerfile
```

-	Layers:
	-	`sha256:04d85d0dfd6b19661dd8e8f64cc8cf00478a0ede951bf7dbdc21aa185bb5a457`  
		Last Modified: Mon, 26 Aug 2024 23:23:14 GMT  
		Size: 640.9 KB (640850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd5145092802478439c747b668f71f175d97c8dea3e590f6e9b66a91049e0ef2`  
		Last Modified: Mon, 26 Aug 2024 23:23:14 GMT  
		Size: 2.9 MB (2948820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37cc3692e367cb6a9a8762eb13dd78079467d3f8bc00705509f9918ab57d7152`  
		Last Modified: Mon, 26 Aug 2024 23:23:14 GMT  
		Size: 2.8 MB (2810234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24d3ff1de61afa5f97b3dff600fe96014d5163b3cb53fceb0329ab72a54f0c25`  
		Last Modified: Mon, 26 Aug 2024 23:23:14 GMT  
		Size: 62.0 KB (61950 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:a5cdbfdca8d3554f054278ae12638956fe843a9593174d26dfa81e96c6bf8395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64321785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888c792ac698bde3c1c1f61b67ff3f5407a865a79cca4046f8ef462704d033ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Sep 2024 23:00:29 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Thu, 05 Sep 2024 23:00:29 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 23:00:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 05 Sep 2024 23:00:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 05 Sep 2024 23:00:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_VERSION=3.13.7
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 23:00:29 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 05 Sep 2024 23:00:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Sep 2024 23:00:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 23:00:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 05 Sep 2024 23:00:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b286cd1742cf77217a70545609ced9d2ea5bedc803f07f76739fe1b9a097c3`  
		Last Modified: Fri, 06 Sep 2024 23:28:34 GMT  
		Size: 33.4 MB (33357551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8539bbaf19d3cd04df06c0a0dc0fa5e3d9f091ec31232ade2560778febfe2af`  
		Last Modified: Fri, 06 Sep 2024 23:28:33 GMT  
		Size: 7.5 MB (7506287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d69dc3d31f3499e8b3a0cdc6365e4c874e8ea52602f87cf5a343f54aeb7b21`  
		Last Modified: Fri, 06 Sep 2024 23:28:33 GMT  
		Size: 1.2 MB (1231482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f94a6a84082734ffad173bc842160c199b970536149bd7823dfdd5995a5404`  
		Last Modified: Fri, 06 Sep 2024 23:28:33 GMT  
		Size: 18.8 MB (18755556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac69f69624d9ed308fd3c1b9d34af819036c95e24561ebe49bcc5ce4be341693`  
		Last Modified: Fri, 06 Sep 2024 23:28:34 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a7c07a41c4150920d5dc01c6436e400c7220ada4e3a17d8d25021066e1306e`  
		Last Modified: Fri, 06 Sep 2024 23:28:34 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02360700e18bcaff02c8258ee8b922e661a9e1ce3c1a0d8c24162c88cec92d37`  
		Last Modified: Fri, 06 Sep 2024 23:28:35 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4de9092fa435012c9d67fb22a865c4c71a71a3aba24a2cd14f2e8966b898c8b`  
		Last Modified: Fri, 06 Sep 2024 23:28:34 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fdeed73c659b0f12132ae4b81bfe82eaaf05cb16f51830604243392f70e05490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6401179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f32c324ceee251eadbb0022b2474344d4bae6a0645d42238e3b116a1fd03de`

```dockerfile
```

-	Layers:
	-	`sha256:8514204381ad2d48247cc04ff69cfba76aef1e6471cfbbc182ea7f4607ef0770`  
		Last Modified: Fri, 06 Sep 2024 23:28:33 GMT  
		Size: 635.4 KB (635440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90e1c8371aed524f08ca6a99a8be67603e2f1672d06d3c36779558b473974cd1`  
		Last Modified: Fri, 06 Sep 2024 23:28:33 GMT  
		Size: 2.9 MB (2921793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e106e641e08e02ec8652059a5acda5dc1072698d7ea6bd24c93e09ced84d6f20`  
		Last Modified: Fri, 06 Sep 2024 23:28:33 GMT  
		Size: 2.8 MB (2784314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdf0899f4997a641697df24118f97a631da9bdac3f663a5fd4d691e59e89c8e7`  
		Last Modified: Fri, 06 Sep 2024 23:28:33 GMT  
		Size: 59.6 KB (59632 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:d1ea49955399cb321017b4e5dcfa06b48689700386047c6ea0696d7642c4bcce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65285421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c2974cdd022e0ebb63ed45b53d0938290632938ad3cbe2d6f01221b301f94e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Mon, 26 Aug 2024 05:05:19 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 26 Aug 2024 05:05:19 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 26 Aug 2024 05:05:19 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_VERSION=3.13.7
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Aug 2024 05:05:19 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 26 Aug 2024 05:05:19 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 26 Aug 2024 05:05:19 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Aug 2024 05:05:19 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 26 Aug 2024 05:05:19 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac555ce06cdd1b1803ad1cccc536261847bc31284daf67faf261da2b56ca355c`  
		Last Modified: Fri, 16 Aug 2024 23:45:21 GMT  
		Size: 33.6 MB (33611323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146bf248658271bde35bd185d35b925e146475d0f47bf2c2ff39e655a69e6358`  
		Last Modified: Fri, 16 Aug 2024 23:45:21 GMT  
		Size: 8.0 MB (7992691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e0cf12e6994981d1f02a7d184b25b4d3de3cd9d4377d5de69830be34dba021`  
		Last Modified: Fri, 16 Aug 2024 23:45:20 GMT  
		Size: 1.4 MB (1352388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c445972a4b347dea3c79fe4c676fbf0b9dec3bdc452f8109e5498fb5fe1ee6`  
		Last Modified: Mon, 26 Aug 2024 23:13:24 GMT  
		Size: 18.8 MB (18755713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e386948d484e9c0130d01c39616c0bfa957c0214ddcdd4cd11d324c007cb697c`  
		Last Modified: Mon, 26 Aug 2024 23:13:23 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211cda63147654d3bb5712e44e94e898b92acec45351190768cb69dee1ca88f3`  
		Last Modified: Mon, 26 Aug 2024 23:13:23 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d29e604c9c8212608a895857680846c7e1e8652be5d1eeeae2a5bc8f488aa0`  
		Last Modified: Mon, 26 Aug 2024 23:13:23 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9368f56a432cb6dce8f105e0196af178ccbde2773888063035967d7c91fd4aae`  
		Last Modified: Mon, 26 Aug 2024 23:13:24 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2d423308703dec26fd7b5d6eccee86a906308b8d4055084dee39f02ae4fb19c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6399875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca6e2062a8c6f47a77d3ed8ed5ec558420c24b5964cb173bc0cc037ce55ef34`

```dockerfile
```

-	Layers:
	-	`sha256:1452a18645a9a2be6088266388ebfa99a74cefc4818b5aa958ec955d5bf6e9df`  
		Last Modified: Mon, 26 Aug 2024 23:13:24 GMT  
		Size: 634.2 KB (634171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd329ede0336826c3dba44399a31ede1ea0ccf7022d9f8dee491586ee09bb9b0`  
		Last Modified: Mon, 26 Aug 2024 23:13:24 GMT  
		Size: 2.9 MB (2921298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe72f2b34bcc40eb0a4e471e4ebf38558f61b9c306c9786efffeab561168574d`  
		Last Modified: Mon, 26 Aug 2024 23:13:24 GMT  
		Size: 2.8 MB (2782700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b32f9a6e88287d97f7e7d9af01d60da464b0cfffafcc1863851903d2ce56465`  
		Last Modified: Mon, 26 Aug 2024 23:13:23 GMT  
		Size: 61.7 KB (61706 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:6f302d5d442215dd6728141771ba59bc7cfc8234704c6bf841bdad2babf19f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66730392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba14769df3d08ff190d2eec089f47c249b90939af8d1748eafd125cda628f10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Mon, 26 Aug 2024 05:05:19 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 26 Aug 2024 05:05:19 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 26 Aug 2024 05:05:19 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_VERSION=3.13.7
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Aug 2024 05:05:19 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 26 Aug 2024 05:05:19 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 26 Aug 2024 05:05:19 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Aug 2024 05:05:19 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 26 Aug 2024 05:05:19 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fde60dda325d92105b2b1274e099d866ce87570a0707985f9752a8ec7da4c03`  
		Last Modified: Sat, 17 Aug 2024 05:25:21 GMT  
		Size: 34.6 MB (34557274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e3971502519b5c963df4629b9c87e1223669b58ccf2f3e8de44cf77dd73c82`  
		Last Modified: Sat, 17 Aug 2024 05:25:17 GMT  
		Size: 8.8 MB (8767142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b56b85ac22c9d7762baf23d6663bd81c3e11f9cace3cb354a608666615b32e`  
		Last Modified: Sat, 17 Aug 2024 05:25:16 GMT  
		Size: 1.3 MB (1277692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d7914bcab7c6addb4d006b441fe2671f316879e99aa389491fb4ddb800855d`  
		Last Modified: Mon, 26 Aug 2024 23:11:11 GMT  
		Size: 18.8 MB (18755859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3edc1bf765f3fcc1a5b75047bff36c7520616092229973c74a0f876f2c4ea02`  
		Last Modified: Mon, 26 Aug 2024 23:11:08 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6201cc1f7280355ca50782bf8d907b30e683cf84db959879043b43cecde5c8`  
		Last Modified: Mon, 26 Aug 2024 23:11:08 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a94c6339beef294fcdfb9982129aab04c9d10836c8d8a57f129daa7ccfb524a`  
		Last Modified: Mon, 26 Aug 2024 23:11:08 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a29bbfddbc16c4035f04462d932b1868355ee2eb56a4dfeaf90f6b793a09f4`  
		Last Modified: Mon, 26 Aug 2024 23:11:09 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2bf4cbc37abdb073a4febec3446ab0b39610e27be95e877d94d816de2bca4357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6434976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c87c2f114f324215caf8f5ea14418706317fd2aa713071e18fbaee5c03de56d`

```dockerfile
```

-	Layers:
	-	`sha256:bf98e0e62b5c204aa7e8c5efd59810e088ab3d1c6a1f5d1818bfcd33f8d32805`  
		Last Modified: Mon, 26 Aug 2024 23:11:08 GMT  
		Size: 637.0 KB (637014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85602055f7987bf064e42cfa6b609eb3f5061afea53f0a75d70cf612180c3806`  
		Last Modified: Mon, 26 Aug 2024 23:11:08 GMT  
		Size: 2.9 MB (2937421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1746acff95faff13288979c9c3d57d382ce1c3ef277667b89ea7855483ae5b88`  
		Last Modified: Mon, 26 Aug 2024 23:11:08 GMT  
		Size: 2.8 MB (2798835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:887c02020937be76192019f2e939ed76b000192ca14a98011a89c647fdbcf678`  
		Last Modified: Mon, 26 Aug 2024 23:11:08 GMT  
		Size: 61.7 KB (61706 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:d623872b268fea1d8831759baa99b90d039fc021727327b815613d583de2dd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63956320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba903a9bfc2564f668328ac04bf91b9a412904124246ede1e46a27e89e3518de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 23:00:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 05 Sep 2024 23:00:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 05 Sep 2024 23:00:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_VERSION=3.13.7
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 23:00:29 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 05 Sep 2024 23:00:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Sep 2024 23:00:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 23:00:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 05 Sep 2024 23:00:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48af7c055d0c95d71150bab6069c87af7c08d95861aedc81c674a0c1f75940a`  
		Last Modified: Fri, 06 Sep 2024 22:29:28 GMT  
		Size: 33.7 MB (33689705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd31a1f6d0585833aca5f24e51747680327e28ed2ab82e723d93ad13ff4c25d2`  
		Last Modified: Fri, 06 Sep 2024 22:29:28 GMT  
		Size: 6.7 MB (6723069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7eb279cad4912bddd20e8d99ad1c7e250f96cf5ae7ac3121a81f322c553001d`  
		Last Modified: Fri, 06 Sep 2024 22:29:27 GMT  
		Size: 1.3 MB (1325151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0918ec033b86ad0f23fdc710a186299e0be0f6d22ead4a209cc7f6147bd7a56e`  
		Last Modified: Fri, 06 Sep 2024 22:29:29 GMT  
		Size: 18.8 MB (18755581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c30f70e2d1285ef80faad18a7743aeb62a56e9465a27e0f74bdbe5cde889df`  
		Last Modified: Fri, 06 Sep 2024 22:29:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ade92383a190042a10ffdb05dd521ba5516ff7ccf279061990957be2599d06`  
		Last Modified: Fri, 06 Sep 2024 22:29:29 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c332834508d18904ea0acf36d6db3f15ff3215845ab726b85b1a7a8f9785d1af`  
		Last Modified: Fri, 06 Sep 2024 22:29:29 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56ff41ad42d28796f2a5e5400da3c4ac79452f1c96d7b7d9d0e10134cef3852`  
		Last Modified: Fri, 06 Sep 2024 22:29:29 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7b1df7dbcb4f26b319aeaf311dcf3fd51db3b9f04ec96d9d36bc9168e1c7f962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6231965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4fd7ff0b933ec85b0fa760f0b2a40322bc846f5db7c84d5406e9e3c36278f7`

```dockerfile
```

-	Layers:
	-	`sha256:f678a85fa1af420d0c0949549e538fabc300f380481cb66309da5995c60f3f19`  
		Last Modified: Fri, 06 Sep 2024 22:29:28 GMT  
		Size: 634.1 KB (634143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc117ef34a8c85d8dafadee9f580fb00dd56fd3c48962e17e8f96dfa4f1e2204`  
		Last Modified: Fri, 06 Sep 2024 22:29:28 GMT  
		Size: 2.8 MB (2838361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f2a622977e89809b1aa6024afab8fb759a4892af6f88e60ed55f54c4207f1e`  
		Last Modified: Fri, 06 Sep 2024 22:29:27 GMT  
		Size: 2.7 MB (2699783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbbb0c3a19b9f3e8995f7cf112e054c6e3a0b575a36417e2bc177d037dbcb8da`  
		Last Modified: Fri, 06 Sep 2024 22:29:27 GMT  
		Size: 59.7 KB (59678 bytes)  
		MIME: application/vnd.in-toto+json
