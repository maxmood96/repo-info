## `rabbitmq:3-alpine`

```console
$ docker pull rabbitmq@sha256:632a1f358aca92a531db8b35f1f9aff6aacda39fc93140c32f95cc7ce302e784
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
$ docker pull rabbitmq@sha256:7ca21950a4be94e914f4e59a4336ce5d97dacca9da71a523ea12a089c0e18e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72275265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e421e476dbbe5a463ef077e54a768ac91fdfc845fa52ff88d68a88038a3bd8`
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

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4248308cf83a8067310f4041039903fb29e459e14c4cfe0302ce782d15fb2394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6776959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b081c06058a4a288d2c4538959170e8d338b4c7c1fd46ee68fa827fc19c76635`

```dockerfile
```

-	Layers:
	-	`sha256:449ba22040530f958ac1d125cf2650d3a1696e0a3437ebb804a79f6368345e6f`  
		Last Modified: Mon, 10 Nov 2025 19:52:57 GMT  
		Size: 664.8 KB (664788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:432b28cefdbcf1ad25e217b7143d1631f936032c6398e61271d1d66dc070b478`  
		Last Modified: Mon, 10 Nov 2025 19:52:58 GMT  
		Size: 3.1 MB (3103701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb84f181e9a0002204ef78d1a249b53b6bed00ecf915e5e82b6845f4cab677fb`  
		Last Modified: Mon, 10 Nov 2025 19:52:59 GMT  
		Size: 2.9 MB (2948839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0079f7715498e3797eefb7a9918c380454f56d9dd801aee08c7f67092aeafa50`  
		Last Modified: Mon, 10 Nov 2025 19:53:00 GMT  
		Size: 59.6 KB (59631 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:751555900986c7de478ce689c8d696289465da819e7c7ef2b07929a0c4ed9b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61318909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc06a322a8af66a897e2a64c79c67d20093e18c34426480bdbc2eca8ad56e06`
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

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:147bfcc450e62e6d64818461637b5a3898bf0477bd09660a8f2cb6107484e724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 KB (59605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a742cb9aaae635f3b08f8a8d9a700c24b1950ba739eff089c44b88aea93f99f`

```dockerfile
```

-	Layers:
	-	`sha256:5d539d1f40f27ed0424404b0e236b695b0492cee435358d34ca18fadba8bd835`  
		Last Modified: Mon, 10 Nov 2025 19:53:05 GMT  
		Size: 59.6 KB (59605 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:40431624283904f9e52dac6daaa7c2b917ee42f203e09ffad7b7ad99fe8105c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60561036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c147c65f7aa4c874314f545fad127bb885cbbe08a3c263e340cc6c475ab34a`
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

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:5a61def26158d7a735074d75f24d74104c30b141acd38e167e97ad1ec49e2b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6541237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5947382211b86392559ab5dfc8739384fa107c0f6f44ff0d5897b2f3290edd4b`

```dockerfile
```

-	Layers:
	-	`sha256:29e4c1ceab3d2ccb3f4ac16e266c968ca60b826332ede3585398058a1547f682`  
		Last Modified: Mon, 10 Nov 2025 19:53:09 GMT  
		Size: 660.6 KB (660574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce2dfbc9771eb178942388f57ce74a5615ee89bef2091081d7b7f3134f277cc8`  
		Last Modified: Mon, 10 Nov 2025 19:53:10 GMT  
		Size: 3.0 MB (2988518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486bc406298edaad8178755a263e4ac73ae91d57ab9040eb9936791b844531aa`  
		Last Modified: Mon, 10 Nov 2025 19:53:11 GMT  
		Size: 2.8 MB (2832325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c99b3ab7b3c8b4f3309b7131b6b1f6c767fd300422f3b6954d982ebdd7425dcd`  
		Last Modified: Mon, 10 Nov 2025 19:53:12 GMT  
		Size: 59.8 KB (59820 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:514315e0efbd6e514c1c5190976b065c4185c225296fafedd60dcebbba7e8617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70488000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7749bdcc79dc6e8dd7f04ba6aec04f1d7cb4760f9ee2c946c77c161875d753c`
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

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2ab87cbf19c0cb826886888cf8846e636b870351312a1f17f44d16c9aad1c405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6885219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d22e1a39b6a45989ff1fdc031b621288885ba68392993dec3eace61f492fff1`

```dockerfile
```

-	Layers:
	-	`sha256:fcfe6ae85742b09a3860fa55d58e6b50b0a0aad8080efefd11b0a99825c25bb1`  
		Last Modified: Mon, 10 Nov 2025 19:53:17 GMT  
		Size: 665.6 KB (665570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2b15488df40a85dee8ce089f45d9090759365ad715bf8ba2abc74c629521027`  
		Last Modified: Mon, 10 Nov 2025 19:53:19 GMT  
		Size: 3.2 MB (3157989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ed23571d003f1e2a223cee6640cf191bf9e1e71f18179e070387f83e155756`  
		Last Modified: Mon, 10 Nov 2025 19:53:20 GMT  
		Size: 3.0 MB (3001802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d94fe8a97f70f19f74ae92b59a753a07889880b99464f6baa3b8ef72c8079ce1`  
		Last Modified: Mon, 10 Nov 2025 19:53:21 GMT  
		Size: 59.9 KB (59858 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:7c5f59c2bfbabc46d66c7f3a29ef3a668ace1620fc09c4c70be867f1717a2a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62601306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab898d14e447c8e170e4030480fbf357141fd2c41a345cc020dd3a1ad315a757`
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

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:160e99fb9b99abc1193290bda529f01e3b564d0f24028e07fbb71f0b2a00661b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6749819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f2dc095e117abb792d77b7d27ef00e71c6214ed10a511a23505187e76d9702`

```dockerfile
```

-	Layers:
	-	`sha256:e2c6713f3f17f38a35746f4c5d36df2ef3c5ca3144ba4b2e1a7cc60c29b957a1`  
		Last Modified: Mon, 10 Nov 2025 19:53:25 GMT  
		Size: 659.8 KB (659788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb4b26e23fd3550495446b0cf563a8ef734768f6f2de0c37263a96167791c31`  
		Last Modified: Mon, 10 Nov 2025 19:53:27 GMT  
		Size: 3.1 MB (3092652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75935345321f1b33c38c312a9d784349dc9233b6fed3431404773d5ecc7d64e2`  
		Last Modified: Mon, 10 Nov 2025 19:53:29 GMT  
		Size: 2.9 MB (2937794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46ccf62fc5c2441ee5a5819a94af830d951fa377bb4c299b1897bb6157922232`  
		Last Modified: Mon, 10 Nov 2025 19:53:30 GMT  
		Size: 59.6 KB (59585 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:4c329474a61666ccb4e41300ad0b0a269bf562de752f7a39ad28d07a7d7d8380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63706979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12ca5c6298f97b4a8be6c760247a6d93bf4096134355c91aec6813789b581aa`
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

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:66069296c57be225242ad6c312aff4618577a623fe4667d853796a9af5213de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6781609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466ea3c675c7fc50afbc6327a24b1131ef8db5806f88bdb6369ae9de8caed6c0`

```dockerfile
```

-	Layers:
	-	`sha256:727c172325a840164c42bba35d026215a4eade834b060ae0a88fa11018a13d5d`  
		Last Modified: Mon, 10 Nov 2025 22:52:47 GMT  
		Size: 658.6 KB (658623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b83f99a5a411556a13ef9de61a983323f42aafef0cab40edcb12716fae75dcae`  
		Last Modified: Mon, 10 Nov 2025 22:52:48 GMT  
		Size: 3.1 MB (3109749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db63545c33844e91e41fa54d6688f334c8d340f792432708f1e2786dcdfa3616`  
		Last Modified: Mon, 10 Nov 2025 22:52:50 GMT  
		Size: 3.0 MB (2953550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd7a808dad7e158d6d61faaea2a71734f712560befa6d67e68d1673e73125c9d`  
		Last Modified: Mon, 10 Nov 2025 22:52:51 GMT  
		Size: 59.7 KB (59687 bytes)  
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
