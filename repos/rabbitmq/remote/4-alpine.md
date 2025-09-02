## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:82382de095bcc28dd29f5fbfa672f5226198278983f328c41d41a1db8791dcd3
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

### `rabbitmq:4-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:cd3cc954df93efe3cba00aa3e37d9f75d22b39404af350fe2bf52250ce000386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81997254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c4d21b842fc0f627d2a157a90ed5cb85c6a69a64c4472e2b9b209b43ca14dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Sep 2025 17:05:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_VERSION=4.1.4
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Sep 2025 17:05:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Sep 2025 17:05:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e599fd0ed15f9ddc40d5a77084242ac37a1b58be6425ec3559818abf37157c`  
		Last Modified: Tue, 02 Sep 2025 19:15:12 GMT  
		Size: 42.8 MB (42838482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8a62080e348341b700597ede5b05ebce0456630584e073c6d7791f400a500`  
		Last Modified: Tue, 02 Sep 2025 19:15:09 GMT  
		Size: 8.3 MB (8314147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b91a4c09ef9b7e44b831b6697e68a02cc0c083520254165ceb9a731d0cba071`  
		Last Modified: Tue, 02 Sep 2025 19:15:10 GMT  
		Size: 2.4 MB (2374083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d957c8ac73489f606b4fff1042e4d317f30f68d325173c025e35f03c74a1ac0d`  
		Last Modified: Tue, 02 Sep 2025 19:15:11 GMT  
		Size: 24.7 MB (24669113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e55e7db24708377fd04e5de748a8bdd244a36d066bc2a37cd32b9c38bbf868`  
		Last Modified: Tue, 02 Sep 2025 19:15:09 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb83d77f2d1563d269da5eee4c6fc81dbf22c4de59d85a6b205c045a51b08319`  
		Last Modified: Tue, 02 Sep 2025 19:15:09 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60eeb532b0222771d8f6a2d112d21460627624737a15fcc978f2899ee016ac2`  
		Last Modified: Tue, 02 Sep 2025 19:15:09 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0a9aa14624c8c14a2e29c48b3b1b31ecc91fe8da014c38c0958a4dda58d60e`  
		Last Modified: Tue, 02 Sep 2025 19:15:10 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6eb26cf3070df13924bc500b8a26393f296db5a05ff67859b45c26a8d1708805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6783110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e17c278b53758da65b9c7755ca97d1cbb054242d49df4d3a2e0628f7e858de`

```dockerfile
```

-	Layers:
	-	`sha256:17a6bb721357c3b663e8689df0c374fba7a7874736a194e2705286ac637b216c`  
		Last Modified: Tue, 02 Sep 2025 21:53:18 GMT  
		Size: 671.3 KB (671338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acda8a829e108ad5193d40a89b4ef3009aef546cb8f5f24e029ad5b69035176e`  
		Last Modified: Tue, 02 Sep 2025 21:53:19 GMT  
		Size: 3.1 MB (3102678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a48239355c09014338c0c15cbcbfd0336d8f3a9894ea31e5423f39c28df1aa6`  
		Last Modified: Tue, 02 Sep 2025 21:53:21 GMT  
		Size: 2.9 MB (2949137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:052fe3c489e95200656b776ae305855bba75dbc1133931b5078cfa9262ca2308`  
		Last Modified: Tue, 02 Sep 2025 21:53:22 GMT  
		Size: 60.0 KB (59957 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:7e4c131b92bc69d449c3e3bdb46849f99dec584efc5c9a4fba51796c8e251aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70048182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d70805edadc534f1fa89e3b0b1eaba337947496e8bffbfa53928dde587dcd33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Sep 2025 17:05:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_VERSION=4.1.4
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Sep 2025 17:05:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Sep 2025 17:05:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3be4fe3b50ab512a8ec703b54df0cb101d900e2c30c5d42027e2a44c8b27cf`  
		Last Modified: Thu, 17 Jul 2025 21:44:30 GMT  
		Size: 33.4 MB (33446070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e42e0de7fccd3307047296469cb5f9c9aa2b44e3cf60cb20e759cbf1005ff0`  
		Last Modified: Thu, 17 Jul 2025 21:44:28 GMT  
		Size: 7.1 MB (7100801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8772a75c3b551a77ce5065f3d0adb0bfa846a523d3405c6f8bfb05352bfd7f65`  
		Last Modified: Thu, 17 Jul 2025 21:44:28 GMT  
		Size: 1.3 MB (1329814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04a7720934ab19063e7323ad9fdaf2aadd908fccf3f5b03ec25d6cf56355b56`  
		Last Modified: Tue, 02 Sep 2025 19:07:08 GMT  
		Size: 24.7 MB (24668842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c67ea256a8d814a9e7a3f54a00afddf4a74ed89884f4727b2e981303636160`  
		Last Modified: Tue, 02 Sep 2025 19:07:02 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2d55899cdff9033e69c56d68abd818b9859aa10530570a17d3768272c7b729`  
		Last Modified: Tue, 02 Sep 2025 19:07:02 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9de00fb6c30ed0e71c4fce90ed222c9c66f2989127688fdcf2aa23ad406222b`  
		Last Modified: Tue, 02 Sep 2025 19:07:02 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f674bb720418e8d0734252e597f1f7347f462cdf86895e34a4bc5215ca9fbe4a`  
		Last Modified: Tue, 02 Sep 2025 19:07:02 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6097b50e875c648a46a5bfec88e3fb2d12ca6f52bf7b89e97dd40d52529aa4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 KB (59934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f9ba0a7b5a5050a6798ece22330759588dbada0974b69042580e72767877c3`

```dockerfile
```

-	Layers:
	-	`sha256:33352c246ce3bc0541602c84ba5a1c6b9710d042d74114b47805af34d01ad308`  
		Last Modified: Tue, 02 Sep 2025 21:53:26 GMT  
		Size: 59.9 KB (59934 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:b40864fdcf2fd2f942614a97e8be0b04ad4837316fb0e0139d00f5f3d9f51442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69233978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60d83cdf35d669c63864b75d1990c3a64e2b4628bfa020d6a835a5d01c6327a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Sep 2025 17:05:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_VERSION=4.1.4
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Sep 2025 17:05:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Sep 2025 17:05:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3e679d2d0ec7b1fb48080f6efc7bda79a7b95ba445c6df26a125283cd01709`  
		Last Modified: Thu, 17 Jul 2025 21:50:45 GMT  
		Size: 33.4 MB (33370909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41015ebcf72a938e41753268064bea0279729fd19f88886b54fb26e816a6a2ff`  
		Last Modified: Thu, 17 Jul 2025 21:50:43 GMT  
		Size: 6.7 MB (6747046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e7d05f7d5f0a96e96248de788396dabc6eddc9358fb2e96695b9fa8ae3524d`  
		Last Modified: Thu, 17 Jul 2025 21:50:43 GMT  
		Size: 1.2 MB (1226708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7706e3143ce082615155b805036078096e5c287cdb827eb3ce8ae8dd1dd735d1`  
		Last Modified: Tue, 02 Sep 2025 19:09:47 GMT  
		Size: 24.7 MB (24668533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1590ae5e7298462c2239249a042830d966f18c2f6712d223300b82a42085ea59`  
		Last Modified: Tue, 02 Sep 2025 19:09:40 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db17130e1ce2d2f8e8dfaed127365f755ac69587a57e5d1060f4f4e37644a90`  
		Last Modified: Tue, 02 Sep 2025 19:09:40 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da0f0a7132c4d7152e9dc2e14b2bb25fd7770c176cadc4d92c6495c207024d8`  
		Last Modified: Tue, 02 Sep 2025 19:09:41 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4ca69b403e4d1b01394478c738d252d5c47be0d1d8166cd96ccf58605678d1`  
		Last Modified: Tue, 02 Sep 2025 19:09:40 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7db942bb6971169ad175063e58dbdb5c612af0c52cea1bb10e04843803c858c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6547413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819adc946e3083c6239004e991824b59dcb980515e30c52fa19408b55d9e75ee`

```dockerfile
```

-	Layers:
	-	`sha256:a7ca806da14ba25926778b2dca47fb80cf53a1c871ed97b4368c92dadb60a91e`  
		Last Modified: Tue, 02 Sep 2025 21:53:30 GMT  
		Size: 667.1 KB (667131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b0d3ea857c49bc94b77664ab6489c091ff2829793f0609fa3be5ad4718c38f0`  
		Last Modified: Tue, 02 Sep 2025 21:53:31 GMT  
		Size: 3.0 MB (2987501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c0611b2e6b53f224669769cf0812cdd2376e736f9729af4ace11bcc5dbdb965`  
		Last Modified: Tue, 02 Sep 2025 21:53:32 GMT  
		Size: 2.8 MB (2832631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7adf47df9cfd12e6a67661c8df958f07bfa70cd3a02fd243d1484a3c1e45ff30`  
		Last Modified: Tue, 02 Sep 2025 21:53:33 GMT  
		Size: 60.1 KB (60150 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:94f139efd48e25067b249a44e5b875e0d80ff2901a303fd13db25377e3ca9f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81109522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdebeeff824714d34ecfb2a11f1b150b6ca91f4d011e03d2104ad49a983d535`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Sep 2025 17:05:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_VERSION=4.1.4
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Sep 2025 17:05:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Sep 2025 17:05:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8bdcf693be5c963cf94535bf3669b1f1d4902d7743b11018181272758f1496`  
		Last Modified: Tue, 02 Sep 2025 19:16:00 GMT  
		Size: 40.8 MB (40845334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6b3f3582fb7caf560c3f287b1665d94eb1d16c19bbe5682e7b2ea334964a66`  
		Last Modified: Tue, 02 Sep 2025 19:15:54 GMT  
		Size: 9.0 MB (9037858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160d3a5b29e1f0f3e6b76776d9f63f0ce57e0a6dd48c49b30ed40c8f68d1b9ff`  
		Last Modified: Tue, 02 Sep 2025 19:15:54 GMT  
		Size: 2.4 MB (2424740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02daf0542cfe850194e6056921c19b862fe164cc851b46a4a28eda46545bfcc9`  
		Last Modified: Tue, 02 Sep 2025 19:15:57 GMT  
		Size: 24.7 MB (24669091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be87324d27891b58a490a07b6099307879ceffa7c3a3d49959590c88ab33b08`  
		Last Modified: Tue, 02 Sep 2025 19:15:54 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030e4a78a41970fa5b5712edbdb9a3da2ef2675147aad135755ae6ce866d2370`  
		Last Modified: Tue, 02 Sep 2025 19:15:54 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53cc6624d9c0317446c46fc04727eb11a177e034ad88d074efe7415fed1e2f2f`  
		Last Modified: Tue, 02 Sep 2025 19:15:55 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4e420457f6caa14e76a0fe53074aa55c0a009e1436baf0008aff1ed46ea806`  
		Last Modified: Tue, 02 Sep 2025 19:15:55 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7847e2a642cc2f41496357b301980ae2ea17660eca5a657f531a21e1ec8f5376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6891414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343fc7143e701c0bcfbed6866b8288439ef784c212d0e27009bc0b2179ff4b36`

```dockerfile
```

-	Layers:
	-	`sha256:be506d3731fef965bef76ccfe067651a7f52d9f975b630b60fbfc8e608c3beb1`  
		Last Modified: Tue, 02 Sep 2025 21:53:38 GMT  
		Size: 672.1 KB (672131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79c97026fbbcf45c26e57f124b11f2ab8d7e22506eb765a471133b5a1da0a2cd`  
		Last Modified: Tue, 02 Sep 2025 21:53:39 GMT  
		Size: 3.2 MB (3156976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c32f59ba8415ff3e9c3f309f0e52e3102084152984cbeeaf38fb512580cc35d`  
		Last Modified: Tue, 02 Sep 2025 21:53:40 GMT  
		Size: 3.0 MB (3002112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5741d89a2bb62368e50590abb05d5f85d1b1b582eb17b3ce5d8c5cc451933b`  
		Last Modified: Tue, 02 Sep 2025 21:53:40 GMT  
		Size: 60.2 KB (60195 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:21101afd651cd9615772e0c9735853a52bba170489bf10afa11611b1ebbff655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71491087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996183a4c1f4bd8ff1e75691614a3234adc02cbfa3b7a1c0888821adf1eac135`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Sep 2025 17:05:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_VERSION=4.1.4
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Sep 2025 17:05:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Sep 2025 17:05:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8618e93aa64021f8b9a3cb5bd250ca35d3d6a8cc96a1f250f5aff00db0da0a7c`  
		Last Modified: Tue, 02 Sep 2025 19:39:27 GMT  
		Size: 33.5 MB (33546148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67d3cb0e9e149922fd74d731b7b8745c2ea2983bdb2d286cc90dad0056418ab`  
		Last Modified: Tue, 02 Sep 2025 19:39:29 GMT  
		Size: 8.3 MB (8327281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39dfd263bfd1cd36a95ba5dd9afa8d3105f54a53e8b02543e37e280e23052ddd`  
		Last Modified: Tue, 02 Sep 2025 19:39:30 GMT  
		Size: 1.3 MB (1332268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9076806a1b653f34d9ba906b0cdd232d6ba25ff6a31153762ff0764b3fd55489`  
		Last Modified: Tue, 02 Sep 2025 19:39:34 GMT  
		Size: 24.7 MB (24668637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56763fa4190a52eb72c0d3f6b819cc217d8577652b51d469f0b4b143558157b`  
		Last Modified: Tue, 02 Sep 2025 19:39:35 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0c49eeafb5a2a68797dd22c151a1e30c6aebe55d244a4dac44a86f8923a5f5`  
		Last Modified: Tue, 02 Sep 2025 19:39:35 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7810af273e08bc7800882f9a07de1ed9a4a8fa1a8093ef3f179c86fc105ca805`  
		Last Modified: Tue, 02 Sep 2025 19:39:36 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b6e287851e3cbd6ee167bfa805bd28c065b6d20dcc6298e317be98087cab13`  
		Last Modified: Tue, 02 Sep 2025 19:39:37 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3aa95e93640c7827bf75141964671172e782dde60038dbeed5bf01616353eff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6755950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67dfbccdc977462ebe63f19a33c69d4c4af347d89fe1b86bde3e08a99967ac7`

```dockerfile
```

-	Layers:
	-	`sha256:938ba693499db8686253bd9e82f38ce7bf03b1c6b1bbd1af29e8558444ced0c8`  
		Last Modified: Tue, 02 Sep 2025 21:53:44 GMT  
		Size: 666.3 KB (666333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa30a03bdf368c1fb48917c3680e6ad87d7eb291e7c32aef4827c518d6b028f4`  
		Last Modified: Tue, 02 Sep 2025 21:53:45 GMT  
		Size: 3.1 MB (3091624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:209706b524753c68d16e71afeb945b75ba004c3d29ea0ec894d3d9503d0a4154`  
		Last Modified: Tue, 02 Sep 2025 21:53:48 GMT  
		Size: 2.9 MB (2938087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8dd4b6bcd79a72d234992ca12d7b535db9b24d0569770c4ac8f0b9403a28b8c`  
		Last Modified: Tue, 02 Sep 2025 21:53:49 GMT  
		Size: 59.9 KB (59906 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:19a4b3905b4621fbad14a365c7b6d12cfe8172c7775eb39d1636e984943ba942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72623100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179398ec3d082bf6443cbeac765ed6107cf8caa16e7d5db815a30658d9e93276`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Sep 2025 17:05:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_VERSION=4.1.4
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Sep 2025 17:05:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Sep 2025 17:05:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f05aeb67e2981c70d5e15065b081eddb6d469a8e4342e310c046e76f8bcd70`  
		Last Modified: Tue, 02 Sep 2025 19:18:12 GMT  
		Size: 33.9 MB (33923908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6be847764ac2737d581ffb1a1421b32a6649bc435a4fae4ba7a8a191da31d23`  
		Last Modified: Tue, 02 Sep 2025 19:18:11 GMT  
		Size: 8.8 MB (8849240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38964b934976f9598ff3725d7bf04e37694bf348c846c7de2e9bf88db2afed82`  
		Last Modified: Tue, 02 Sep 2025 19:18:10 GMT  
		Size: 1.5 MB (1452397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d0882564f95958e9eb08aa4d117243d7357912f7b7dee5681744bcefbe8edf`  
		Last Modified: Tue, 02 Sep 2025 19:18:13 GMT  
		Size: 24.7 MB (24668691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f823ed05c359587dc7adf7136d065d2177e08b4fbdefe6f4069f4ac9dfd68e`  
		Last Modified: Tue, 02 Sep 2025 19:18:09 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0dc36873b72f7368ac76d29b7cb0fbc94244c626cbd89ae512faf148e3cf9f`  
		Last Modified: Tue, 02 Sep 2025 19:18:09 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2432ab9f6fac2407e78257bdcd88e7a014b4cc8c9a341963766ece329e9b08e6`  
		Last Modified: Tue, 02 Sep 2025 19:18:09 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6bf8e3d1fded9251dbf429153d29a6f76f411ff364916a53e6d48b27c776ba`  
		Last Modified: Tue, 02 Sep 2025 19:18:10 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2c948f6104fe1a821eb6bfce13527e6951c5c7b498ea5de9fc8903f81a9ab82b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6787781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7f6cc38fc76246a7b2f57ec038b64c053457c4917685c97fbd0159834cbe0c`

```dockerfile
```

-	Layers:
	-	`sha256:770f34c6ff72f8993b4974d20c03b839d5b9652991ba018e404f5e252b55a544`  
		Last Modified: Tue, 02 Sep 2025 21:53:53 GMT  
		Size: 665.2 KB (665178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c6bc75309884aac3094a5db136c8ca5b1a46d09dd66beb4442f197cbc8193a`  
		Last Modified: Tue, 02 Sep 2025 21:53:54 GMT  
		Size: 3.1 MB (3108730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c268026d33076e73ede3da647586b19ea0a252baf6b9c3e2f5bb8fe6b2c01c16`  
		Last Modified: Tue, 02 Sep 2025 21:53:56 GMT  
		Size: 3.0 MB (2953854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aaf72f43abe8e8ed20d047e03ccd25340d9df9bfa7f98ed3f2b6eebd70baf4c`  
		Last Modified: Tue, 02 Sep 2025 21:53:56 GMT  
		Size: 60.0 KB (60019 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:8dff801bde87722556d3da75052e1e93771bff68627e7adbe01beda5476a9e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78235487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ae0979264b4ed3caf5ebe818789c80a745317db66a6369a00a76fa264bbeb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 04 Aug 2025 17:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 04 Aug 2025 17:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 04 Aug 2025 17:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_VERSION=4.1.3
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 17:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 04 Aug 2025 17:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 04 Aug 2025 17:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Aug 2025 17:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 04 Aug 2025 17:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073ffd46dcb637c8d387387cc47d80a04e265c17305ecaf85b0db6cb5c7a8275`  
		Last Modified: Fri, 18 Jul 2025 23:47:00 GMT  
		Size: 34.9 MB (34878055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7a629412ea555306ed6a1c0603271783da81388541d4b65aacab9e8acd27aa`  
		Last Modified: Fri, 18 Jul 2025 23:46:58 GMT  
		Size: 9.9 MB (9863423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5dd69413818eb9ba00ac5708f3f11d9071a5877b3968515ebcbfdb51cf08cbc`  
		Last Modified: Fri, 18 Jul 2025 23:46:58 GMT  
		Size: 1.4 MB (1366276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e44a5b80f0b933b7db0a3709b70515e3b477d94f45ca30fbc14faa3b1d7cf1`  
		Last Modified: Wed, 06 Aug 2025 06:10:59 GMT  
		Size: 28.6 MB (28613180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b3508946f996f52e62530e4289b92b33fbae1cb875144bfbe5f24cae48b5da`  
		Last Modified: Wed, 06 Aug 2025 06:10:57 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2f0630593803eaee0e0a7c08cd928644e96bba50a9c18af60cc9007aaddab0`  
		Last Modified: Wed, 06 Aug 2025 06:10:57 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fdee96b8b8371b1f52641a93a447dc3a09e1a2671e7cdd280adfea53100cc2`  
		Last Modified: Wed, 06 Aug 2025 06:10:57 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0de390a5f16e8a3c279f3339d17df9a7d16df6ad69dc42b0d38954789bae36`  
		Last Modified: Wed, 06 Aug 2025 06:10:57 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fc9fee7c9e27e763d9d50bacdeb3f90d19bd5405dabb2959a01a3435575cd006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6867108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afcc1ea405606450b217cb9525672e286cf4388948258e00ad66ca073140fa6`

```dockerfile
```

-	Layers:
	-	`sha256:075639df7eeb77f6fab2f85616fd6151a1f69e49ceb63d4106dd5cbd63dfb748`  
		Last Modified: Wed, 06 Aug 2025 09:52:57 GMT  
		Size: 668.1 KB (668147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef30bba69be66a432f5faa13c77b8346f128f7d7394935d940810461abceeaf6`  
		Last Modified: Wed, 06 Aug 2025 09:52:58 GMT  
		Size: 3.1 MB (3146903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2858e37ce8032694c7edcad0f6ee6ebcf2faf34d4a7a35f85d43876dc9b287a`  
		Last Modified: Wed, 06 Aug 2025 09:52:59 GMT  
		Size: 3.0 MB (2992039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0bbbe455498d862ec5b682102ea72b830060ae11c2c24b0c85238dd4c48bcb`  
		Last Modified: Wed, 06 Aug 2025 09:52:59 GMT  
		Size: 60.0 KB (60019 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:62712a8f94ead72c5b1e6ed9e886d8fa2a16f6eca058339bd8f87cb044f060d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75161433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd42e082a087bdbb8d5479bcd93d440bd1631e5a66b0fb31f10bf40dcf59c6b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 04 Aug 2025 17:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 04 Aug 2025 17:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 04 Aug 2025 17:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_VERSION=4.1.3
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 17:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 04 Aug 2025 17:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 04 Aug 2025 17:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Aug 2025 17:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 04 Aug 2025 17:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f435efa4903bcc9bcce5e00045170d90ab626d8cc251aa7d16cc6e93034e7d`  
		Last Modified: Tue, 05 Aug 2025 02:03:46 GMT  
		Size: 34.0 MB (33958015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b5156b91c1a20d7472a7b6a543a2fdf0864bd2fafdaa8f5a9f1e81258d793a`  
		Last Modified: Tue, 05 Aug 2025 01:52:46 GMT  
		Size: 7.5 MB (7513271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ec2c7c9f66df6014c07e4bd4e65deae31c11517b3300c007c8a9357352b4fd`  
		Last Modified: Tue, 05 Aug 2025 01:52:44 GMT  
		Size: 1.4 MB (1430447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a799e6dbe85f7451ba4a13d548a0fc417a9f368c06dd01cfe6a2576e5cabc635`  
		Last Modified: Tue, 05 Aug 2025 01:52:50 GMT  
		Size: 28.6 MB (28612982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4f6af42c5220c8490752e16f4c6d42a6583fe4afb35ce6852c2b81f54d3965`  
		Last Modified: Tue, 05 Aug 2025 01:52:44 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db275c5c34aa3b6a56f31c4015df585c4e0917a3b3a6cd71d28c1da4d782ea1`  
		Last Modified: Tue, 05 Aug 2025 01:52:43 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008d13876c6cc2140323321b85d7b4c7e5ed87d59d7f0956bc1c9c030ccf0c00`  
		Last Modified: Tue, 05 Aug 2025 01:52:44 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9403ba672bf99029d6a26d07e2da1f308445a2ee05498454692f42b634aea76`  
		Last Modified: Tue, 05 Aug 2025 01:52:44 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:22b44a87d8059452847f9a7189557391eaeb2cae9a4725ff3908814b0e529ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6566588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcec4b33d12d24cc8023d321d6ba3ea92796af1d8e8fcc6e403787acc1984490`

```dockerfile
```

-	Layers:
	-	`sha256:aea25c79d76f7ef1beeed176471d5be00b4c452dae02a1a14f862eeaa63cfeb0`  
		Last Modified: Tue, 05 Aug 2025 03:53:12 GMT  
		Size: 665.1 KB (665144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:002efa0cb3fed8a28885dd4e593588299ea6fdfa029d384c4b4fa2eeefb42a8e`  
		Last Modified: Tue, 05 Aug 2025 03:53:13 GMT  
		Size: 3.0 MB (2998167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d83806333839668ac4daad18fe48dc76221ab529f05af526a8edc5a6d05da4a4`  
		Last Modified: Tue, 05 Aug 2025 03:53:14 GMT  
		Size: 2.8 MB (2843321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:007229a438d01472bf364563cedab72b74ae31a60169ed339ed49cd48c3f01e9`  
		Last Modified: Tue, 05 Aug 2025 03:53:15 GMT  
		Size: 60.0 KB (59956 bytes)  
		MIME: application/vnd.in-toto+json
