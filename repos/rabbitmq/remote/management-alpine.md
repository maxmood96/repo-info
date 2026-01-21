## `rabbitmq:management-alpine`

```console
$ docker pull rabbitmq@sha256:a9ea3979390492de3c580c9ac92d1d3f19f41c45cf60885e21652521a7b142f7
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
$ docker pull rabbitmq@sha256:e353a4ae91469f818989bdf7e1920e5e3d5fc936f4ca45819d77fbf36fafa6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88181930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4ac0303e35b761794b7e213a985abc291075360f1ce64277b0eaa3e5521c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 21:52:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 16 Jan 2026 21:52:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 16 Jan 2026 21:52:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 16 Jan 2026 21:52:23 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 16 Jan 2026 21:52:23 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:52:23 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 16 Jan 2026 21:52:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 16 Jan 2026 21:52:25 GMT
ENV RABBITMQ_VERSION=4.2.2
# Fri, 16 Jan 2026 21:52:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 16 Jan 2026 21:52:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 16 Jan 2026 21:52:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:52:30 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 16 Jan 2026 21:52:31 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 16 Jan 2026 21:52:31 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 16 Jan 2026 21:52:31 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 16 Jan 2026 21:52:31 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 16 Jan 2026 21:52:31 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 16 Jan 2026 21:52:31 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 16 Jan 2026 21:52:31 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 16 Jan 2026 21:52:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:52:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:52:31 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 16 Jan 2026 21:52:31 GMT
CMD ["rabbitmq-server"]
# Tue, 20 Jan 2026 18:50:11 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 20 Jan 2026 18:50:12 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-musl'; digest='0dc5e39dac98f38ad50f2aee15cfc5ea53c0ef5e649d79b41c2a7a94376aaf9f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-musl'; digest='fc7ca78e16824a2c77583d067ac1ae4eacbed1516a9a66bec50b5a772530d546' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 20 Jan 2026 18:50:12 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9ae8834b665a1ead6e60f3768e8228e6e0f5221105d473a49ba02f96c58e95`  
		Last Modified: Fri, 16 Jan 2026 21:52:47 GMT  
		Size: 42.6 MB (42598704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5fc11aec69751b7227d4a4bd3e32db57f73755468baa1fcebb4bda6eeda181`  
		Last Modified: Fri, 16 Jan 2026 21:52:56 GMT  
		Size: 9.2 MB (9206857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211e4153f42f046c6a2b510359996c67c01fff7c027890dbe601d1cdc91dc7b2`  
		Last Modified: Fri, 16 Jan 2026 21:52:55 GMT  
		Size: 2.5 MB (2465570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34843266e9b66144602134e04bc3a1ebd7e12c0594fd2c96b90102ed459b461a`  
		Last Modified: Fri, 16 Jan 2026 21:52:58 GMT  
		Size: 25.3 MB (25317583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78be03c36d4f1a3ad406accfdb0e41f2b7c989d48f368c7369e294fffa8ee31`  
		Last Modified: Fri, 16 Jan 2026 21:52:54 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f97330c3395589d3f1107be6753723040818d54dcfe890024fed98fe453264`  
		Last Modified: Fri, 16 Jan 2026 21:52:47 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08707b0de1833560375be3100a395d098de9b98cd9b944f23c5e3fc36caacce`  
		Last Modified: Fri, 16 Jan 2026 21:52:54 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6d63eeb279fb44c0a97d44b71b8ff54c21392a55b949ae27e8fb4eeb6f3432`  
		Last Modified: Fri, 16 Jan 2026 21:52:54 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c10a2a18373dbedc6c6db2648d63c07f5db22b08295be466c472c2a9715bd2`  
		Last Modified: Tue, 20 Jan 2026 19:32:49 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a9229e914cb7e8681d978cdf54e978e5936f9470427edd0cf91f52f6359338`  
		Last Modified: Tue, 20 Jan 2026 18:50:25 GMT  
		Size: 4.7 MB (4731091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:324bcd9152cc33692a445b5642c03af185f33e6f97b2d6d00450356265282f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.0 KB (691024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336784fb6c315648a5853c95ad3c2d5a17111691d81b826e94ed660fdfeb956d`

```dockerfile
```

-	Layers:
	-	`sha256:ddad707f024d12bff3eae3de306eae8f28807ef53a575b858a05147a23e6e8f3`  
		Last Modified: Tue, 20 Jan 2026 18:50:19 GMT  
		Size: 675.8 KB (675785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:685bf81a7f3fa0fc4eee8b2b86f5e452d32a17ad99da125ef0e642a3ee08e80a`  
		Last Modified: Tue, 20 Jan 2026 18:50:19 GMT  
		Size: 15.2 KB (15239 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:c94841a97fa1b23432a4cd580f5ce1d738893d7e7de3938aeeaaf975c6f65354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71654070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832fca90c6f2c50f9c610a8ffae567c03e30c75ce6bc45228376c7d37b3d6c4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 21:51:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 16 Jan 2026 21:51:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 16 Jan 2026 21:51:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 16 Jan 2026 21:51:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 16 Jan 2026 21:51:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:51:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 16 Jan 2026 21:51:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 16 Jan 2026 21:51:29 GMT
ENV RABBITMQ_VERSION=4.2.2
# Fri, 16 Jan 2026 21:51:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 16 Jan 2026 21:51:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 16 Jan 2026 21:51:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:51:39 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 16 Jan 2026 21:51:41 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 16 Jan 2026 21:51:41 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 16 Jan 2026 21:51:41 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 16 Jan 2026 21:51:41 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 16 Jan 2026 21:51:41 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 16 Jan 2026 21:51:41 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 16 Jan 2026 21:51:41 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 16 Jan 2026 21:51:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:51:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:51:41 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 16 Jan 2026 21:51:41 GMT
CMD ["rabbitmq-server"]
# Tue, 20 Jan 2026 18:48:00 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 20 Jan 2026 18:48:00 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-musl'; digest='0dc5e39dac98f38ad50f2aee15cfc5ea53c0ef5e649d79b41c2a7a94376aaf9f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-musl'; digest='fc7ca78e16824a2c77583d067ac1ae4eacbed1516a9a66bec50b5a772530d546' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 20 Jan 2026 18:48:00 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f629dec1a6fb9ba8c0ed25aba968c1cfbbc65ec99fca0952c459ec0b1e3a7f98`  
		Last Modified: Fri, 16 Jan 2026 21:51:59 GMT  
		Size: 33.5 MB (33504366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705aaf9cf200a67548ae28c3d6d957b8ec05852f56738ca724b91911389cd315`  
		Last Modified: Fri, 16 Jan 2026 21:51:57 GMT  
		Size: 7.9 MB (7857225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71e53a42c7457e79be93be8c8b7afc5d5f5e417a62403ef9847d2c8e13f8834`  
		Last Modified: Fri, 16 Jan 2026 21:51:48 GMT  
		Size: 1.4 MB (1404626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796a68c8323033f74c88243674a906c3e49848ed6f7e25e21216b796ef4121d1`  
		Last Modified: Fri, 16 Jan 2026 21:51:59 GMT  
		Size: 25.3 MB (25317366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12319b7338a96a383e36bbb372ac78d4a3603d47228ed75dc307978ab5179047`  
		Last Modified: Fri, 16 Jan 2026 21:51:49 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb063cd4d57f00ff8295717fb091b0855db83c8a8cf5d6c861a5fcdc53f1f103`  
		Last Modified: Fri, 16 Jan 2026 21:51:56 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb86a1d200a2b296163ef57ccf23c27fbc3a5136ef12d452ac7f1311e34c12`  
		Last Modified: Fri, 16 Jan 2026 21:51:50 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21101f16a1eb7fc277278349ac54b3e6acf8d22638a94ccc0590f0566bd8d027`  
		Last Modified: Fri, 16 Jan 2026 21:51:50 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb892106fb231ce3387b65005ab813f942f7b1e4566ac43541982a9d5d962032`  
		Last Modified: Tue, 20 Jan 2026 18:48:04 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7e29efee1b72256e5883d14628147006fbfc47ed6f7226a6d4d31eeae779b3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 KB (15112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bd8bd18a588c911032e81b2743d31f651f0eb731848f06a5831bf0abc0ee1d`

```dockerfile
```

-	Layers:
	-	`sha256:44b088a245f96f001ba049247373e2cd7ab42b49ed7af809bb9d4ab66c503dbd`  
		Last Modified: Tue, 20 Jan 2026 19:53:16 GMT  
		Size: 15.1 KB (15112 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:f4d594ba971146a5791a279e986a48fde35a9ac0b1a78fedad90fb8c1f7e88b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70751656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18881138cdd61fbcd7c3906a637ad35ec6106a65bdc51d97c500677064e0e25e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 21:50:57 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 16 Jan 2026 21:50:57 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 16 Jan 2026 21:50:57 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 16 Jan 2026 21:50:57 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 16 Jan 2026 21:50:57 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:50:57 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 16 Jan 2026 21:50:59 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 16 Jan 2026 21:50:59 GMT
ENV RABBITMQ_VERSION=4.2.2
# Fri, 16 Jan 2026 21:50:59 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 16 Jan 2026 21:50:59 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 16 Jan 2026 21:50:59 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:51:05 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 16 Jan 2026 21:51:06 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 16 Jan 2026 21:51:06 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 16 Jan 2026 21:51:06 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 16 Jan 2026 21:51:06 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 16 Jan 2026 21:51:06 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 16 Jan 2026 21:51:06 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 16 Jan 2026 21:51:06 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 16 Jan 2026 21:51:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:51:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:51:06 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 16 Jan 2026 21:51:06 GMT
CMD ["rabbitmq-server"]
# Tue, 20 Jan 2026 18:48:28 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 20 Jan 2026 18:48:28 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-musl'; digest='0dc5e39dac98f38ad50f2aee15cfc5ea53c0ef5e649d79b41c2a7a94376aaf9f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-musl'; digest='fc7ca78e16824a2c77583d067ac1ae4eacbed1516a9a66bec50b5a772530d546' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 20 Jan 2026 18:48:28 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e51da9badca04fb8841f65315206b188aaee4bad4f8f840fd372f0508dc2b0c`  
		Last Modified: Fri, 16 Jan 2026 21:51:22 GMT  
		Size: 33.4 MB (33410024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06368101746589571e15992e443d56d41a96fcdb671298a998a5d160ef5b58`  
		Last Modified: Fri, 16 Jan 2026 21:51:21 GMT  
		Size: 7.4 MB (7447234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe432bf90a216e33904c7afe99786a070fc3184541ab9bbd4f9348644597d081`  
		Last Modified: Fri, 16 Jan 2026 21:51:20 GMT  
		Size: 1.3 MB (1295839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043e934235c0685ecf5d9c815ee9557d6717a27c339456608dfdf7471bfc0391`  
		Last Modified: Fri, 16 Jan 2026 21:51:31 GMT  
		Size: 25.3 MB (25317116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8c9a10777e1767e748e048fe16097b044ed889ec6c3ff67dce51bcbf8b35f5`  
		Last Modified: Fri, 16 Jan 2026 21:51:29 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d202056d99e0bc6f41585a194a9f7722a40b48975ad8435b99177eb50ba2a2a`  
		Last Modified: Fri, 16 Jan 2026 21:51:22 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9872b4f34c2fada214e99ceedd92afb33b99bea9b0adf10fe364210813907127`  
		Last Modified: Fri, 16 Jan 2026 21:51:29 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae8e19cada269335c1bf582ace9c8f7282cf0c95d66dd42356b3d1a213a54dc`  
		Last Modified: Fri, 16 Jan 2026 21:51:29 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960420748ed674a5f4e55fb8325ec8c15deae7df6dc53ce619746d71a24687ed`  
		Last Modified: Tue, 20 Jan 2026 18:48:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:582c2122bc9b401a3009eb1e09172e26a7b6b45b909eb54cb8d7215ae4af45c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.3 KB (686255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:333703456bcd263d0781bf88d3539fbb7dd19e07cf7353ae357a42e109f43f37`

```dockerfile
```

-	Layers:
	-	`sha256:557fde12ff6ed9f4e2b76cd52acf6341a0274e2c4bf4e3b43ac8ee0f06e822d0`  
		Last Modified: Tue, 20 Jan 2026 18:48:34 GMT  
		Size: 670.9 KB (670928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8df61c7241efd298e58a8f71e51c947d1805284248579dd905106b1b4f5f530c`  
		Last Modified: Tue, 20 Jan 2026 18:48:34 GMT  
		Size: 15.3 KB (15327 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:72e1ef9e4fa41133dc18191a36681afd3f30bc010f6717436ec12240562c9a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86863204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092eea8ab914720178eb63822bc651c2a2052fdeeb008479d719f9b9678ba10d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 21:52:56 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 16 Jan 2026 21:52:56 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 16 Jan 2026 21:52:56 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 16 Jan 2026 21:52:56 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 16 Jan 2026 21:52:56 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:52:56 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 16 Jan 2026 21:52:59 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 16 Jan 2026 21:52:59 GMT
ENV RABBITMQ_VERSION=4.2.2
# Fri, 16 Jan 2026 21:52:59 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 16 Jan 2026 21:52:59 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 16 Jan 2026 21:52:59 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:53:05 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 16 Jan 2026 21:53:05 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 16 Jan 2026 21:53:05 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 16 Jan 2026 21:53:05 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 16 Jan 2026 21:53:05 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 16 Jan 2026 21:53:05 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 16 Jan 2026 21:53:05 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 16 Jan 2026 21:53:06 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 16 Jan 2026 21:53:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:53:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:53:06 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 16 Jan 2026 21:53:06 GMT
CMD ["rabbitmq-server"]
# Tue, 20 Jan 2026 18:50:07 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 20 Jan 2026 18:50:08 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-musl'; digest='0dc5e39dac98f38ad50f2aee15cfc5ea53c0ef5e649d79b41c2a7a94376aaf9f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-musl'; digest='fc7ca78e16824a2c77583d067ac1ae4eacbed1516a9a66bec50b5a772530d546' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 20 Jan 2026 18:50:08 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae232892808ba010301bc1e49752d4fec306162acb5cb0d01435a6d8596894a2`  
		Last Modified: Fri, 16 Jan 2026 21:53:23 GMT  
		Size: 40.5 MB (40454972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100abd2c8abf3480bc0b29b2f29075b065401a4cec82dbb82f13d1665b7da09a`  
		Last Modified: Fri, 16 Jan 2026 21:53:22 GMT  
		Size: 10.0 MB (9987909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e879355bf32506fde06fb15ae56e81b3c7facc200ccd334f8a520a303549142`  
		Last Modified: Fri, 16 Jan 2026 21:53:29 GMT  
		Size: 2.5 MB (2514388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146b8b41c3e5233f017068cedc142b17adac3b75f2a94aca37538cc718c8ba5d`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 25.3 MB (25317643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fab64ba23082a8a6ce109f85b45bd935cc696f863bb703a21002e83aa240dd0`  
		Last Modified: Fri, 16 Jan 2026 21:53:29 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53aff81e5782c4ed7d12da809ea09e000d6ed6d600b9dcdaf19b0f4fd71e2f0`  
		Last Modified: Fri, 16 Jan 2026 21:53:29 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093720c3ff621e7ec9bb94ca488520d40963ccdaeb2a01e319fc7597e7df6ffd`  
		Last Modified: Fri, 16 Jan 2026 21:53:23 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3933c2c38b8d60b1a3c56a61b3f1b0096dcfb4deb31c5c09044733f1e75f175a`  
		Last Modified: Fri, 16 Jan 2026 21:53:24 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e725f1eaecbc3dd214b085a842dd59cb846016f1fa81f3683fb22f3cfa0fcd0`  
		Last Modified: Tue, 20 Jan 2026 18:50:15 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28acde163a9739864f92af8ddd8afc1e003aebec9ee00e996cefb6a55ae68c2d`  
		Last Modified: Tue, 20 Jan 2026 18:50:22 GMT  
		Size: 4.4 MB (4390527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:22d98fe96aa89d8cb4c74d883c1a4d32e1ead6113f299f1dd17a030a22d77165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.3 KB (691286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839f10fa271e0c177fd3e844096b91e61f11dd4a3606161f2eef05a860a73e53`

```dockerfile
```

-	Layers:
	-	`sha256:22a890a98505a5b74a551afd261e7908c6404567a41a8d654aff89c4ba0965f5`  
		Last Modified: Tue, 20 Jan 2026 19:53:25 GMT  
		Size: 675.9 KB (675928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c08d7f12bdd5aaa4769611a5bf12b4a35f57adcaa457c066b89a8630e3c97b7`  
		Last Modified: Tue, 20 Jan 2026 18:50:14 GMT  
		Size: 15.4 KB (15358 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:c15b0a80585cc76064747f8e056cc07ca275d32f643866b7333d0a684636b185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73071148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aaa65b2c45f09ce96ec7c6a3b94b5acd608f4a64d80ee727790640232aace19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 21:50:51 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 16 Jan 2026 21:50:51 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 16 Jan 2026 21:50:51 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 16 Jan 2026 21:50:51 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 16 Jan 2026 21:50:51 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:50:51 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 16 Jan 2026 21:50:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 16 Jan 2026 21:50:53 GMT
ENV RABBITMQ_VERSION=4.2.2
# Fri, 16 Jan 2026 21:50:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 16 Jan 2026 21:50:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 16 Jan 2026 21:50:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:50:59 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 16 Jan 2026 21:51:00 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 16 Jan 2026 21:51:00 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 16 Jan 2026 21:51:00 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 16 Jan 2026 21:51:00 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 16 Jan 2026 21:51:00 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 16 Jan 2026 21:51:00 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 16 Jan 2026 21:51:00 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 16 Jan 2026 21:51:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:51:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:51:00 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 16 Jan 2026 21:51:00 GMT
CMD ["rabbitmq-server"]
# Tue, 20 Jan 2026 18:48:01 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 20 Jan 2026 18:48:01 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-musl'; digest='0dc5e39dac98f38ad50f2aee15cfc5ea53c0ef5e649d79b41c2a7a94376aaf9f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-musl'; digest='fc7ca78e16824a2c77583d067ac1ae4eacbed1516a9a66bec50b5a772530d546' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 20 Jan 2026 18:48:01 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c803aeada6dfe43204f0d9d37dbadafc6637c9f580fd06fd44efccda03874`  
		Last Modified: Fri, 16 Jan 2026 21:51:24 GMT  
		Size: 33.5 MB (33459157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fe8c74f32bf3b523cb3977395ed94c56040681db7993f0f160b8c252144ea0`  
		Last Modified: Fri, 16 Jan 2026 21:51:15 GMT  
		Size: 9.2 MB (9197842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20798a64402ff6a927e6bfcb5fa642134bab1ae8dfe36c7846889bce47897e41`  
		Last Modified: Fri, 16 Jan 2026 21:51:22 GMT  
		Size: 1.4 MB (1409000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d2b32d9276bdf9b00adbed12f61e2f5c62e575674b6f0d882993ca00e87989`  
		Last Modified: Fri, 16 Jan 2026 21:51:26 GMT  
		Size: 25.3 MB (25316995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5711759438c15dedb1ff63838b58322742e1ad32ecd0ce5a182a179b59bae88`  
		Last Modified: Fri, 16 Jan 2026 21:51:21 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f878c33bdf76180577861fcbc5714d407e5f1532710f7bc283d13df0f9f1c7a5`  
		Last Modified: Fri, 16 Jan 2026 21:51:21 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24cd23c17d08b5599336acdf4e6a23a1047ff9d334f2f52809adbd44645d309`  
		Last Modified: Fri, 16 Jan 2026 21:51:17 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b72fee3cdb08257f8e94681414c636a2165e9870015b29a0172fee735eb2a1`  
		Last Modified: Fri, 16 Jan 2026 21:51:21 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d49f87654c6b433356fcf9d8450351b576479cdd09279a874a98ee5074616ab`  
		Last Modified: Tue, 20 Jan 2026 18:48:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b9e69d5b87deae1f70725501dc17dd1f3626686100f993ff79390b367d9d9ea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.0 KB (685980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb340617f24fcee5e9e7505df56c02dabd547005cf7929c5265bb72249bde631`

```dockerfile
```

-	Layers:
	-	`sha256:bf53888909bc7210966b600e5a2198ea9088d481ccf5551ca3aa85299d1ce061`  
		Last Modified: Tue, 20 Jan 2026 19:53:32 GMT  
		Size: 670.8 KB (670780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ccc15c9af2f74358efe520e2be0613cb07cd142e58790c72f4c7b832f29c1b0`  
		Last Modified: Tue, 20 Jan 2026 18:48:07 GMT  
		Size: 15.2 KB (15200 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:d07c0d5acdb66a8cd063796818f59715dd1ba156cc6048ce3c2cc52933ed0a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37878e562f9035b17fc2f47875b6926fb7c9aa85d54323fb7b2faa5f9ec3b78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 22:04:51 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 16 Jan 2026 22:04:51 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 16 Jan 2026 22:04:51 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 16 Jan 2026 22:04:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 16 Jan 2026 22:04:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 22:04:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 16 Jan 2026 22:05:00 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 16 Jan 2026 22:05:00 GMT
ENV RABBITMQ_VERSION=4.2.2
# Fri, 16 Jan 2026 22:05:00 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 16 Jan 2026 22:05:00 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 16 Jan 2026 22:05:00 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 22:05:17 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 16 Jan 2026 22:05:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 16 Jan 2026 22:05:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 16 Jan 2026 22:05:21 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 16 Jan 2026 22:05:21 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 16 Jan 2026 22:05:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 16 Jan 2026 22:05:21 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 16 Jan 2026 22:05:22 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 16 Jan 2026 22:05:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 22:05:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 22:05:23 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 16 Jan 2026 22:05:23 GMT
CMD ["rabbitmq-server"]
# Fri, 16 Jan 2026 22:29:02 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 20 Jan 2026 18:46:05 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-musl'; digest='0dc5e39dac98f38ad50f2aee15cfc5ea53c0ef5e649d79b41c2a7a94376aaf9f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-musl'; digest='fc7ca78e16824a2c77583d067ac1ae4eacbed1516a9a66bec50b5a772530d546' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 20 Jan 2026 18:46:05 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e8476c5fb2ee33ff8d9e070314e37155747ff62db433260e64f2204af0f548`  
		Last Modified: Fri, 16 Jan 2026 22:06:14 GMT  
		Size: 34.1 MB (34067450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4acb3ea94eb6294cda790a2da6c6caab84dad75807dd9678053e3c6f171e066`  
		Last Modified: Fri, 16 Jan 2026 22:06:21 GMT  
		Size: 10.0 MB (9956659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721090c8af8b0bd3d26f3c79f71d5a6fa60a3c8f94081552584c57fd39b96c92`  
		Last Modified: Fri, 16 Jan 2026 22:06:20 GMT  
		Size: 1.5 MB (1542668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a86f398473b0aecc3aa4b34ed6350608a4ecdbda078411f0cee4a1dc87e9cc`  
		Last Modified: Fri, 16 Jan 2026 22:06:22 GMT  
		Size: 25.3 MB (25317065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d851ad983368416341fef6b5221a19dc3c488a86fd4f3181584f135e276bfbf1`  
		Last Modified: Fri, 16 Jan 2026 22:06:13 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00533fed9e70fdea30a78ed9df3821d7cd47eb63b056e0deb7a00400fa47dd10`  
		Last Modified: Fri, 16 Jan 2026 22:06:20 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097a74b7afe537f42918b5a4161b4a67fabde0dc8af8260a6137c8fe88fe137e`  
		Last Modified: Fri, 16 Jan 2026 22:06:20 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bd23d8b3fe4411a29a771b99e3b7fb55eb52887dc088efac1166d72340e4b3`  
		Last Modified: Fri, 16 Jan 2026 22:06:15 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bee1600f96da6c205352765bb73096215ddd220f07cacdc9f7f9074150ac22`  
		Last Modified: Fri, 16 Jan 2026 22:29:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9e493e7a6cb828d0f3efabfd7ac0c49982366d3a8a55bbfb80e054d317c5602b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.2 KB (686205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c2e4529512131f6e170ce10ddfad1ab1b195ec020cab8a35dc8fbd4d87ba4c`

```dockerfile
```

-	Layers:
	-	`sha256:9033c589476e770056a7273b4b5e504094f3bb4ad99f5080658dc3c406700570`  
		Last Modified: Tue, 20 Jan 2026 19:53:35 GMT  
		Size: 670.9 KB (670925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ecdc5186e3a1aa6fb921990602ae52e7ad19186e288cb733e85f8cc43ff4331`  
		Last Modified: Tue, 20 Jan 2026 19:53:36 GMT  
		Size: 15.3 KB (15280 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:73bef2385a88590ee283f18b9ad338f95b6e8fc841ba6228c207ced8aaac47b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78639193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff49f0bb406a2f5f4934d551a2d1f118b4cc72843070888603a9401e113ce79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 10:52:06 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 19 Dec 2025 10:52:06 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 19 Dec 2025 10:52:06 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 19 Dec 2025 10:52:07 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 19 Dec 2025 10:52:07 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Dec 2025 10:52:07 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 19 Dec 2025 10:52:19 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 19 Dec 2025 10:52:19 GMT
ENV RABBITMQ_VERSION=4.2.2
# Fri, 19 Dec 2025 10:52:19 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 19 Dec 2025 10:52:19 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 19 Dec 2025 10:52:19 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Dec 2025 10:52:56 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 19 Dec 2025 10:53:05 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 19 Dec 2025 10:53:05 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 19 Dec 2025 10:53:05 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 19 Dec 2025 10:53:05 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 19 Dec 2025 10:53:05 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 19 Dec 2025 10:53:05 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 19 Dec 2025 10:53:06 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 19 Jan 2026 04:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 Jan 2026 04:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 Jan 2026 04:35:40 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 19 Jan 2026 04:35:40 GMT
CMD ["rabbitmq-server"]
# Tue, 20 Jan 2026 05:54:44 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 20 Jan 2026 05:54:44 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.22.0/rabbitmqadmin-2.22.0-x86_64-unknown-linux-musl'; digest='ed3a1cf449e9ab7b24d35308e45973da671f7ed014bd8f8dff1908668e64ba36' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.22.0/rabbitmqadmin-2.22.0-aarch64-unknown-linux-musl'; digest='3348c28d466e95bf03a0a6c4ca3e8e985f44d85f630fe1cd7b72b12b7fb28dec' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 20 Jan 2026 05:54:44 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b16024bea26483c4ecdc60f404c46f57cb84a272c2b594f7f0c40f0b7ca50fb`  
		Last Modified: Fri, 19 Dec 2025 10:57:23 GMT  
		Size: 37.5 MB (37499627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76990ab68bc0fa49949abd7d842d2e3cec338241d21b8d9c5bfb92f2e9746b54`  
		Last Modified: Fri, 19 Dec 2025 10:57:21 GMT  
		Size: 10.8 MB (10786312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff510e29b3470403ce0d3bd1912ea1c8a301f188fadac32a33a5bf6a7940f12f`  
		Last Modified: Fri, 19 Dec 2025 10:57:20 GMT  
		Size: 1.4 MB (1449944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666f4cf3f20e4f9a788134aab3e97c7f6b6824f97c9ae8b231a412121e1b6d08`  
		Last Modified: Fri, 19 Dec 2025 10:57:22 GMT  
		Size: 25.3 MB (25317306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34db82d643b5fb83f1ee2788f9dec1b8d0ce2069d4353f8eec6335713bd0ed9b`  
		Last Modified: Fri, 19 Dec 2025 10:57:20 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b5c0f5d1d4ecba1131ed45747ea34fa1474cb0e4541d511e3c8cc2a4633adf`  
		Last Modified: Fri, 19 Dec 2025 10:57:20 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d9f78729104f576101b211bdac1f9d14473ccc12a8f0bcc0c8e7553f3d99fb`  
		Last Modified: Fri, 19 Dec 2025 10:57:21 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce64930298f84d1563e787be09e772a50afba7bafd4efe68a9fdeb2e3f70679`  
		Last Modified: Mon, 19 Jan 2026 05:55:53 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926c3184b0d325afbeaf5aa04cfa4e4aaaf438729e31767b15a16ec669c0c7b1`  
		Last Modified: Tue, 20 Jan 2026 05:55:38 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d9a70c9e6cfe70e1dd99c853bd8ba31c6ed28fdd85b284502b8b3a811af7588b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **689.2 KB (689177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aedbd24efeb6fa5f14fc5ce5bf66b6e4309be3941447cbdb866ce68929c1536`

```dockerfile
```

-	Layers:
	-	`sha256:a49d6c5d85017b423df7c4fb56409d93bdbc4738df4e124ffd2c4b2a45c9d0ec`  
		Last Modified: Tue, 20 Jan 2026 05:55:38 GMT  
		Size: 673.9 KB (673894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e4d4bf6d84a85377405cc95af549cc17ee7c96b0e7515cdad5aa0ee4b5261fc`  
		Last Modified: Tue, 20 Jan 2026 05:55:38 GMT  
		Size: 15.3 KB (15283 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:6c635e4e07fcb90f6866e7496028ae0a36bb6abee3086b60e17624a3b2914a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72825652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8f328b66601a74390130287d9cb5db4289a02ede6dec4a672f2241ce0353fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 21:52:59 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 16 Jan 2026 21:52:59 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 16 Jan 2026 21:52:59 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 16 Jan 2026 21:52:59 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 16 Jan 2026 21:52:59 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:52:59 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 16 Jan 2026 21:53:02 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 16 Jan 2026 21:53:02 GMT
ENV RABBITMQ_VERSION=4.2.2
# Fri, 16 Jan 2026 21:53:02 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 16 Jan 2026 21:53:02 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 16 Jan 2026 21:53:02 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:53:10 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 16 Jan 2026 21:53:11 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 16 Jan 2026 21:53:11 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 16 Jan 2026 21:53:11 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 16 Jan 2026 21:53:11 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 16 Jan 2026 21:53:11 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 16 Jan 2026 21:53:11 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 16 Jan 2026 21:53:11 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 16 Jan 2026 21:53:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:53:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:53:11 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 16 Jan 2026 21:53:11 GMT
CMD ["rabbitmq-server"]
# Fri, 16 Jan 2026 22:10:07 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 20 Jan 2026 18:46:30 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-musl'; digest='0dc5e39dac98f38ad50f2aee15cfc5ea53c0ef5e649d79b41c2a7a94376aaf9f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-musl'; digest='fc7ca78e16824a2c77583d067ac1ae4eacbed1516a9a66bec50b5a772530d546' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 20 Jan 2026 18:46:30 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:04 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681fb2b49f38fc322c40fb1799468be1f5389784f3e8609e81e794347497faef`  
		Last Modified: Fri, 16 Jan 2026 21:53:33 GMT  
		Size: 33.9 MB (33919393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca8701ce62ac7375c235a3c9b86f8f7212828166e788c73a7b7c31b53a49f26`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 8.3 MB (8346917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7432bfb1d8aedf7ebcc8b43143fb0f854e676924caa12048ca5cdc6446033c33`  
		Last Modified: Fri, 16 Jan 2026 21:53:40 GMT  
		Size: 1.5 MB (1515892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc09d82f9b13b99a95f414f2cc0d87f89d1e5221e969a48ef0e9a17c1ff53851`  
		Last Modified: Fri, 16 Jan 2026 21:53:32 GMT  
		Size: 25.3 MB (25317084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5de5e14df68c3039933bca59da323ad441396577da06be9681a2441488de32`  
		Last Modified: Fri, 16 Jan 2026 21:53:40 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205bac8595f6927080611fbc6a7f4e351e548dfbfda60d1728384f33459467ea`  
		Last Modified: Fri, 16 Jan 2026 21:53:40 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca299d1fe604aa912977e8a84faf451eb958acf6768ddc87514868e93f51ae5`  
		Last Modified: Fri, 16 Jan 2026 21:53:40 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9da55587f5889f5edd9f55f0128e933aeda98807bfaf0469d510f33cae825c`  
		Last Modified: Fri, 16 Jan 2026 21:53:34 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66d535c17b190d54a2f3482d5d885566a2de9e0b60f1c329971d3e5aefde09e`  
		Last Modified: Fri, 16 Jan 2026 22:10:23 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3b5f56a3ce22526e2342911a85070c2802d1654cf90676822ad5bf22dd057119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.1 KB (686125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d6b6b728d34078ad64c80d8f737ce3d272210c7cc99939a8640355eb61858c`

```dockerfile
```

-	Layers:
	-	`sha256:3e6599dc386911b53d6dcb6595302ee4be0275ce0dfe9654455f677eaf7e7e70`  
		Last Modified: Tue, 20 Jan 2026 18:46:42 GMT  
		Size: 670.9 KB (670891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65a0befe8ce73b66f3d309782d0b0b7d8b1cd5e34b54469ea80182354f36e722`  
		Last Modified: Tue, 20 Jan 2026 18:46:42 GMT  
		Size: 15.2 KB (15234 bytes)  
		MIME: application/vnd.in-toto+json
