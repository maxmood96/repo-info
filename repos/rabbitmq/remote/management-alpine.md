## `rabbitmq:management-alpine`

```console
$ docker pull rabbitmq@sha256:7f0e22dce6a456d963b6a96ef785fafa308c4e35838c9d64c95ba24a83058cce
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
$ docker pull rabbitmq@sha256:99657709d66ae6a9c3269a98f5ca290e8464072723184120d1e7649583ffbc37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88491605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d4ac0ad3472ca161200b14a6ebf53ba0e2d3ae64070937342465c25fa6508a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 26 May 2026 18:42:34 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 26 May 2026 18:42:34 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 26 May 2026 18:42:34 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 26 May 2026 18:42:34 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 26 May 2026 18:42:34 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 18:42:34 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 26 May 2026 18:42:36 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 26 May 2026 18:42:36 GMT
ENV RABBITMQ_VERSION=4.3.1
# Tue, 26 May 2026 18:42:36 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 26 May 2026 18:42:36 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 26 May 2026 18:42:36 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 18:42:42 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 26 May 2026 18:42:43 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 26 May 2026 18:42:43 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 26 May 2026 18:42:43 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 26 May 2026 18:42:43 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 26 May 2026 18:42:43 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 26 May 2026 18:42:43 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 26 May 2026 18:42:43 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 26 May 2026 18:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 18:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 18:42:43 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 26 May 2026 18:42:43 GMT
CMD ["rabbitmq-server"]
# Tue, 26 May 2026 18:59:23 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 26 May 2026 18:59:23 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.30.0/rabbitmqadmin-2.30.0-x86_64-unknown-linux-musl'; digest='70d136a0cb1f105b0904748aae04a0fdb1619e1eb6cf93afacca773d4c7973f4' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.30.0/rabbitmqadmin-2.30.0-aarch64-unknown-linux-musl'; digest='3082218c983fdf6d4a7cbbf1b038829a391c9eba056e9828dddf97c46ac43488' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 26 May 2026 18:59:23 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877961bb3673166c60c2828f3d381a12e32f28ad5522e2c799d4ad883f9be5b9`  
		Last Modified: Tue, 26 May 2026 18:43:00 GMT  
		Size: 42.6 MB (42624994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3508ce9bfbce3ae00a8adadb006b6f42e62316970e43139ffc301b1223cabca6`  
		Last Modified: Tue, 26 May 2026 18:42:59 GMT  
		Size: 9.2 MB (9201534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40c3801eb5843bacae232f079d7dbb7796294982c75eac07511de1ce8910741`  
		Last Modified: Tue, 26 May 2026 18:42:59 GMT  
		Size: 2.5 MB (2465160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971c4467de39cc3468bfe59fc9f4088ec4aa0f8dfec1ba31c0d9f397becbc7f8`  
		Last Modified: Tue, 26 May 2026 18:43:00 GMT  
		Size: 25.9 MB (25897441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71b59ec85b2e7ae7953c3e2fc0b9e43b49523a129ef3570e3019c110b0d856e`  
		Last Modified: Tue, 26 May 2026 18:43:00 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e9d7b1c12c4a72bf6a741fa9b8a2daba17a693a54be0169c8ba92b5b3bf91a`  
		Last Modified: Tue, 26 May 2026 18:43:00 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ae4cff8d342f11f4a50b56d22390348fd216af4b35d6f9e1b1e0b8b30beee1`  
		Last Modified: Tue, 26 May 2026 18:43:01 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2d08c9830b01a1f55e42e25dbcb52bad824a95d317d3b6efca3db22ce106d9`  
		Last Modified: Tue, 26 May 2026 18:43:02 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac07993954caaf71e9ebe2855523ed6e6d01325c06d28cdbbc210760f70945c`  
		Last Modified: Tue, 26 May 2026 18:59:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ee458435833de1a501068cc9e1aad909bb7aa7451bd5a6ae3d2554427b50d4`  
		Last Modified: Tue, 26 May 2026 18:59:30 GMT  
		Size: 4.4 MB (4436265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b688d20e5a7f6379d5926dbe5643e2f31e9c0e5bc6b8b6df16a6535153e1717e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.1 KB (691136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea693a832a158a5a79bcc5812110b0279b21796f2600786f1e2453f419a57075`

```dockerfile
```

-	Layers:
	-	`sha256:102ae3beb2942004349c03100b717b8407428ba99d4b96ef15eb0eb4cb693f2c`  
		Last Modified: Tue, 26 May 2026 18:59:30 GMT  
		Size: 675.9 KB (675897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b16cabbb3edd60c86f8b55fdd86ff6f396cc8fa088c3d9a6abfeb3f2fb1ea5ca`  
		Last Modified: Tue, 26 May 2026 18:59:30 GMT  
		Size: 15.2 KB (15239 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:b8c304cad7b590f2519969e618431873cb039e623b6df47af034ef907eea98dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72252227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fc0abce4e6a360e3576dc38865b414818b38065752c6c6ec681048f0300b4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 26 May 2026 18:41:57 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 26 May 2026 18:41:57 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 26 May 2026 18:41:57 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 26 May 2026 18:41:57 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 26 May 2026 18:41:57 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 18:41:57 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 26 May 2026 18:42:00 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 26 May 2026 18:42:00 GMT
ENV RABBITMQ_VERSION=4.3.1
# Tue, 26 May 2026 18:42:00 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 26 May 2026 18:42:00 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 26 May 2026 18:42:00 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 18:42:10 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 26 May 2026 18:42:12 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 26 May 2026 18:42:12 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 26 May 2026 18:42:12 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 26 May 2026 18:42:12 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 26 May 2026 18:42:12 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 26 May 2026 18:42:12 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 26 May 2026 18:42:12 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 26 May 2026 18:42:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 18:42:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 18:42:12 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 26 May 2026 18:42:12 GMT
CMD ["rabbitmq-server"]
# Tue, 26 May 2026 19:07:27 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 26 May 2026 19:07:27 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.30.0/rabbitmqadmin-2.30.0-x86_64-unknown-linux-musl'; digest='70d136a0cb1f105b0904748aae04a0fdb1619e1eb6cf93afacca773d4c7973f4' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.30.0/rabbitmqadmin-2.30.0-aarch64-unknown-linux-musl'; digest='3082218c983fdf6d4a7cbbf1b038829a391c9eba056e9828dddf97c46ac43488' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 26 May 2026 19:07:27 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c994e2a8be4c4ecf09a8b7e02895b9923b87dc42f06c66a01189eb7141c3f7`  
		Last Modified: Tue, 26 May 2026 18:42:21 GMT  
		Size: 33.5 MB (33520086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02628eaf94c5efdc3f09dde1f631f2301fdaab3cde0e6ee516c3bfe8d06ebdf`  
		Last Modified: Tue, 26 May 2026 18:42:19 GMT  
		Size: 7.9 MB (7856542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd88ac32e5fffd4f5e8fdf83362806aa7bf73fe28939943bc9c2f2d023d48450`  
		Last Modified: Tue, 26 May 2026 18:42:19 GMT  
		Size: 1.4 MB (1404208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810df0c456c20d3537d7cc91a155bf009dc18f3a3335a19a8e6c7beb947f7b8a`  
		Last Modified: Tue, 26 May 2026 18:42:20 GMT  
		Size: 25.9 MB (25897473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1caff106ee30454bb5b59213b971fa12d164227e51952cc18bd11e1fdd25e5`  
		Last Modified: Tue, 26 May 2026 18:42:20 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086887b98a2d000fefe2031863f0c95a88da23fe92110a20c98d29ec209c9937`  
		Last Modified: Tue, 26 May 2026 18:42:21 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f03215ff5f1c15580a2167ba675e522bc9b54eef61c49922e43e2e66c9de518`  
		Last Modified: Tue, 26 May 2026 18:42:22 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b998c02e52e3a921a61523cb4b0856523ebb666e78ad41a5205cb1cf9fa19ea`  
		Last Modified: Tue, 26 May 2026 18:42:22 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e19f58f1d2b5c7230555cb6e663c88e4a19c6c9d9866034825a7571dcaaf85`  
		Last Modified: Tue, 26 May 2026 19:07:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:04dd01591091188c01983ae29092327b839b64ea4df6a6879f6fa32c937ae863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 KB (15111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5d70b671df80a2b574d23f1fa0f8ed55b5ce14afb0a376d3f640f9b353b81c`

```dockerfile
```

-	Layers:
	-	`sha256:b335c3cb4541c6a47e885335f8e63355f411c9b0a45f77fdbde3eded194d20ab`  
		Last Modified: Tue, 26 May 2026 19:07:31 GMT  
		Size: 15.1 KB (15111 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:73eb80aa93f469d0f67360d558546903f894804905239201cae143c065f843d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71345702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd15da75add7c7d9fb55754316d237307d1ccf649adea4e77749311757bd8722`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 26 May 2026 18:42:56 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 26 May 2026 18:42:56 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 26 May 2026 18:42:56 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 26 May 2026 18:42:56 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 26 May 2026 18:42:56 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 18:42:56 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 26 May 2026 18:42:58 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 26 May 2026 18:42:58 GMT
ENV RABBITMQ_VERSION=4.3.1
# Tue, 26 May 2026 18:42:58 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 26 May 2026 18:42:58 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 26 May 2026 18:42:58 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 18:43:05 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 26 May 2026 18:43:06 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 26 May 2026 18:43:06 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 26 May 2026 18:43:06 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 26 May 2026 18:43:06 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 26 May 2026 18:43:06 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 26 May 2026 18:43:06 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 26 May 2026 18:43:06 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 26 May 2026 18:43:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 18:43:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 18:43:06 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 26 May 2026 18:43:06 GMT
CMD ["rabbitmq-server"]
# Tue, 26 May 2026 19:19:03 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 26 May 2026 19:19:04 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.30.0/rabbitmqadmin-2.30.0-x86_64-unknown-linux-musl'; digest='70d136a0cb1f105b0904748aae04a0fdb1619e1eb6cf93afacca773d4c7973f4' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.30.0/rabbitmqadmin-2.30.0-aarch64-unknown-linux-musl'; digest='3082218c983fdf6d4a7cbbf1b038829a391c9eba056e9828dddf97c46ac43488' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 26 May 2026 19:19:04 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab6ad5cc830749780fdbec10d6bd1e324609154d69dd9974a2e086330adc0d9`  
		Last Modified: Tue, 26 May 2026 18:43:22 GMT  
		Size: 33.4 MB (33429529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3fbbbccfecd8bfdfbd3e5ba2420c0579ae00358a23bf16fe38b79a59361398`  
		Last Modified: Tue, 26 May 2026 18:43:21 GMT  
		Size: 7.4 MB (7437814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83c5d693051b95bf5aed20ce82f5005bfcfed4475c38d230bb896ba6d241500`  
		Last Modified: Tue, 26 May 2026 18:43:21 GMT  
		Size: 1.3 MB (1295487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83a022c4904059bfb99e7c61310b068d561e55a98bf3b6debf372721eab2cd8`  
		Last Modified: Tue, 26 May 2026 18:43:22 GMT  
		Size: 25.9 MB (25897699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca7ef48cef32522c5fb0f9ed2933607c888b39f96150f0e171748dca27bf32a`  
		Last Modified: Tue, 26 May 2026 18:43:22 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07fd8923d2beec8238d1c501e9008dac772fb6259eba5d7bbfebee641c99a00a`  
		Last Modified: Tue, 26 May 2026 18:43:22 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc219c23cfd79d6beaa8241efba85f754551dee45b05bd3f5db941d766d08cbb`  
		Last Modified: Tue, 26 May 2026 18:43:23 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9911caf4ef60e5096f31df72016e282e98654b53b63adbf89a9ad874ddbee865`  
		Last Modified: Tue, 26 May 2026 18:43:23 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f536829a52c8b39276583b58fc4714d1a23b61117b93f7055e80883d698c8f`  
		Last Modified: Tue, 26 May 2026 19:19:09 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f45572a68258770c9967047217bbb949a46d4224acaa75646710bd3594d158ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.4 KB (686367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee381143ae8558cbccb4f1bd9a5dd66876c00fcd6d539c58bc84005e1128c6d`

```dockerfile
```

-	Layers:
	-	`sha256:f4d89de8c4fcad355c6ff9615df35d9c668a73b4110ca533728e4fa87392e4b8`  
		Last Modified: Tue, 26 May 2026 19:19:09 GMT  
		Size: 671.0 KB (671040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d76b610ff9061b1f252bf06f65c27d242cab1f8599ec437a08f49b3216cda14`  
		Last Modified: Tue, 26 May 2026 19:19:09 GMT  
		Size: 15.3 KB (15327 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:9741019ebfbd1886e5090f91f6d994bb2492f4c5172599bf6c6fa0bda2bf902e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87224794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6736e4e0facf3297f8d8e9622171053fdcb5e263349b80f499f91d409f8c26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 26 May 2026 18:42:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 26 May 2026 18:42:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 26 May 2026 18:42:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 26 May 2026 18:42:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 26 May 2026 18:42:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 18:42:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 26 May 2026 18:42:24 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 26 May 2026 18:42:24 GMT
ENV RABBITMQ_VERSION=4.3.1
# Tue, 26 May 2026 18:42:24 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 26 May 2026 18:42:24 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 26 May 2026 18:42:24 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 18:42:30 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 26 May 2026 18:42:31 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 26 May 2026 18:42:31 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 26 May 2026 18:42:31 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 26 May 2026 18:42:31 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 26 May 2026 18:42:31 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 26 May 2026 18:42:31 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 26 May 2026 18:42:31 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 26 May 2026 18:42:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 18:42:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 18:42:32 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 26 May 2026 18:42:32 GMT
CMD ["rabbitmq-server"]
# Tue, 26 May 2026 19:12:51 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 26 May 2026 19:12:51 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.30.0/rabbitmqadmin-2.30.0-x86_64-unknown-linux-musl'; digest='70d136a0cb1f105b0904748aae04a0fdb1619e1eb6cf93afacca773d4c7973f4' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.30.0/rabbitmqadmin-2.30.0-aarch64-unknown-linux-musl'; digest='3082218c983fdf6d4a7cbbf1b038829a391c9eba056e9828dddf97c46ac43488' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 26 May 2026 19:12:51 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc97485cc7dacf444b638527962aecc4589345b499821497e31ca0bc081c06ef`  
		Last Modified: Tue, 26 May 2026 18:42:49 GMT  
		Size: 40.5 MB (40485398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64c986d659f78015c05834eedb22e9163dcc2ce4e0316781ed84ddc794494bd`  
		Last Modified: Tue, 26 May 2026 18:42:48 GMT  
		Size: 10.0 MB (9984560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947cc1139e74ebc0a5c13837484a8caf8c2954e266796c2279663fa9a8f07d77`  
		Last Modified: Tue, 26 May 2026 18:42:48 GMT  
		Size: 2.5 MB (2514045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e44e55bc5ba790412736ac4d5a6602406fccee0fefe7a1b86fa2e3f8cb7deb2`  
		Last Modified: Tue, 26 May 2026 18:42:49 GMT  
		Size: 25.9 MB (25897457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bea4bc0ca8511bc23ea46d9261ae615539dc8e8c6391dc0c0f185999ba81d0`  
		Last Modified: Tue, 26 May 2026 18:42:49 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7100e2a8c21d075b772a3bc24fb012a55b145785f90cd03945796633dcc017e5`  
		Last Modified: Tue, 26 May 2026 18:42:50 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66e4e65578e2dbd244fac1239c6a02c4dd2792ed40242f966d7f12ab0a1621e`  
		Last Modified: Tue, 26 May 2026 18:42:50 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe9c8f3042f1967c04da37f3eab274359d538b88f0b6d2c3cc7c789b8c26de9`  
		Last Modified: Tue, 26 May 2026 18:42:51 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109ef473e3b8eda576c40ec2519d759b0c7f1d8254d1d03df11c7302c3c54f66`  
		Last Modified: Tue, 26 May 2026 19:12:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09ea2fdfd42f10482c618c6eb91f34ebdfd60fc15b84c68a30cc53bdcacdfa4`  
		Last Modified: Tue, 26 May 2026 19:12:58 GMT  
		Size: 4.1 MB (4141443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ec4aa64dc72fe38ae07602b07f30aa48948b44231031f8f58090e92b0bcbb6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.4 KB (691398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3701a9921e8f64040e0e95ad9ff35513cb3e43debaf480836f22a76a2df86eb7`

```dockerfile
```

-	Layers:
	-	`sha256:3aa716f4cddf7a4fe2a2f3d5748cab3adaf1e885b9957e8ee602b20a9045ff57`  
		Last Modified: Tue, 26 May 2026 19:12:58 GMT  
		Size: 676.0 KB (676040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b06ff6d4836d665e4556cc384b5ec3b21ea667d449cdf7c5d1c4897a959ddfdf`  
		Last Modified: Tue, 26 May 2026 19:12:57 GMT  
		Size: 15.4 KB (15358 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:38848d0f046a686484366ca6ef085b18bda6c4b41145fc98304cb0016f6cf6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73676650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9da096bf5c04a411aec5d3770720b53e3aec3b304a15206f268283ac073b8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Tue, 26 May 2026 21:47:05 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 26 May 2026 21:47:05 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 26 May 2026 21:47:05 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 26 May 2026 21:47:05 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 26 May 2026 21:47:05 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 21:47:05 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 26 May 2026 21:47:08 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 26 May 2026 21:47:08 GMT
ENV RABBITMQ_VERSION=4.3.1
# Tue, 26 May 2026 21:47:08 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 26 May 2026 21:47:08 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 26 May 2026 21:47:08 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 21:47:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 26 May 2026 21:47:15 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 26 May 2026 21:47:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 26 May 2026 21:47:15 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 26 May 2026 21:47:15 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 26 May 2026 21:47:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 26 May 2026 21:47:15 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 26 May 2026 21:47:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 26 May 2026 21:47:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 21:47:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 21:47:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 26 May 2026 21:47:15 GMT
CMD ["rabbitmq-server"]
# Tue, 26 May 2026 23:27:52 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 26 May 2026 23:27:52 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.30.0/rabbitmqadmin-2.30.0-x86_64-unknown-linux-musl'; digest='70d136a0cb1f105b0904748aae04a0fdb1619e1eb6cf93afacca773d4c7973f4' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.30.0/rabbitmqadmin-2.30.0-aarch64-unknown-linux-musl'; digest='3082218c983fdf6d4a7cbbf1b038829a391c9eba056e9828dddf97c46ac43488' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 26 May 2026 23:27:52 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae04b2429d3c0caaeec762d7b5980c8d732937504b195cca938fdfad2ee0785a`  
		Last Modified: Tue, 26 May 2026 21:47:30 GMT  
		Size: 33.5 MB (33485640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9581802570192672f762159807a985e79971e2920e65342f386ff3eb6acf86fc`  
		Last Modified: Tue, 26 May 2026 21:47:30 GMT  
		Size: 9.2 MB (9192187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99642e562c756b16ada59c4cc0f9c71702afce1d446f0e5ae35863b7dd148ca`  
		Last Modified: Tue, 26 May 2026 21:47:29 GMT  
		Size: 1.4 MB (1408657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2417c0848bf608cdd034fd8000536a4721d7addd73c44534470019b8f1576ed5`  
		Last Modified: Tue, 26 May 2026 21:47:30 GMT  
		Size: 25.9 MB (25897664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fc3c3fc17a3e42d3057ed7d19ca8f1a0059d4582dc835df923d5925899dfe1`  
		Last Modified: Tue, 26 May 2026 21:47:30 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e52043f3c771e189ff2ce0d16c70d3dde7f38abd412eb964481295b4659a63`  
		Last Modified: Tue, 26 May 2026 21:47:31 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657d71fdc2cb6617326380a3ac03f93ad17cdc45efb83f52cd7543d032a4f0f5`  
		Last Modified: Tue, 26 May 2026 21:47:31 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3320f10092ad90abd50e6938e3d5bc0d47a28f82b03fe103f218075eafa781`  
		Last Modified: Tue, 26 May 2026 21:47:32 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b990c72640f070402e4235343cb6097ab79ff8790f7551e661a670219b599170`  
		Last Modified: Tue, 26 May 2026 23:27:58 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e67b33c4896a030f7623fe1f21fa7e22c00e611ef7c7fa7ce1a223676b046b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.1 KB (686092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20477e8766fb26bee6771caa93231043e354a3da24a74018829b33100275223`

```dockerfile
```

-	Layers:
	-	`sha256:3f8b3be56ffceecd807203b210a66c340bcf3d19c3670381c554724e57fbcdd6`  
		Last Modified: Tue, 26 May 2026 23:27:58 GMT  
		Size: 670.9 KB (670892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:852469f077f154cf9ea4a345ae9252164321931bdd970ba2023135aed4162671`  
		Last Modified: Tue, 26 May 2026 23:27:57 GMT  
		Size: 15.2 KB (15200 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:365beb20ecd2ebbf74f9323dc64969ed7c228ef3ecd7e17888e72bbeca975bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75326153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48764589e37ea16689a3fe5cdcf3d2c6e6cd459e444f83909767e64bb1909400`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 26 May 2026 18:43:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 26 May 2026 18:43:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 26 May 2026 18:43:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 26 May 2026 18:43:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 26 May 2026 18:43:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 18:43:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 26 May 2026 18:43:35 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 26 May 2026 18:43:35 GMT
ENV RABBITMQ_VERSION=4.3.1
# Tue, 26 May 2026 18:43:35 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 26 May 2026 18:43:35 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 26 May 2026 18:43:35 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 18:43:44 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 26 May 2026 18:43:46 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 26 May 2026 18:43:46 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 26 May 2026 18:43:46 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 26 May 2026 18:43:46 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 26 May 2026 18:43:46 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 26 May 2026 18:43:46 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 26 May 2026 18:43:47 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 26 May 2026 18:43:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 18:43:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 18:43:47 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 26 May 2026 18:43:47 GMT
CMD ["rabbitmq-server"]
# Tue, 26 May 2026 20:11:30 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 26 May 2026 20:11:31 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.30.0/rabbitmqadmin-2.30.0-x86_64-unknown-linux-musl'; digest='70d136a0cb1f105b0904748aae04a0fdb1619e1eb6cf93afacca773d4c7973f4' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.30.0/rabbitmqadmin-2.30.0-aarch64-unknown-linux-musl'; digest='3082218c983fdf6d4a7cbbf1b038829a391c9eba056e9828dddf97c46ac43488' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 26 May 2026 20:11:31 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025d7d2456bea9d4a0fb71c98748a02ff2b7f7d1c5c4b27e131f90b9e4286c45`  
		Last Modified: Tue, 26 May 2026 18:44:17 GMT  
		Size: 34.1 MB (34093445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b0c1a56d37566227807ea21f9caf8a27154f79806672a665dac8ab86e40870`  
		Last Modified: Tue, 26 May 2026 18:44:16 GMT  
		Size: 10.0 MB (9959827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a5fb02d8bf78e43e977f4ff5a9b3b79f5e77f6e8c40dfd151541397496f21a`  
		Last Modified: Tue, 26 May 2026 18:44:15 GMT  
		Size: 1.5 MB (1542256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bef4b05ebeafa140c61bb04a4b55b3490e8e2ed9cb5d5817a95a899bd4131fe`  
		Last Modified: Tue, 26 May 2026 18:44:16 GMT  
		Size: 25.9 MB (25897640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8e82645c5490afe243615cde35a0d2bebf7438d179d4d582df56338af76ef5`  
		Last Modified: Tue, 26 May 2026 18:44:16 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358e9b472c69846709d2eb49c9764370970b626cf7d34f64c9c7f168222f7e7d`  
		Last Modified: Tue, 26 May 2026 18:44:17 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dc384756c97754296c18e72229ad8102425198a173519e1ffb8d200694fde8`  
		Last Modified: Tue, 26 May 2026 18:44:18 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0fb8cf5a7bd88769012d4600c749ed576cbfd0def5e4476748ed2f49e2dcbb`  
		Last Modified: Tue, 26 May 2026 18:44:18 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7448c2bc99dd564b78a669df026398ed63f984b62a1f9a5619af5a56574872`  
		Last Modified: Tue, 26 May 2026 20:11:40 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:971c2fd2f0ee153916de161669b91ee50229976aec3bec21bbdc12ec03bddb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.3 KB (686317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44bff4cfb031a814e05d79fcd88337ff1caf36ea26c7b4db63d65c52948c9e57`

```dockerfile
```

-	Layers:
	-	`sha256:6b80879283d8213c0d6c7aa2fc1e563576a16cf317e189865263324e16458af5`  
		Last Modified: Tue, 26 May 2026 20:11:40 GMT  
		Size: 671.0 KB (671037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3cbb9b7f66efdd2b918892c23ff18f44e7bcbad8b1e4f748052e74fd35919f7`  
		Last Modified: Tue, 26 May 2026 20:11:40 GMT  
		Size: 15.3 KB (15280 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:d7fb68947c9b667f5ceb855fcb6a3d947c391978006c1d30f08b71faac9c272d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79256590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c4173c733f7124f5cbd0cb2b5bfb249fbfdd9720a706ac1f45a22f33cc3dab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 05:13:42 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 22 Apr 2026 05:13:42 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 22 Apr 2026 05:13:42 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 22 Apr 2026 05:13:43 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 22 Apr 2026 05:13:43 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 05:13:43 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 22 Apr 2026 05:13:55 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 22 Apr 2026 05:13:55 GMT
ENV RABBITMQ_VERSION=4.3.0
# Wed, 22 Apr 2026 05:13:55 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 22 Apr 2026 05:13:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 22 Apr 2026 05:13:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 26 Apr 2026 11:24:25 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sun, 26 Apr 2026 11:24:34 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sun, 26 Apr 2026 11:24:34 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sun, 26 Apr 2026 11:24:34 GMT
ENV HOME=/var/lib/rabbitmq
# Sun, 26 Apr 2026 11:24:34 GMT
VOLUME [/var/lib/rabbitmq]
# Sun, 26 Apr 2026 11:24:34 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sun, 26 Apr 2026 11:24:34 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Sun, 26 Apr 2026 11:24:34 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sun, 26 Apr 2026 11:24:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 26 Apr 2026 11:24:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Apr 2026 11:24:35 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sun, 26 Apr 2026 11:24:35 GMT
CMD ["rabbitmq-server"]
# Sun, 26 Apr 2026 16:18:40 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Wed, 06 May 2026 08:18:01 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.30.0/rabbitmqadmin-2.30.0-x86_64-unknown-linux-musl'; digest='70d136a0cb1f105b0904748aae04a0fdb1619e1eb6cf93afacca773d4c7973f4' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.30.0/rabbitmqadmin-2.30.0-aarch64-unknown-linux-musl'; digest='3082218c983fdf6d4a7cbbf1b038829a391c9eba056e9828dddf97c46ac43488' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Wed, 06 May 2026 08:18:01 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7284d49606fd8c9ded6e25796a5ad27b9e244b31297cc29534b9bdee49ef3a70`  
		Last Modified: Wed, 22 Apr 2026 05:20:23 GMT  
		Size: 37.5 MB (37522961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5eebf0555295aa4ed26459e2ade5294de5efa786d39c6e1347cb6f531e2c60a`  
		Last Modified: Wed, 22 Apr 2026 05:20:16 GMT  
		Size: 10.8 MB (10787537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140184dfa92cc52240860bed267a85fda593c871da39645b662022532ab667c0`  
		Last Modified: Wed, 22 Apr 2026 05:20:12 GMT  
		Size: 1.4 MB (1449763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc2ca766b10c17bb222495fdc155eeaff8c7d4997db5e9ede9c72d8af1e7e7d`  
		Last Modified: Sun, 26 Apr 2026 11:30:30 GMT  
		Size: 25.9 MB (25906613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525f17f417f72cdada05f1312fa2aa6b6ef7318a32c7c512b7ee086cfdf65861`  
		Last Modified: Sun, 26 Apr 2026 11:30:25 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34392c466b15fb57504f6c308a860597cd05a50d60aa87f8af34fbd449acb38`  
		Last Modified: Sun, 26 Apr 2026 11:30:26 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371aa1e169aeb7b48fb00826d13795bd717905f6bcc982454598e03335154b89`  
		Last Modified: Sun, 26 Apr 2026 11:30:25 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7faca2dd53692ad5440ea09b1ceb93905eb81ae9c922e6da8936eee0abc5cf7c`  
		Last Modified: Sun, 26 Apr 2026 11:30:27 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0582fb05338dada97f68f6da24bf0862336119663b59d2a1b32c47ecde7b2b`  
		Last Modified: Sun, 26 Apr 2026 16:19:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1bc313d6b9ad6575a18e7f99b6f1a34038ddafdbfcfb432740b55a700bdd6ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **689.3 KB (689289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad2a70ba698e55b702f228442eb3c9bdc675035df71babf4c0bc6edfcf0b1f7`

```dockerfile
```

-	Layers:
	-	`sha256:6d1a60914dd2e944a6b5c6d708a3f843d83842cd137fd62eb7ff6d6aba9f4069`  
		Last Modified: Wed, 06 May 2026 08:18:55 GMT  
		Size: 674.0 KB (674006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27ec65616d291d87d19d6cd983e1bf0b5b51e9bd5d6b5dd84b6f87b0f6b7432e`  
		Last Modified: Wed, 06 May 2026 08:18:55 GMT  
		Size: 15.3 KB (15283 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:737e09dc2736fdc6b300654a17f70ab5b7432aafa8023ab2f7e9a9aa30e79245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73435390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b677e737fbe0e20267d0d387a1860be5274f40e1970b6bfc46612cae9ff552cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 26 May 2026 18:42:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 26 May 2026 18:42:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 26 May 2026 18:42:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 26 May 2026 18:42:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 26 May 2026 18:42:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 18:42:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 26 May 2026 18:42:33 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 26 May 2026 18:42:33 GMT
ENV RABBITMQ_VERSION=4.3.1
# Tue, 26 May 2026 18:42:33 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 26 May 2026 18:42:33 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 26 May 2026 18:42:33 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 18:42:41 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 26 May 2026 18:42:43 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 26 May 2026 18:42:43 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 26 May 2026 18:42:43 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 26 May 2026 18:42:43 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 26 May 2026 18:42:43 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 26 May 2026 18:42:43 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 26 May 2026 18:42:43 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 26 May 2026 18:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 18:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 18:42:43 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 26 May 2026 18:42:43 GMT
CMD ["rabbitmq-server"]
# Tue, 26 May 2026 19:53:08 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 26 May 2026 19:53:08 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.30.0/rabbitmqadmin-2.30.0-x86_64-unknown-linux-musl'; digest='70d136a0cb1f105b0904748aae04a0fdb1619e1eb6cf93afacca773d4c7973f4' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.30.0/rabbitmqadmin-2.30.0-aarch64-unknown-linux-musl'; digest='3082218c983fdf6d4a7cbbf1b038829a391c9eba056e9828dddf97c46ac43488' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 26 May 2026 19:53:08 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c3017548ebe3684ac7a39d1b455fb07febea049181d9968621be051a6f2e57`  
		Last Modified: Tue, 26 May 2026 18:43:28 GMT  
		Size: 33.9 MB (33948854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93578fceaaaa022402c28ea286b19c7a8bba10408129b06649103d28a6fd3c54`  
		Last Modified: Tue, 26 May 2026 18:43:27 GMT  
		Size: 8.3 MB (8344807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c571e719615ae140d964b78407de72bdeb93b8a9d865e76e7feaef8dfedbde01`  
		Last Modified: Tue, 26 May 2026 18:43:27 GMT  
		Size: 1.5 MB (1515540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79550b62a010ab4a01bf6d69063f423ea63346a14221f76323543b888682975`  
		Last Modified: Tue, 26 May 2026 18:43:29 GMT  
		Size: 25.9 MB (25897601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106e0f9724fa86e1697bc4f56100f8f2dfacad562de9d9eeec9fefc5b553e409`  
		Last Modified: Tue, 26 May 2026 18:43:28 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e9d7b1c12c4a72bf6a741fa9b8a2daba17a693a54be0169c8ba92b5b3bf91a`  
		Last Modified: Tue, 26 May 2026 18:43:00 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdc03e4e4330fc790451102a1aedba5716eaae8c2ab04eef5e1567c10ac05e6`  
		Last Modified: Tue, 26 May 2026 18:43:29 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6298cc784435a5fa31aef4f96f0bdce75a0dcde44017ce6957f76076af03ac01`  
		Last Modified: Tue, 26 May 2026 18:43:30 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad65a74228f35a5a0c37123a4f09701b7c45cf3ffd0d2c8dd14030efe5f11b`  
		Last Modified: Tue, 26 May 2026 19:53:17 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:82d6b292c05e82aea499a32118edf252d9fe2b066189b22eef6920e049aa010e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.2 KB (686237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a9d24892e5275f4318da2fe26557ba03bb3bfae50e6c1003905ffed3c597f1`

```dockerfile
```

-	Layers:
	-	`sha256:d208207097968e4006581730150590efbc2a21837331fe38627387f472716a71`  
		Last Modified: Tue, 26 May 2026 19:53:17 GMT  
		Size: 671.0 KB (671003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:978a9a54b2e79f94f591505dbbb6bdaa3f019fad1c9cfc5edceccd5d172ccf96`  
		Last Modified: Tue, 26 May 2026 19:53:17 GMT  
		Size: 15.2 KB (15234 bytes)  
		MIME: application/vnd.in-toto+json
