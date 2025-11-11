## `rabbitmq:3-management-alpine`

```console
$ docker pull rabbitmq@sha256:0c64ec4fc5596406d755dcca75e8a3b618192cc5fb69f8f0340f06290b1cc08c
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

### `rabbitmq:3-management-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:e7fff3a44d75e9a3d361e5bb61ef6997c04c87ba93ba7d80b67502d135046812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (85988254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d906574d31c75ab12a468948aac46e5acd323f1856c0d003bc532a27c79cf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 19:34:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 10 Nov 2025 19:34:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 10 Nov 2025 19:34:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 10 Nov 2025 19:34:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 10 Nov 2025 19:34:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:34:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:34:52 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 10 Nov 2025 19:34:52 GMT
ENV RABBITMQ_VERSION=3.13.7
# Mon, 10 Nov 2025 19:34:52 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 10 Nov 2025 19:34:52 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 10 Nov 2025 19:34:52 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:34:58 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 10 Nov 2025 19:34:59 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 10 Nov 2025 19:34:59 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 10 Nov 2025 19:34:59 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:34:59 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 10 Nov 2025 19:34:59 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 10 Nov 2025 19:34:59 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 10 Nov 2025 19:34:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:34:59 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 10 Nov 2025 19:34:59 GMT
CMD ["rabbitmq-server"]
# Mon, 10 Nov 2025 19:51:17 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Mon, 10 Nov 2025 19:51:17 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23323e8c9675781f0d065e44a09936961a5ebb1493b27e4e736fd8bfd05c19b`  
		Last Modified: Mon, 10 Nov 2025 19:35:26 GMT  
		Size: 39.7 MB (39741068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9b9b4a183d519f24a4c49d1aa130039a9600cf27ab534a8c81e504f5d10cc2`  
		Last Modified: Mon, 10 Nov 2025 19:35:24 GMT  
		Size: 7.6 MB (7599185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff34b79c9876b4fbf147afb5ef8d8808d66889c610666603b119a55af7420da`  
		Last Modified: Mon, 10 Nov 2025 19:35:24 GMT  
		Size: 2.4 MB (2374083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16f870390d2194a20aa9c363ad14fe416803fc0841472e7eae9f9d4aa7a7305`  
		Last Modified: Mon, 10 Nov 2025 19:35:29 GMT  
		Size: 18.8 MB (18756726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a51f1aa1d0556c4670ebffef88e9607f685061835d5f16609e311078cfe762e`  
		Last Modified: Mon, 10 Nov 2025 19:35:25 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beee5f766572bd5bcc5fdcd466fb06f0c6eb3845934616abcef80e0375f8314`  
		Last Modified: Mon, 10 Nov 2025 19:35:26 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cc3908ff9696e118b55a9a27cf0eb2cca92d3912e6ea68d0d92852206ddb25`  
		Last Modified: Mon, 10 Nov 2025 19:35:26 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c5c51dc61bebcd6d68a0695cf69d20c1f3f7eb307773c9f1497b575bb9bbb8`  
		Last Modified: Mon, 10 Nov 2025 19:35:27 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a19be838ecdc7e3fdbd85b03930c9a38e1ea18710f7ac4e52a62e35cc2da00`  
		Last Modified: Mon, 10 Nov 2025 19:51:30 GMT  
		Size: 13.7 MB (13712989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3ce12087afe413cef0271c16f6f6a445a8305d7f0956131cdd13385d35b733dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1650381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8035b9b3e9c4801be3a3719d3d0604ff4b8d96968805e33a73418f82ca2dee26`

```dockerfile
```

-	Layers:
	-	`sha256:3618f1ea5389277ef57021beb1010a4c8765f2b33d3012c903ca72ae1824dac6`  
		Last Modified: Mon, 10 Nov 2025 22:53:01 GMT  
		Size: 1.6 MB (1639513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea87cdc546d73810f7347d7ea03daf02f19e4bbac9eda7ee7313c7a5c1fcc821`  
		Last Modified: Mon, 10 Nov 2025 22:53:02 GMT  
		Size: 10.9 KB (10868 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:58d963e75b035102093b8afae13f157e45b266b5e16b50ee8e20fe5cd8309a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75709972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9622ee29a68c3d519259dbc7c37d1f512c92bbfea7f921e6a3599b7d98bc316`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 19:35:34 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 10 Nov 2025 19:35:34 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 10 Nov 2025 19:35:34 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 10 Nov 2025 19:35:34 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 10 Nov 2025 19:35:34 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:35:34 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:35:37 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 10 Nov 2025 19:35:37 GMT
ENV RABBITMQ_VERSION=3.13.7
# Mon, 10 Nov 2025 19:35:37 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 10 Nov 2025 19:35:37 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 10 Nov 2025 19:35:37 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:35:45 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 10 Nov 2025 19:35:46 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 10 Nov 2025 19:35:46 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 10 Nov 2025 19:35:46 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:35:46 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 10 Nov 2025 19:35:46 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 10 Nov 2025 19:35:47 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 10 Nov 2025 19:35:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:35:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:35:47 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 10 Nov 2025 19:35:47 GMT
CMD ["rabbitmq-server"]
# Mon, 10 Nov 2025 19:43:23 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Mon, 10 Nov 2025 19:43:23 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d0a1e9a3b8a5b5c6525d557fb439335bc052a0af7e1a7fcfea39c8eb57d40e`  
		Last Modified: Mon, 10 Nov 2025 19:36:12 GMT  
		Size: 31.3 MB (31301215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbf25bfcac1ebd4d823ac312a9c5ce82a898dcd994618e985f4f130fe81be3b`  
		Last Modified: Mon, 10 Nov 2025 19:36:02 GMT  
		Size: 6.4 MB (6425292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40aac6eb18cc9b5094810e378d48536aa8ee5ca705fa1a4d0b052c83f2adc97`  
		Last Modified: Mon, 10 Nov 2025 19:36:02 GMT  
		Size: 1.3 MB (1329814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513cbc1f2177eb01ff085dae7b061ecac6b1218169877b6d50f8ddbd628ec476`  
		Last Modified: Mon, 10 Nov 2025 19:36:03 GMT  
		Size: 18.8 MB (18756756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9a1353cde6cb28a8292f9c66e7fedc0839ed3233e5a2f03eee5c0a084ee87e`  
		Last Modified: Mon, 10 Nov 2025 19:36:01 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e641d4f96d34da0bc239a83c3ffd49554839823cb0550625ab110a339e68e7c0`  
		Last Modified: Mon, 10 Nov 2025 19:36:01 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212344de9c9daf679a61390dc0e98d3913999085d659a7cb2acfd644f1922dee`  
		Last Modified: Mon, 10 Nov 2025 19:36:01 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b8973bb70ba0c30426533d761bc4aaacfb5c1b007624bc328bbc27fa9647b4`  
		Last Modified: Mon, 10 Nov 2025 19:36:01 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbbbc49396a713c4d2f9314a278e6f484835463c9aae1f9836951ca8c2afd14`  
		Last Modified: Mon, 10 Nov 2025 19:43:38 GMT  
		Size: 14.4 MB (14391063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:25fdcc2cbfefb333f78ee4c31c8e26be3bfdba7e5f43ccb4450e76e9ea184236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e05d3706bb11b33eb46182ccdf3e00bab1bf66ca848cbefe185486ad25ad88d`

```dockerfile
```

-	Layers:
	-	`sha256:774d3394e31cd1e8ea1096b94b75d9e7a0d9e1ecf2bbb74a5c9a7681129baa5d`  
		Last Modified: Mon, 10 Nov 2025 19:53:08 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:d4232e37bcdb344df7e9be9e8ad3a52ca333d57bb6195a4e4773da2b08b320ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74619504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78eb9a2e8154a1f6ac24c69d7dc4a6f18759b127714c1c4ae9a4df0c4670520b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 19:35:40 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 10 Nov 2025 19:35:40 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 10 Nov 2025 19:35:40 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 10 Nov 2025 19:35:40 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 10 Nov 2025 19:35:40 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:35:40 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:35:43 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 10 Nov 2025 19:35:43 GMT
ENV RABBITMQ_VERSION=3.13.7
# Mon, 10 Nov 2025 19:35:43 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 10 Nov 2025 19:35:43 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 10 Nov 2025 19:35:43 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:35:48 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 10 Nov 2025 19:35:49 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 10 Nov 2025 19:35:49 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 10 Nov 2025 19:35:49 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:35:49 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 10 Nov 2025 19:35:49 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 10 Nov 2025 19:35:49 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 10 Nov 2025 19:35:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:35:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:35:49 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 10 Nov 2025 19:35:49 GMT
CMD ["rabbitmq-server"]
# Mon, 10 Nov 2025 19:44:49 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Mon, 10 Nov 2025 19:44:49 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b275a4ffa814608bc963c3b9e3c88a424939b36cf65d044e321f43e52179304`  
		Last Modified: Mon, 10 Nov 2025 19:36:14 GMT  
		Size: 31.2 MB (31229259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558ec4e5224ed7b49760daa641c34850d615a842ebca87fd8a553641b262bad5`  
		Last Modified: Mon, 10 Nov 2025 19:36:13 GMT  
		Size: 6.1 MB (6125199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8289195b1e8010df32a2cca39c544d83a9f47f4d9ad6bae8b6743aa00c362bd`  
		Last Modified: Mon, 10 Nov 2025 19:36:12 GMT  
		Size: 1.2 MB (1226752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85576f14be8b2fdb613b6b79c177875d6799e28674584afbc308fecdf7ddb26a`  
		Last Modified: Mon, 10 Nov 2025 19:36:13 GMT  
		Size: 18.8 MB (18756521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134610e8d41b8a528a66f7e4ace10c2998f1c9ff40069beb49a16db937250900`  
		Last Modified: Mon, 10 Nov 2025 19:36:12 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff10c61c9930c5024d8bb5d228c02ac69b2c2cc6d6e6188c5496126fa6a43350`  
		Last Modified: Mon, 10 Nov 2025 19:36:13 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd3203625f217b61422f85b59640ea4b2b999730c79f503124a0e217dac3f1e`  
		Last Modified: Mon, 10 Nov 2025 19:36:12 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e95f11c6273926e1808ecd1f27530c459a82857ef6ee89eb28d16a27329f2d5`  
		Last Modified: Mon, 10 Nov 2025 19:36:14 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83af380f446bdcccfb21e2c4901025e45c545ef6b96ae9ada672b34febf17290`  
		Last Modified: Mon, 10 Nov 2025 19:45:08 GMT  
		Size: 14.1 MB (14058468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7f45249e819ba3ca09c017629199d0e01accf3101f96139780a1eeb60655664e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1651477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6bae13dd9d881c3f00893fa6df3c0f948c36326e61bc73bafef576da50b82e`

```dockerfile
```

-	Layers:
	-	`sha256:de55550e9faa30db0aa74b21b6bc2b5bb6738fea2d91eeffee5c1fa20462d6e5`  
		Last Modified: Mon, 10 Nov 2025 22:53:07 GMT  
		Size: 1.6 MB (1640537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8045f13ed45703eaf7397a00c790062c22754fcd51bf0b9c4e4214ff0ea0e9d2`  
		Last Modified: Mon, 10 Nov 2025 22:53:08 GMT  
		Size: 10.9 KB (10940 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:42c204a43fb4b46addbbfd9874214502e204dc7a92948d0d73e49334809cd3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84232953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3031cdbb4ee6ca39e19c82e93a56b84cc065a490cb9e7ba7641955618d6963`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 19:35:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 10 Nov 2025 19:35:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 10 Nov 2025 19:35:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 10 Nov 2025 19:35:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 10 Nov 2025 19:35:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:35:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:35:56 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 10 Nov 2025 19:35:56 GMT
ENV RABBITMQ_VERSION=3.13.7
# Mon, 10 Nov 2025 19:35:56 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 10 Nov 2025 19:35:56 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 10 Nov 2025 19:35:56 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:36:02 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 10 Nov 2025 19:36:03 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 10 Nov 2025 19:36:03 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 10 Nov 2025 19:36:03 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:36:03 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 10 Nov 2025 19:36:03 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 10 Nov 2025 19:36:03 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 10 Nov 2025 19:36:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:36:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:36:03 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 10 Nov 2025 19:36:03 GMT
CMD ["rabbitmq-server"]
# Mon, 10 Nov 2025 19:51:35 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Mon, 10 Nov 2025 19:51:35 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25725847c05f368a8f591eb833128ed35e1c7bae071ee8804702d1fd05e37dba`  
		Last Modified: Mon, 10 Nov 2025 19:36:30 GMT  
		Size: 37.9 MB (37926305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac79bd71a80b211166c55bd64668ff5e3d5f5322e79f7e5ca19b691574b04e2`  
		Last Modified: Mon, 10 Nov 2025 19:36:27 GMT  
		Size: 7.2 MB (7240423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d461c52db5477ced7f6e29fff9b4d3f90d76aa4d093a63e68399cf1a3210b00`  
		Last Modified: Mon, 10 Nov 2025 19:36:26 GMT  
		Size: 2.4 MB (2424728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f36ae71767dc7dc223540afd07f7bea43d9ca3a99fac41f109e6965d12efa9`  
		Last Modified: Mon, 10 Nov 2025 19:36:27 GMT  
		Size: 18.8 MB (18756728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7286110b9850bf52c711a4f523865cf1b4ddfb53c005b84badba43c28feea566`  
		Last Modified: Mon, 10 Nov 2025 19:36:26 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a893c16e5e13d560dd44bb589093b741105e63f33ac9cc354e7ecf1fd5abe01`  
		Last Modified: Mon, 10 Nov 2025 19:36:26 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0469c59d690d13addedc8c241aa8efa95956c97497ff8497497f3bab097ac80d`  
		Last Modified: Mon, 10 Nov 2025 19:36:26 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a4d395b8f1a1b350525e3bacf8e6ff5df80d56b6eb0efe3aa7af8dceff28cf`  
		Last Modified: Mon, 10 Nov 2025 19:36:26 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ff09d4a58e06e5d03e0877372a259f90ca6faf68847f4330c679b42670fbee`  
		Last Modified: Mon, 10 Nov 2025 19:51:50 GMT  
		Size: 13.7 MB (13744953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f536b7537fb5d38752eb5cddc55a1db459730172a74310ab300c11db2c8ae2c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1651341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeea2ec2b98964837a2555e439890aa6dda4786ae19625790f14472780cdcf6d`

```dockerfile
```

-	Layers:
	-	`sha256:214a5a8f3df3ac51e234112eba9375e41f373120bb8f8cf45394136ba64c2471`  
		Last Modified: Mon, 10 Nov 2025 22:53:12 GMT  
		Size: 1.6 MB (1640381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1f40e963099b45c92420d3cc3a89ea2e98a3c51719a65069380d8f92b9d1af`  
		Last Modified: Mon, 10 Nov 2025 22:53:13 GMT  
		Size: 11.0 KB (10960 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:e58f99ccf9a614a16091d87fdb677b5ac2e27c588eb4c9d86fb42825a3297bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77832870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8eae9c70e41d3ce5d476aedeb74ef38437742bcde6aa2c3bcc0de0ec20bb063`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 19:34:16 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 10 Nov 2025 19:34:16 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 10 Nov 2025 19:34:16 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 10 Nov 2025 19:34:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 10 Nov 2025 19:34:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:34:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:34:19 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 10 Nov 2025 19:34:19 GMT
ENV RABBITMQ_VERSION=3.13.7
# Mon, 10 Nov 2025 19:34:19 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 10 Nov 2025 19:34:19 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 10 Nov 2025 19:34:19 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:34:24 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 10 Nov 2025 19:34:25 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 10 Nov 2025 19:34:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 10 Nov 2025 19:34:25 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:34:25 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 10 Nov 2025 19:34:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 10 Nov 2025 19:34:25 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 10 Nov 2025 19:34:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:34:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 10 Nov 2025 19:34:25 GMT
CMD ["rabbitmq-server"]
# Mon, 10 Nov 2025 19:48:31 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Mon, 10 Nov 2025 19:48:31 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb214da3f6f7d90dcb7787f1c477574c97fc4c428adaf8eabd6ec6839b92caed`  
		Last Modified: Mon, 10 Nov 2025 19:34:46 GMT  
		Size: 31.4 MB (31384375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd78f49c056a5296630ef37c554d90d5b466d8fb21f2dc5c6a4bf6b87129f0b`  
		Last Modified: Mon, 10 Nov 2025 19:34:45 GMT  
		Size: 7.5 MB (7507437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d385c50be069c328a42976c9391d0f43429e3aaae4261d9add0f7d5c0cef25c2`  
		Last Modified: Mon, 10 Nov 2025 19:34:45 GMT  
		Size: 1.3 MB (1332266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d1c740a600b1c04e667cad4372f24740f50a22c897cdeddc5f549660e77cb9`  
		Last Modified: Mon, 10 Nov 2025 19:34:46 GMT  
		Size: 18.8 MB (18756550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c39fa9b7dbac5f764949b158030357defd334b1ea1efc401f2893156d52130c`  
		Last Modified: Mon, 10 Nov 2025 19:34:45 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4156f1a0b7eaabd6c62d778b35412ee90b9a4f1f2ba09bd399081cc551534aa5`  
		Last Modified: Mon, 10 Nov 2025 19:34:44 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02680668978f032c4fc96eeded1800d27bacba8c6c124e417db8216069573c92`  
		Last Modified: Mon, 10 Nov 2025 19:34:45 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35907687889ef1879d9e0d56f83567d7902ec4f3156384bbd2c9f50f0ca356c`  
		Last Modified: Mon, 10 Nov 2025 19:34:45 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf395e7d2bd5a4166df54352d3f997ce15798635d85b73b6d3abdb6e71b536f`  
		Last Modified: Mon, 10 Nov 2025 19:48:47 GMT  
		Size: 15.2 MB (15231564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d7b7a26d1434f00da91cbf699d627b0de1abcc81c95607260ff9abdc0a41d7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1650162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5fcf0bb5baa9217ebfac566b1d70ab4d91892566776ddf6f8ae81578ef5158`

```dockerfile
```

-	Layers:
	-	`sha256:4c6c1eedd03dc91f7db5fc923a76e95aa774d212a06e587e996eed8199960d93`  
		Last Modified: Mon, 10 Nov 2025 22:53:16 GMT  
		Size: 1.6 MB (1639321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bcd595d7079e68e66b677dfbec04a5cb7620ea59e3ad12f4464f7c4a1260154`  
		Last Modified: Mon, 10 Nov 2025 22:53:17 GMT  
		Size: 10.8 KB (10841 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:5b81cfc8dfdd5d44f4b10cbcbc1464d991e9e6e2a388577e8cb215e10e3c3ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79096400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a77dd9f7b3372e2bdcc15641451bce8d5b787a9615693266c1323d7c4b51ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 21:08:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 10 Nov 2025 21:08:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 10 Nov 2025 21:08:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 10 Nov 2025 21:08:27 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 10 Nov 2025 21:08:27 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 21:08:27 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 10 Nov 2025 21:08:31 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 10 Nov 2025 21:08:31 GMT
ENV RABBITMQ_VERSION=3.13.7
# Mon, 10 Nov 2025 21:08:31 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 10 Nov 2025 21:08:31 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 10 Nov 2025 21:08:31 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 21:08:39 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 10 Nov 2025 21:08:41 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 10 Nov 2025 21:08:42 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 10 Nov 2025 21:08:42 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 10 Nov 2025 21:08:42 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 10 Nov 2025 21:08:42 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 10 Nov 2025 21:08:43 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 10 Nov 2025 21:08:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 21:08:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 21:08:43 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 10 Nov 2025 21:08:43 GMT
CMD ["rabbitmq-server"]
# Mon, 10 Nov 2025 22:55:19 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Mon, 10 Nov 2025 22:55:19 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089344208842e1bef4f29758fa764dfc08960e3ae7b9a0d939f6ce6bfebddddb`  
		Last Modified: Mon, 10 Nov 2025 21:09:25 GMT  
		Size: 31.8 MB (31760508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e062a927989a9a23fde939fae8536383c4dd222fd453c9787bb70108449a0f17`  
		Last Modified: Mon, 10 Nov 2025 21:09:24 GMT  
		Size: 8.0 MB (8003737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220480871c031be3b40197b11ef6623ef3f63572813d51cd9797f5d5301c2d0b`  
		Last Modified: Mon, 10 Nov 2025 21:09:24 GMT  
		Size: 1.5 MB (1452388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cbbe42dc270327a650a049adb6aab9401b5dd9ac462f9288f511cefde4e969`  
		Last Modified: Mon, 10 Nov 2025 21:09:25 GMT  
		Size: 18.8 MB (18756350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dffc0276e7330b66b265b9690d7663ad8e15e6c8e1dc9acc5448edac5975ddc`  
		Last Modified: Mon, 10 Nov 2025 21:09:24 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b42bde1875b86696520796d59457d0b07c25afe2ecd38e7a2c862d5df929bbf`  
		Last Modified: Mon, 10 Nov 2025 21:09:24 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1313b9876b8003d91a3ab5589d087455d04747d34b9ef33be3a8ce00e7fe9f3`  
		Last Modified: Mon, 10 Nov 2025 21:09:24 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27259b65dcf705675852f3f7d73335fc42441431acc1e4d94ef65b7ba7e30293`  
		Last Modified: Mon, 10 Nov 2025 21:09:24 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9a0d86e1ccf40800f009e6d27e4a80aa2827546706ca23ca7b43e01f223b20`  
		Last Modified: Mon, 10 Nov 2025 22:55:45 GMT  
		Size: 15.4 MB (15389421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:5393db0134564f0a1eff56d9546a523aa613a3a2b1b875de4eb05b9ce8f5abce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1649664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98a8d6e0ccecabccf8fbe6e8ff9248f825f8cde6cdde2eb7aa5fe7444c3a040`

```dockerfile
```

-	Layers:
	-	`sha256:12341655db7a78413ea45d0002db0d7b36bb050d0c58915a85c812b8819829a9`  
		Last Modified: Tue, 11 Nov 2025 01:52:57 GMT  
		Size: 1.6 MB (1638758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:653f411d199184ddf6bed47a34056d69ba635c0ad2644d73a83300986132e5a5`  
		Last Modified: Tue, 11 Nov 2025 01:52:57 GMT  
		Size: 10.9 KB (10906 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:59fdc08979f76a903bbbeec51c1dd59b57395dcc1146c0ecdbba7615a709f2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (79987475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00b7ff043e2049da982ae121d3ebdd9f38d892580a786209d7716d0a096575f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 11 Nov 2025 03:09:02 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 11 Nov 2025 03:09:02 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 11 Nov 2025 03:09:02 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 11 Nov 2025 03:09:03 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 11 Nov 2025 03:09:03 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 03:09:03 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 11 Nov 2025 03:09:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 11 Nov 2025 03:09:15 GMT
ENV RABBITMQ_VERSION=3.13.7
# Tue, 11 Nov 2025 03:09:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 11 Nov 2025 03:09:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 11 Nov 2025 03:09:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 03:09:51 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 11 Nov 2025 03:09:59 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 11 Nov 2025 03:10:00 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 11 Nov 2025 03:10:00 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 11 Nov 2025 03:10:00 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 11 Nov 2025 03:10:00 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 11 Nov 2025 03:10:00 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 11 Nov 2025 03:10:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 03:10:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Nov 2025 03:10:00 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 11 Nov 2025 03:10:00 GMT
CMD ["rabbitmq-server"]
# Tue, 11 Nov 2025 15:35:49 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Tue, 11 Nov 2025 15:35:49 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc59d8d8ebe851a6bbb3a0febdebbf5d2ac15f1ce63e386a9ff164be9f271165`  
		Last Modified: Tue, 11 Nov 2025 03:13:35 GMT  
		Size: 32.7 MB (32722831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909b5d7bd7b2f571e8c3b87b372a07c0ea18c5417441ff4271ff5833815463d4`  
		Last Modified: Tue, 11 Nov 2025 03:13:34 GMT  
		Size: 8.8 MB (8758932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afe0db7817d15a57be547a55379bdf40b6b2891d1fd9c32f1c78c361feda63e`  
		Last Modified: Tue, 11 Nov 2025 03:13:33 GMT  
		Size: 1.4 MB (1366259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bd95e48c70502cbfaa69d48fe231303fe4a76e73eba4ebcc23028877e3eed3`  
		Last Modified: Tue, 11 Nov 2025 03:13:35 GMT  
		Size: 18.8 MB (18756761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506d0d7e601739970e5c4d4fa0b8a6fa6ede8f8c2d83b4f72e6572ce3ef92ba9`  
		Last Modified: Tue, 11 Nov 2025 03:13:33 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4e97f094b218a43bcf7fe3fc810ac73f51697371f1c2f0c7537a60e2eefe38`  
		Last Modified: Tue, 11 Nov 2025 03:13:33 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcce97cbab195b48f8a3aee8c0a6bf50c873fdb6ee66818379a01d57af1e837`  
		Last Modified: Tue, 11 Nov 2025 03:13:33 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f06a9a96b93e39603c60f8aaaaa3194246c3e445252b7200ee197332b6a5c34`  
		Last Modified: Tue, 11 Nov 2025 03:13:35 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01eb44099cc644f9aed438f0eefb32473be3fc219aece6a5276b70cd2b500f66`  
		Last Modified: Tue, 11 Nov 2025 15:37:11 GMT  
		Size: 14.9 MB (14865699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d30360ad20d2cfb850117f68ecf93ba8228ceccc7de7c54d66be4783d55c9e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1651273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e19fb7fe199fbf38868382c0b71568e3bef601490db8b082fa4f288fc9ebac9`

```dockerfile
```

-	Layers:
	-	`sha256:7f1d981c770de735549cda297091fe60cd0b180d3dba52889660a615f12ec864`  
		Last Modified: Tue, 11 Nov 2025 16:52:44 GMT  
		Size: 1.6 MB (1640367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:548c40b26cbc0e327b392f7d1ce672f0b61ed5dfdc4b246440022bbab276097d`  
		Last Modified: Tue, 11 Nov 2025 16:52:44 GMT  
		Size: 10.9 KB (10906 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:fb7ce546bc8f94034030a6f2ef1881f8777f29b17477dfb927a04cef4fdbb0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77774586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9dd5b7a1205e7deb7aac5a6452746664ad6e1789e46d0377683cd32e7dc64c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 22:34:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 10 Nov 2025 22:34:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 10 Nov 2025 22:34:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 10 Nov 2025 22:34:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 10 Nov 2025 22:34:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 22:34:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 10 Nov 2025 22:34:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 10 Nov 2025 22:34:20 GMT
ENV RABBITMQ_VERSION=3.13.7
# Mon, 10 Nov 2025 22:34:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 10 Nov 2025 22:34:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 10 Nov 2025 22:34:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 22:34:38 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 10 Nov 2025 22:34:43 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 10 Nov 2025 22:34:44 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 10 Nov 2025 22:34:44 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 10 Nov 2025 22:34:44 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 10 Nov 2025 22:34:44 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 10 Nov 2025 22:34:45 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 10 Nov 2025 22:34:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 22:34:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 22:34:46 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 10 Nov 2025 22:34:46 GMT
CMD ["rabbitmq-server"]
# Mon, 10 Nov 2025 23:45:57 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Mon, 10 Nov 2025 23:45:57 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05be0e625a58406dae2fa08d88c0e81192c8f14100876379c8904126983d793`  
		Last Modified: Mon, 10 Nov 2025 22:35:42 GMT  
		Size: 31.8 MB (31794839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac95b98cf9dabf17a3ce8fe3b5ed45c26db73899b0e83de21ce4cf9fa7ab27da`  
		Last Modified: Mon, 10 Nov 2025 22:35:37 GMT  
		Size: 6.7 MB (6745373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51ef7c8a6d0050fa30352dd65af8d2fb20f488d3a6b670fd1d53a4757550bfa`  
		Last Modified: Mon, 10 Nov 2025 22:35:36 GMT  
		Size: 1.4 MB (1430472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c091b4a8bd2af1c8e1a6cc159a1d8167b725ba0fcf6e9a83cc485b18fc707f21`  
		Last Modified: Mon, 10 Nov 2025 22:35:40 GMT  
		Size: 18.8 MB (18756519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580e76628664fc7d64087e1b60704e110d03783f5e393c93ecf9ab4542e28292`  
		Last Modified: Mon, 10 Nov 2025 22:35:36 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736336556cfea8a37f235de4d59c14b2963271668e6e9660e69c95423bae430b`  
		Last Modified: Mon, 10 Nov 2025 22:35:36 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84de8f3c04a8d54064cb3b3f6d66b40e36669a00f15024012402bffd5c48344`  
		Last Modified: Mon, 10 Nov 2025 22:35:37 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a27787438687ec4ba24949e8976913b46d8af41c12f966f48bec288e1812c4`  
		Last Modified: Mon, 10 Nov 2025 22:35:38 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff05f1da28a2fd0ba78e35d194b3ab7472187d0076f60159001355e7dcbce40c`  
		Last Modified: Mon, 10 Nov 2025 23:46:25 GMT  
		Size: 15.4 MB (15396385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2997a80dbf8441ea481b1ccf5e8c485eca28c9a5b7ecde3487739127f3d5b8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1649082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413f3418a1f62d643285acbb37c9669a32c2538c62d08111fd74e19beef1c241`

```dockerfile
```

-	Layers:
	-	`sha256:277f31c80a67c84f2942a21f352512e89b5acbc910086ba0f275e4d6f3f1b942`  
		Last Modified: Tue, 11 Nov 2025 01:53:03 GMT  
		Size: 1.6 MB (1638214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd0b354a7455b7f07fb0c5a60a106ffc7d9a0b21d63cf52a7c2a8b04ec90f5cf`  
		Last Modified: Tue, 11 Nov 2025 01:53:04 GMT  
		Size: 10.9 KB (10868 bytes)  
		MIME: application/vnd.in-toto+json
