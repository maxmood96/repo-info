## `rabbitmq:4-management-alpine`

```console
$ docker pull rabbitmq@sha256:4c1fde38ebd939da04ad895fc450c41516503290b6450387e5ffd43e95a34cc3
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
$ docker pull rabbitmq@sha256:236bb5ddf99476e9856e3ecc157c81bc8666379c4bc85253af42996f0bae74e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87918632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb25a0fa2377274a1d073a12a4249d35931a782d0404aef5c71c7f3234bee00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 17 Mar 2026 18:08:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 17 Mar 2026 18:08:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 17 Mar 2026 18:08:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 17 Mar 2026 18:08:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 17 Mar 2026 18:08:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:08:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 17 Mar 2026 18:08:52 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 17 Mar 2026 18:08:52 GMT
ENV RABBITMQ_VERSION=4.2.5
# Tue, 17 Mar 2026 18:08:52 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 17 Mar 2026 18:08:52 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 17 Mar 2026 18:08:52 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:08:58 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 17 Mar 2026 18:08:59 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 17 Mar 2026 18:08:59 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 17 Mar 2026 18:08:59 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 17 Mar 2026 18:08:59 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 17 Mar 2026 18:08:59 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 18:08:59 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 17 Mar 2026 18:08:59 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 17 Mar 2026 18:08:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:08:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:08:59 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 17 Mar 2026 18:08:59 GMT
CMD ["rabbitmq-server"]
# Tue, 17 Mar 2026 19:11:40 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 17 Mar 2026 19:11:42 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.28.0/rabbitmqadmin-2.28.0-x86_64-unknown-linux-musl'; digest='57fe4a2bd4708d956a1707c61107c5c091fda8e7f8287bd778e453af03c9d808' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.28.0/rabbitmqadmin-2.28.0-aarch64-unknown-linux-musl'; digest='ab16863159a7991664d72bf84235a29b653b29cc5eb61af6ba76f42d9d69ed26' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 17 Mar 2026 19:11:42 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655ea906b356355730eca9cc4ca99cad68c8e30427ba2cbfc50ad227600d6f87`  
		Last Modified: Tue, 17 Mar 2026 18:09:15 GMT  
		Size: 42.6 MB (42622777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd927dfb996bce2f0b920eb197ce0bd2ae01fed549f2a8a7907f0db4543c6d8`  
		Last Modified: Tue, 17 Mar 2026 18:09:14 GMT  
		Size: 9.2 MB (9198215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c3f9f9dac4397a037373400c92262787e892cb3898033ae863cfe240b9a6c5`  
		Last Modified: Tue, 17 Mar 2026 18:09:13 GMT  
		Size: 2.5 MB (2465376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74161576d1324d2a11125e05512f3eed903be198aaf57c44bda03722f572261b`  
		Last Modified: Tue, 17 Mar 2026 18:09:15 GMT  
		Size: 25.4 MB (25416431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6cdaeb29cfef805429b7083900a128d70e1463079459eae73dc85126a976f0`  
		Last Modified: Tue, 17 Mar 2026 18:09:15 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca3cdb9d855e27a67c6f9a32e6d20befa9f4fdb742f15359d23770028c2662b`  
		Last Modified: Tue, 17 Mar 2026 18:09:15 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21c07d465ef3019ed11f23f3b4d9bcbc09c37c67416f266cc1c5ebb4c41bea8`  
		Last Modified: Tue, 17 Mar 2026 18:09:16 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d6342d6d08e354b4f30bb928bfbf3ff8ff34853b18f4f915eb82df3cbba3d3`  
		Last Modified: Tue, 17 Mar 2026 18:09:16 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d0ae7764135213b1cd8efe7ad62105172d0fc4fe2b097fe1377477f604bf7c`  
		Last Modified: Tue, 17 Mar 2026 19:11:48 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c627e598f3f7760e151fc665976eb2ea13c90b767795bd622a594fb62caf98`  
		Last Modified: Tue, 17 Mar 2026 19:11:48 GMT  
		Size: 4.4 MB (4351988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:63b509c0e6d26097b2851a7b8fff1d5e871f1f902bfd6b824509a17792705873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.0 KB (691036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92622a569a0bafbed27f112fe36257f8494d9ea34a6ae660876e6f098ab68e9`

```dockerfile
```

-	Layers:
	-	`sha256:ad21d0ae72458076c7846e463c7606d0dc87bc08b214d4ee5d641b0e50c5ef7e`  
		Last Modified: Tue, 17 Mar 2026 19:11:48 GMT  
		Size: 675.8 KB (675797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d13170fa843189f1e71f5c8f711f89181c957eb0dcc9e53eecf9bf03741d25`  
		Last Modified: Tue, 17 Mar 2026 19:11:48 GMT  
		Size: 15.2 KB (15239 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:d25d16221dc606970b8f5a54f237ba2cec86b5c230165782b51d2343a3e8b29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71766040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de3e1f86516dd29d01e0ccfc34d74eb818d9d2294ee6219cec5cb9a3a3a79e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 17 Mar 2026 18:08:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 17 Mar 2026 18:08:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 17 Mar 2026 18:08:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 17 Mar 2026 18:08:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 17 Mar 2026 18:08:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:08:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 17 Mar 2026 18:08:23 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 17 Mar 2026 18:08:23 GMT
ENV RABBITMQ_VERSION=4.2.5
# Tue, 17 Mar 2026 18:08:23 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 17 Mar 2026 18:08:23 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 17 Mar 2026 18:08:23 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:08:33 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 17 Mar 2026 18:08:35 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 17 Mar 2026 18:08:36 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 17 Mar 2026 18:08:36 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 17 Mar 2026 18:08:36 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 17 Mar 2026 18:08:36 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 18:08:36 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 17 Mar 2026 18:08:36 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 17 Mar 2026 18:08:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:08:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:08:36 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 17 Mar 2026 18:08:36 GMT
CMD ["rabbitmq-server"]
# Tue, 17 Mar 2026 19:10:35 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 17 Mar 2026 19:10:35 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.28.0/rabbitmqadmin-2.28.0-x86_64-unknown-linux-musl'; digest='57fe4a2bd4708d956a1707c61107c5c091fda8e7f8287bd778e453af03c9d808' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.28.0/rabbitmqadmin-2.28.0-aarch64-unknown-linux-musl'; digest='ab16863159a7991664d72bf84235a29b653b29cc5eb61af6ba76f42d9d69ed26' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 17 Mar 2026 19:10:35 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e876319fdc1cf2c4deeda75044346f0d61cea427a59fd6d3862d55abe61977`  
		Last Modified: Tue, 17 Mar 2026 18:08:43 GMT  
		Size: 33.5 MB (33518912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f50b0659e162f748ca81d59c57a6805b5bd9149c92be92da7b36f7bda976e3`  
		Last Modified: Tue, 17 Mar 2026 18:08:42 GMT  
		Size: 7.9 MB (7854413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876b53d2d5511c98ad93ab0ecbce5569ee22a21ce4efac6b92cbd37dd01456b1`  
		Last Modified: Tue, 17 Mar 2026 18:08:42 GMT  
		Size: 1.4 MB (1404375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119b046fe37dbb5f65a1a959f82ab99177859611c84d77298c38974319da6015`  
		Last Modified: Tue, 17 Mar 2026 18:08:43 GMT  
		Size: 25.4 MB (25416458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dfd97a8ce01090739cbaa1e5481e31bdff4ca2ec83a0b0328387dba3d5624d`  
		Last Modified: Tue, 17 Mar 2026 18:08:43 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0713e99d5517d7a6715dde2ca7f12c122e4f3266be0cb78eb9ac4a93f20340`  
		Last Modified: Tue, 17 Mar 2026 18:08:44 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012cc216084fbdfd9a5d8f573a42824df59ba2e1658e0352a88d999ad02bb489`  
		Last Modified: Tue, 17 Mar 2026 18:08:44 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2e80ced0b7aa4ad47cc1dfbdf2146c21d23776c0a2b550d17ef74fcef19fa3`  
		Last Modified: Tue, 17 Mar 2026 18:08:45 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3ad410f2431a67cd395e8ebecd210abd1942b0212699c1880b5c550e1403fc`  
		Last Modified: Tue, 17 Mar 2026 19:10:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:928f413e0f517d1f9d81d33d3f1f8ea8ad4a242cb59c1397ec4c0e4d1164177f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 KB (15111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f3d5cae6dd53754ffc91083530265546e9302e8058dd13c2a73bcdeb004403`

```dockerfile
```

-	Layers:
	-	`sha256:4756d3e772394b3367a234c0cb06cf3be88c4be1f7ff8ea70c3bb72aafc6ea5f`  
		Last Modified: Tue, 17 Mar 2026 19:10:39 GMT  
		Size: 15.1 KB (15111 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:f76f512f30f63458371171b608eb6a7e02a6afd0a52fd3f3fd906f5d9990e22b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70860927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74bd9cfe80c2aaaa9f09b13ded1f64b105d913eeded8645cf146a07ac52a3ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 17 Mar 2026 18:09:02 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 17 Mar 2026 18:09:02 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 17 Mar 2026 18:09:02 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 17 Mar 2026 18:09:02 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 17 Mar 2026 18:09:02 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:09:02 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 17 Mar 2026 18:09:05 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 17 Mar 2026 18:09:05 GMT
ENV RABBITMQ_VERSION=4.2.5
# Tue, 17 Mar 2026 18:09:05 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 17 Mar 2026 18:09:05 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 17 Mar 2026 18:09:05 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:09:11 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 17 Mar 2026 18:09:12 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 17 Mar 2026 18:09:12 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 17 Mar 2026 18:09:12 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 17 Mar 2026 18:09:12 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 17 Mar 2026 18:09:12 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 18:09:12 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 17 Mar 2026 18:09:12 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 17 Mar 2026 18:09:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:09:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:09:12 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 17 Mar 2026 18:09:12 GMT
CMD ["rabbitmq-server"]
# Tue, 17 Mar 2026 19:11:04 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 17 Mar 2026 19:11:04 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.28.0/rabbitmqadmin-2.28.0-x86_64-unknown-linux-musl'; digest='57fe4a2bd4708d956a1707c61107c5c091fda8e7f8287bd778e453af03c9d808' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.28.0/rabbitmqadmin-2.28.0-aarch64-unknown-linux-musl'; digest='ab16863159a7991664d72bf84235a29b653b29cc5eb61af6ba76f42d9d69ed26' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 17 Mar 2026 19:11:04 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e859418ed8c01109438c6a37b07f7200fef2d13dcbc1892640c5408e75850e5c`  
		Last Modified: Tue, 17 Mar 2026 18:09:28 GMT  
		Size: 33.4 MB (33429810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eaf7e5fe9bc24ed0bd10a0ac7e78e57e6dda17b3103c8177c0f2d5af745950`  
		Last Modified: Tue, 17 Mar 2026 18:09:27 GMT  
		Size: 7.4 MB (7435279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9331f455b9723c95f50026b0e1f998b235f8357ecd490b427577469de1e4b1e6`  
		Last Modified: Tue, 17 Mar 2026 18:09:27 GMT  
		Size: 1.3 MB (1295664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a847b4882739e3d9259eeee818f5f7af9429d36e3c3b91361c82c8517fed98`  
		Last Modified: Tue, 17 Mar 2026 18:09:28 GMT  
		Size: 25.4 MB (25416395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462a281107d7dfd85134655edffee186ee98019da125b871cda5c5dd0f093892`  
		Last Modified: Tue, 17 Mar 2026 18:09:28 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf4ad40dbdc29285c9b59f521145a2628c607a83eb7af922198b2ff83e8cee9`  
		Last Modified: Tue, 17 Mar 2026 18:09:29 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba55895697ca088cf41fe1778ed9dda56758df43d82337613a87d0186bc06947`  
		Last Modified: Tue, 17 Mar 2026 18:09:29 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7572af7a118ea454ae88749bc91cd2cd1135bc05fc316455d7cfa16d92fb2530`  
		Last Modified: Tue, 17 Mar 2026 18:09:30 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4ac30dd4511cfd18c1ab2d7b9aaeb9caee933b0cb63613a3417aa0988f78ba`  
		Last Modified: Tue, 17 Mar 2026 19:11:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1da04107bd5ee25c15eaadc103d87a9203e2e19fdeb12564a389ad9cf86d9433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.3 KB (686267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d03b0f77d3904c25a139dc653d34cfa762b00f16c56ed829ec7bc87b1d49834`

```dockerfile
```

-	Layers:
	-	`sha256:79b5146e1463ef998a0ce6c0aa1af95ec24400f849f1584c272eac3ea9a4b576`  
		Last Modified: Tue, 17 Mar 2026 19:11:09 GMT  
		Size: 670.9 KB (670940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65f6104002eaf9bbadadadc4bb90a7d39fe1455b91900e60435baec2b710ee81`  
		Last Modified: Tue, 17 Mar 2026 19:11:09 GMT  
		Size: 15.3 KB (15327 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:3b31740ab33addea532df384fe078ff1fcd1760f1b28e6e84a907b8f8e64b14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86630433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f52d837d8acf6fd23966dd1bef9271d80de908d5a067ac0960ecace8661c831`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 17 Mar 2026 18:08:40 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 17 Mar 2026 18:08:40 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 17 Mar 2026 18:08:40 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 17 Mar 2026 18:08:40 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 17 Mar 2026 18:08:40 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:08:40 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 17 Mar 2026 18:08:42 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 17 Mar 2026 18:08:42 GMT
ENV RABBITMQ_VERSION=4.2.5
# Tue, 17 Mar 2026 18:08:42 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 17 Mar 2026 18:08:42 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 17 Mar 2026 18:08:42 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:08:48 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 17 Mar 2026 18:08:49 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 17 Mar 2026 18:08:49 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 17 Mar 2026 18:08:49 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 17 Mar 2026 18:08:49 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 17 Mar 2026 18:08:49 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 18:08:49 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 17 Mar 2026 18:08:49 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 17 Mar 2026 18:08:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:08:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:08:49 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 17 Mar 2026 18:08:49 GMT
CMD ["rabbitmq-server"]
# Tue, 17 Mar 2026 19:12:27 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 17 Mar 2026 19:12:27 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.28.0/rabbitmqadmin-2.28.0-x86_64-unknown-linux-musl'; digest='57fe4a2bd4708d956a1707c61107c5c091fda8e7f8287bd778e453af03c9d808' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.28.0/rabbitmqadmin-2.28.0-aarch64-unknown-linux-musl'; digest='ab16863159a7991664d72bf84235a29b653b29cc5eb61af6ba76f42d9d69ed26' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 17 Mar 2026 19:12:27 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65880e184d723a6e43f3692b0de483fd8df9bdf6ff642cb48b467797696ea830`  
		Last Modified: Tue, 17 Mar 2026 18:09:06 GMT  
		Size: 40.5 MB (40480384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470b9b483c4b484dc447c4de1e40f5576fe5b01eb45a3795be416fb0f7d21034`  
		Last Modified: Tue, 17 Mar 2026 18:09:05 GMT  
		Size: 10.0 MB (9979263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19b0e3462264bddb692f72e44ba224ff7aa99b7a66bec07e5ad0152abfbdacd`  
		Last Modified: Tue, 17 Mar 2026 18:09:04 GMT  
		Size: 2.5 MB (2514183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804a493372e3b69635e28b6843f3cd068dd50b4635c5ae815839da4b4a6b7ced`  
		Last Modified: Tue, 17 Mar 2026 18:09:05 GMT  
		Size: 25.4 MB (25416524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a086d95b92f7b3f99e7cab0b2413399b8edc38cf68133ce29b1c1e8c710bfd`  
		Last Modified: Tue, 17 Mar 2026 18:09:05 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a291b2846fe24c223783b0c3376cf12d6b70ec9b88c4030fdb258158dd90451`  
		Last Modified: Tue, 17 Mar 2026 18:09:06 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f6716e7eb633b3e765de962c99b27fe4a68b414b09ab0beb3adda7c3005ecc`  
		Last Modified: Tue, 17 Mar 2026 18:09:07 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83952466b9d4cc046c5d0a410c12b35ca0f2eb2bdc6cd9cea48ae5c612aa0c6b`  
		Last Modified: Tue, 17 Mar 2026 18:09:07 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f761300599df66648158ba46bc4a65c438fc4ba19e84c6d11cb6f4738e970b0`  
		Last Modified: Tue, 17 Mar 2026 19:12:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4ec313f3392070ea5ca5b811e78163d4e4554468855b316eabe22844e958f4`  
		Last Modified: Tue, 17 Mar 2026 19:12:34 GMT  
		Size: 4.0 MB (4040965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8e4a86f23d94691b101527369bcfd5fc00772a5da8e74d0a3f19558a381c8875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.3 KB (691298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae9bed605dfaa48ac454137119b331f6cd963ae96c1a7d5a03883dad3adb055`

```dockerfile
```

-	Layers:
	-	`sha256:0c57a65b276279c629e1e97347eb15434448ecc294d64f9a0c67d886452dec57`  
		Last Modified: Tue, 17 Mar 2026 19:12:34 GMT  
		Size: 675.9 KB (675940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f2ac9e2258bbfbab6660744d105c15dfe1a644bae000499f4cc5a6f400e74e7`  
		Last Modified: Tue, 17 Mar 2026 19:12:34 GMT  
		Size: 15.4 KB (15358 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:0aec51f8d3cc77851c8e22c7c4562bbf4869e441b3e20786fd5fdbe5364bc782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73185865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974d5ce125f3990042729292e6f66bc169e4f664b95ce1d0c8508949c0757b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Tue, 17 Mar 2026 18:08:57 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 17 Mar 2026 18:08:57 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 17 Mar 2026 18:08:57 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 17 Mar 2026 18:08:57 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 17 Mar 2026 18:08:57 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:08:57 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 17 Mar 2026 18:08:59 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 17 Mar 2026 18:08:59 GMT
ENV RABBITMQ_VERSION=4.2.5
# Tue, 17 Mar 2026 18:08:59 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 17 Mar 2026 18:08:59 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 17 Mar 2026 18:08:59 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:09:05 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 17 Mar 2026 18:09:06 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 17 Mar 2026 18:09:06 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 17 Mar 2026 18:09:06 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 17 Mar 2026 18:09:06 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 17 Mar 2026 18:09:06 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 18:09:06 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 17 Mar 2026 18:09:06 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 17 Mar 2026 18:09:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:09:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:09:06 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 17 Mar 2026 18:09:06 GMT
CMD ["rabbitmq-server"]
# Tue, 17 Mar 2026 19:25:45 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 17 Mar 2026 19:25:45 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.28.0/rabbitmqadmin-2.28.0-x86_64-unknown-linux-musl'; digest='57fe4a2bd4708d956a1707c61107c5c091fda8e7f8287bd778e453af03c9d808' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.28.0/rabbitmqadmin-2.28.0-aarch64-unknown-linux-musl'; digest='ab16863159a7991664d72bf84235a29b653b29cc5eb61af6ba76f42d9d69ed26' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 17 Mar 2026 19:25:45 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d9353dc07471527ff6054eee7fb7195bd1561becf30ce3bce43abfd5aa87f5`  
		Last Modified: Tue, 17 Mar 2026 18:09:21 GMT  
		Size: 33.5 MB (33480205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd6712277958de3f0a7c1f323626b0e3fa16436629e9d8dfb2d317dc9f9f3ae`  
		Last Modified: Tue, 17 Mar 2026 18:09:21 GMT  
		Size: 9.2 MB (9191411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a64b910f8304728437b7f3d434cb0372497c6685a8295f93b7504e5cb37047`  
		Last Modified: Tue, 17 Mar 2026 18:09:20 GMT  
		Size: 1.4 MB (1408809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a3760cac87a66c0306a8bc3588184c78f982f60a554ac84bb43036eb1717c7`  
		Last Modified: Tue, 17 Mar 2026 18:09:21 GMT  
		Size: 25.4 MB (25416388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbfc7520479e43ea7ed001edfdc4bfebc9043b5467a7bcbc35253b2b34d6a927`  
		Last Modified: Tue, 17 Mar 2026 18:09:21 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe272b23b3ee5cca0110f40962c5ebef3e6d11cfdb82857a1e5fb8a3ba98009`  
		Last Modified: Tue, 17 Mar 2026 18:09:22 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700d981083d6c5a5e412a4f004235fb3b08ffe6e6e63b804180d81702c104cb7`  
		Last Modified: Tue, 17 Mar 2026 18:09:22 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78e88a801e5ec9715317b07a13dc728c890e2709fc924a270b5c47142824826`  
		Last Modified: Tue, 17 Mar 2026 18:09:23 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae334f124a642d137ffb1657e564ef6cafab6bdbb1e0678126ef0e3b397d2938`  
		Last Modified: Tue, 17 Mar 2026 19:25:51 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9c9d749b281a370126ebf50194ebd34eaaf27708194c13f593dafd8e3b08eeda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.0 KB (685992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4797fc347918deade9999ec3df9a1c6d5a116df311c746e66d30e66a3be1397`

```dockerfile
```

-	Layers:
	-	`sha256:8b0fa19681be01e058c72e367c67ec0cbe56d54856225fe1e59da6349be7d2bc`  
		Last Modified: Tue, 17 Mar 2026 19:25:51 GMT  
		Size: 670.8 KB (670792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a03e75630fb73b4f7c2b7bb47f13c637e552ad490d5fbf7bb4c3e38f031bf0a0`  
		Last Modified: Tue, 17 Mar 2026 19:25:51 GMT  
		Size: 15.2 KB (15200 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:f6d66e0090338aefcdab2ff355a35da4cc04b79233d6c165eb61f00c22e35891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74833665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d82b56b6821ea60ad39293f6911fd38e387c9878e77016a97d9502fe0c2f1174`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 13 Mar 2026 00:51:01 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 13 Mar 2026 00:51:01 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 13 Mar 2026 00:51:01 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 13 Mar 2026 00:51:02 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 13 Mar 2026 00:51:02 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Mar 2026 00:51:02 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 13 Mar 2026 00:51:07 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 13 Mar 2026 00:51:07 GMT
ENV RABBITMQ_VERSION=4.2.5
# Fri, 13 Mar 2026 00:51:07 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 13 Mar 2026 00:51:07 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 13 Mar 2026 00:51:07 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 19:14:22 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 17 Mar 2026 19:14:24 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 17 Mar 2026 19:14:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 17 Mar 2026 19:14:25 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 17 Mar 2026 19:14:25 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 17 Mar 2026 19:14:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 19:14:25 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 17 Mar 2026 19:14:25 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 17 Mar 2026 19:14:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 19:14:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 19:14:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 17 Mar 2026 19:14:26 GMT
CMD ["rabbitmq-server"]
# Tue, 17 Mar 2026 22:02:06 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 17 Mar 2026 22:02:07 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.28.0/rabbitmqadmin-2.28.0-x86_64-unknown-linux-musl'; digest='57fe4a2bd4708d956a1707c61107c5c091fda8e7f8287bd778e453af03c9d808' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.28.0/rabbitmqadmin-2.28.0-aarch64-unknown-linux-musl'; digest='ab16863159a7991664d72bf84235a29b653b29cc5eb61af6ba76f42d9d69ed26' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 17 Mar 2026 22:02:07 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d8cd1921e4e3d9fd51c29bee7b8afab30a82bf3954f1ac76cfbe8a8b104c38`  
		Last Modified: Fri, 13 Mar 2026 00:51:54 GMT  
		Size: 34.1 MB (34090498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f14e5671c9d9439ecd91975e1dbdbb6686c4620af0a43e1d1d393a1a7a3ef4`  
		Last Modified: Fri, 13 Mar 2026 00:51:53 GMT  
		Size: 10.0 MB (9952645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b754b83ff9f91d67c8547d007ac1d1f9460af6cd84369096d6b20b0bfd318da9`  
		Last Modified: Fri, 13 Mar 2026 00:51:53 GMT  
		Size: 1.5 MB (1542432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0790a63cbf25f4dc02d8668cfb2fbd4ad7b0506650413153863bf34aed189b7`  
		Last Modified: Tue, 17 Mar 2026 19:18:47 GMT  
		Size: 25.4 MB (25416385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6850e39afb82a8b7465d961751ac943fde950c79593713a61631c92fa7ace08`  
		Last Modified: Tue, 17 Mar 2026 19:18:46 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be125a5e5096cc98c97dbb7dce2b273784a2d6ef371c977965826d1aeacb07f1`  
		Last Modified: Tue, 17 Mar 2026 19:18:46 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c37041b031cac8122cc1b05b790a8f41035d7805cb24a0940cf63f15fca0edd`  
		Last Modified: Tue, 17 Mar 2026 19:18:46 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac1f57f2a0f1402f00faf9fc9fef79c4af77543128865ebbd0115c71ba7ac2d`  
		Last Modified: Tue, 17 Mar 2026 19:18:47 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2f66417439c9bdd2020ef7f81a321659089efb30e8a180bd755b6d311cdbb9`  
		Last Modified: Tue, 17 Mar 2026 22:02:22 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bf0c588d80d2cf8aa5557043013691ffe6f9e21c98e6323637e1f76dbc7b790f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.2 KB (686217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481610b16a3b79fcc62ca472591fae23e4aa8b1c318e6d4f7217e4b605c4d47a`

```dockerfile
```

-	Layers:
	-	`sha256:cf540683d61b9782a9a5da3cbb99849f6f410f7363a1669591314236a5421b60`  
		Last Modified: Tue, 17 Mar 2026 22:02:22 GMT  
		Size: 670.9 KB (670937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a43fe326efa6e5fbdd20b56be93ed893ca6d94beaec190b3285a05e30b25f7f3`  
		Last Modified: Tue, 17 Mar 2026 22:02:22 GMT  
		Size: 15.3 KB (15280 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:a8f6a5e99ab92a1e98b00ca2750743ce7cd4cbf02fa797d661f00c124763c24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78741175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9040c9697fa50e7419ce012636f92cd72562241357aac2df54b3a4a6990a2128`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Fri, 13 Mar 2026 22:32:46 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 13 Mar 2026 22:32:46 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 13 Mar 2026 22:32:46 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 13 Mar 2026 22:32:47 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 13 Mar 2026 22:32:47 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Mar 2026 22:32:47 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 13 Mar 2026 22:32:58 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 13 Mar 2026 22:32:58 GMT
ENV RABBITMQ_VERSION=4.2.4
# Fri, 13 Mar 2026 22:32:58 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 13 Mar 2026 22:32:58 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 13 Mar 2026 22:32:58 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Mar 2026 22:33:35 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 13 Mar 2026 22:33:44 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 13 Mar 2026 22:33:44 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 13 Mar 2026 22:33:44 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Mar 2026 22:33:44 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Mar 2026 22:33:44 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 13 Mar 2026 22:33:44 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 13 Mar 2026 22:33:44 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 13 Mar 2026 22:33:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 22:33:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 22:33:44 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 13 Mar 2026 22:33:44 GMT
CMD ["rabbitmq-server"]
# Sat, 14 Mar 2026 07:39:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Sat, 14 Mar 2026 07:39:09 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-x86_64-unknown-linux-musl'; digest='19597fe995ada6603aee6c0bb2ce6f0db894858f51a40d35ee9f8eb5cc49aa54' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-aarch64-unknown-linux-musl'; digest='2984085052189414af736b4947f5e8ff35c3457c3e9aa7ab2eedeec9b800d71b' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Sat, 14 Mar 2026 07:39:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de39d1c1f4d5b0bdbe3793bf8f89b2da2d79b2afc078f369c0809f3d4e3826da`  
		Last Modified: Fri, 13 Mar 2026 22:37:46 GMT  
		Size: 37.5 MB (37522210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc6495bc34389ebb7c9e1b02e858a0ea5573b0721a324d6003aae5f51d19c72`  
		Last Modified: Fri, 13 Mar 2026 22:37:40 GMT  
		Size: 10.8 MB (10780485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce197503e0faaf7e87ab4e4bb4ab1d824bd0b4a0de11587a550ea16d3410bbd9`  
		Last Modified: Fri, 13 Mar 2026 22:37:35 GMT  
		Size: 1.4 MB (1449729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bbc7cb60fe8fe6fd3ffca43144e6582ec4dbddf22b8ff33291e8b7ebaf0f05`  
		Last Modified: Fri, 13 Mar 2026 22:37:45 GMT  
		Size: 25.4 MB (25401403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0097aaa0ec1feb8e324fc862817746858bfa7d80a4c1b4761dee7cd3b8eac985`  
		Last Modified: Fri, 13 Mar 2026 22:37:38 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebdf8348923cb073542702eb09c203c8c33e84d74d60b6e1694a3f1dce82a3b`  
		Last Modified: Fri, 13 Mar 2026 22:37:40 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74096641d1b08a383ec606c6e6cd6232cbc5b8d92d45f90bcb9789383cddde8b`  
		Last Modified: Fri, 13 Mar 2026 22:37:42 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd8eda1c03e99390ac851f735a21fc2568ff69a4f1f0848c5e79643135e43db`  
		Last Modified: Fri, 13 Mar 2026 22:37:42 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ba3aea09521dc9cae982b5e5e8f45bbb9ac61cdb116aaccb64096a411184b6`  
		Last Modified: Sat, 14 Mar 2026 07:40:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fec8853329ea21281cf3a8fee45849a7784498a808baf76cb5493f34dc679b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **689.2 KB (689189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67a99c0a520f25ec1f69a6cc52f96d0c406d0e8332e3512698668b9ba1bfb43`

```dockerfile
```

-	Layers:
	-	`sha256:b2eb7178ce729f8397e638a1501c236425c4412423a85e5879de17ae239de7da`  
		Last Modified: Sat, 14 Mar 2026 07:40:03 GMT  
		Size: 673.9 KB (673906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31f0cf59bde6e1516bab7ea9e3a859aa8568707454580fe6b0c5342e2dfb0b3b`  
		Last Modified: Sat, 14 Mar 2026 07:40:03 GMT  
		Size: 15.3 KB (15283 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:af76ce8135abd8b8cba7d1c0183664499e8c330682e2c015a93113c29e4cc6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72931341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475fe5760c8388c2e69a760a2d8d176aea46a8a2b38ab05e9f171c8bc6b2a553`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 13 Mar 2026 00:13:46 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 13 Mar 2026 00:13:46 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 13 Mar 2026 00:13:46 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 13 Mar 2026 00:13:46 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 13 Mar 2026 00:13:46 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Mar 2026 00:13:46 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 13 Mar 2026 00:13:49 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 13 Mar 2026 00:13:49 GMT
ENV RABBITMQ_VERSION=4.2.5
# Fri, 13 Mar 2026 00:13:49 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 13 Mar 2026 00:13:49 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 13 Mar 2026 00:13:49 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:03:57 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 17 Mar 2026 18:03:58 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 17 Mar 2026 18:03:58 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 17 Mar 2026 18:03:58 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 17 Mar 2026 18:03:58 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 17 Mar 2026 18:03:58 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 18:03:58 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 17 Mar 2026 18:03:59 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 17 Mar 2026 18:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:03:59 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 17 Mar 2026 18:03:59 GMT
CMD ["rabbitmq-server"]
# Tue, 17 Mar 2026 19:10:03 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 17 Mar 2026 19:10:04 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.28.0/rabbitmqadmin-2.28.0-x86_64-unknown-linux-musl'; digest='57fe4a2bd4708d956a1707c61107c5c091fda8e7f8287bd778e453af03c9d808' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.28.0/rabbitmqadmin-2.28.0-aarch64-unknown-linux-musl'; digest='ab16863159a7991664d72bf84235a29b653b29cc5eb61af6ba76f42d9d69ed26' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 17 Mar 2026 19:10:04 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083a4a57e2fe05473e484468a7e23282656197f65c69ca14ed1325a33526ad00`  
		Last Modified: Fri, 13 Mar 2026 00:14:23 GMT  
		Size: 33.9 MB (33932033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589a4c29b2d52b88ee1e56480dc348f5cd3ae6b0c85c863cdd61e1b921ac5ccf`  
		Last Modified: Fri, 13 Mar 2026 00:14:22 GMT  
		Size: 8.3 MB (8339905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdb8a51c2063f1f2e696f3a059e1ec0a1d43fed6af61a1e6038d9001a86002b`  
		Last Modified: Fri, 13 Mar 2026 00:14:22 GMT  
		Size: 1.5 MB (1515670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a8c39fa994841c9611c5b689527f219ad2a04115b7c05daa9a6374831afbe7`  
		Last Modified: Tue, 17 Mar 2026 18:09:18 GMT  
		Size: 25.4 MB (25416340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19b6cbececa258dcde22010098175c0826fd24fbe5b1a59d61a78d39cda8d9f`  
		Last Modified: Tue, 17 Mar 2026 18:09:18 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bb44e267c3e3180a22ca1c9b26a20680f0e6dfe78776dee67dff2d2f32755d`  
		Last Modified: Tue, 17 Mar 2026 18:09:18 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2a87435e12e449a442b3304374cca7bed28c613168e64780c1947f3da19f85`  
		Last Modified: Tue, 17 Mar 2026 18:09:19 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c01e6b5e6b3da35452e03b3da7d8f2337964fa72e4f794046f6b72a33cc1bd`  
		Last Modified: Tue, 17 Mar 2026 18:09:19 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5100a1498de5af4ff06fffbe360ed4e8b464cb5c9f5eb392a5c5e456ede3f9`  
		Last Modified: Tue, 17 Mar 2026 19:10:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c8654603f2cc157e8486cf7d4bdf794d48e167772beb4b9a42ea4c17fb1a1f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.1 KB (686137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631e727d1e64cb61aa6aae77190a6bbcf6153d755c5c160f120537d5b9c6b052`

```dockerfile
```

-	Layers:
	-	`sha256:5d20cf38304a4179a8cea2a56ee05db61904161da91718fc0691ed96b38d953e`  
		Last Modified: Tue, 17 Mar 2026 19:10:44 GMT  
		Size: 670.9 KB (670903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0613826e93dfdecf3038dbb46cfe75478d10992836febbb59682d146c0e8d19`  
		Last Modified: Tue, 17 Mar 2026 19:10:44 GMT  
		Size: 15.2 KB (15234 bytes)  
		MIME: application/vnd.in-toto+json
