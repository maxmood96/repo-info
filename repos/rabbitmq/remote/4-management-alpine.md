## `rabbitmq:4-management-alpine`

```console
$ docker pull rabbitmq@sha256:2f8a91462dc3c9eb11d2ddf075d3eba2201ccb75beceb3b6166dec450f412d01
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
$ docker pull rabbitmq@sha256:90e2abaaea813185085a8c57b5c8b8772f16979eb8b646b4d503f9d74c97f906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88498291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a14a7d152b37f29facdefbcd81392a6b91e43a7495448edec1056f2b1c0e5da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 20:09:49 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 09 Jun 2026 20:09:49 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 09 Jun 2026 20:09:49 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 09 Jun 2026 20:09:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 09 Jun 2026 20:09:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:09:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 09 Jun 2026 20:09:52 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 09 Jun 2026 20:09:52 GMT
ENV RABBITMQ_VERSION=4.3.1
# Tue, 09 Jun 2026 20:09:52 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 09 Jun 2026 20:09:52 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 09 Jun 2026 20:09:52 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:09:57 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 09 Jun 2026 20:09:58 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 09 Jun 2026 20:09:58 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 09 Jun 2026 20:09:58 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 09 Jun 2026 20:09:58 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 09 Jun 2026 20:09:58 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 09 Jun 2026 20:09:58 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 09 Jun 2026 20:09:58 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 09 Jun 2026 20:09:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jun 2026 20:09:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 20:09:58 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 09 Jun 2026 20:09:58 GMT
CMD ["rabbitmq-server"]
# Tue, 09 Jun 2026 20:16:27 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 09 Jun 2026 20:16:28 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.32.0/rabbitmqadmin-2.32.0-x86_64-unknown-linux-musl'; digest='be19cca3ccbaaff0d778c8ac34c5dd96481df219cf1831ec4bb15927e29374ea' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.32.0/rabbitmqadmin-2.32.0-aarch64-unknown-linux-musl'; digest='fab009d193fcbe1a5947f4066a66d8b4c967da23659584e869d0d7b6edaa2b51' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 09 Jun 2026 20:16:28 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b30c255037e69955c5756177ad5cb626284ff98178efcb0edd1b0c0e619fd01`  
		Last Modified: Tue, 09 Jun 2026 20:10:14 GMT  
		Size: 42.6 MB (42625827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44cae5ed2dfad2e9ee64a49d4800d41e100541dc1fb3cf5bcd772a27ae9c687`  
		Last Modified: Tue, 09 Jun 2026 20:10:13 GMT  
		Size: 9.2 MB (9206066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0ffe50ac7a1c9a343f84e9b4e8c8d6c798ec4fbdad14c9826822b8b528d92f`  
		Last Modified: Tue, 09 Jun 2026 20:10:13 GMT  
		Size: 2.5 MB (2465166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305ada4ad5b34886f3ed46693cd6e324f9eb6b5057a4a99ead2943f30a420888`  
		Last Modified: Tue, 09 Jun 2026 20:10:14 GMT  
		Size: 25.9 MB (25897365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131cd88fd637214b8878a917fe0b7eb18fd0e19281bc06afd2a8ee58aec9c5bf`  
		Last Modified: Tue, 09 Jun 2026 20:10:15 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372fb8b72d9f7d6ecb96c567fd61abe468f81801251df91f3dab9b5037005b1b`  
		Last Modified: Tue, 09 Jun 2026 20:10:15 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522114cf4683ac7f98d39e870a74ca09608b125774ae44c0cb95c11566ffb6a9`  
		Last Modified: Tue, 09 Jun 2026 20:10:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7341855fdc47b838c693b4719ef8ad16d150c68a7fe513407546f0a7d3ba2394`  
		Last Modified: Tue, 09 Jun 2026 20:10:16 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9becbd435bba87be32f68997318ec30d4ae76e4301fae4f58ceaf10ee55ed74`  
		Last Modified: Tue, 09 Jun 2026 20:16:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3911748d2b57f2c668e73a037f567afd2b5018aa6e01f3e8cbed8b733f3d84e`  
		Last Modified: Tue, 09 Jun 2026 20:16:34 GMT  
		Size: 4.4 MB (4437659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:eef50b49a69f1295b53bdd5ab8b6f2b4f30b149f371db1f1f3d278f482d9db02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.1 KB (691136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4371e5b1b630ea060e5b7f5179ea4335c820aeabb360f14b9d0505e457908b1`

```dockerfile
```

-	Layers:
	-	`sha256:a0bf098cf4f4c5d743f91483baabdb813cf738bd9dde88d63e93ce7a302ded1f`  
		Last Modified: Tue, 09 Jun 2026 20:16:34 GMT  
		Size: 675.9 KB (675897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7415d66ec046bc0a00270e5a8ae64c07d5a1c6248a695d65ef0a59297081cfd8`  
		Last Modified: Tue, 09 Jun 2026 20:16:34 GMT  
		Size: 15.2 KB (15239 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:d76ed1437772e7e82e17063eb096b0dd58765ed89715aabdfdf4b13ee58de677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72259233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b7030c2546e4484895ad883a990ead02a8f30661794155dce8484c9acf2f3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 20:08:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 09 Jun 2026 20:08:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 09 Jun 2026 20:08:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 09 Jun 2026 20:08:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 09 Jun 2026 20:08:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:08:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 09 Jun 2026 20:08:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 09 Jun 2026 20:08:53 GMT
ENV RABBITMQ_VERSION=4.3.1
# Tue, 09 Jun 2026 20:08:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 09 Jun 2026 20:08:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 09 Jun 2026 20:08:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:09:03 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 09 Jun 2026 20:09:05 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 09 Jun 2026 20:09:05 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 09 Jun 2026 20:09:05 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 09 Jun 2026 20:09:05 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 09 Jun 2026 20:09:05 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 09 Jun 2026 20:09:05 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 09 Jun 2026 20:09:05 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 09 Jun 2026 20:09:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jun 2026 20:09:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 20:09:05 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 09 Jun 2026 20:09:05 GMT
CMD ["rabbitmq-server"]
# Tue, 09 Jun 2026 20:16:34 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 09 Jun 2026 20:16:34 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.32.0/rabbitmqadmin-2.32.0-x86_64-unknown-linux-musl'; digest='be19cca3ccbaaff0d778c8ac34c5dd96481df219cf1831ec4bb15927e29374ea' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.32.0/rabbitmqadmin-2.32.0-aarch64-unknown-linux-musl'; digest='fab009d193fcbe1a5947f4066a66d8b4c967da23659584e869d0d7b6edaa2b51' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 09 Jun 2026 20:16:34 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7acf5ad25e7a5a1f6129c21937f7448331e2d6521e02a94534196094e555e74`  
		Last Modified: Tue, 09 Jun 2026 20:09:13 GMT  
		Size: 33.5 MB (33521154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69705a53d5dfecca41b17de55ef20aa0824e99acff528d04e8949dae9c276924`  
		Last Modified: Tue, 09 Jun 2026 20:09:12 GMT  
		Size: 7.9 MB (7862482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8308f878a4d1b7f1e6a85f26991cdcccf3a85959915f7dd8e0a41f5a41e34`  
		Last Modified: Tue, 09 Jun 2026 20:09:12 GMT  
		Size: 1.4 MB (1404194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7342968a0f6e997f9b1a0baf5f24cfe214369be8855fdcf9f24ec3715fe1797e`  
		Last Modified: Tue, 09 Jun 2026 20:09:13 GMT  
		Size: 25.9 MB (25897484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba0ce7a6ecbb966dffe158ac0368a49278f5dc15099e16b83636024dbcbe166`  
		Last Modified: Tue, 09 Jun 2026 20:09:13 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d456a6c02fb941f08071f0ca74e0837e618a82212f7d48b66ab6eb5e4b2564cd`  
		Last Modified: Tue, 09 Jun 2026 20:09:14 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35341b5405537cfeb94593b30cdb7779953d62a6b65a62022a852da8f8857a6`  
		Last Modified: Tue, 09 Jun 2026 20:09:15 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48eb1dfaa8242f36fa01cf7f1e5cbab7ceacc374f82e02b6bc0c94a35901380f`  
		Last Modified: Tue, 09 Jun 2026 20:09:15 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c088358806eb53c957e2cc9453d94da7b7b4962d1578003fc6d13d2b09dc0bb2`  
		Last Modified: Tue, 09 Jun 2026 20:16:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4c7213d8f9c6c9eba389a45469b00083525286b08e4073ce4811fdbc47d8bc3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 KB (15112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4c4794859cecc982a8d5edf52c82ed268afbf513a17946ec15bf2f41a87ca7`

```dockerfile
```

-	Layers:
	-	`sha256:ed4987e683acbf1dc6736b418a94cdec5d1074e5540ee6730f05c1dacf52eccb`  
		Last Modified: Tue, 09 Jun 2026 20:16:38 GMT  
		Size: 15.1 KB (15112 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:5e01e6e4bbe51d4618080a7fbc7e77dfa3e12bbaab69412bbd66e75577630f4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71352022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73bf81777333b8260598f4165da2383f2f3dd6e36bb680fcc653a762e892c2be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 20:10:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 09 Jun 2026 20:10:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 09 Jun 2026 20:10:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 09 Jun 2026 20:10:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 09 Jun 2026 20:10:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:10:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 09 Jun 2026 20:10:56 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 09 Jun 2026 20:10:56 GMT
ENV RABBITMQ_VERSION=4.3.1
# Tue, 09 Jun 2026 20:10:56 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 09 Jun 2026 20:10:56 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 09 Jun 2026 20:10:56 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:11:02 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 09 Jun 2026 20:11:03 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 09 Jun 2026 20:11:03 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 09 Jun 2026 20:11:03 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 09 Jun 2026 20:11:03 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 09 Jun 2026 20:11:03 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 09 Jun 2026 20:11:03 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 09 Jun 2026 20:11:03 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 09 Jun 2026 20:11:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jun 2026 20:11:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 20:11:03 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 09 Jun 2026 20:11:03 GMT
CMD ["rabbitmq-server"]
# Tue, 09 Jun 2026 20:16:28 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 09 Jun 2026 20:16:28 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.32.0/rabbitmqadmin-2.32.0-x86_64-unknown-linux-musl'; digest='be19cca3ccbaaff0d778c8ac34c5dd96481df219cf1831ec4bb15927e29374ea' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.32.0/rabbitmqadmin-2.32.0-aarch64-unknown-linux-musl'; digest='fab009d193fcbe1a5947f4066a66d8b4c967da23659584e869d0d7b6edaa2b51' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 09 Jun 2026 20:16:28 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07805f304384bd2ad90c813db62a86e013c27c15dccf1877a004319d8080a73d`  
		Last Modified: Tue, 09 Jun 2026 20:11:19 GMT  
		Size: 33.4 MB (33430746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df642f95dce7e2b19de9c0643b15934d5913add1f7260d81682273b95382510`  
		Last Modified: Tue, 09 Jun 2026 20:11:18 GMT  
		Size: 7.4 MB (7442936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e388232ed235f6c185c53e088f6f53b6ec0cdc37906df34a8a8933e5fc93d3`  
		Last Modified: Tue, 09 Jun 2026 20:11:18 GMT  
		Size: 1.3 MB (1295488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dd48eb42747698d8a80deb1841b95d0954daccf393d80b58273c9a120bba72`  
		Last Modified: Tue, 09 Jun 2026 20:11:19 GMT  
		Size: 25.9 MB (25897678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdec7e9352d14a447a8ca12a0aa2112dcae2060e37cdb4296e90f05017ebb85`  
		Last Modified: Tue, 09 Jun 2026 20:11:19 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2840772d7a446bb9424421a3b89f20aacf29c4fc3e152778e06e1a88ed78238c`  
		Last Modified: Tue, 09 Jun 2026 20:11:20 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74416a65c7b79a3cf90cc9fb2f18bc1376e83dfeaa9f8e1e53ff904766bff7ae`  
		Last Modified: Tue, 09 Jun 2026 20:11:20 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdfa4f8a5442a6d856bf6ec467e1e179380875abaafa3234aacc5059ab83059`  
		Last Modified: Tue, 09 Jun 2026 20:11:21 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980ba71a9d98fcdf2ddcbc27829f6cd1534525281b498a93c82b42dcd4277274`  
		Last Modified: Tue, 09 Jun 2026 20:16:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4799c0fb8ed90ca62f65906534f890d4fa9a5b2fe001085f6d3c0f066b829dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.4 KB (686367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d4ee8ca89e590cb993f8c81f383bdbc54777ec0e5d95cd6a91c652dd6e9706`

```dockerfile
```

-	Layers:
	-	`sha256:0e01b2e343aeeb9ca5937603c24438035f60c08db99b1ea0542a09bfb12a6766`  
		Last Modified: Tue, 09 Jun 2026 20:16:34 GMT  
		Size: 671.0 KB (671040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2997007cca462d7d8ae46713f199da40826ee731f17471879702ed0b63cec4f6`  
		Last Modified: Tue, 09 Jun 2026 20:16:34 GMT  
		Size: 15.3 KB (15327 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:de7465bce60935e22e0ede4d890d34c42b7faf847ed5ed86f1d8ce424d2d0a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87236561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0825016fcdb8863ff3e3e75333a69b4a774ef5f428b2ee577fbd460df9d8d5cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 20:09:41 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 09 Jun 2026 20:09:41 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 09 Jun 2026 20:09:41 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 09 Jun 2026 20:09:41 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 09 Jun 2026 20:09:41 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:09:41 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 09 Jun 2026 20:09:43 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 09 Jun 2026 20:09:43 GMT
ENV RABBITMQ_VERSION=4.3.1
# Tue, 09 Jun 2026 20:09:43 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 09 Jun 2026 20:09:43 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 09 Jun 2026 20:09:43 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:09:49 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 09 Jun 2026 20:09:50 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 09 Jun 2026 20:09:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 09 Jun 2026 20:09:50 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 09 Jun 2026 20:09:50 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 09 Jun 2026 20:09:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 09 Jun 2026 20:09:50 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 09 Jun 2026 20:09:50 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 09 Jun 2026 20:09:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jun 2026 20:09:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 20:09:50 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 09 Jun 2026 20:09:50 GMT
CMD ["rabbitmq-server"]
# Tue, 09 Jun 2026 20:16:20 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 09 Jun 2026 20:16:21 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.32.0/rabbitmqadmin-2.32.0-x86_64-unknown-linux-musl'; digest='be19cca3ccbaaff0d778c8ac34c5dd96481df219cf1831ec4bb15927e29374ea' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.32.0/rabbitmqadmin-2.32.0-aarch64-unknown-linux-musl'; digest='fab009d193fcbe1a5947f4066a66d8b4c967da23659584e869d0d7b6edaa2b51' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 09 Jun 2026 20:16:21 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44c15ca721eb9fbcd8df673405b02a1ddbc39878f59445045add63eb6bdb091`  
		Last Modified: Tue, 09 Jun 2026 20:10:07 GMT  
		Size: 40.5 MB (40488136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aed0c6bf3dca32199cdd644cc4c492d441d4c43ba0e7d17aff60244a64bdc8d`  
		Last Modified: Tue, 09 Jun 2026 20:10:06 GMT  
		Size: 10.0 MB (9992283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94736badf2195fabf3fb5fa52d66fea0f4c56b402e50b8242d3aa6721cf079f6`  
		Last Modified: Tue, 09 Jun 2026 20:10:05 GMT  
		Size: 2.5 MB (2514011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bb378fbb38a5d2c9295c4bbe0e374502fc88bfbedf4469a14b375523c373f1`  
		Last Modified: Tue, 09 Jun 2026 20:10:07 GMT  
		Size: 25.9 MB (25897398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49449095c66955b790069d6062cb9e13b3ed4144dcb4e8811c0356059f27308`  
		Last Modified: Tue, 09 Jun 2026 20:10:07 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e18af93cd141267c43d6ed686f20e82a1244f13008a9421d090e7690ca3846`  
		Last Modified: Tue, 09 Jun 2026 20:10:07 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c014c119fb6c2a0080bd507455c4942ffef779ebb7e457562a92944125115dcd`  
		Last Modified: Tue, 09 Jun 2026 20:10:08 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162f90244c76a09932c861a4d4e5e496479a705dc66c60d8374a2e7af2540a30`  
		Last Modified: Tue, 09 Jun 2026 20:10:08 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aa7a94d149fd42e49df95af555d081808dcabc030b398ef8ebcac8344c1fde`  
		Last Modified: Tue, 09 Jun 2026 20:16:26 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1935487fffaa630872e044e7ac2bb825d94fd052e2ba7b9048e99caf0747e4b4`  
		Last Modified: Tue, 09 Jun 2026 20:16:27 GMT  
		Size: 4.1 MB (4142842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:376f2f40d8b325f5e84d491f3ea610557cc6e2363944eb9db924254e6d773476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.4 KB (691398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8841594d031d0736e6026a0ae4874d2bab1160dccdba668148c118ca89d79c99`

```dockerfile
```

-	Layers:
	-	`sha256:3a4adac033d1565974a7edf082ad3ff69b2ec4f07288892033516fc3ddd8a500`  
		Last Modified: Tue, 09 Jun 2026 20:16:26 GMT  
		Size: 676.0 KB (676040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6568e4e31045c3ff3804ff03c18e5815f66df30192b87d0a26b4b73cd82a477`  
		Last Modified: Tue, 09 Jun 2026 20:16:26 GMT  
		Size: 15.4 KB (15358 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:d992ac5938ad54804464d09fb9477496776a4042787c681f1ee312a279091627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73682314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c70fdd2b1d6ca36683e34207d9a07bf149ff90557fd4d9e5c63205128a5fe7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 20:09:51 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 09 Jun 2026 20:09:51 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 09 Jun 2026 20:09:51 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 09 Jun 2026 20:09:51 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 09 Jun 2026 20:09:51 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:09:51 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 09 Jun 2026 20:09:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 09 Jun 2026 20:09:53 GMT
ENV RABBITMQ_VERSION=4.3.1
# Tue, 09 Jun 2026 20:09:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 09 Jun 2026 20:09:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 09 Jun 2026 20:09:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:09:59 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 09 Jun 2026 20:09:59 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 09 Jun 2026 20:09:59 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 09 Jun 2026 20:09:59 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 09 Jun 2026 20:09:59 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 09 Jun 2026 20:09:59 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 09 Jun 2026 20:09:59 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 09 Jun 2026 20:09:59 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 09 Jun 2026 20:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jun 2026 20:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 20:09:59 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 09 Jun 2026 20:09:59 GMT
CMD ["rabbitmq-server"]
# Tue, 09 Jun 2026 20:16:23 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 09 Jun 2026 20:16:23 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.32.0/rabbitmqadmin-2.32.0-x86_64-unknown-linux-musl'; digest='be19cca3ccbaaff0d778c8ac34c5dd96481df219cf1831ec4bb15927e29374ea' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.32.0/rabbitmqadmin-2.32.0-aarch64-unknown-linux-musl'; digest='fab009d193fcbe1a5947f4066a66d8b4c967da23659584e869d0d7b6edaa2b51' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 09 Jun 2026 20:16:23 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f3a569f79cb43129f145dc7bb64f64c1dc0b3ab84e24f034b8f4a54bc78a84`  
		Last Modified: Tue, 09 Jun 2026 20:10:15 GMT  
		Size: 33.5 MB (33487552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab53101ad514e3bb2d40b0fd88d954015da5d362814b2804860f29a73b95c94`  
		Last Modified: Tue, 09 Jun 2026 20:10:14 GMT  
		Size: 9.2 MB (9196031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b320053e0c8be8349dabce7aca4a7e2d9b01bde891ba1f8cef9de1ce58260a60`  
		Last Modified: Tue, 09 Jun 2026 20:10:14 GMT  
		Size: 1.4 MB (1408628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e17cef0b7b089366a9a5d7b6147c75005a5ef31eb5c6920a04f84acc278402`  
		Last Modified: Tue, 09 Jun 2026 20:10:15 GMT  
		Size: 25.9 MB (25897609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0df0b4223e5db0ee55846de9021c0bd06c38b8111ef2cdeac852830cf66814`  
		Last Modified: Tue, 09 Jun 2026 20:10:15 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debdb690a72186fc4c3797fa010ed0c8323c7e95515156e78c81f7086081d7de`  
		Last Modified: Tue, 09 Jun 2026 20:10:16 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22084efd569e95fac8accccce14ed7add59fbe759366be59873de3faeae24974`  
		Last Modified: Tue, 09 Jun 2026 20:10:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39785345e7889e9bc2f69535418147f03481e13b45c418bd1b460a53337cb321`  
		Last Modified: Tue, 09 Jun 2026 20:10:16 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546decd8722208d4546d5988560df94cb77993f2a2dd01f56ab91004accfdb5c`  
		Last Modified: Tue, 09 Jun 2026 20:16:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a63d825011f9d522cfd191dcb45b58ae563d11e7fc5cfd1a66f04f1d96947a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.1 KB (686092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434a0751f8b65066e52c82b09da51942f27daa3115827d64d4a8e087bf91b552`

```dockerfile
```

-	Layers:
	-	`sha256:75417d4e4edb82b9b7326cf2161ac529e3ddf789d89541ad4e2af735da9afa56`  
		Last Modified: Tue, 09 Jun 2026 20:16:28 GMT  
		Size: 670.9 KB (670892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4db51d95b43ec79c85bc41f7bb39493826e66c5f0cd67869a180d14cee18e3c1`  
		Last Modified: Tue, 09 Jun 2026 20:16:28 GMT  
		Size: 15.2 KB (15200 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:8a20e08d17ad3c80ab89828fe9ed322909ccc9ebb6d6f0b399d6738fcbace132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75333953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14cfc91e603d1e2eeb30f199103c5fb170a49efa15ad5a12b1f7d6cd9a2e0a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 20:16:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 09 Jun 2026 20:16:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 09 Jun 2026 20:16:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 09 Jun 2026 20:16:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 09 Jun 2026 20:16:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:16:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 09 Jun 2026 20:16:24 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 09 Jun 2026 20:16:24 GMT
ENV RABBITMQ_VERSION=4.3.1
# Tue, 09 Jun 2026 20:16:24 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 09 Jun 2026 20:16:24 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 09 Jun 2026 20:16:24 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:16:33 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 09 Jun 2026 20:16:35 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 09 Jun 2026 20:16:35 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 09 Jun 2026 20:16:35 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 09 Jun 2026 20:16:35 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 09 Jun 2026 20:16:35 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 09 Jun 2026 20:16:35 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 09 Jun 2026 20:16:35 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 09 Jun 2026 20:16:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jun 2026 20:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 20:16:36 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 09 Jun 2026 20:16:36 GMT
CMD ["rabbitmq-server"]
# Tue, 09 Jun 2026 21:09:10 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 09 Jun 2026 21:09:11 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.32.0/rabbitmqadmin-2.32.0-x86_64-unknown-linux-musl'; digest='be19cca3ccbaaff0d778c8ac34c5dd96481df219cf1831ec4bb15927e29374ea' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.32.0/rabbitmqadmin-2.32.0-aarch64-unknown-linux-musl'; digest='fab009d193fcbe1a5947f4066a66d8b4c967da23659584e869d0d7b6edaa2b51' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 09 Jun 2026 21:09:11 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15798d1f7c52a4b7ab48d1fe8922e2d5c530d6abfbd29ba3592e717d28539891`  
		Last Modified: Tue, 09 Jun 2026 20:17:15 GMT  
		Size: 34.1 MB (34094262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e399bd990fe3d0837c24a42d584706207bdb34505a29de8bf1450d09d4e414d2`  
		Last Modified: Tue, 09 Jun 2026 20:17:14 GMT  
		Size: 10.0 MB (9966894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59935d981ca541f7ff4219dee4b2f79baf4584bc5acd21974d74af935a69234`  
		Last Modified: Tue, 09 Jun 2026 20:17:13 GMT  
		Size: 1.5 MB (1542249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959c90e5a4d06ead5e19e01a34b8eafbbe91ed7196e6cab7b15c48167fa977a9`  
		Last Modified: Tue, 09 Jun 2026 20:17:14 GMT  
		Size: 25.9 MB (25897562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de4b595ecf2c1146fbf2ff5e1b42ae44f1f01d8ca952d48fb09b910f470949`  
		Last Modified: Tue, 09 Jun 2026 20:17:14 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26496be70d619c811e6b97c8a9e5e8223d3c0d58081e033128af367fffb7db7e`  
		Last Modified: Tue, 09 Jun 2026 20:17:15 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835c47a779028dc80eae010a9f5173acd56f0e542a5c3f1f00d3265ea30488f3`  
		Last Modified: Tue, 09 Jun 2026 20:17:15 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554fa6722285c4102c2defd13c2562d734fabba8852960cd4c2f32169e63d237`  
		Last Modified: Tue, 09 Jun 2026 20:17:16 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb8fe4f097938039d22a1497c91f6fe06f9de8bc7a2bc4790081dac535f37fc`  
		Last Modified: Tue, 09 Jun 2026 21:09:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e7075d10782ce1bd322e6fbc92fcbf9f111ac494f7b0954ef03f04dab429f168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.3 KB (686317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96764c1b5e875f5024ec6faa2d6901dcd4359f982291b8eafe653d3ceb81f9f1`

```dockerfile
```

-	Layers:
	-	`sha256:a7253a5b264089100a1d129b9caa1ceb45de5bd307e3cbdba1c9c875426157f5`  
		Last Modified: Tue, 09 Jun 2026 21:09:28 GMT  
		Size: 671.0 KB (671037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9561b2b1ad4d891daf1f86d29fb5d3d86490e21b39a77744dc51d643820c8bc`  
		Last Modified: Tue, 09 Jun 2026 21:09:28 GMT  
		Size: 15.3 KB (15280 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:455b6e6b6189b15910d858d0e522680631f3adab7175f791df5d492517ef12cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79255645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ddebf39901c4eb7bbaac08d129017d848a4c096b317cf1f17537c98cc080ea`
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
# Wed, 10 Jun 2026 00:26:08 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Wed, 10 Jun 2026 00:26:08 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.32.0/rabbitmqadmin-2.32.0-x86_64-unknown-linux-musl'; digest='be19cca3ccbaaff0d778c8ac34c5dd96481df219cf1831ec4bb15927e29374ea' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.32.0/rabbitmqadmin-2.32.0-aarch64-unknown-linux-musl'; digest='fab009d193fcbe1a5947f4066a66d8b4c967da23659584e869d0d7b6edaa2b51' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Wed, 10 Jun 2026 00:26:08 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
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
	-	`sha256:c9393d0b16f4b07ba394303fda62c4adf5ff7db206b64afaf91b510f54687cd6`  
		Last Modified: Wed, 10 Jun 2026 00:27:01 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f7d2fff3e9a7e547cbcca0d03fd8f8d5e36aea41d20461e8520a6625ebf6b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **689.3 KB (689289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6655f26d95572e684040c6cec36634b0b894caa43c432c3874fe3cd54fe46933`

```dockerfile
```

-	Layers:
	-	`sha256:8cc635796d1195a8ad153b71acecb5668c32dcd11bc9a452472459b8e4d859a3`  
		Last Modified: Wed, 10 Jun 2026 00:27:01 GMT  
		Size: 674.0 KB (674006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f74f59175288d27ac5f2171c3ab6c342d67f99d5b4a10792dab5337deec846ff`  
		Last Modified: Wed, 10 Jun 2026 00:27:01 GMT  
		Size: 15.3 KB (15283 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:5511c0ffc525ec7d5423d54d5a539e7facb459fdea26791f54aaaa164a93af9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73442133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785535257fd187dac83bf3447f7511560135c74f9f708883d76e8b1cc0e30293`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 20:09:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 09 Jun 2026 20:09:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 09 Jun 2026 20:09:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 09 Jun 2026 20:09:27 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 09 Jun 2026 20:09:27 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:09:27 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 09 Jun 2026 20:09:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 09 Jun 2026 20:09:29 GMT
ENV RABBITMQ_VERSION=4.3.1
# Tue, 09 Jun 2026 20:09:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 09 Jun 2026 20:09:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 09 Jun 2026 20:09:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:09:35 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 09 Jun 2026 20:09:36 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 09 Jun 2026 20:09:36 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 09 Jun 2026 20:09:36 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 09 Jun 2026 20:09:36 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 09 Jun 2026 20:09:36 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 09 Jun 2026 20:09:36 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 09 Jun 2026 20:09:36 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 09 Jun 2026 20:09:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jun 2026 20:09:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 20:09:36 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 09 Jun 2026 20:09:36 GMT
CMD ["rabbitmq-server"]
# Tue, 09 Jun 2026 20:18:26 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 09 Jun 2026 20:18:26 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.32.0/rabbitmqadmin-2.32.0-x86_64-unknown-linux-musl'; digest='be19cca3ccbaaff0d778c8ac34c5dd96481df219cf1831ec4bb15927e29374ea' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.32.0/rabbitmqadmin-2.32.0-aarch64-unknown-linux-musl'; digest='fab009d193fcbe1a5947f4066a66d8b4c967da23659584e869d0d7b6edaa2b51' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 09 Jun 2026 20:18:26 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5dfc0d122f575965ebd75bc2620a17b8e17b7d468532a46ceb70f0a41fdece`  
		Last Modified: Tue, 09 Jun 2026 20:09:59 GMT  
		Size: 34.0 MB (33950289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8d58e9d5e14916349b2553d387a17f13ab66855a4b50b2de06e137f48631fe`  
		Last Modified: Tue, 09 Jun 2026 20:09:59 GMT  
		Size: 8.4 MB (8350137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2284c98ebc0c982c11249a10edd6f4a3729e6150f4ac6d34e54f61741da2324`  
		Last Modified: Tue, 09 Jun 2026 20:09:58 GMT  
		Size: 1.5 MB (1515536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263e52357d17975554eee7a3e2956ae3bd064f87d1026e0b6e920a9255417936`  
		Last Modified: Tue, 09 Jun 2026 20:09:59 GMT  
		Size: 25.9 MB (25897593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38775ca3b6521b1c2425944fa56aeb59972abad841ee397ada629a4082fe2074`  
		Last Modified: Tue, 09 Jun 2026 20:09:59 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2a81e58ca5f22b05f5baa3f7009cf86ba23f8b76fbedd3de64575eac5dbfbb`  
		Last Modified: Tue, 09 Jun 2026 20:10:00 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940598fd4db1155f1f8131d0090e1d9d862ccb37e0c18c15d9a8aeaa714eee10`  
		Last Modified: Tue, 09 Jun 2026 20:10:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716c3c2f07b45d1e9fca2fc0f2d1eb564233da1c001c90a2e70905868ad02b9d`  
		Last Modified: Tue, 09 Jun 2026 20:10:00 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575131ba2bbb57f306fd1f6006c85973fb4cb4e0c68a84e813338fe873f2997`  
		Last Modified: Tue, 09 Jun 2026 20:18:36 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:30fc286a788c87274cb7bc6dfc93c24921b3f016e436a9d7a763bc24e5bd0513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.2 KB (686237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a562ccbcd1120b553dee398974598a2cb6684962d11bce43353a77d074a0cf`

```dockerfile
```

-	Layers:
	-	`sha256:e5fb220281ecf2439f320650a4e952b8d97a6ba9a8f58fd7b0d1e7f6feef5bc7`  
		Last Modified: Tue, 09 Jun 2026 20:18:37 GMT  
		Size: 671.0 KB (671003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cbf79abe34990f6f25611add1ffef210c52425cecbb19683a1431fb04d4c238`  
		Last Modified: Tue, 09 Jun 2026 20:18:36 GMT  
		Size: 15.2 KB (15234 bytes)  
		MIME: application/vnd.in-toto+json
