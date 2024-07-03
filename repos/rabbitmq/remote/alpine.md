## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:fadf2c493e98b269edb68f037e3eb7cc20e4c94e1863709b5d63d969fb8465f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `rabbitmq:alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:931c05dc86b8b15b2221d128235851fce482918eb6428bee8780009c30d62fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73654713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527546f287b61f51690bf84ae33233218a8d462c272255ba5d9d320edd8e2f80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:04 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 20 Jun 2024 20:17:04 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 11:05:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 03 Jul 2024 11:05:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 03 Jul 2024 11:05:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_VERSION=3.13.4
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jul 2024 11:05:20 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 03 Jul 2024 11:05:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 03 Jul 2024 11:05:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jul 2024 11:05:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 03 Jul 2024 11:05:20 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a64a7a04199813c119fd27c63509e0e6ed5c6c334259fa40a86f5c7293f0fc`  
		Last Modified: Wed, 03 Jul 2024 19:05:40 GMT  
		Size: 41.6 MB (41563790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c82c8b86b5470f9218cdb5308a1fda3310b21adf4b4a8cb443f6e0026a9a5e`  
		Last Modified: Wed, 03 Jul 2024 19:05:40 GMT  
		Size: 7.6 MB (7578197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281696388f883f2468ae03f8dfa5c1bddf578a8b3203a123b7ae4a8f4a5c3d1c`  
		Last Modified: Wed, 03 Jul 2024 19:05:40 GMT  
		Size: 2.4 MB (2405749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d122f72cab3aeed31c5e7476e4b1c66785899f760322786312c39ecd76d585d1`  
		Last Modified: Wed, 03 Jul 2024 19:05:40 GMT  
		Size: 18.7 MB (18687893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f72c476b93bac29e69826ee19da6e2c72bb137e542471a700772e2ad710e32`  
		Last Modified: Wed, 03 Jul 2024 19:05:41 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a0415e3bf1fb1dbdaf12bc0309931e1f130b8cac596200560a201406913342`  
		Last Modified: Wed, 03 Jul 2024 19:05:41 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bc500a544751df963614c8f461f0488b4f06ff15bbb103738ef73f715bc5c3`  
		Last Modified: Wed, 03 Jul 2024 19:05:41 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6961cfa5708ba26021a76b685ab8962b0a8874187239d0d4ad77a5e0de6046`  
		Last Modified: Wed, 03 Jul 2024 19:05:42 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a3bf0b2eb407bcdabb622dcbe7a867b89ef062ee9d015741960a8ef2b1b2c3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6745493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b5410c7d0b8faa8f15ed030261e78e153fd1260b4ffb0f9db64e91f3d3aee1`

```dockerfile
```

-	Layers:
	-	`sha256:6b2fa7a9eca6f6d68cbb066efc9e010e36aaf078d38e7103639a3d48bf3d71c1`  
		Last Modified: Wed, 03 Jul 2024 19:05:40 GMT  
		Size: 998.9 KB (998946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20ea4a9c548b8fa655e847fbd0bafb65bdcf93b29f0b0385c1014e2647e36128`  
		Last Modified: Wed, 03 Jul 2024 19:05:40 GMT  
		Size: 2.9 MB (2903559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4844aa497f42420ac58778e643639a56026de2fb8a3cf7927ac1d1ae28be3898`  
		Last Modified: Wed, 03 Jul 2024 19:05:40 GMT  
		Size: 2.8 MB (2781449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f32c5d2f4cd9c93e9342ca3d161e3f0517372589b489f02c35572c1a2b01eda`  
		Last Modified: Wed, 03 Jul 2024 19:05:40 GMT  
		Size: 61.5 KB (61539 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:759d27120ecf164d7578f219d7eea4985863e51ee360e758296e2395100c75d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62852910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d922ba472eeb0514fdde83a612b8066b1dcc925a7d284e5ea1a3f5643cf723e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 11:05:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 03 Jul 2024 11:05:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 03 Jul 2024 11:05:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_VERSION=3.13.4
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jul 2024 11:05:20 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 03 Jul 2024 11:05:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 03 Jul 2024 11:05:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jul 2024 11:05:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 03 Jul 2024 11:05:20 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d3c206dd3804c9ab495e7f6e209755ebb9216cbbf2747bbaf077904de383bd`  
		Last Modified: Wed, 03 Jul 2024 19:05:08 GMT  
		Size: 33.2 MB (33181917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e45c3a9d9acde531e2b4f546debde6ba853ec57a9de50855ed47b65c7d7bfb`  
		Last Modified: Wed, 03 Jul 2024 19:05:07 GMT  
		Size: 6.4 MB (6406018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2322b96e7d12f8fd7fade2a074db7d463ef5d79f469bfd4bedd68c52cfbc178e`  
		Last Modified: Wed, 03 Jul 2024 19:05:07 GMT  
		Size: 1.4 MB (1401701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369df73e714534807272fbe72ffdc053a35476247d4247ec84277760413cda45`  
		Last Modified: Wed, 03 Jul 2024 19:05:07 GMT  
		Size: 18.7 MB (18687614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b33ae6597a02312d24b9e220cb06b1a6c6cbd81fe99cc7222f331a02076ccad`  
		Last Modified: Wed, 03 Jul 2024 19:05:08 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4858940129395b20e8e6ff1132d935cd8aefb64b17d0dc0b29f27d1ab32a34a0`  
		Last Modified: Wed, 03 Jul 2024 19:05:09 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c638c70e092cbb9bcc12b05a71ba8908d0563605c41f40b4568886d9da7f553e`  
		Last Modified: Wed, 03 Jul 2024 19:05:09 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f2b1f43d475e069cb8b8805212f2474f853d34107a31edb758fcb7f4f51c91`  
		Last Modified: Wed, 03 Jul 2024 19:05:09 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ba62d3403b8061c3e19a17f6015ab07af40fa37dfc79db9cde86a9371d3ba239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 KB (61507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7de2f9318688c935ab9fb821fad4c0eded4b42d46256d1ca53f0ad549d1a93a`

```dockerfile
```

-	Layers:
	-	`sha256:ed8b3bffd31ce0ccb62ee2db315264d37ef45dda18c89635db64800a9b89a4a9`  
		Last Modified: Wed, 03 Jul 2024 19:05:06 GMT  
		Size: 61.5 KB (61507 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:91a848ed4526c8c480ac9ef9ed2addf5a9991fc2690657167d1fb27b140ea9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62111004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4818d910f4ff27878b23304676f5cba3239aa99b1b9d82ef42269f9de86425`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:32 GMT
ADD file:a79253a22e927307fa2edd1752e7945fd88afbb97c73bbbe771cc99947c0517a in / 
# Thu, 20 Jun 2024 18:00:32 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 11:05:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 03 Jul 2024 11:05:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 03 Jul 2024 11:05:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_VERSION=3.13.4
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jul 2024 11:05:20 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 03 Jul 2024 11:05:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 03 Jul 2024 11:05:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jul 2024 11:05:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 03 Jul 2024 11:05:20 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4007367bb0cf596fd27d2207989b3864272eb2e5caf7429c07e68abc3bd47b0c`  
		Last Modified: Thu, 20 Jun 2024 18:01:06 GMT  
		Size: 2.9 MB (2926498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98435a62bf9faf8efb2d2c709fd24a68236b4c50d936730dab498cf15f60f213`  
		Last Modified: Wed, 03 Jul 2024 20:08:17 GMT  
		Size: 33.1 MB (33082761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c4b9773640d0e399b0c9ecae9304bfd353d1b7a4bf1323b383fd1850fe7b5f`  
		Last Modified: Wed, 03 Jul 2024 20:08:16 GMT  
		Size: 6.1 MB (6106917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfc282be46b09e1fb39e345761a38f305d8961dfe946cdab240074986bcb6aa`  
		Last Modified: Wed, 03 Jul 2024 20:08:16 GMT  
		Size: 1.3 MB (1305643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc31fa20d226bde752b1aec2ed083b1c21139b2d6dfbb0537b282ece84d3a00`  
		Last Modified: Wed, 03 Jul 2024 20:08:17 GMT  
		Size: 18.7 MB (18687439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abc96e50cb17e21cdd6bc1125fbee498dff5c4058feffefea250ed828cccedf`  
		Last Modified: Wed, 03 Jul 2024 20:08:17 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5765bb89ab750279b317507ec8617ac875f3084f2f76bb9e0aa9925e00de048`  
		Last Modified: Wed, 03 Jul 2024 20:08:17 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb90ef407aa5f7e2e8f944a80660bc85cd69870fe073532ff6252175fbe38a5`  
		Last Modified: Wed, 03 Jul 2024 20:08:18 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89837f99d1964f0c55ff5c19b8c0438011c6bd201a52419dc098a82a20cada22`  
		Last Modified: Wed, 03 Jul 2024 20:08:18 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:355809da50553d933bf979f305057ee9a974df1d1cc8ef7702278b7c6bfa0ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6539593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad3f097c2fb373b1e338b4a11eb95a1019d5db693e7a2d5f09874939e40ae31`

```dockerfile
```

-	Layers:
	-	`sha256:edeb35a75a7493b8701ecf7ef30d544969e1fbc498b48ae0725e653aab2e4896`  
		Last Modified: Wed, 03 Jul 2024 20:08:16 GMT  
		Size: 995.3 KB (995340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b98a857a5d75e8829586f64817c72e982e56230a86bd3ac78f08f006c8262f2`  
		Last Modified: Wed, 03 Jul 2024 20:08:16 GMT  
		Size: 2.8 MB (2802874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e0621ad00b818d126bc8a82f49e333fcee6c76f1ac133421fab1eca43619253`  
		Last Modified: Wed, 03 Jul 2024 20:08:16 GMT  
		Size: 2.7 MB (2679653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6128d23915f3a20750ef45aa34758bfcfb796b04102cec11231db5bc6cb7489`  
		Last Modified: Wed, 03 Jul 2024 20:08:16 GMT  
		Size: 61.7 KB (61726 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:dbbf5f50f765346ec4bc6d8c2a915e97ac4969ffc80cae9e42c18c0fddee545d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71422442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e781b281ca2b1c1ce666eef4523d1c8295a764160fd34d75ad552ecb1c6ecfe1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 11:05:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 03 Jul 2024 11:05:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 03 Jul 2024 11:05:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_VERSION=3.13.4
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jul 2024 11:05:20 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 03 Jul 2024 11:05:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 03 Jul 2024 11:05:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jul 2024 11:05:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 03 Jul 2024 11:05:20 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f06c6f59278742a85cf487daf844eba4be4f69b04b37cef069a1c86a7385b0`  
		Last Modified: Wed, 03 Jul 2024 19:36:16 GMT  
		Size: 39.7 MB (39684757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107918694120a9a56da1b6f6a01f4c9752ffdfd6acfb9648ac23cfeaa1b615b0`  
		Last Modified: Wed, 03 Jul 2024 19:36:15 GMT  
		Size: 7.2 MB (7200829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e3290fb15647f2f6f5b0711b2c2765ea488ae02e5713ca493c1a66fc46d289`  
		Last Modified: Wed, 03 Jul 2024 19:36:14 GMT  
		Size: 2.5 MB (2490007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88af84931b9a43a62f30addc6531f0becd3392e7e183dba9c004b42807f45283`  
		Last Modified: Wed, 03 Jul 2024 19:36:15 GMT  
		Size: 18.7 MB (18687895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b3738b2854c485388babd3dcf49bf7504889265ae11cbb5b729433e4c65ddf`  
		Last Modified: Wed, 03 Jul 2024 19:36:16 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a967809164922a174984b7f3ba4991c4fdf86c029c02a2b42e742f16ccd723`  
		Last Modified: Wed, 03 Jul 2024 19:36:16 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7cec1b54f3e6f1920ee35a2daf304833e106c9d900b2cf80ea78f0ef4f640c`  
		Last Modified: Wed, 03 Jul 2024 19:36:16 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a197d7f5fb223dec174b09291cdd88b15360affad7ad857771d29a91604715`  
		Last Modified: Wed, 03 Jul 2024 19:36:17 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fd3ede8ec8bbb83f7136e14b01f3f23538e32865a14435838a403b359e554f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6779870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa33166f02a2396cc25c1c4cdb47a8e947f425ed7e8dbb1b82bf763d674204c6`

```dockerfile
```

-	Layers:
	-	`sha256:d97fe83143c884075ec77e877f6b665afdcf5c9b025e665ed8e42149ca0f63f1`  
		Last Modified: Wed, 03 Jul 2024 19:36:14 GMT  
		Size: 999.6 KB (999634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78ea695c9f84254a860ccf59a46149037d0bc8c8bf168108b46dd95d2fe625b6`  
		Last Modified: Wed, 03 Jul 2024 19:36:14 GMT  
		Size: 2.9 MB (2920807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a4e0c07a3fcd6590f843c9b6cf0147bb5e4f3d1c2ce3a12b2556b783fac650`  
		Last Modified: Wed, 03 Jul 2024 19:36:14 GMT  
		Size: 2.8 MB (2797590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d5f408e87c28f04835de47f72ecd704fc5e196188b17b44dc57195b8bb0eff9`  
		Last Modified: Wed, 03 Jul 2024 19:36:14 GMT  
		Size: 61.8 KB (61839 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:307b538987d3e193373b93129415dbb46b7a1c5c7ebe89f99875d41ed6657a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64203875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432bce9d3420b88311dd5e1785572693ef42c99db2f7b46ee43963f79aa89b6b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:29 GMT
ADD file:fef5870f3bb90ed437c0331d7e65e52da6728b66d231aea95a605935fef056d7 in / 
# Thu, 20 Jun 2024 17:38:29 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 11:05:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 03 Jul 2024 11:05:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 03 Jul 2024 11:05:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_VERSION=3.13.4
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 03 Jul 2024 11:05:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jul 2024 11:05:20 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 03 Jul 2024 11:05:20 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 03 Jul 2024 11:05:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 03 Jul 2024 11:05:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Jul 2024 11:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jul 2024 11:05:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 03 Jul 2024 11:05:20 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:e9c6bf0d8f3154c26ee87ffe9feb02c91666069b8cbe0668cfae10922ad80c49`  
		Last Modified: Thu, 20 Jun 2024 17:39:06 GMT  
		Size: 3.3 MB (3250890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79299eb4816f9de4c615be6857af2714a383e8edbfb09c9038aae9d91dd72569`  
		Last Modified: Wed, 03 Jul 2024 19:05:18 GMT  
		Size: 33.4 MB (33354734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f706d831505daa75a4135d2e433f6fe93dbee111de8feeafb07b65863d97e3e`  
		Last Modified: Wed, 03 Jul 2024 19:05:17 GMT  
		Size: 7.5 MB (7504741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb7687727992fe86d7b36fd55d4f48520e994d6a8f36b05d34ad1a2a76ceb41`  
		Last Modified: Wed, 03 Jul 2024 19:05:16 GMT  
		Size: 1.4 MB (1404354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9559abe0707a065ab71e4ae8ac0533d7ca8bd06fe649133f8d536eaf018e8715`  
		Last Modified: Wed, 03 Jul 2024 19:05:17 GMT  
		Size: 18.7 MB (18687404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82576c22f3461113a4ec3c45acb5532fc3d846aa516f5422a32c79437147370a`  
		Last Modified: Wed, 03 Jul 2024 19:05:17 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80dd98f478907703ea0af9de9b16b1113ec0c0e28dfff5cca0d5d56588fe8ac`  
		Last Modified: Wed, 03 Jul 2024 19:05:17 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c11db3b941fcbef65ab32e76d235e1b969ca3d73601cd681ffd9994012505`  
		Last Modified: Wed, 03 Jul 2024 19:05:18 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75aabef9f9f3cb473853d32222fb1909576941aff3ab0965495724311ea1c0da`  
		Last Modified: Wed, 03 Jul 2024 19:05:18 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3a4c6f930833395d26d24faa52841029f4bbbf7134d428adf891b69689b97856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6721593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cefb8eb77bc0416b8755c1e72d27f02b1c50664104d63ef8af961b2ea80eef15`

```dockerfile
```

-	Layers:
	-	`sha256:535aa8a19ca875bf18bc89dae732aea71b8cea62519f6359d18023a54502c261`  
		Last Modified: Wed, 03 Jul 2024 19:05:16 GMT  
		Size: 994.6 KB (994647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74152b0ff376f91ca2bdbb0bd24a3fb6a3966d3c9ee08a2311054ce9e4e008ee`  
		Last Modified: Wed, 03 Jul 2024 19:05:16 GMT  
		Size: 2.9 MB (2893781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:173475c7b26f975ca4e5e5c729b056f3084c69f8fb31b12eb28e0b3a002e059c`  
		Last Modified: Wed, 03 Jul 2024 19:05:16 GMT  
		Size: 2.8 MB (2771673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06a39714d1b8a21d6887b653d03eb0faf941be9fb25f8a3caba76629474502b5`  
		Last Modified: Wed, 03 Jul 2024 19:05:16 GMT  
		Size: 61.5 KB (61492 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:f1821c2d0224c005f5ec0cba1dc94f6e72c5c177efaf1bfb039b043fe052ec44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65199236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb0ae9020b62355d587a08c0b60b079036df0ed810bf7a2106b15e056ccb40d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:27 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Thu, 20 Jun 2024 18:18:28 GMT
CMD ["/bin/sh"]
# Tue, 25 Jun 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 25 Jun 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 25 Jun 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.3
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jun 2024 11:05:22 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 25 Jun 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 25 Jun 2024 11:05:22 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 25 Jun 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9916ff05de722b6e7353ed6886f06f776a1564a1e02ecc14e244e8b97d73b9`  
		Last Modified: Wed, 26 Jun 2024 00:03:40 GMT  
		Size: 33.6 MB (33608736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11df5be3043bb8491e45ca9cdc4def4259a9833d8bf65633dd390ce728fc8fc`  
		Last Modified: Wed, 26 Jun 2024 00:03:40 GMT  
		Size: 8.0 MB (7992852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b82a7d83391675554902ac2ad1ac775af6315238e17ecff9ed4a5bb243d092`  
		Last Modified: Wed, 26 Jun 2024 00:03:39 GMT  
		Size: 1.5 MB (1515691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6973a07553a6c17a034fe61db42e2ece691dc07e4afed16213f919f9cf7d5660`  
		Last Modified: Wed, 26 Jun 2024 00:03:40 GMT  
		Size: 18.7 MB (18719569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ebaa1fcbfe66e1c64b2a7a05b0e3c54f5b6d6803e7203e452882e09bc9bcac`  
		Last Modified: Wed, 26 Jun 2024 00:03:40 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f93ab8cd0dd8045af4774c15e5b7039a5f0c79e0dbefd89fb9b9a80bb21285`  
		Last Modified: Wed, 26 Jun 2024 00:03:42 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560c9a27163ef56283908f33f2def7f86c2e5b9f3ab4879a36d5ca44d2021348`  
		Last Modified: Wed, 26 Jun 2024 00:03:42 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26ac46631b3e877f5a94cdb28ba17a68f66218723a27bb9a9efbb5ba6e536d`  
		Last Modified: Wed, 26 Jun 2024 00:03:42 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:eb2304537fc08dd7b07a8152fa37fec1e8c8fb41a810038fd771ee95b7d6f7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6718305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305f185fab5cbf95dc954f81471bb81a78ce0fb453a6e1d05e89f8a787a6513b`

```dockerfile
```

-	Layers:
	-	`sha256:25ffe4c3521556c5843eb8c0f507ac7c0b646614dd3a7d06cf6b880a425835ca`  
		Last Modified: Wed, 26 Jun 2024 00:03:39 GMT  
		Size: 993.4 KB (993381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2068685b54cd6e0cbb06ac1f057a2bd18c373d16f3012aad6ee22da75945b88`  
		Last Modified: Wed, 26 Jun 2024 00:03:39 GMT  
		Size: 2.9 MB (2893277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca509a2cad5e269fd5eca3b6d09eaa38b9a3d938b3cad40ce4ddc4c5312e89cd`  
		Last Modified: Wed, 26 Jun 2024 00:03:39 GMT  
		Size: 2.8 MB (2770052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e140dec2f1b2bbfd7f481e30a647306911f57fd61b7daf1669f7490e2ba8d43`  
		Last Modified: Wed, 26 Jun 2024 00:03:39 GMT  
		Size: 61.6 KB (61595 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:08d1e58e264de168df45285942a110aa243969ce03dd450454ad41a5575444fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63878470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1e762043470b8fde47aee3f7298def94a092bed8595ff45914a907872340d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:12 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Thu, 20 Jun 2024 17:42:12 GMT
CMD ["/bin/sh"]
# Tue, 25 Jun 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 25 Jun 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 25 Jun 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.3
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 25 Jun 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jun 2024 11:05:22 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 25 Jun 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 25 Jun 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 25 Jun 2024 11:05:22 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 25 Jun 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb514cf9cc0400ae8f59fe2b584b752e933754ced33cbb35376883734256ed2`  
		Last Modified: Tue, 25 Jun 2024 23:41:59 GMT  
		Size: 33.7 MB (33686414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388c7766ea0499da7c3e9dbbd4300892650f6c1b9eaa0a3d36b487e0fe5d5e64`  
		Last Modified: Tue, 25 Jun 2024 23:41:58 GMT  
		Size: 6.7 MB (6721770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2305c5fef7855dc02807177ebb70af9ab8ba1b960e44f115234be9252fe4240`  
		Last Modified: Tue, 25 Jun 2024 23:41:58 GMT  
		Size: 1.5 MB (1496574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b97b3b76ffb09fc3a74baaa9eb6f3cf4dd811a9dbf651c45dce1bae8c0c85a3`  
		Last Modified: Tue, 25 Jun 2024 23:41:58 GMT  
		Size: 18.7 MB (18719471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236e34340ffeb4765e4c3b8614e9e07f711aed5f98b3e8cde79df291ee98f250`  
		Last Modified: Tue, 25 Jun 2024 23:41:59 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b831429477c630a7cd77aec37fc76abe14a1c34e86bd57784479182ddf13260`  
		Last Modified: Tue, 25 Jun 2024 23:41:59 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffbf075cecb4c748d4fdd2655cad8370ad5e1ae0d818a7e2cd6fb676074d722`  
		Last Modified: Tue, 25 Jun 2024 23:41:59 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819e2e755a9f5489b3ef86bc083496e042d6edafe931bb7016ccb437d32fa696`  
		Last Modified: Tue, 25 Jun 2024 23:42:00 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4b08a04203d0d47308ec4145d79ac334bce7ad4ef0feec53f83c3e02cacc8d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6552373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b505d852401c4c6ca9003135f4b4e8993caeda36e369d4de078270db3a6c57c`

```dockerfile
```

-	Layers:
	-	`sha256:e592235ab6f14115b4eb02b6ff54c419c5521c8d6c6842d0fc1dc409eb22d9de`  
		Last Modified: Tue, 25 Jun 2024 23:41:58 GMT  
		Size: 993.3 KB (993347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcfd97047cd86f6c3dfef8a7b08abd100f0bf37c7b3485671e07cde6b7bb29f7`  
		Last Modified: Tue, 25 Jun 2024 23:41:58 GMT  
		Size: 2.8 MB (2810346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d46015f666c8150149bac3cb68c963d262eb658caa92d7532efa65a08934af`  
		Last Modified: Tue, 25 Jun 2024 23:41:58 GMT  
		Size: 2.7 MB (2687141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58957e6e65225212457914dcd729aeec4aeea7dc3cf591ed95d66b702258aac2`  
		Last Modified: Tue, 25 Jun 2024 23:41:58 GMT  
		Size: 61.5 KB (61539 bytes)  
		MIME: application/vnd.in-toto+json
