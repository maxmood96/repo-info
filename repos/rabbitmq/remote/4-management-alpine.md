## `rabbitmq:4-management-alpine`

```console
$ docker pull rabbitmq@sha256:304c771246b261babf09677f27b82c99b5c05330b0e8c73fcc133498cb021aec
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

### `rabbitmq:4-management-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:3ccebd72e620fc7483a8d95da422b3784b3096934f62796a48b4a1482e9386b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97159415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7d038ca2763a266df4c8b5164ad6cb0d4ae18d6aa1b0fa0591c567418586c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:33:48 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 14 Nov 2025 17:33:48 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 14 Nov 2025 17:33:48 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 14 Nov 2025 17:33:48 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 14 Nov 2025 17:33:48 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:33:48 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:33:51 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 14 Nov 2025 17:33:51 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 14 Nov 2025 17:33:51 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 14 Nov 2025 17:33:51 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 14 Nov 2025 17:33:51 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:33:56 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 14 Nov 2025 17:33:57 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 14 Nov 2025 17:33:57 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 14 Nov 2025 17:33:57 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:33:57 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 14 Nov 2025 17:33:57 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 14 Nov 2025 17:33:57 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 14 Nov 2025 17:33:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:33:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:33:57 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 14 Nov 2025 17:33:57 GMT
CMD ["rabbitmq-server"]
# Fri, 14 Nov 2025 17:48:05 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 14 Nov 2025 17:48:05 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169f34d1fa32d09df2c2525969cf69ae27efb3f47900085529bd22c63b13cd0b`  
		Last Modified: Fri, 14 Nov 2025 17:34:26 GMT  
		Size: 42.9 MB (42857516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ccb0591298dda9af032cc572d2fa223cb3020f72c85062bed542fcab933375`  
		Last Modified: Fri, 14 Nov 2025 17:34:23 GMT  
		Size: 9.1 MB (9143912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6899f0b97deeab7804f52df3bbc1683e1ba3fc2c184e1f274c19b6dec37702b6`  
		Last Modified: Fri, 14 Nov 2025 17:34:22 GMT  
		Size: 2.4 MB (2374328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb11cb2aaa848287d04cc4497e7bddcfa7f7baf51b08cb528b6e6d9f23901cb`  
		Last Modified: Fri, 14 Nov 2025 17:34:24 GMT  
		Size: 25.3 MB (25266366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d381b26ba458a6983ade58e1183a662d146c7b32a794f7c02fafcaae935d280`  
		Last Modified: Fri, 14 Nov 2025 17:34:22 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690361d9d1bc97ba917286e612a6e819dcd3c383a62b55ee9bd05231741e2dd9`  
		Last Modified: Fri, 14 Nov 2025 17:34:22 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0876231dd8718902fcc59c201d55cbe8b7752cea7a58516f7dc2caf5f7a86870`  
		Last Modified: Fri, 14 Nov 2025 17:34:22 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b268f423b21de86527ef0e4782d2b0dd7878c2e7037d607a16dbe8d0a0d3b5`  
		Last Modified: Fri, 14 Nov 2025 17:34:22 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb58d9b934f2000bf69be57689bc64539c1d4b69c2f811f17ffc7f1e4955c428`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 13.7 MB (13713091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3bca32d72c4e868c068adc54aec793bbbd08f55c91f11e8662e67dcf561c266a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1661184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf4004ac7a52561bfa8a4d7b28b44d6bd638786105b379c85826527d8816537`

```dockerfile
```

-	Layers:
	-	`sha256:8de59703f26824b720f9dd2f4da0452941f113dfe39d7dba7f3228ef4444de41`  
		Last Modified: Fri, 14 Nov 2025 19:53:47 GMT  
		Size: 1.7 MB (1650004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14b747af92f2178a140f669ce06ce29b8f32d6740c2b570ce104511d9fc602e6`  
		Last Modified: Fri, 14 Nov 2025 19:53:48 GMT  
		Size: 11.2 KB (11180 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:6b2457f083159cd0005754bee324872999ef03689319d159245f0932cee45d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85729806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb8ffed8a17f20b1010babeaea701c1d5e8e519979219d29576f32fc9b2b1c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:31:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 14 Nov 2025 17:31:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 14 Nov 2025 17:31:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 14 Nov 2025 17:31:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 14 Nov 2025 17:31:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:31:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:31:32 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 14 Nov 2025 17:31:32 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 14 Nov 2025 17:31:32 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 14 Nov 2025 17:31:32 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 14 Nov 2025 17:31:32 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:31:41 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 14 Nov 2025 17:31:43 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 14 Nov 2025 17:31:43 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 14 Nov 2025 17:31:43 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:31:43 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 14 Nov 2025 17:31:43 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 14 Nov 2025 17:31:43 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 14 Nov 2025 17:31:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:31:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:31:43 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 14 Nov 2025 17:31:43 GMT
CMD ["rabbitmq-server"]
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed656272cb1dc7876328e857f93d6aee0a618eb48328b850d289a9c708e747c8`  
		Last Modified: Fri, 14 Nov 2025 17:32:04 GMT  
		Size: 33.4 MB (33447709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ded828e604fcc5de0d84b626aefeda8862523f8ae339aba31e96e48a5767306`  
		Last Modified: Fri, 14 Nov 2025 17:32:02 GMT  
		Size: 7.8 MB (7788825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465a15a4e03d29a4a6ef8b34eaa84a1dc1d29670ba3cebfec4790efdc652f921`  
		Last Modified: Fri, 14 Nov 2025 17:32:02 GMT  
		Size: 1.3 MB (1330050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516cc515fdf05269b3aeca9b16671f166d39e5423d3e9f4b4cad83de6db10e47`  
		Last Modified: Fri, 14 Nov 2025 17:32:05 GMT  
		Size: 25.3 MB (25266224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cc7cfe5078d0f43ae9e10ce48ff6725e6bb4bd8ce4b982e3ae00d9434f6461`  
		Last Modified: Fri, 14 Nov 2025 17:32:02 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd7344ec4dfb2afa0b0cf0c0607ef11c30e8cdedd4bc3e05eadd0ffc83277bd`  
		Last Modified: Fri, 14 Nov 2025 17:32:02 GMT  
		Size: 107.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f144ed3e0eb033f6e7ab7deed990830436ff4f143bdf37b0b206990eb64fd1c`  
		Last Modified: Fri, 14 Nov 2025 17:32:02 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d6d48073fa53fe3bc1846da0f6ee7d8a7b3b5b69440ec1077d13a7454dc7de`  
		Last Modified: Fri, 14 Nov 2025 17:32:02 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0e9c7864832561efd8480aa9bb03e4d88c820f8624713f11ef3fce24a264a4`  
		Last Modified: Fri, 14 Nov 2025 17:42:56 GMT  
		Size: 14.4 MB (14391177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3991cd14cc72a05806c31cfedeec2731548ae8e896a3a32167a077f52706820c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 KB (11045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffa6c638a27af9287050f781a86bc4e2eb309db98cd9f68b7d2992047a65f63`

```dockerfile
```

-	Layers:
	-	`sha256:ce97412392db25b28c7cdaf669e365a0440d3b51d996c19cc5c616fae08005f8`  
		Last Modified: Fri, 14 Nov 2025 19:57:05 GMT  
		Size: 11.0 KB (11045 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:8a0baaae6d04d470c9d893f4b331058df39db408614bc62950f87d23d9f141cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84557935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa32aa501ba2ed2347689d7f5af6e8649682e7c68d4c3e453d341a02e6ce5c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:31:24 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 14 Nov 2025 17:31:24 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 14 Nov 2025 17:31:24 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 14 Nov 2025 17:31:24 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 14 Nov 2025 17:31:24 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:31:24 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:31:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 14 Nov 2025 17:31:26 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 14 Nov 2025 17:31:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 14 Nov 2025 17:31:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 14 Nov 2025 17:31:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:31:33 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 14 Nov 2025 17:31:34 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 14 Nov 2025 17:31:34 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 14 Nov 2025 17:31:34 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:31:34 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 14 Nov 2025 17:31:34 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 14 Nov 2025 17:31:34 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 14 Nov 2025 17:31:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:31:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:31:34 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 14 Nov 2025 17:31:34 GMT
CMD ["rabbitmq-server"]
# Fri, 14 Nov 2025 17:45:38 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 14 Nov 2025 17:45:38 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27fdc18a754f52bc62b30b3b7999afa90c1e0e052e14967b9c7c03783b96d5e`  
		Last Modified: Fri, 14 Nov 2025 17:32:11 GMT  
		Size: 33.4 MB (33392521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba82da88e82ba71f89e084767eafbd253e24c68debd0f74021baa55ffae1fa89`  
		Last Modified: Fri, 14 Nov 2025 17:32:08 GMT  
		Size: 7.4 MB (7390626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19047886b37b4dde251adf7f4ec4379f49331f598f7227090ef63ad9433acff`  
		Last Modified: Fri, 14 Nov 2025 17:32:08 GMT  
		Size: 1.2 MB (1227065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d86125be362278d970e7cbaf406fadcfa16e06b7ab1b76381eeb1234dab30f`  
		Last Modified: Fri, 14 Nov 2025 17:32:11 GMT  
		Size: 25.3 MB (25265893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce8239dded45a104f17aaaa26f64e9172f7eb990edfbd6d27d29dbf321685d7`  
		Last Modified: Fri, 14 Nov 2025 17:32:08 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18eaa53e10230e50f6116389edd1095730cc727fba6486e4dbcfc39ed2878c2e`  
		Last Modified: Fri, 14 Nov 2025 17:32:08 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67fe2a88316f07ab6360071d8334f8967ffc318a48c2ac2f00edba4113b25ae`  
		Last Modified: Fri, 14 Nov 2025 17:32:08 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480a8166515d2cda65adff11344ccab60fab1503baebd93902759c9ff931334a`  
		Last Modified: Fri, 14 Nov 2025 17:32:08 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1127afb9b350da12bbeb01be46b4f637102abdce546b7d673e6304adc6496a6`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 14.1 MB (14058529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f6006002894c8db71864b8665891dc96283b1c48f363a0f94581fb7dacf5a4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1662293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfde77f77979b1eaf673966dfcbb53735cdf6b140c5d172c280e8b716b45402d`

```dockerfile
```

-	Layers:
	-	`sha256:f8a2c1f1a16c4207a0f132bae2b517c5ff0003922b1f0398fce5b649eb9766bc`  
		Last Modified: Fri, 14 Nov 2025 19:57:09 GMT  
		Size: 1.7 MB (1651035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b5262a32b568fa20e094e5d1300c662751344f2edfb072efbf90322b7b1bb3e`  
		Last Modified: Fri, 14 Nov 2025 19:57:10 GMT  
		Size: 11.3 KB (11258 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:168b832c3922bebd0839064e88eb498399e6866132bcef9e02f91ea556bcee84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96254878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e379b3effb75587780a6e6569bcfc2696845811bc75d672359e35d2877180783`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:34:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 14 Nov 2025 17:34:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 14 Nov 2025 17:34:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 14 Nov 2025 17:34:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 14 Nov 2025 17:34:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:34:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:34:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 14 Nov 2025 17:34:30 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 14 Nov 2025 17:34:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 14 Nov 2025 17:34:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 14 Nov 2025 17:34:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:34:36 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 14 Nov 2025 17:34:37 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 14 Nov 2025 17:34:37 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 14 Nov 2025 17:34:37 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:34:37 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 14 Nov 2025 17:34:37 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 14 Nov 2025 17:34:37 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 14 Nov 2025 17:34:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:34:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:34:37 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 14 Nov 2025 17:34:37 GMT
CMD ["rabbitmq-server"]
# Fri, 14 Nov 2025 17:47:04 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 14 Nov 2025 17:47:04 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5429a8626360c369da06b60ba474d0992bd0510d0d397a1641032d0867c120`  
		Last Modified: Fri, 14 Nov 2025 17:35:16 GMT  
		Size: 40.9 MB (40854521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f6c6346d45df30a18f734896524081c0be42972cc23a2c4f08b76712be6f4f`  
		Last Modified: Fri, 14 Nov 2025 17:35:13 GMT  
		Size: 9.8 MB (9824246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd216a74f292f49e79bfc5035abcc53d33c2c4ab5f9d4e1d520affa44834f814`  
		Last Modified: Fri, 14 Nov 2025 17:35:11 GMT  
		Size: 2.4 MB (2424771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137f0949950d3e817602c2faacd97aa8660923f1a147811d3ae4a9d441869166`  
		Last Modified: Fri, 14 Nov 2025 17:35:15 GMT  
		Size: 25.3 MB (25266408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47249f4d73665ba6f0a6fdeebefbb35d5a404df99a8d87855e25043dcdb7d96`  
		Last Modified: Fri, 14 Nov 2025 17:35:11 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b60687c7142c3fa63bdd26dd10ce35d8c3931580a14e2ca98865ff7f34b25e`  
		Last Modified: Fri, 14 Nov 2025 17:35:11 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ada3ecfcd6a46fbcfd5560f83d7247995f0a74d6e82fb9a46144705c617c6f`  
		Last Modified: Fri, 14 Nov 2025 17:35:11 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fced45be321a9f78764c287d764e0f11ff7cbd9ad72f552779d61e2c2cd868e`  
		Last Modified: Fri, 14 Nov 2025 17:35:12 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261041ae4dc5f065f584f9a997955b86cebf0eca2865c85ee4e55976b308f44f`  
		Last Modified: Fri, 14 Nov 2025 17:47:19 GMT  
		Size: 13.7 MB (13745116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a500b7c0e99f8ac35a4ab2532c52e94494c336e8b276e99d29d302c5023397af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1662167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a073ff2c34ddb446be14d53cf2cb7bcee9258231a6e785e1814db03eb6adbc09`

```dockerfile
```

-	Layers:
	-	`sha256:688e9aaa1caae173eef780b3b99187d323ba1d0bbd0eb9e70216a11f9d4dfb1e`  
		Last Modified: Fri, 14 Nov 2025 19:57:14 GMT  
		Size: 1.7 MB (1650883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe1715cf89dd5341da8e970bd467b9af612c510966df0632b499ba71a078885c`  
		Last Modified: Fri, 14 Nov 2025 19:57:16 GMT  
		Size: 11.3 KB (11284 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:9cc7d5ae423f6864c2edb8943a558cc17ef8ca02d41b314beaff1eb952969435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88146694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1373e8b608c2db926a10a644f4a7d7c7d1718e9acb8dcf316160f8e0b0ded8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:31:11 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 14 Nov 2025 17:31:11 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 14 Nov 2025 17:31:11 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 14 Nov 2025 17:31:11 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 14 Nov 2025 17:31:11 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:31:11 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:31:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 14 Nov 2025 17:31:14 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 14 Nov 2025 17:31:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 14 Nov 2025 17:31:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 14 Nov 2025 17:31:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:31:19 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 14 Nov 2025 17:31:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 14 Nov 2025 17:31:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 14 Nov 2025 17:31:20 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:31:20 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 14 Nov 2025 17:31:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 14 Nov 2025 17:31:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 14 Nov 2025 17:31:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:31:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:31:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 14 Nov 2025 17:31:20 GMT
CMD ["rabbitmq-server"]
# Fri, 14 Nov 2025 17:47:47 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 14 Nov 2025 17:47:47 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d778ac831077e85bc0b5aaabf6165be63631f84743d6e12a8a865e0da744bc`  
		Last Modified: Fri, 14 Nov 2025 17:31:52 GMT  
		Size: 33.5 MB (33537206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c8c6febe1e5ba8d5aca319dd7c12c9854d0b4f3b07699a3b3e830112c4422e`  
		Last Modified: Fri, 14 Nov 2025 17:31:50 GMT  
		Size: 9.2 MB (9159109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b68032e45f83d7244514d8c39109829659b7a2d038c31366f204b6e42a6f8a`  
		Last Modified: Fri, 14 Nov 2025 17:31:49 GMT  
		Size: 1.3 MB (1332478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e73addeeab1afe20941b41b9d395a784f66a2225a35436b0e96db31ef9b42d`  
		Last Modified: Fri, 14 Nov 2025 17:31:52 GMT  
		Size: 25.3 MB (25265745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f432f4bfabaf69eed93c0b3b93adaa6d6094b24ec0651524db036a9f15823d`  
		Last Modified: Fri, 14 Nov 2025 17:31:49 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35fb893f9bc7a00859b4a6a52d0127531c87533919c418bd58b470ba1d7b857`  
		Last Modified: Fri, 14 Nov 2025 17:31:49 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d7b5882c41968bddf918ac09d78936b71bfa4f02f8fa352232c14eff38f1a7`  
		Last Modified: Fri, 14 Nov 2025 17:31:49 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5374b6efa56b7f268cbd7a8296421bb215cec6b562ca5251d390340d0ca1a72`  
		Last Modified: Fri, 14 Nov 2025 17:31:49 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4d63e41aff9ca49fefb9f554aa7b28d17b3d8de5924e4459ed8151b2e7c963`  
		Last Modified: Fri, 14 Nov 2025 17:48:02 GMT  
		Size: 15.2 MB (15231479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f585dced6364ad50f0d954306a80849cbc37fcf15cb51d95dd8695a14f504308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1660955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f2f75f6637d73cb84a1b6dc8dead3754ad955d005fed6bbd83f6693247ca2d`

```dockerfile
```

-	Layers:
	-	`sha256:c23826e3ccfde63e0978bed0ff4ba171c179df3753f86ac331557c2ca4762ec7`  
		Last Modified: Fri, 14 Nov 2025 19:57:20 GMT  
		Size: 1.6 MB (1649807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a38d5cf60b8b94af9feb52f841cdf2ea4ed7c4605a9b58b3517085a81f393f1`  
		Last Modified: Fri, 14 Nov 2025 19:57:21 GMT  
		Size: 11.1 KB (11148 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:856d39672d941aa1375ddde974ae634c6c776ec6877015dcc5cf1c07e4b25d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89544605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5802c7e50e4840f00db0cc224cc114aec7f5ab8cf8448998492ea1054509b9eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:14:42 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 14 Nov 2025 19:14:42 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 14 Nov 2025 19:14:42 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 14 Nov 2025 19:14:43 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 14 Nov 2025 19:14:43 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 19:14:43 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 14 Nov 2025 19:14:47 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 14 Nov 2025 19:14:47 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 14 Nov 2025 19:14:47 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 14 Nov 2025 19:14:47 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 14 Nov 2025 19:14:47 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 19:14:57 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 14 Nov 2025 19:15:02 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 14 Nov 2025 19:15:02 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 14 Nov 2025 19:15:02 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 14 Nov 2025 19:15:02 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 14 Nov 2025 19:15:02 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 14 Nov 2025 19:15:03 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 14 Nov 2025 19:15:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:15:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:15:04 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 14 Nov 2025 19:15:04 GMT
CMD ["rabbitmq-server"]
# Fri, 14 Nov 2025 20:10:17 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 14 Nov 2025 20:10:17 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaa900e9d6ef3065872bc442df1a96294cc331aafa72563993a7cbc9248e799`  
		Last Modified: Fri, 14 Nov 2025 19:15:53 GMT  
		Size: 33.9 MB (33928492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc4e1eec0ae82c73bec5eddf8d6bd090fc1bbc1bab910a01b6fb17f3bee11d6`  
		Last Modified: Fri, 14 Nov 2025 19:15:51 GMT  
		Size: 9.8 MB (9774080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9494003fd5d13a10f29866599f6b08e4fa4c468ed3e29dfef022619deddd86cf`  
		Last Modified: Fri, 14 Nov 2025 19:15:50 GMT  
		Size: 1.5 MB (1452640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81eed9c7bcfde4baca5e1a186936e910f21bb245ecd228e7b0d6b1ee996ac0d7`  
		Last Modified: Fri, 14 Nov 2025 19:15:52 GMT  
		Size: 25.3 MB (25265887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9897e4ac50b15888563d086090bf67ba7c8963b04b466a3fdef5b592771b231e`  
		Last Modified: Fri, 14 Nov 2025 19:15:50 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a63647a1fb7f337637f2323d87ea43974b30fbed30abb83f4241ede1b361443`  
		Last Modified: Fri, 14 Nov 2025 19:15:50 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafb94f92bfccf368ec8db779fd191e34f931e94a169219c6e9846278c45bc6b`  
		Last Modified: Fri, 14 Nov 2025 19:15:50 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b51b8b2f3f7e447b305465104113d8f525884315041e2b22109f4ba8773d47`  
		Last Modified: Fri, 14 Nov 2025 19:15:50 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9a7409bd8d783b255ec081c1e39e6efcfc809ec2f2fa84d1f3f094fbcd68c0`  
		Last Modified: Fri, 14 Nov 2025 20:11:03 GMT  
		Size: 15.4 MB (15389513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0f412b58477a0a5eb3245f7e20e20a814d2756a351a7913a7107744f9be69b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1660478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf14cc907bb2b91b9e5fe00309f2964726a2c4b6b4b69a2779cf7ccb10c66d2`

```dockerfile
```

-	Layers:
	-	`sha256:0ad6755f6c7b7fb2d746d3e3865e0ccfbe00fdfe9738a88ad8e81a58ba2c3cec`  
		Last Modified: Fri, 14 Nov 2025 22:53:10 GMT  
		Size: 1.6 MB (1649254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1a68aa63df21a5639ca6bf3954ad878a366f12a80dfc9522fdd630e6020e20`  
		Last Modified: Fri, 14 Nov 2025 22:53:11 GMT  
		Size: 11.2 KB (11224 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:2b618a3613de278e4a2aeed47fb715f02d955121fd523b67228b63cc08abbda8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90815024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef49b483d1e0aaeb0a719216731cb2f136031b8d4d372976418cf5a7d83e5c8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 15 Nov 2025 12:40:37 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 15 Nov 2025 12:40:37 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 15 Nov 2025 12:40:37 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 15 Nov 2025 12:40:38 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 15 Nov 2025 12:40:38 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 12:40:38 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 15 Nov 2025 12:40:51 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 15 Nov 2025 12:40:51 GMT
ENV RABBITMQ_VERSION=4.2.0
# Sat, 15 Nov 2025 12:40:51 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 15 Nov 2025 12:40:51 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 15 Nov 2025 12:40:51 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 17:16:34 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 15 Nov 2025 17:16:43 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 15 Nov 2025 17:16:43 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 15 Nov 2025 17:16:43 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 15 Nov 2025 17:16:43 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 15 Nov 2025 17:16:43 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 15 Nov 2025 17:16:43 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 15 Nov 2025 17:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 15 Nov 2025 17:16:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 15 Nov 2025 17:16:43 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 15 Nov 2025 17:16:43 GMT
CMD ["rabbitmq-server"]
# Sat, 15 Nov 2025 23:31:36 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Sat, 15 Nov 2025 23:31:36 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e59a1c1b9f6e68d2e81dfe93f128277d090e8d42bb80d9fdce1bd0812253e90`  
		Last Modified: Sat, 15 Nov 2025 12:47:29 GMT  
		Size: 34.9 MB (34892992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b82b64d03f44428bb7c7c84bc38b196743066f1c2cd8073fa6e2958a1f2364`  
		Last Modified: Sat, 15 Nov 2025 12:47:25 GMT  
		Size: 10.9 MB (10906598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445ba2528747173700141a982a31baa29e2bb537c0faf37187397c5cef3d8ac0`  
		Last Modified: Sat, 15 Nov 2025 12:47:24 GMT  
		Size: 1.4 MB (1366487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fcfbfdf817325087e5b054832afb3382b82a30a05a55e24a8a67e61b5f958b3`  
		Last Modified: Sat, 15 Nov 2025 18:35:28 GMT  
		Size: 25.3 MB (25266204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f190a5d7ea9c656538c8316e1d5feeb079e1b2a4817a443a03d3e692536cd176`  
		Last Modified: Sat, 15 Nov 2025 18:35:23 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7938067cb2802b62ef50b714975ca45c022b0b9ca5e9f39763dc8de7c5eb308`  
		Last Modified: Sat, 15 Nov 2025 18:35:23 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60db8887d6a4b582f83e414ada73f983e6807fad96b7e3824b2cd0644a4dbcd7`  
		Last Modified: Sat, 15 Nov 2025 18:35:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e41671b6eadfcf1aab785dfcc8a728fba2486ad19e7511954115e736579c8dc`  
		Last Modified: Sat, 15 Nov 2025 18:35:23 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b283198c250bfc9cf0398f9f94a2ffdc029707d6ff6b040112f398346b643938`  
		Last Modified: Sat, 15 Nov 2025 23:33:08 GMT  
		Size: 14.9 MB (14865758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fe82591c36b5ee150cc3096e8c33d84dcb0cbd720b590fac8e4429d900ecd7cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1662089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4222fc5177a3742ece3a264bab8e88225c9b7c1e3985685cd88e8ca8ea697fcb`

```dockerfile
```

-	Layers:
	-	`sha256:9b351cd9ab2036e9a9a8125f2d4428c18f370dda6eaf69597fa8eba26744e239`  
		Last Modified: Sun, 16 Nov 2025 01:52:52 GMT  
		Size: 1.7 MB (1650863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16408f57a2202452fb95109bf9b64e1525913df761e714b7f4c3082ddc5d4515`  
		Last Modified: Sun, 16 Nov 2025 01:52:53 GMT  
		Size: 11.2 KB (11226 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:cb36d30aa1bad30e5ae0e9c9b5eaf0f3a4682c243a3976a1a22ad1d39150dc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88054985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f1e27d1e3f84eed1b945ce071451be54f9889a8e3e7df549cacb561ff6183f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:32:33 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 14 Nov 2025 17:32:33 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 14 Nov 2025 17:32:33 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 14 Nov 2025 17:32:33 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 14 Nov 2025 17:32:33 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:32:33 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:32:36 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 14 Nov 2025 17:32:36 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 14 Nov 2025 17:32:36 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 14 Nov 2025 17:32:36 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 14 Nov 2025 17:32:36 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:32:43 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 14 Nov 2025 17:32:43 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 14 Nov 2025 17:32:43 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 14 Nov 2025 17:32:43 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:32:43 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 14 Nov 2025 17:32:43 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 14 Nov 2025 17:32:44 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 14 Nov 2025 17:32:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:32:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:32:44 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 14 Nov 2025 17:32:44 GMT
CMD ["rabbitmq-server"]
# Fri, 14 Nov 2025 18:00:14 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 14 Nov 2025 18:00:14 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf19dc786e7146ac66f96833a9722c5bc83d7ddc7799ab6e6f8872ac24ad163`  
		Last Modified: Fri, 14 Nov 2025 17:33:23 GMT  
		Size: 34.0 MB (33963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cc957cadda9e73e64de07d656462cb108e148515232cbc504b1a8ff8af5678`  
		Last Modified: Fri, 14 Nov 2025 17:33:22 GMT  
		Size: 8.3 MB (8347174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8c2fb2646dac35cf3ca4279dce3c3af62715ef5a7d8541e9faf78b85cd28d3`  
		Last Modified: Fri, 14 Nov 2025 17:33:21 GMT  
		Size: 1.4 MB (1430636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c52cb498814d9bfca9239abbfcdd43f990e8fb7cc0e1746c66ad9279b2602a0`  
		Last Modified: Fri, 14 Nov 2025 17:33:22 GMT  
		Size: 25.3 MB (25265972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3710775f6190416be4998c5e1d12702f1f17aa01c9ed2e995c6974d3ab4394dc`  
		Last Modified: Fri, 14 Nov 2025 17:33:21 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829c6233ecb1ad517b3ee4d373872530e7760d6db6cc6cf85b8b5936b749a6a3`  
		Last Modified: Fri, 14 Nov 2025 17:33:20 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9660d2439b58a6f430843848111550ce1cf7d960686c49a085502d5d011184`  
		Last Modified: Fri, 14 Nov 2025 17:33:20 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5507e2da10dbba82e8da8e856f93d94264dce7593ca0c082bd2adb498e9e3b`  
		Last Modified: Fri, 14 Nov 2025 17:33:21 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625a219f5b218d357587cff11feee6075c5df85e6657eb080e1505b1a909c4a6`  
		Last Modified: Fri, 14 Nov 2025 18:00:53 GMT  
		Size: 15.4 MB (15396501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ea523eac6d893d0959f2991ecb3f91c7aa77d218cd18d0c6e0838bc8f4a917d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1659884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4918f7f4d5bb1767250b1a256a7f12ce0ba53cfb72c7ab10c9a3f05a4423b82`

```dockerfile
```

-	Layers:
	-	`sha256:172d029bea6bd3f274c5a1879dbaf244d42a87689e0b01a3ff2f648788d52572`  
		Last Modified: Fri, 14 Nov 2025 19:57:30 GMT  
		Size: 1.6 MB (1648704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef5aac2244755d7dea2f1be766581bcd92a44affc9d176eaa6397864d788675d`  
		Last Modified: Fri, 14 Nov 2025 19:57:31 GMT  
		Size: 11.2 KB (11180 bytes)  
		MIME: application/vnd.in-toto+json
