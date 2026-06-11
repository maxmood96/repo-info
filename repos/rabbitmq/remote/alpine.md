## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:cbcb4b54ab4fed7a87cf6beba834222eae15fe85848ce6a970e097f3434a6432
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
$ docker pull rabbitmq@sha256:90ecef73594cf77d8732e21ef4c9a20293dcdfd203e6e529450233943fd8c6dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84057952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a0276665c2c828f7a4c29deb235d35235dc8401cf91f350c0f32388ee4eee6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:36:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Jun 2026 20:36:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Jun 2026 20:36:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Jun 2026 20:36:15 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Jun 2026 20:36:15 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:36:15 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Jun 2026 20:36:17 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Jun 2026 20:36:17 GMT
ENV RABBITMQ_VERSION=4.3.1
# Wed, 10 Jun 2026 20:36:17 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Jun 2026 20:36:17 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Jun 2026 20:36:17 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:36:22 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Jun 2026 20:36:23 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Jun 2026 20:36:23 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Jun 2026 20:36:23 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Jun 2026 20:36:23 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Jun 2026 20:36:23 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Jun 2026 20:36:23 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Wed, 10 Jun 2026 20:36:23 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Jun 2026 20:36:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:36:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 20:36:23 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Jun 2026 20:36:23 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57716cf2c14e87d437735ef0f99b7a85111849ef974429420f20507d7b61e71d`  
		Last Modified: Wed, 10 Jun 2026 20:36:40 GMT  
		Size: 42.6 MB (42623468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620a54bd707fec8ffe5fe2b400899bb132c358703e0bb4034c9f4e520574f42e`  
		Last Modified: Wed, 10 Jun 2026 20:36:38 GMT  
		Size: 9.2 MB (9206045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39886eb75bd7a99924b34fdd633f2d992ee2a4e52feeb5a714b9c1c41967d65`  
		Last Modified: Wed, 10 Jun 2026 20:36:38 GMT  
		Size: 2.5 MB (2465164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373ffc3254c93302626d0c696dedba5d8ec757e858a25bda6e75d6b04d111f2b`  
		Last Modified: Wed, 10 Jun 2026 20:36:39 GMT  
		Size: 25.9 MB (25897342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076a49573b429c5942fdb6531150c98fcd6d7ed555f8a7b8fd2b5a22f2831020`  
		Last Modified: Wed, 10 Jun 2026 20:36:40 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c73c32d3026f54f11491a8a15075e1ff41a0745bd95fb36c1716004e52c974`  
		Last Modified: Wed, 10 Jun 2026 20:36:40 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a82d302aa905f0fc2ea2d8a80ef2d544acd3f5bb62b44a2108414d402b4c52e`  
		Last Modified: Wed, 10 Jun 2026 20:36:41 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b00ad77374065864c068eda32f129876ebc8c5ff6de70c28b5cf23af16f6913`  
		Last Modified: Wed, 10 Jun 2026 20:36:41 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f49dc8af92a6e0d24f3b2e7a85661ab895a25b6b259c886e78fe6b71047cb3da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6963430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21c54bc101f25eb181ee562d2dcb6e01bdb4aab09cfb5553ac73ec753921170`

```dockerfile
```

-	Layers:
	-	`sha256:268bd01541b1bacf92954f5e3b3fe1c8feb900d22d7e5a25d5d2e39d3ac2448a`  
		Last Modified: Wed, 10 Jun 2026 20:36:38 GMT  
		Size: 675.8 KB (675815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce5643297c6f510d2d9c2cfb7c289fb839f380bb1f1859216e500a0baee7959b`  
		Last Modified: Wed, 10 Jun 2026 20:36:38 GMT  
		Size: 3.2 MB (3190523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d533d3e03d43ef78d9dc8dc83f4d9913d9447f118dc91c76e6cd311860ec627`  
		Last Modified: Wed, 10 Jun 2026 20:36:38 GMT  
		Size: 3.0 MB (3036779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d1085b49c60fe9c6f6ff1a4ca2a863efc31b057ae074973cca9042f9d6b6d38`  
		Last Modified: Wed, 10 Jun 2026 20:36:43 GMT  
		Size: 60.3 KB (60313 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:29ecb203b10af1e4875e9c881609210db59b704e55467a5162056f2e9663c00b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72255811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90bde749c7e7035c7c1f05dc3bb0da4fbc6b0acf168e7adbb8f329fc22aa8eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:35:32 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Jun 2026 20:35:32 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Jun 2026 20:35:32 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Jun 2026 20:35:32 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Jun 2026 20:35:32 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:35:32 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Jun 2026 20:35:35 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Jun 2026 20:35:35 GMT
ENV RABBITMQ_VERSION=4.3.1
# Wed, 10 Jun 2026 20:35:35 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Jun 2026 20:35:35 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Jun 2026 20:35:35 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:35:44 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Jun 2026 20:35:46 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Jun 2026 20:35:46 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Jun 2026 20:35:46 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Jun 2026 20:35:46 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Jun 2026 20:35:46 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Jun 2026 20:35:46 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Wed, 10 Jun 2026 20:35:46 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Jun 2026 20:35:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:35:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 20:35:46 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Jun 2026 20:35:46 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8eb6af2a2ef8e13381e3cb2f661a4e69419991ea9ac38dc0e98d89c1f6142d`  
		Last Modified: Wed, 10 Jun 2026 20:35:53 GMT  
		Size: 33.5 MB (33518016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39d3aa9f17ac718095e70219a67483313546486d2f3e9304287917f70900b7b`  
		Last Modified: Wed, 10 Jun 2026 20:35:52 GMT  
		Size: 7.9 MB (7862483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bae76adc590ead27e0af5b3bc7e20fbbf59edbc5267bbc923388f93b96d08e7`  
		Last Modified: Wed, 10 Jun 2026 20:35:52 GMT  
		Size: 1.4 MB (1404170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18e493d065ea71c220a407e0434e0db7c195f084411f1f948d65b57c451044f`  
		Last Modified: Wed, 10 Jun 2026 20:35:53 GMT  
		Size: 25.9 MB (25897530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1968fc113d035f7d24cadf1e8625f56277f34cd3cf7366418583794f2c9f915c`  
		Last Modified: Wed, 10 Jun 2026 20:35:53 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16422663ddb1bc31f1815317bfc01dad17fe0f8181702276ee4a686ea8de08ea`  
		Last Modified: Wed, 10 Jun 2026 20:35:54 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369fcf0a87cceee72375701e3247b2c8054f8d2889b9fc7d4e45e553a76abc94`  
		Last Modified: Wed, 10 Jun 2026 20:35:55 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de31157b18a8c899d3994cafdaace28319b368ebd8e3d2b8de947f5bbc86dce7`  
		Last Modified: Wed, 10 Jun 2026 20:35:55 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:59c8c8e249ba231c651b7faf333ce0d4d13f85e407036c6ea81cb0e66dc7c105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 KB (60295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4799e464fdac78243df81317e77ba823aaadc5bdcf80faaeb8ba0d90183e279c`

```dockerfile
```

-	Layers:
	-	`sha256:ae9838a403b7231046bfff75ae317028254802ccc5ff5136afedcc3823fffd85`  
		Last Modified: Wed, 10 Jun 2026 20:35:52 GMT  
		Size: 60.3 KB (60295 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:7726c6b523ae654fff8dff02cb729d58dc167367efd52457c9e5bf02dcdafd04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71351258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b688d671dd6c302b24879e2a7a3c1d8a1abf637d3c258eb4b18a530033e1ab3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:39:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Jun 2026 20:39:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Jun 2026 20:39:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Jun 2026 20:39:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Jun 2026 20:39:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:39:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Jun 2026 20:39:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Jun 2026 20:39:30 GMT
ENV RABBITMQ_VERSION=4.3.1
# Wed, 10 Jun 2026 20:39:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Jun 2026 20:39:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Jun 2026 20:39:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:39:37 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Jun 2026 20:39:38 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Jun 2026 20:39:38 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Jun 2026 20:39:38 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Jun 2026 20:39:38 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Jun 2026 20:39:38 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Jun 2026 20:39:38 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Wed, 10 Jun 2026 20:39:38 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Jun 2026 20:39:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:39:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 20:39:38 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Jun 2026 20:39:38 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7101ba75e75ff6ca4f0baba1c6e6c33fc7af2d8ef05345de2bcbfd81fec88a`  
		Last Modified: Wed, 10 Jun 2026 20:39:54 GMT  
		Size: 33.4 MB (33430310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17bb13a60a2d61db8e8e94b36113d6cd7ebd5da6123311912703cc3b539f301`  
		Last Modified: Wed, 10 Jun 2026 20:39:53 GMT  
		Size: 7.4 MB (7442917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56287f46774c19bc68de9c2aa00e01511922dae90f4218c0fddca2e4b84427b7`  
		Last Modified: Wed, 10 Jun 2026 20:39:53 GMT  
		Size: 1.3 MB (1295453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4de59753af2e4de71bf4ae006fc01322d23fc568ebcce70cc3427f96a3d549`  
		Last Modified: Wed, 10 Jun 2026 20:39:54 GMT  
		Size: 25.9 MB (25897709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a770aaff4efe18ba7310aed91439e0fec4164295bca4dcf102ad891642d93098`  
		Last Modified: Wed, 10 Jun 2026 20:39:54 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df52c5bf26f42e23298800b4ce0bf3b8793c29155a39ec53dc55dca1f54a42b`  
		Last Modified: Wed, 10 Jun 2026 20:39:55 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd253bb3e1a778297feba4b4a2bb0a66b135375493064608c91e5dbce871894`  
		Last Modified: Wed, 10 Jun 2026 20:39:55 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b33b34e5fc1b433de96efffdd8bf02a23700e786e201f69b215ff65755497a`  
		Last Modified: Wed, 10 Jun 2026 20:39:56 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:290564e4f5fea8d58c725d2818138893e57f3cf74e7f5274a92d4700f00222ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341811e65f1ed93a14c1ceede9717b4d1dc8c49035bedb5d2cea2d6a3b986c19`

```dockerfile
```

-	Layers:
	-	`sha256:282067c4332b3888e75c31d404f964eb12f019ef8e0c1cc4a161d08bcc522e1a`  
		Last Modified: Wed, 10 Jun 2026 20:39:52 GMT  
		Size: 671.0 KB (670958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05f007a7e1ba498850f6d06c72609d9c43661ff50788cdcde856789da5702aa3`  
		Last Modified: Wed, 10 Jun 2026 20:39:52 GMT  
		Size: 3.1 MB (3057015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84562e05a99e9577e037250758fd688561dc114811069e8e3ed066522e7072e6`  
		Last Modified: Wed, 10 Jun 2026 20:39:53 GMT  
		Size: 2.9 MB (2901941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a35fcb46e3bc345dfd31f6ab03d4b4115253c5fa35a359a3a17370382302fc8`  
		Last Modified: Wed, 10 Jun 2026 20:39:52 GMT  
		Size: 60.5 KB (60509 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:d26e7ced7bd98c44b307dfaa21bfaa0c2e56e0deb44039a05a1907949715b99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83088891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9207cd75adcbcd37f45c439db8aac945d9307f99bae763bf86c190a240c2272e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:36:49 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Jun 2026 20:36:49 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Jun 2026 20:36:49 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Jun 2026 20:36:49 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Jun 2026 20:36:49 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:36:49 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Jun 2026 20:36:52 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Jun 2026 20:36:52 GMT
ENV RABBITMQ_VERSION=4.3.1
# Wed, 10 Jun 2026 20:36:52 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Jun 2026 20:36:52 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Jun 2026 20:36:52 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:36:58 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Jun 2026 20:36:59 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Jun 2026 20:36:59 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Jun 2026 20:36:59 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Jun 2026 20:36:59 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Jun 2026 20:36:59 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Jun 2026 20:36:59 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Wed, 10 Jun 2026 20:36:59 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Jun 2026 20:36:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:36:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 20:36:59 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Jun 2026 20:36:59 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8c13963b5ec79685a91dfe29fed11ac0ea685950be57b8a84013c65d08bfff`  
		Last Modified: Wed, 10 Jun 2026 20:37:16 GMT  
		Size: 40.5 MB (40483601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092e8608e0bd99661422aa6e771c75f28725d837558cbbf5331aee909e64179`  
		Last Modified: Wed, 10 Jun 2026 20:37:15 GMT  
		Size: 10.0 MB (9992259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e315ca9468d26606dd98888028d1fe44bc0d417b84f294ee8ad94b50e35c2865`  
		Last Modified: Wed, 10 Jun 2026 20:37:14 GMT  
		Size: 2.5 MB (2514024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0c16fb26325fa53cb2aeebba3b1255b55af5bc616fd0085cd8be192b35f675`  
		Last Modified: Wed, 10 Jun 2026 20:37:15 GMT  
		Size: 25.9 MB (25897393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c90e905f7a75d6f6763209bf717d04b905ed4d0ef49fee4d1d97c367b491233`  
		Last Modified: Wed, 10 Jun 2026 20:37:16 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae86693114faca2d7cadc4f3d2d6afe98aed325c1fea5680b6049d71f77beb6d`  
		Last Modified: Wed, 10 Jun 2026 20:37:16 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5954c6cdac9ebe2c3ce5aad17ce0e00412c9a32e963fc98a8240d835f8f39dbc`  
		Last Modified: Wed, 10 Jun 2026 20:37:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbe2e69432ff7110ed82bf002a6ac1c3f30d00903f26f7d29464b83c524b4cb`  
		Last Modified: Wed, 10 Jun 2026 20:37:17 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b4acc1d780f42a87e383b8d6bbf2c00d8b704ea987caa42c33914f20762f4bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7036408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4394b4960362af0cd10da54da8fb34db4cc2a7e92200aae6fd015347d2b787a5`

```dockerfile
```

-	Layers:
	-	`sha256:deec50d66fe5c8ee2d70c6c477a0f11829f956efc94eb7cca119e5ab5ce4685b`  
		Last Modified: Wed, 10 Jun 2026 20:37:14 GMT  
		Size: 676.0 KB (675958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58dd2e7fbadf6fc843aa93fb3028efdba9c5cdadbc8dfae991b7e0726eea8981`  
		Last Modified: Wed, 10 Jun 2026 20:37:14 GMT  
		Size: 3.2 MB (3227483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:964ed1a8a31b42121dbfb8ddb6314708ab752ea554027fcfd9ad2332a4fdc20a`  
		Last Modified: Wed, 10 Jun 2026 20:37:14 GMT  
		Size: 3.1 MB (3072415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dbd28e95f2bfda7682c0bdb2b5d45c2257f4b4370b2925391ce4cf940e65671`  
		Last Modified: Wed, 10 Jun 2026 20:37:14 GMT  
		Size: 60.6 KB (60552 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:aa03e18d25ca63325d40ff4d7ac39e71b4d8cbbdaf762e0fc051ac68c1ff4647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73677395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c4e39e803aaedba56fbb74933c1e54450ec0963c0bbf1435e01200851173ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 21:53:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Jun 2026 21:53:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Jun 2026 21:53:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Jun 2026 21:53:15 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Jun 2026 21:53:15 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 21:53:15 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Jun 2026 21:53:17 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Jun 2026 21:53:17 GMT
ENV RABBITMQ_VERSION=4.3.1
# Wed, 10 Jun 2026 21:53:17 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Jun 2026 21:53:17 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Jun 2026 21:53:17 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 21:53:23 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Jun 2026 21:53:24 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Jun 2026 21:53:24 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Jun 2026 21:53:24 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Jun 2026 21:53:24 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Jun 2026 21:53:24 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Jun 2026 21:53:24 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Wed, 10 Jun 2026 21:53:24 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Jun 2026 21:53:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 21:53:24 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Jun 2026 21:53:24 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc606350052373c6c681ca029c55807da97d9919ebc6bf1af10b001d7355f9bb`  
		Last Modified: Wed, 10 Jun 2026 21:53:39 GMT  
		Size: 33.5 MB (33482904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daceecb9ffc5e5c8127a348a3c13bf1ecef088af0b409fa2783fc096826dafad`  
		Last Modified: Wed, 10 Jun 2026 21:53:38 GMT  
		Size: 9.2 MB (9196018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d244b77a19ddcfd308912ad2c9f704a9b2557559cbab34c7c3997fc5c1a413`  
		Last Modified: Wed, 10 Jun 2026 21:53:38 GMT  
		Size: 1.4 MB (1408636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0142de6e9b65748621cab82dbca68cf9c59eb1e4e21cbfcfcca58218258e5c57`  
		Last Modified: Wed, 10 Jun 2026 21:53:39 GMT  
		Size: 25.9 MB (25897642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64acb5e1b69b80373c0d3ccc6fe18633243a27a4b8789d589f1dac6ce108394`  
		Last Modified: Wed, 10 Jun 2026 21:53:39 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38e5be3cd646a68da5a9bd61016bfec59c4a401257e6120fe080d2bf5c972d1`  
		Last Modified: Wed, 10 Jun 2026 21:53:39 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3575a6905641959ef143c3fc67eebae90a8223083df47c46e9ea6204229c77`  
		Last Modified: Wed, 10 Jun 2026 21:53:41 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dc37fc83350dc08d2f8548b2f1037b3739ac7426756bfee681385dba8da754`  
		Last Modified: Wed, 10 Jun 2026 21:53:40 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e379eb3553cd558c4e92a169a5cf4676fcded0b245b51806947024a4c9395bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6914885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efe38c0e46c7213516bd470090cd725518d35691931c3534c4e2be13e9b70dc`

```dockerfile
```

-	Layers:
	-	`sha256:ae41fa2086a660d355f7a40c3dac4af4615434a4077a8349533b20df6d90b064`  
		Last Modified: Wed, 10 Jun 2026 21:53:37 GMT  
		Size: 670.8 KB (670810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dc0315fe1bc8bf984c393ca5b09713b55e9b8a687678d3886ae048a01c1b836`  
		Last Modified: Wed, 10 Jun 2026 21:53:38 GMT  
		Size: 3.2 MB (3168776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9f014e43dfbde312dae919c76af1c65ab0869d737e428c1257dfffd856d5112`  
		Last Modified: Wed, 10 Jun 2026 21:53:38 GMT  
		Size: 3.0 MB (3015036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20c9b6ebd9ef13e4a870e3ccdb3fba7ae7e5c69675f4037fcca704aa11009b3c`  
		Last Modified: Wed, 10 Jun 2026 21:53:37 GMT  
		Size: 60.3 KB (60263 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:44e47f7cd47705382be7f5dc80c018e83d76a171989361869a6292f40aaf25e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75330944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7127e6f9052984e6c5a3b99644fbeaa1815f3ce7f306ac02800b5e964974dac8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:36:31 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Jun 2026 20:36:31 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Jun 2026 20:36:31 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Jun 2026 20:36:32 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Jun 2026 20:36:32 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:36:32 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Jun 2026 20:36:36 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Jun 2026 20:36:36 GMT
ENV RABBITMQ_VERSION=4.3.1
# Wed, 10 Jun 2026 20:36:36 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Jun 2026 20:36:36 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Jun 2026 20:36:36 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:36:46 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Jun 2026 20:36:48 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Jun 2026 20:36:48 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Jun 2026 20:36:48 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Jun 2026 20:36:48 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Jun 2026 20:36:48 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Jun 2026 20:36:48 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Wed, 10 Jun 2026 20:36:49 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Jun 2026 20:36:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:36:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 20:36:49 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Jun 2026 20:36:49 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa22709dd4be137b4bda4ecdaedd05a24418c560140baaa183a4a76219488f2`  
		Last Modified: Wed, 10 Jun 2026 20:37:22 GMT  
		Size: 34.1 MB (34091524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79befadaa45c78a7913de7300aa6a9bce59638f88d314c0bfe135b474212e83`  
		Last Modified: Wed, 10 Jun 2026 20:37:21 GMT  
		Size: 10.0 MB (9966909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c76dbe7ea1428c0045a108842102e5c8b379c8bf956d0cf3ec76dc747311f3`  
		Last Modified: Wed, 10 Jun 2026 20:37:20 GMT  
		Size: 1.5 MB (1542240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88734d5bc8b1bde041680552f5e6b9c19aabfaf90d6fe49471e42fdbae8d8020`  
		Last Modified: Wed, 10 Jun 2026 20:37:22 GMT  
		Size: 25.9 MB (25897586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e59c4776f74862335f7fd89efd56ddd3241f5a86d1842b3ba9c61eef208a7c`  
		Last Modified: Wed, 10 Jun 2026 20:37:22 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57231bd09ab4d17108375ed9ba1e79806bead956b1b279049f04fffd510837a2`  
		Last Modified: Wed, 10 Jun 2026 20:37:22 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d981a5888cdaa4542bb9742e3036d10bdfcdee3a46bf16f2f740e748c87d29`  
		Last Modified: Wed, 10 Jun 2026 20:37:23 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafdcf09af324c010dbe97a959b929e2de7f5b848137759c9078a77d545e4e91`  
		Last Modified: Wed, 10 Jun 2026 20:37:23 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f85cf31dbf1d37dbfc8cce809f20c27245790cf2e09eac59d5eacc3367e73629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6938086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65465c27db89f3bdd2ea4d74090f2f48766ce18f27aba08bc919d6a827f5c42f`

```dockerfile
```

-	Layers:
	-	`sha256:c854e010d4b263a5583142b7233f8d99785605ba8f0f50bd513858a6663f83e6`  
		Last Modified: Wed, 10 Jun 2026 20:37:20 GMT  
		Size: 671.0 KB (670955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18d8ba9481c1d82c8054a86aad38784b3d3b7400046ded129c7a8a1ed4277ac5`  
		Last Modified: Wed, 10 Jun 2026 20:37:21 GMT  
		Size: 3.2 MB (3180918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5763d36c7ee20e57cfe24d91fc67be83d80c20058b6d60babaf8aa5cd651a8b0`  
		Last Modified: Wed, 10 Jun 2026 20:37:21 GMT  
		Size: 3.0 MB (3025838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2d511c6df8ac0f53f0365cfd25759d284d0a31ab40cb925aec70784f15edf4`  
		Last Modified: Wed, 10 Jun 2026 20:37:20 GMT  
		Size: 60.4 KB (60375 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:f19a5635439c8dbe39aa8bcd2d57ad818c310855fa47a3be3574e42122196b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79255335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16b46ecee60f949ecf87ad168e625a205aeca5d24874dc762a83b514ab0cebb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 23:32:07 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 09 Jun 2026 23:32:07 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 09 Jun 2026 23:32:07 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 09 Jun 2026 23:32:08 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 09 Jun 2026 23:32:08 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 23:32:08 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 09 Jun 2026 23:32:19 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 09 Jun 2026 23:32:19 GMT
ENV RABBITMQ_VERSION=4.3.1
# Tue, 09 Jun 2026 23:32:19 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 09 Jun 2026 23:32:19 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 09 Jun 2026 23:32:19 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 23:32:59 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 09 Jun 2026 23:33:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 09 Jun 2026 23:33:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 09 Jun 2026 23:33:09 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 09 Jun 2026 23:33:09 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 09 Jun 2026 23:33:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 09 Jun 2026 23:33:09 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 09 Jun 2026 23:33:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 09 Jun 2026 23:33:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jun 2026 23:33:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 23:33:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 09 Jun 2026 23:33:09 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32d98821fd9c6305584b9f552ee554e71be7d18e2f5e8519e5d8088a4974db5`  
		Last Modified: Tue, 09 Jun 2026 23:38:58 GMT  
		Size: 37.5 MB (37522812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5193be1d56ffd66341524dacbcb52fa0a97e603f0611eccb39f8c3f66a18b4e3`  
		Last Modified: Tue, 09 Jun 2026 23:38:52 GMT  
		Size: 10.8 MB (10796143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5758ddb2459059fc3469198bf8296c1f3624ed3257c9a6ce75e6bb99927453`  
		Last Modified: Tue, 09 Jun 2026 23:38:47 GMT  
		Size: 1.4 MB (1449503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a724af5b6c215f6bd2bd85a4819cff31d357ab4e4ae5d547e11e157f7fb350`  
		Last Modified: Tue, 09 Jun 2026 23:38:57 GMT  
		Size: 25.9 MB (25897473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0990d252c22ca662af8dc3a303e6328f64cbc94a776ee5c775d34be65c2826b3`  
		Last Modified: Tue, 09 Jun 2026 23:38:50 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9fe936a6664094f7b721876c043b193dfcf99550b7044b06c8730efb5111c8`  
		Last Modified: Tue, 09 Jun 2026 23:38:52 GMT  
		Size: 105.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8409800a0b30afe968e71e3be16bd101e5631802a6555f25fcaf2c54a87ef9`  
		Last Modified: Tue, 09 Jun 2026 23:38:54 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e78a32330f92fad488ef108a6b8557a404b792d7390ca4d827b76ec99ccf46`  
		Last Modified: Tue, 09 Jun 2026 23:38:54 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d42379f067f7288eae4cb928d9e4ec5e188eff7cd7eb26f980f96c53aa4d5c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7017283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7023feb5ec3099108be7288db8a222fb9de392289f197e48a6d00a7c1be4aed`

```dockerfile
```

-	Layers:
	-	`sha256:46024c7b7c686812056d11c726a9f3e846c4f9602acf402799fbfce51c495590`  
		Last Modified: Tue, 09 Jun 2026 23:38:48 GMT  
		Size: 673.9 KB (673918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8271eb5ac73dd1ff6e1b2f45a56355d4c860f17ef8fde0e4e3b505c55e91b539`  
		Last Modified: Tue, 09 Jun 2026 23:38:49 GMT  
		Size: 3.2 MB (3219019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c1391d62e2706ea5c0a57f5de6caae827fbf0e7ad27f3a9f3b00f699df1af81`  
		Last Modified: Tue, 09 Jun 2026 23:38:48 GMT  
		Size: 3.1 MB (3063965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:556b4d50489a4e91cae21461515d06dc578b589c17c344340d5cda1f005e074f`  
		Last Modified: Tue, 09 Jun 2026 23:38:46 GMT  
		Size: 60.4 KB (60381 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:c580bda8b9e1aa0291f65d9b19124f1591dc0d173b5ba0dc8e07e5dad123c4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73437866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f69983632a1ddb4d19596e102d831be1351525f9efb47d9d56685299cfdc8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:43:51 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Jun 2026 20:43:51 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Jun 2026 20:43:51 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Jun 2026 20:43:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Jun 2026 20:43:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:43:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Jun 2026 20:43:55 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Jun 2026 20:43:55 GMT
ENV RABBITMQ_VERSION=4.3.1
# Wed, 10 Jun 2026 20:43:55 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Jun 2026 20:43:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Jun 2026 20:43:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:44:06 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Jun 2026 20:44:08 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Jun 2026 20:44:08 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Jun 2026 20:44:08 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Jun 2026 20:44:08 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Jun 2026 20:44:08 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Jun 2026 20:44:08 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Wed, 10 Jun 2026 20:44:08 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Jun 2026 20:44:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:44:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 20:44:08 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Jun 2026 20:44:08 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4fe59431b7df178eeb572ae0e0576aadaf2c6e13988afef7cc32ca99983a53`  
		Last Modified: Wed, 10 Jun 2026 20:44:41 GMT  
		Size: 33.9 MB (33946334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83d29aac9a1f9d7c2303091c6e216d7709a17fb21c49686aa1d329d5350f52c`  
		Last Modified: Wed, 10 Jun 2026 20:44:40 GMT  
		Size: 8.4 MB (8350147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf8079df51f2de0bc2b2ed42ec8dd3bed384ba4ac2250705108c9056d3cafdf`  
		Last Modified: Wed, 10 Jun 2026 20:44:39 GMT  
		Size: 1.5 MB (1515528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af4aa0e834b89fb9325b0822ca11ff697dd56dc08e37691bbc9d01f4414cba8`  
		Last Modified: Wed, 10 Jun 2026 20:44:40 GMT  
		Size: 25.9 MB (25897568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9021c2df996a28780bcd4612396e04543770a2fa508c5387bf671521b3d28422`  
		Last Modified: Wed, 10 Jun 2026 20:44:40 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c60b956945ca778fc61b66bea875ca3877c35f2b3858b4f93bae2e33370d971`  
		Last Modified: Wed, 10 Jun 2026 20:44:41 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c252ce5b2e53063683814cfe2406613c747e2e1ec34594e5718608c2db557c3`  
		Last Modified: Wed, 10 Jun 2026 20:44:42 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d83063d6c0be1dac36134fc0db87e268af1f29abab15804f65780854e5d87d`  
		Last Modified: Wed, 10 Jun 2026 20:44:42 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6bf3cc03fc2eef089b445f0a8326f0a193a4aebb5b250f9e0034ff5f913c933b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6714468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4613d179dfbd1997384e765116ec08e03e02eb9df3ca4dcacbe2c67b6d8e2640`

```dockerfile
```

-	Layers:
	-	`sha256:95687c7d65b2a05994fd677923c4baa8775f556971cf79b39f69787e74c5f298`  
		Last Modified: Wed, 10 Jun 2026 20:44:39 GMT  
		Size: 670.9 KB (670921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ab22d99729d45a280ca561baf91300381655cf4b8512bdbd538c166c1c677a9`  
		Last Modified: Wed, 10 Jun 2026 20:44:39 GMT  
		Size: 3.1 MB (3069142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3edd4fc662255da5dd00734b0cd6331c624c5cb0915c79fe1600d19464f2d7a`  
		Last Modified: Wed, 10 Jun 2026 20:44:39 GMT  
		Size: 2.9 MB (2914092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08145eab572b311033bd379faddff130f476611f143b16c8b8c8ff87a15831aa`  
		Last Modified: Wed, 10 Jun 2026 20:44:39 GMT  
		Size: 60.3 KB (60313 bytes)  
		MIME: application/vnd.in-toto+json
