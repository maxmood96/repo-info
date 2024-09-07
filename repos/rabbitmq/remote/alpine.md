## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:4c53c9515be353e6ba6f2de921b3d7a738a54207c2f9a2c7c8007eed5182e355
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
$ docker pull rabbitmq@sha256:696bee21d3e6ca9c247448d0286ab529c2bc3b8fa88fb94f3189f1adb78cfbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73768194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca98669e517f564b1eb634cf2ae12cc8a66143c80972c625cd671b8f3058f71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Sep 2024 23:00:29 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eca09f2c72a68a8a2b9a9cd88e88eba995e6079529c2d523715d7bbd05436c3`  
		Last Modified: Fri, 06 Sep 2024 23:28:48 GMT  
		Size: 41.6 MB (41572554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f51652a4a75ea3a6f3db36c5d0d7aab8c592d03e61bcac9abfb6de9b1153172`  
		Last Modified: Fri, 06 Sep 2024 23:28:47 GMT  
		Size: 7.6 MB (7579756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33fdf0d0877b326f80b28f633c204a99d44498557d6a9b34bfbbb862e73e1f7`  
		Last Modified: Fri, 06 Sep 2024 23:28:47 GMT  
		Size: 2.2 MB (2234309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3c6ae62a4d460acbd40f51176a3896f45f507cf515a084d35625c4e949fbf1`  
		Last Modified: Fri, 06 Sep 2024 23:28:47 GMT  
		Size: 18.8 MB (18756021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f6f52386725331f1f6d55e1c4b7f03cc69372fec4b076d4245437102201640`  
		Last Modified: Fri, 06 Sep 2024 23:28:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4150d8cad9c558ca89d1e26fb5e0a63c245805a93d2e6c9586cf41325aa23f2`  
		Last Modified: Fri, 06 Sep 2024 23:28:48 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd0f0ddf296a11ace5bcabd1031f752ac4bd5d29a62f0eb8b60ab2544a6cc6f`  
		Last Modified: Fri, 06 Sep 2024 23:28:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d30a403f4e672ab273fba972a4f477b14ab4f2f42ec15fded76fe30010da9bd`  
		Last Modified: Fri, 06 Sep 2024 23:28:49 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d4ec299474da2345176aded75991bb3913a6f2163b431053adacb508808e7d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6425514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8301fb0ed81ef41974b7bd3cd2f03a090a03e801bd4e3fcbbb2c846104af1859`

```dockerfile
```

-	Layers:
	-	`sha256:ec82ea0373e870e3cbf66a3f64acfbb9db373b6d289410967e782a0eb6b46fb6`  
		Last Modified: Fri, 06 Sep 2024 23:28:47 GMT  
		Size: 640.2 KB (640168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33a4d9916250323ab13e2dbe88b1fb69501d781677d46607241298f145de5720`  
		Last Modified: Fri, 06 Sep 2024 23:28:47 GMT  
		Size: 2.9 MB (2931575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ad447f634d29a45e35717ff9344cb9f42e15dbd16eff3d936677cb39147af55`  
		Last Modified: Fri, 06 Sep 2024 23:28:47 GMT  
		Size: 2.8 MB (2794092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f901b1f4de5d27b21d332933a46e2454d7e00b5c67c60d7b0474f977cd36eb`  
		Last Modified: Fri, 06 Sep 2024 23:28:47 GMT  
		Size: 59.7 KB (59679 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:c75d21f53b3490cd50f521becdd630653eba6f2b82d262671e062de091670530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62946896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef39716540d4451f27bcaab24b1294fd0d5af225c2bee329783dd47dbc4db205`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Sep 2024 23:00:29 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc66c1a3e27e27c5a970b8b37549acb21251eb5842567c950bfc82024f709de7`  
		Last Modified: Sat, 07 Sep 2024 12:09:23 GMT  
		Size: 33.2 MB (33186251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3abc50462927f03260582322cb2c3d6210f59904ef9608305fe8de8fb9e1ace`  
		Last Modified: Sat, 07 Sep 2024 12:09:22 GMT  
		Size: 6.4 MB (6406534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9872d01a1e6350181a7ef1c990cfe1df0908063f4471e5a854b579da652154b2`  
		Last Modified: Sat, 07 Sep 2024 12:09:22 GMT  
		Size: 1.2 MB (1229998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fef2b80fa175cfe621e41561718490bb6601edffaa06d358d84bb1ffd799ce`  
		Last Modified: Sat, 07 Sep 2024 12:09:23 GMT  
		Size: 18.8 MB (18755851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56c54a1a16c51b92db2859eca27871508d091c858d2ac97ed8e646fe5b8c09f`  
		Last Modified: Sat, 07 Sep 2024 12:09:23 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2ef7f626a8725c177edfc3a1cd9a08f767194bddf76141ed07715a52e8aace`  
		Last Modified: Sat, 07 Sep 2024 12:09:24 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f92ce766854fa14edcdc988455dddb21ad47bffbf82c39bf2296b112a56004`  
		Last Modified: Sat, 07 Sep 2024 12:09:24 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fa159c008603ef47d16dd0b067ce761d88957e7064c630da879da4bc7df992`  
		Last Modified: Sat, 07 Sep 2024 12:09:24 GMT  
		Size: 835.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c8347bbf996b5c4553b04202a67abbe8adebf2494c3dd77f820b302c4f20869b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 KB (59647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86389f9d4cd4873b01957474df229788025726818a48b10da1347ab551412d37`

```dockerfile
```

-	Layers:
	-	`sha256:9b73a1bafff265ffffca8eca4dc69368e748a86741cfa92246140d4281d4b63b`  
		Last Modified: Sat, 07 Sep 2024 12:09:22 GMT  
		Size: 59.6 KB (59647 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:baf4bfa8e0979e52387ff71bb0633ad5411648a05f1d7064d340606fe30b31a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62180983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1283b8cdeaec8381f53f06d2280793fb3ac57254d2e1b95003d246cb68f8fbdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Sep 2024 23:00:29 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fd3c0e8feec6a6ab4290fc3975760063ed1791ecbbf7dcae19825084262a20`  
		Last Modified: Sat, 07 Sep 2024 12:31:54 GMT  
		Size: 33.1 MB (33087587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bc81f6e6d8eb1bbf37ee57929251a6f51c5192b69f5a58bdb3310316ee4655`  
		Last Modified: Sat, 07 Sep 2024 12:31:53 GMT  
		Size: 6.1 MB (6107616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e9b5001e1ba05fd7132db4b889c1ae537a9b36a7855e09ae5c089562d4ecc0`  
		Last Modified: Sat, 07 Sep 2024 12:31:53 GMT  
		Size: 1.1 MB (1132935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500d10f933f31f97607181b105189f27b377acde57bf462941392d7c47c5cc04`  
		Last Modified: Sat, 07 Sep 2024 12:31:54 GMT  
		Size: 18.8 MB (18755588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cc7c1bd822ffa94654fc74d921d1f290a8079e2800ef62bf98a5a01aafb421`  
		Last Modified: Sat, 07 Sep 2024 12:31:54 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09e594c766cc910786038de623a4d668e7f4a15d3b11d872866500c2b317d51`  
		Last Modified: Sat, 07 Sep 2024 12:31:54 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6144efd948ebc0adc15a27d33a1be9ffdcfd823ba2679fb9f05927a1250d24`  
		Last Modified: Sat, 07 Sep 2024 12:31:55 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df8ab039380adb3ec4301dafff1228098d335303621932cb45b601e416a66e3`  
		Last Modified: Sat, 07 Sep 2024 12:31:55 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:154820bdb7a2b0eebe04f45a2c799699ec68dc168f7296b88b9255212aa363a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2efd57c5ab13c919e9d0e1f9d81ded38852be66deda954f4c47b6e17446f8ee7`

```dockerfile
```

-	Layers:
	-	`sha256:84c0662c507951dc16c63464958c8e0701549c0ce29b554bcaac36e5ad5edfae`  
		Last Modified: Sat, 07 Sep 2024 12:31:53 GMT  
		Size: 636.1 KB (636133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:538e9e89d11fd999f5d22e78fbe349d2212c330f649a7849685359059548952e`  
		Last Modified: Sat, 07 Sep 2024 12:31:53 GMT  
		Size: 2.8 MB (2830903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b16e29931d26da791e5adc36eeaf6f3be302da1760c948e279f7bb04d6bc0d5a`  
		Last Modified: Sat, 07 Sep 2024 12:31:53 GMT  
		Size: 2.7 MB (2692301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6c437c2f66ae8737727852fdb3ef0d933096bf52108e166221a4b4388add0a9`  
		Last Modified: Sat, 07 Sep 2024 12:31:53 GMT  
		Size: 59.9 KB (59866 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:26800f3bb7cc000f72356f109fecd1c9bf1591836fa803b1585c57753f6f207c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72058308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0adb35fe363dee7a72b0e9c828d6c9bde7593bb7c3e67a41b848a955f7bb5da2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Sep 2024 23:00:29 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef39ecb8e5ae49d901da90ba925a549c7c1be290dd2605ed1e270498ca288417`  
		Last Modified: Sat, 07 Sep 2024 11:26:00 GMT  
		Size: 39.7 MB (39689974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468b5523a25ca1e2584731cd6a594e3b7f795f691841a1241c54040bac702916`  
		Last Modified: Sat, 07 Sep 2024 11:25:59 GMT  
		Size: 7.2 MB (7201680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80315518550f7f731986b2f491c82069f38a9a33797b865866ecf7b3c8450627`  
		Last Modified: Sat, 07 Sep 2024 11:25:59 GMT  
		Size: 2.3 MB (2321272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041bd73499b2e81f362db83447aedd71a9be3c76bdeedcd9c218bfffc938ccd9`  
		Last Modified: Sat, 07 Sep 2024 11:26:00 GMT  
		Size: 18.8 MB (18755983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8fdfdb07ca7f00acb10754bc51bd17e13cb986b6b495ac5c47229b45dbbd18`  
		Last Modified: Sat, 07 Sep 2024 11:26:00 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ba849f3be038cb0df7edd33cae8f6096512cef6c4811873c7294f27ff5b4b4`  
		Last Modified: Sat, 07 Sep 2024 11:26:01 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d67cc0a10c03f2438ffe34edc914a29594654e2dd794fb0c0558463ab3b66cb`  
		Last Modified: Sat, 07 Sep 2024 11:26:01 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47a6b27f12b5a1bb5b95e4d9f864f4ba6f68e85f22ebba5ba7599de6f501ac3`  
		Last Modified: Sat, 07 Sep 2024 11:26:01 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7a87cc039784b967306b66964d9e9593279dd07a455bbb75b1f07d8e015f261b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6459899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e4a9e65e899cbd6b2cbecd0b98d2b3533d3de2e119b87fe96466084540b8e8`

```dockerfile
```

-	Layers:
	-	`sha256:fe670d30e47e61ed80827a0b0be50c46399bfa6a4ca7a59dad155df9de203a15`  
		Last Modified: Sat, 07 Sep 2024 11:25:59 GMT  
		Size: 640.9 KB (640856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:822afd961124173d918f0c67f0aea93e036481dcc44e4600619fc057417bd06d`  
		Last Modified: Sat, 07 Sep 2024 11:25:59 GMT  
		Size: 2.9 MB (2948830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e913b093738e832ff00cd712c1a15f2c320cba9fb045c33f1a11681a6b5927fa`  
		Last Modified: Sat, 07 Sep 2024 11:25:59 GMT  
		Size: 2.8 MB (2810234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2e446b1154b69b8c82684827f02e770e81a1c15741035760f03d7b3c574966`  
		Last Modified: Sat, 07 Sep 2024 11:25:59 GMT  
		Size: 60.0 KB (59979 bytes)  
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
$ docker pull rabbitmq@sha256:039d4c1f274a624e0659afbc65765b033d7688eba682a56dcbb695b3b5b72886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65286285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69ec5bed78865e781c81527119d5300123ae90725262ac03cdc12e4e93138c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Sep 2024 23:00:29 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1853e19b9abd45415d5e4426c0c96f3b988eeb05be651638465d692498bbf22`  
		Last Modified: Sat, 07 Sep 2024 11:19:38 GMT  
		Size: 33.6 MB (33614555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb62eafad1788476117534a89908e5e57b22e7bb4056ecfe8fa65373e0e734b`  
		Last Modified: Sat, 07 Sep 2024 11:19:37 GMT  
		Size: 8.0 MB (7995995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f321a62a9d77407d36ddded2ac266624d8ec25220d9c695c69ef7b9e10eb482`  
		Last Modified: Sat, 07 Sep 2024 11:19:37 GMT  
		Size: 1.3 MB (1346085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf7e0d01699e6c16216c282588dcadcee119f728a7489d9027d7768c73d7e8d`  
		Last Modified: Sat, 07 Sep 2024 11:19:37 GMT  
		Size: 18.8 MB (18755476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b018785deec9e05ed90cdbc7369b1933785fca7d34ad94b77498e5ffe5716b7c`  
		Last Modified: Sat, 07 Sep 2024 11:19:38 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368e9b1e150953224ce3dfc66e098f81e08de259d24bca6ff0572296e118e9e9`  
		Last Modified: Sat, 07 Sep 2024 11:19:38 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae218a695c671ac7b97bc0fd036f519a770441521846ca1d89a0e488fdc39330`  
		Last Modified: Sat, 07 Sep 2024 11:19:39 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1354e4d697d5d38905590488b2f431faaff0b3b047e9a2641dbf31eba5f57d`  
		Last Modified: Sat, 07 Sep 2024 11:19:39 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3e5c86d9c0431fc30c32aa28f77d688310844ea9a4246f48a1df20cd0d8216ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5ccdc15c37b8fb425b2aa616f0817572c7c914ba4c7ac02de6b8944a759d5e`

```dockerfile
```

-	Layers:
	-	`sha256:3d800897b8a5dc79a031729a9b5411ba50fbc6f66d58cb02f4a8a76fc960b9e4`  
		Last Modified: Sat, 07 Sep 2024 11:19:37 GMT  
		Size: 634.2 KB (634177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a3b19807e020480ab4d1df0217644260e3c1fcb1502bcc8b7a19eefb98b1d34`  
		Last Modified: Sat, 07 Sep 2024 11:19:37 GMT  
		Size: 2.9 MB (2921308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6db21dd6d81f5b2da030d5742c9b9e98b64c146b919654ac7e752948ed6186a`  
		Last Modified: Sat, 07 Sep 2024 11:19:37 GMT  
		Size: 2.8 MB (2782700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41fd4569763897918e1b8ae60eae841ec2f1ff5df5450de8925ad1814e09d4aa`  
		Last Modified: Sat, 07 Sep 2024 11:19:36 GMT  
		Size: 59.7 KB (59735 bytes)  
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
$ docker pull rabbitmq@sha256:7319d1ea7970ae6ff9bdece5eb6f5622ac6c280d616571f8cdfb5c6110eebc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63956872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d26fcd119c8ebe9355e6f4deea13b071b499136d7a710afc8d40d2fc47e9697`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Sep 2024 23:00:29 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f12f0ac580e40a0271dff2c75704d774bfa06b22d4db67fdd2d272f92631f52`  
		Last Modified: Sat, 07 Sep 2024 10:22:03 GMT  
		Size: 33.7 MB (33689704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8187148a8e52b1885ffb2b43d79a96c797117380153ed8f2a8011988536f5aa`  
		Last Modified: Sat, 07 Sep 2024 10:22:02 GMT  
		Size: 6.7 MB (6723060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6997532942272ba891350636cb761dc04c6a5f13a5a744ca32f553f17bad00f`  
		Last Modified: Sat, 07 Sep 2024 10:22:02 GMT  
		Size: 1.3 MB (1325175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f492041a4b074b756f1310a02b21da369b0e99079dd6ff2b7d3249ada81ed8`  
		Last Modified: Sat, 07 Sep 2024 10:22:02 GMT  
		Size: 18.8 MB (18755582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680672a22953a2903262bf3bb24c346296259ac1831a17a45313ca68f84754f3`  
		Last Modified: Sat, 07 Sep 2024 10:22:02 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92387649c42123fff7d39a08c67d54bcaac29b38c1ffa0fbd088cfcf825781a`  
		Last Modified: Sat, 07 Sep 2024 10:22:02 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4247c03a560e720f7a36ea032068613b62cbb93740d61458e5de28b609ee2f8`  
		Last Modified: Sat, 07 Sep 2024 10:22:03 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7bd20aa3725877861e6c00905d70537c05db1e40b65ce9cc707ff50519a602`  
		Last Modified: Sat, 07 Sep 2024 10:22:03 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:63bcb9f5b741ba96bed590e7e4689c8f0af119854cf430c74402038474bf72ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6231966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deea36c0d34ecf653af2fc99d94ef4d9b02bb36d574392bd1534e6aa0cdb3d9e`

```dockerfile
```

-	Layers:
	-	`sha256:ab7ca7add1c9d6e979fcc687606b8b5a7eae7837698e2d27df5b629f0fb6380c`  
		Last Modified: Sat, 07 Sep 2024 10:22:02 GMT  
		Size: 634.1 KB (634143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28608bcb27323f58778265c4b271406291eabbfc22c511c113198090f14f86df`  
		Last Modified: Sat, 07 Sep 2024 10:22:02 GMT  
		Size: 2.8 MB (2838361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ad7cc0c7ba1125b033904ffe9110cce1df5051a7c906da5444f7435544d9659`  
		Last Modified: Sat, 07 Sep 2024 10:22:01 GMT  
		Size: 2.7 MB (2699783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40a2db69a863040ad55c7f88dd251e142034e4c0cd7cc663f8b83c120e235661`  
		Last Modified: Sat, 07 Sep 2024 10:22:01 GMT  
		Size: 59.7 KB (59679 bytes)  
		MIME: application/vnd.in-toto+json
