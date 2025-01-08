## `rabbitmq:3-management-alpine`

```console
$ docker pull rabbitmq@sha256:4a4d400ce112808681712eaa8689d561fb48fd1e0a3a750088ce3e11a247e8ff
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
$ docker pull rabbitmq@sha256:f87e700130aa206c9438c408e7313ceb422344b7694ecd67ec72b1939324b572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87723783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f2bee5ada1e2f1e3ade706fad59033e6ce9c0467130ba8cbca1d78871461ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9124d348f6203c1b080ac51694e86499558b9d3cdef1f89cefa8b3b3c07eb389`  
		Last Modified: Wed, 08 Jan 2025 00:38:10 GMT  
		Size: 41.7 MB (41724815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f90326b986ea66d8538cd87e6e40a52b94cade2d42d12a9e82a5bfbb0a7147a`  
		Last Modified: Wed, 08 Jan 2025 04:54:32 GMT  
		Size: 7.6 MB (7597244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6678c7003132a45d3e0a5157c6db41326e8ee67857b91c884d5b793c1eb941c4`  
		Last Modified: Wed, 08 Jan 2025 00:38:09 GMT  
		Size: 2.3 MB (2277969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce53f9c5430ea4e7ace498f7dd96637b3ae9e5a25252545e7f4c03f147e69b19`  
		Last Modified: Wed, 08 Jan 2025 00:38:10 GMT  
		Size: 18.8 MB (18756242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cc370a9b7379109c421fd47baead7c378164fac482841bfbc6aee19df69133`  
		Last Modified: Wed, 08 Jan 2025 00:38:10 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4f29fe2a4396eacecca57118d1011bcb78d423cc9ce691da8ff9c9360b48e9`  
		Last Modified: Wed, 08 Jan 2025 00:38:10 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb6ff01c4ee9689e809a0e27e325dfbb758436186a58a15e39f21d9c76d6aa`  
		Last Modified: Wed, 08 Jan 2025 00:38:11 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccc7ec3a21f458fae494784474a714f730590915f97b999641e892c4aa9f4d3`  
		Last Modified: Wed, 08 Jan 2025 00:38:11 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2f0059f3233b1cf43f2dd54ceb7876234519e5d64ee75b4ff429b9a94a2796`  
		Last Modified: Wed, 08 Jan 2025 01:30:28 GMT  
		Size: 13.7 MB (13729540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:67f75efe059dbfd30ef0808474aaa7d459ac97e28924b79d6f57146c5904deb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1639277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22feaed0446747aa75e04888ed0ddc4afc630b4b94ec3ff9bf67b6b2c54c5f0`

```dockerfile
```

-	Layers:
	-	`sha256:3bc29696165e9e35d7e3879143329f5f05a31296363b4fa0feee9b60114b1b2e`  
		Last Modified: Wed, 08 Jan 2025 01:30:28 GMT  
		Size: 1.6 MB (1628366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b2885e2e53e2655e751bc1cd98d908c953f468c2c3fc1d75a4ab034d373545`  
		Last Modified: Wed, 08 Jan 2025 01:30:28 GMT  
		Size: 10.9 KB (10911 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:2be062bcafbba166bab9ef454307d7bc3c2c97bbc49bea04cdf2570b5b6e067c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77418949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef0e3418e2ab2cb4ffc048e41011f88cab9ef8b3e5470e70ccfcffe13a823b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfcae69b1410d49939dadc571747f5d97968ee9d9c94618afe642df5e71a735`  
		Last Modified: Tue, 07 Jan 2025 17:48:04 GMT  
		Size: 33.3 MB (33288346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3879d6a1074cdd3c13c93715b5963c8fde05efcc942958c21bd8a19057cfc37`  
		Last Modified: Tue, 07 Jan 2025 17:48:03 GMT  
		Size: 6.4 MB (6418904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf441b8a8969249807363e519736281016fbebf6c6ecaf914e64961340660d43`  
		Last Modified: Tue, 07 Jan 2025 17:48:03 GMT  
		Size: 1.2 MB (1225389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618ffc202c6919f0744b6a2cc8217982f9d9328d3a99a6493d19455397b5b6f8`  
		Last Modified: Tue, 07 Jan 2025 17:48:04 GMT  
		Size: 18.8 MB (18756170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875098b9d13d2ad7f8f50ba91a992e0917fadc482870cb9da47e72957a9a1e8f`  
		Last Modified: Tue, 07 Jan 2025 17:48:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e60fab0dce9e17d854b1fe940558028452a524cf3849018d5b698416f76e89e`  
		Last Modified: Tue, 07 Jan 2025 17:48:04 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490ed7e1e3568990b68c4680500e59e975f55741494c4be26fba1307dc371547`  
		Last Modified: Tue, 07 Jan 2025 17:48:05 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec69fa61439223eb01a278fb1c79d6808cba53b2a0781d422704b06b28adee5`  
		Size: 835.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438a7a029c0fe04508a5ca0350bc0ed0e12457079075402e97b874a5f9821eb0`  
		Last Modified: Tue, 07 Jan 2025 20:30:49 GMT  
		Size: 14.4 MB (14367345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f1855dd80853c9480f6d71fc5bd17cc071685f2e8323d99c2936c7447fec39be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 KB (10764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c12ba02195c4dcfc2700795022cb7ed2b1c437cdfe8146525c71047177343c`

```dockerfile
```

-	Layers:
	-	`sha256:2fe1370bde4fd438a2c1fe44ec98f2def44f94258a3cb4f7635e5e94cb54f346`  
		Size: 10.8 KB (10764 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:98212e98a91d91d7a7f5feac80e2d3d037b49955631f54e21b6dac6b985983de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76341946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8bb63359d186bb52e7d829a348e0fc8e652177b0de0970c1cf87f08408a789`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b36cee7ca597126290562cf6ed11da098ca91cf8c3ae60d0e29761ed02429c3`  
		Last Modified: Sat, 14 Dec 2024 02:01:34 GMT  
		Size: 33.2 MB (33219241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6952a386502354aae3d447d452b6fbcb9e1c393a4ed6c690ec5e533d97ea702b`  
		Last Modified: Sat, 14 Dec 2024 02:01:34 GMT  
		Size: 6.1 MB (6120501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deb4306b5961a85056e4b3996b51be2a7009248aff81219ae781744093e7c10`  
		Last Modified: Sat, 14 Dec 2024 02:01:33 GMT  
		Size: 1.1 MB (1133166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac625879eadc8ac5c1b2f260117e4c7bcc5578999ceebc82c62582546a2e2346`  
		Last Modified: Sat, 14 Dec 2024 02:01:34 GMT  
		Size: 18.8 MB (18756025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5e4e0e4b68af4b4e90cfbc5100421da902ce5e472b22f0a95f4b90d393961b`  
		Last Modified: Sat, 14 Dec 2024 02:01:34 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22ea49a54da8efc62582a4bd283d06c9d98add1ee91dedc7aa9b829c9668837`  
		Last Modified: Sat, 14 Dec 2024 02:01:35 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7eaff8a3aa4891790c05217ff29036a79f1af343f2330ce8c8b269e8af9169`  
		Last Modified: Sat, 14 Dec 2024 02:01:35 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1d257ed2ddfc6f52eb9029e5b7b248681c54c2054c54f712c25998b53b6a7a`  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc5651401a76d4391b3141c2553ebff5f3e374f93c94ee7db7b582649753e38`  
		Last Modified: Sat, 14 Dec 2024 02:19:02 GMT  
		Size: 14.0 MB (14011227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bc35847b315121821de4260454b53399f57cd6553e03a2f75d9c0a08eb7375e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1641747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b185e32505bbb00188a04fe75fb704839caa63f391d3c3ed92f1c66a851e3d`

```dockerfile
```

-	Layers:
	-	`sha256:cc82d74b3e268174e33d6af8807f5006524f9fb257fc75f00fdd447bb3087d71`  
		Last Modified: Sat, 14 Dec 2024 02:19:00 GMT  
		Size: 1.6 MB (1630768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42ac4191d2ee817a1b45d88cf8249e3569a297f2bbe0aa1a8c9f72af31da2b07`  
		Last Modified: Sat, 14 Dec 2024 02:19:00 GMT  
		Size: 11.0 KB (10979 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:29bf5f0dc909c0a2a8070d523452b3b2fee283a9cc718d15b07de3769e31b78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85904078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751ff6c1fef44f19f291728db25742f876ea9e53e1e17b40d4f12f32ad37e318`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad84355b218b39155bac05ef827041551dd2aa90c327edc6bbd90fa6d787cd2`  
		Last Modified: Wed, 08 Jan 2025 05:52:59 GMT  
		Size: 39.9 MB (39915048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bead00b48fd161f1109d43d9398d3a2749ec702c850d9797c5f695a156e1518b`  
		Last Modified: Tue, 07 Jan 2025 14:48:01 GMT  
		Size: 7.2 MB (7235079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4239044cf28d0980e56fba406a6b9017c232a27950d1c7913dc923aee4030d`  
		Last Modified: Tue, 07 Jan 2025 14:48:01 GMT  
		Size: 2.3 MB (2322581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c85fd4c93967670ef693d6416da6b7ef457abfa8080b040f7864103ae8f19ca`  
		Last Modified: Tue, 07 Jan 2025 14:48:01 GMT  
		Size: 18.8 MB (18756222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49fef107433df53bf348284afabe202647aa6efc734b85be407c4326a18a56b`  
		Last Modified: Tue, 07 Jan 2025 14:48:02 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01be404803ed65f88ac2993d28aa3afb61cc76e76970bac1336bd3bed207d6d9`  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a1229296215815f6a9b5a8a20a969aa2588ba808bf5bcae26f2f4564f406fb`  
		Last Modified: Tue, 07 Jan 2025 14:48:03 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99feb9c3012f2e2c5fb082ff0a9b7a4e13f50f58d29af9300300fe84a0eb78d7`  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1956958dc0d1eb896d5b40ae143b25336f0ac015bd00afdcec92681e361897`  
		Last Modified: Tue, 07 Jan 2025 17:23:25 GMT  
		Size: 13.7 MB (13690392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f14b6fbce860c92a1f5b573198f485e2434315624cf91a875891f44945856bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1640236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f6c41737aba9daeee12952192adb9bf329c2cb7617e0ff5932bd3abfe3ede1`

```dockerfile
```

-	Layers:
	-	`sha256:62725103729cc8116d97180f96bb15aaa6a3eaf8cc2a0db7ee1d871dfba2b5e2`  
		Last Modified: Tue, 07 Jan 2025 17:23:24 GMT  
		Size: 1.6 MB (1629233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:688d7dc638d85cbe69f447eb43e5cbd31f961cc293ef404c05434f1128a82615`  
		Size: 11.0 KB (11003 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:08f4441c4cd6226a660f8ee0994a1b1c8e86cfb9764abb327175da6a1b0670a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79544517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738a84fb4811b515eb912cdd7c4a540a3362571b145cad2d194605b0f9087a79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:1b51cef20fac755ea70acf005c7461407387b0deae88500e38a1982868469f7a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de9033a0d90370cbc690b0adbb1a2d29f48051ddcbe01c123255a8e10adaf1d`  
		Last Modified: Wed, 08 Jan 2025 00:37:19 GMT  
		Size: 33.4 MB (33370666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d44ec365b67bf8f1ec87ed7e6b73470781cb6d7b36f50e1b72de215bbe7b7e`  
		Last Modified: Wed, 08 Jan 2025 00:37:18 GMT  
		Size: 7.5 MB (7502211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d92c099ebca7b414239f623f08ad6b9a73e156e0142b1e342ecd1993563653`  
		Last Modified: Wed, 08 Jan 2025 00:37:18 GMT  
		Size: 1.2 MB (1229372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153b3a2e73f8e1e51ba41b5dff4bf684d650edc163e087297fa1254ccd17c2ef`  
		Last Modified: Wed, 08 Jan 2025 00:37:18 GMT  
		Size: 18.8 MB (18756101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4236dd2f57a611ed8c9f8927e9d5c8d21e73c541b06fe11289b304dd71a93f3`  
		Last Modified: Wed, 08 Jan 2025 00:37:09 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f288d8fdd84ebfaa72e523f9ac67cdf661f59ad5a068b7fdeae7b603c0efa2`  
		Last Modified: Wed, 08 Jan 2025 00:37:19 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f25c93669299b165b142915b89c288e54a4468752b4d1fd346c799d7aebf88`  
		Last Modified: Wed, 08 Jan 2025 00:37:19 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8ebc9f4e74b5a6f3f9a331fe27aa3b7b4f31e9ccbd0e1e537dbe1baafcdafe`  
		Last Modified: Wed, 08 Jan 2025 00:37:19 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8fccc7c3cc256e3786789fdc7952bf192c3133ae36a9bd711cce2a1680a2d4`  
		Size: 15.2 MB (15226144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:63843e86acc728a1e22f778d257bf8bf09c5f29f791ce2838215356e411d3196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1639058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c888ac1c144ba8bdc9f8c651299a52b1adbc3b104d8184029e34905aba1654e5`

```dockerfile
```

-	Layers:
	-	`sha256:ab845e10799493aa95574220319af7d78178f4eeb6dc22cc7d0c54bfb7387011`  
		Last Modified: Wed, 08 Jan 2025 01:30:23 GMT  
		Size: 1.6 MB (1628174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6295be426e62568faa9d96e280f179d8ac3299f4c10e14436f880c4207d34c71`  
		Last Modified: Wed, 08 Jan 2025 01:30:23 GMT  
		Size: 10.9 KB (10884 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:c22d0685f8c51b6716604a4874cd45f65588ddb48fdf311f3740d634834f2fb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80653290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8357d1eb2680453d3a37def1f12775b5353a07aa6686c6397ab8836304cd4f8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Wed, 08 Jan 2025 04:50:40 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50736003ae49594e1e9f686acab1a4fc32bf3d6305d71f7df93e953f3570db56`  
		Last Modified: Wed, 08 Jan 2025 01:02:53 GMT  
		Size: 33.7 MB (33744620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0285cf92df70f70d5e5c7d74810645e86ebfe56cfb8951b2fca461c1afeead0`  
		Last Modified: Wed, 08 Jan 2025 01:02:52 GMT  
		Size: 8.0 MB (8001656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb84ae6cda5d7b1e23a6ef2ad0e5326b57e8e0b5784c602f7c2bb7b5161b19a`  
		Last Modified: Wed, 08 Jan 2025 01:02:51 GMT  
		Size: 1.3 MB (1345111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367841d5b51a14a009789d26204df6be1a82f975bc41abb26cdb249bb72fdb05`  
		Last Modified: Wed, 08 Jan 2025 01:02:53 GMT  
		Size: 18.8 MB (18756096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94278334cc28c3c98f24a041a499a2fae26ea8a50def38d278a60bc362130a15`  
		Last Modified: Wed, 08 Jan 2025 01:02:52 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfc6aa076bfa0a00b706d67d8f13e651f326fa56a8f20cafbb93c86195634f9`  
		Last Modified: Wed, 08 Jan 2025 01:02:53 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdda85f699a09572d6f086f77bcaaf03cb6fa245372f048eb2f531cd539ffb0`  
		Last Modified: Wed, 08 Jan 2025 01:02:53 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e06eb3b241de57f1723df5129fccae415504a50537f9e0a89d42f7e6a121f48`  
		Last Modified: Wed, 08 Jan 2025 01:02:54 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e4d52de3b96decada9652b424489cc985760c6b42435f6372f5fef52cb4798`  
		Size: 15.2 MB (15236309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ab4c24851ee6b4aabfe2f4afeb6ed1d133c421d20b35fcc8b76ea8f2a6c5226d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1638559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bbf71c3d9036df1f024b69ca835377ba515788c4ab250bed1959f30e54d9a4`

```dockerfile
```

-	Layers:
	-	`sha256:5ba2caa5cd297d013dd28ed98929bf77b716ef41808a71cb93d27bfbb3d4e666`  
		Size: 1.6 MB (1627610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cbe45301b6e92e7e278179bf51d94a2629a5e7ba9728977ca2a0ede6bae00f4`  
		Last Modified: Wed, 08 Jan 2025 01:40:51 GMT  
		Size: 10.9 KB (10949 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:24767a0839135a8e97a16ad75bfa65314797825c91c72cf9480d70226625e628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81611422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6945739aa90aa2a6b8a11b5121c76e3c0a0342797c77af03c208d3792a3ba5eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d101dfaa1d966308871d898b0114ad10de26e2de2362bee857980900cdbcab`  
		Last Modified: Sat, 14 Dec 2024 06:00:34 GMT  
		Size: 34.7 MB (34703357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2399ae6285dbe54310639fef4eaa4c7ecf4afce5cf263d7a4da9c096ca6c6c2f`  
		Last Modified: Sat, 14 Dec 2024 06:00:30 GMT  
		Size: 8.8 MB (8752448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3d65e9f0b6ee3ee32880d37e579d48fbc4590695df130be3d6ed39808dd6b1`  
		Last Modified: Sat, 14 Dec 2024 06:00:29 GMT  
		Size: 1.3 MB (1265027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcac1fc9b7c58fb9f972485ad34fccae926a1d112e7c60ed2dab109ac1c1741`  
		Last Modified: Sat, 14 Dec 2024 06:00:32 GMT  
		Size: 18.8 MB (18756208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284721e9dec4ef035ad06ffc09e1aad97bec89916e486ef128d5d0d3cbb1df91`  
		Last Modified: Sat, 14 Dec 2024 06:00:30 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93f7ac7e76ef4ba8d8fe3ef62f300d0c65688f2442758f66b0b18a90d366730`  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e193fcdcbd15d1cf7b43755b587be306c6559e86a5084bbb9d9a407543d26c`  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b415d756dc67342213804a0f80b60c79a9cadca9d5acf0470efe0541c9d77c`  
		Last Modified: Sat, 14 Dec 2024 06:00:32 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7285c6ab3eaf936350b0c23a60d5a24b2a951aa80896df8e094389f2c8a76de`  
		Last Modified: Sat, 14 Dec 2024 06:11:40 GMT  
		Size: 14.8 MB (14778607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:831dc3eb1cc5f5f785f5324855d75b202c19c2bf72166e8069a653500ac5912a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1641369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071c5453899855251946b68c862b7a163717ec02fb88057b9dc52356dd387180`

```dockerfile
```

-	Layers:
	-	`sha256:1883bbfe0c6e37fc89ac8da530ce4d04da245926528650e9f6537d8f700de2b8`  
		Last Modified: Sat, 14 Dec 2024 06:11:37 GMT  
		Size: 1.6 MB (1630420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d38b8dd1d5a3514a346a1cbbec3e3aad9cab4373db8906657c31315d8f6061`  
		Last Modified: Sat, 14 Dec 2024 06:11:37 GMT  
		Size: 10.9 KB (10949 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:3367b28c3da9c6a3fb875e2e88a1e4253f56352676476de17410fa2bac1e7a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79327287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7b492e561ab83921641b12af4ca073ebaf13281fee4ea4a02020a141837cbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d609f80a5bf59592c8a7e0d9e3c7ba8d3efb4feeeace9a4ad6e4bd2fa61befea`  
		Last Modified: Tue, 07 Jan 2025 14:57:49 GMT  
		Size: 33.8 MB (33779044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a400588b47b9e3e94bfaa0140cc5b701de8ff1a2ef98f970d32c96f4a73fa8b5`  
		Size: 6.7 MB (6744382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c186e3d59874bda690fe281426b35e7a7f95e15bc8c818057d0056734d91a0e3`  
		Last Modified: Tue, 07 Jan 2025 14:57:48 GMT  
		Size: 1.3 MB (1323342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269583e901314efd209e79fcee1bec3476acd0b68be67b0de196f2611ffbfe8c`  
		Last Modified: Tue, 07 Jan 2025 14:57:49 GMT  
		Size: 18.8 MB (18756082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b5911f2a4d205f4fc63ade3ca0eb8e3412153cf8314421a00437297be79c1f`  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb4982f9828d637cc00995d65dc4360c23fd40836df35efe52514a681cc0c76`  
		Last Modified: Tue, 07 Jan 2025 14:57:49 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b685b0f9adeaf968a5697b2ef5814419c7c90479046a21076431da3a197fef`  
		Last Modified: Tue, 07 Jan 2025 14:57:50 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a61c1f37265003e609139708d3a575f75b200cde2380c8d0e5a119aff5fdb9`  
		Last Modified: Tue, 07 Jan 2025 14:57:50 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c266367b19794670f65f8963df0dd32a29b6dd46f3e906df8c42fbb368dee4c`  
		Last Modified: Tue, 07 Jan 2025 16:54:39 GMT  
		Size: 15.3 MB (15263235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6acffd67496d392614b30cee616b4ba505ea76afa39dad1b60abc212160f8b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1637976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16abe74b47d7bcc3843ded46521bfd078a69e11e346cb249e9c4085619eaeef`

```dockerfile
```

-	Layers:
	-	`sha256:1a5d9daf320d9b8733dcc53f457c98ea3eda38f6dced8c707bb971454bee9705`  
		Last Modified: Tue, 07 Jan 2025 16:54:38 GMT  
		Size: 1.6 MB (1627066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac5050ecf52b8b00056baf1879e911bb5b3b4038b162f7444513fbd109ef374b`  
		Last Modified: Tue, 07 Jan 2025 16:54:38 GMT  
		Size: 10.9 KB (10910 bytes)  
		MIME: application/vnd.in-toto+json
