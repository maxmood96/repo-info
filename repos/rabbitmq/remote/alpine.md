## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:4caf8be3d1f989304be1d0f5a5a3364688443dc0096de24ba8ffd8613f19eae7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `rabbitmq:alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:925e0b8251bdff63b8b91df42fb6bf6f89843d23e2e06d446180d2fbe4e252c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73664569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1077e9a373ff57ac7dd3087cf7b98dc8a7067db35b66599ae84b8107c23436e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 23:16:53 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 May 2024 23:16:53 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 May 2024 23:16:53 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 May 2024 23:16:53 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 May 2024 23:16:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_VERSION=3.13.3
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 May 2024 23:16:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 May 2024 23:16:53 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 May 2024 23:16:53 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 May 2024 23:16:53 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 May 2024 23:16:53 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 May 2024 23:16:53 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 May 2024 23:16:53 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 May 2024 23:16:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 23:16:53 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 May 2024 23:16:53 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c1666b2c13f3d2a5750b65b0dc5608a6c4595b58267ded3214a4f7b21d2f5b`  
		Last Modified: Mon, 03 Jun 2024 19:07:28 GMT  
		Size: 41.6 MB (41561262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8689f0214d1efd1ea522300fc7c8897263b3cc3bedf29b9c66ac2698c89e0b6`  
		Last Modified: Mon, 03 Jun 2024 19:07:29 GMT  
		Size: 7.6 MB (7567787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56356f4fc37373d8c84591858ccda010686589f182529a8802a56449b562b21`  
		Last Modified: Mon, 03 Jun 2024 19:07:28 GMT  
		Size: 2.4 MB (2405786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e09ac0aed3d874446fb1c4732d31e77b55f9e118adb2c4f3a0900b0d2930c3`  
		Last Modified: Mon, 03 Jun 2024 19:07:28 GMT  
		Size: 18.7 MB (18719256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea39665d8a9bd759dd94bdfbd1e4cb30b34b39e7a714c2a90d053d3173896df7`  
		Last Modified: Mon, 03 Jun 2024 19:07:29 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79fb845653d6565ffe55d487ea93009b77128bfb83e9fe8db52e94ed9b8e569`  
		Last Modified: Mon, 03 Jun 2024 19:07:29 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8339e1c57127d8efaed3889422430aa54dce6fe83d6348462a16857d0f541a`  
		Last Modified: Mon, 03 Jun 2024 19:07:29 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ed5c85134ced889eeefe949ec9a872ff5481c541980755ee639f463ed35c75`  
		Last Modified: Mon, 03 Jun 2024 19:07:30 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0751e449e3dc3d808e20da689b452a19892587e07015c2e098ec68056c483975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6745089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f0edc7e9afa9f31267563400136245d2c3822f4ec48beb97d6791969c583b9`

```dockerfile
```

-	Layers:
	-	`sha256:7cb744481695976873f394c19bca4a2705b75bff97bf96a914dc824ac0bf847e`  
		Last Modified: Mon, 03 Jun 2024 19:07:28 GMT  
		Size: 998.9 KB (998912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06595f598d06a4fcccd8f430a8933ad9bad5ac776ff1dea01814d22f0b59c8ef`  
		Last Modified: Mon, 03 Jun 2024 19:07:28 GMT  
		Size: 2.9 MB (2903254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc51b536d5014af100794f17c3bed8d68cec975b68361418306e8e78569a6f17`  
		Last Modified: Mon, 03 Jun 2024 19:07:28 GMT  
		Size: 2.8 MB (2781448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40557fa3de35c4330e114b451b63aade7c043767f383bfa2fec195c228330c9c`  
		Last Modified: Mon, 03 Jun 2024 19:07:28 GMT  
		Size: 61.5 KB (61475 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:a4bb86b6d145db4cab87bc12bb3433c25b6878f62a3804984b0c67af41e7af37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62869751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d87560c31f0fe155f597c2aef102fff2008ab241a2af4b2bbff80d0ebf36932`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 23:16:53 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 May 2024 23:16:53 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 May 2024 23:16:53 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 May 2024 23:16:53 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 May 2024 23:16:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_VERSION=3.13.3
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 May 2024 23:16:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 May 2024 23:16:53 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 May 2024 23:16:53 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 May 2024 23:16:53 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 May 2024 23:16:53 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 May 2024 23:16:53 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 May 2024 23:16:53 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 May 2024 23:16:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 23:16:53 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 May 2024 23:16:53 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d369e563d75ef22aada975555bb22425f6d469c583fb0f47f3f5427fd43fc3`  
		Last Modified: Mon, 03 Jun 2024 20:13:59 GMT  
		Size: 33.2 MB (33180669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e789a00e38c3def8d3b3768bcb168f1aa9c02a3a0d73b7249525bddaac954cd`  
		Last Modified: Mon, 03 Jun 2024 20:13:58 GMT  
		Size: 6.4 MB (6400973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1003cebd4e28a7f0670c1cd0a58d5af21e45debe89510f80381c992a1d3cd0c0`  
		Last Modified: Mon, 03 Jun 2024 20:13:58 GMT  
		Size: 1.4 MB (1401659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188305cd0a1c765c81868975d6ae4b9bad3978c4a0d8162a6906d5b765f6ed68`  
		Last Modified: Mon, 03 Jun 2024 20:13:59 GMT  
		Size: 18.7 MB (18719301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a3b7963ee912e742e5c2e95cd42b0acc95e136e875b9c464c6c8fee65942b6`  
		Last Modified: Mon, 03 Jun 2024 20:13:59 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d7e711566216dd5ac31b31c868b0ee1962fc3ec702a68d0d25831264934725`  
		Last Modified: Mon, 03 Jun 2024 20:13:59 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53147c70a72bf1c0254f0779fcff83563c17b97a4164f308e36d9749dfc2db39`  
		Last Modified: Mon, 03 Jun 2024 20:14:01 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ffe9c32e106b1ce38c6b970a8c9cdeda9bece2f83417c90d0ae0e45e9d5c63`  
		Last Modified: Mon, 03 Jun 2024 20:14:00 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d02cbb5583fea503a70bdc88ba3f1aa1a75d43e3bde4eb5f8c26ab9ae2f4b15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 KB (61444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e0faccfc7f437141ba3c776886ded242b982bada196b7d6915e735e51f32ff`

```dockerfile
```

-	Layers:
	-	`sha256:b966a4fcbf2e52eed68ad5aa7ae208ca3acea3c62aaed5d6993a71cbea1ae6f2`  
		Last Modified: Mon, 03 Jun 2024 20:13:57 GMT  
		Size: 61.4 KB (61444 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:c9c9df3561807b7b465f9934e6afbb14333c685c983952c0165c0bb31a189675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62112682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f12a090a9c840ea653a6d23c0f4c179cff9507c6ed24ccb279122d7454423d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 19:07:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 02 May 2024 19:07:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 02 May 2024 19:07:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 02 May 2024 19:07:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 02 May 2024 19:07:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 19:07:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 02 May 2024 19:07:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 02 May 2024 19:07:14 GMT
ENV RABBITMQ_VERSION=3.13.2
# Thu, 02 May 2024 19:07:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 02 May 2024 19:07:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 02 May 2024 19:07:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 19:07:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 02 May 2024 19:07:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 02 May 2024 19:07:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 02 May 2024 19:07:14 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 02 May 2024 19:07:14 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 02 May 2024 19:07:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 02 May 2024 19:07:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 02 May 2024 19:07:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 May 2024 19:07:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 May 2024 19:07:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 02 May 2024 19:07:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8161d8f3e6dc629e15a16b01b9791a16c8529b37abccc2afcfbf3a17d9f5bce5`  
		Last Modified: Fri, 03 May 2024 00:22:46 GMT  
		Size: 33.1 MB (33080541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65e4557c740fb15b47eece7174157004d20779729dd2e9ae8bb6107caf8a86f`  
		Last Modified: Fri, 03 May 2024 00:22:45 GMT  
		Size: 6.1 MB (6099224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b468f5d884bed8d02c8db363ac490e31f132ee0c89f3304e1ef934e3338dedd`  
		Last Modified: Fri, 03 May 2024 00:22:45 GMT  
		Size: 1.3 MB (1305609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a6b3daf8faeebe6aeb8e0b00404d3184d7642b960a27923d6558d642d3a7d1`  
		Last Modified: Fri, 03 May 2024 00:22:46 GMT  
		Size: 18.7 MB (18706661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3557657b03755a80d67a37bbc1c4050a8de0fbc9e817aaa865a07f23b71fc41`  
		Last Modified: Fri, 03 May 2024 00:22:46 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1860e55de1b1f0aaa2e70b506476b2bf38b0ad164aba14201f98973b2b380b7f`  
		Last Modified: Fri, 03 May 2024 00:22:46 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cf48eec463d2bc5bf3760f086e7d50b4c7782474af0a8bbd28a109652a780a`  
		Last Modified: Fri, 03 May 2024 00:22:47 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c6e7335c47001246e8fc6c54c7f634d9ce612c5cec8c36a6225f9596564d3d`  
		Last Modified: Fri, 03 May 2024 00:22:47 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:93b7512990ea8371b50115b3bfc7b8e4b30e5dcc077300891c2fc8ed40941e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c3a85b014c4c93efe1be7636ac044ac1380c89ae64ac6dbc2fb633ab898e6d`

```dockerfile
```

-	Layers:
	-	`sha256:661a9501363957628d7714d0c1f214f9d45b528478ce1d63244767dec77e3ae9`  
		Last Modified: Fri, 03 May 2024 00:22:45 GMT  
		Size: 993.7 KB (993708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1c9914cfd32f28a49add346d526192b808ecffff90588fe7a97bdccdf3e7098`  
		Last Modified: Fri, 03 May 2024 00:22:45 GMT  
		Size: 2.8 MB (2800055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f57800ddc005b7062a98ae525d38824ff902c7915dbc991631d0a5b898ae6d67`  
		Last Modified: Fri, 03 May 2024 00:22:45 GMT  
		Size: 2.7 MB (2679652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7d2fe6ed45d554abdf783cf68396ffdef0f52d7d0edddc4b44dd5b2133fb5ff`  
		Last Modified: Fri, 03 May 2024 00:22:44 GMT  
		Size: 61.7 KB (61663 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:2fba8f2cf43847f1318e54c8d8954486719d8ab7e70ba62e45d8feea44e6bb1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71417978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d337d744eaf15e66a1820d2fc6db088845ebdfbf21862b660f2820d5f135db60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 19:07:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 02 May 2024 19:07:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 02 May 2024 19:07:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 02 May 2024 19:07:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 02 May 2024 19:07:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 19:07:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 02 May 2024 19:07:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 02 May 2024 19:07:14 GMT
ENV RABBITMQ_VERSION=3.13.2
# Thu, 02 May 2024 19:07:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 02 May 2024 19:07:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 02 May 2024 19:07:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 19:07:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 02 May 2024 19:07:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 02 May 2024 19:07:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 02 May 2024 19:07:14 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 02 May 2024 19:07:14 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 02 May 2024 19:07:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 02 May 2024 19:07:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 02 May 2024 19:07:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 May 2024 19:07:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 May 2024 19:07:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 02 May 2024 19:07:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5c8847845aed6a3781a464cd18365e0cda3688f2c241c55ecebdeb203b8bad`  
		Last Modified: Fri, 03 May 2024 02:42:38 GMT  
		Size: 39.7 MB (39682713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2663a3b03050496c42d29e24ec56507e1cf57f6c1e3951b4e79a9031be8a04f1`  
		Last Modified: Fri, 03 May 2024 02:42:38 GMT  
		Size: 7.2 MB (7189423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988d62de9ae0ebc881db8c3b6a859a4e704ff8cadb35fd3b7876626d9e6f522c`  
		Last Modified: Fri, 03 May 2024 02:42:37 GMT  
		Size: 2.5 MB (2489919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83702914d34cdb65958d40296fc6cc6cec1970f476a470cc55db55176b23c297`  
		Last Modified: Fri, 03 May 2024 02:42:38 GMT  
		Size: 18.7 MB (18706463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc1b309f49ae40426ade76a42d7f70b47b4f8561c36d8b2d931b694922d770f`  
		Last Modified: Fri, 03 May 2024 02:42:39 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d071db94b20101f9b7f6669d732263f6a9f7f54ce5b245c4ac254c70eef7ff`  
		Last Modified: Fri, 03 May 2024 02:42:39 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4df7a5ad30f4e860c2b758a1c7e8a4020033db38087fafa4c7203647d40aed`  
		Last Modified: Fri, 03 May 2024 02:42:40 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b61a2f13c3e01d4f126db8d49883ef456eac5a30e1de994f234d85a932f1fd`  
		Last Modified: Fri, 03 May 2024 02:42:40 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0dd29661c03c9a39714f3b1f4c266bd8404cdf130b9d8867bd20d09ac6207b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6775100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16ad4ee15125801df71d1c8945a64ef9721555bc683c46a4dea7bfbcf893822`

```dockerfile
```

-	Layers:
	-	`sha256:01e247045d94741b4fba8e53145b9f87bc97967a2b3a8bf6e781954c92418701`  
		Last Modified: Fri, 03 May 2024 02:42:38 GMT  
		Size: 998.0 KB (997957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab72cc1942c9fe40e109073ef42aeea6ba1709c762ce8a2f596d15c534ed270f`  
		Last Modified: Fri, 03 May 2024 02:42:38 GMT  
		Size: 2.9 MB (2917947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faad313092387582364e130b037f521b0cc22231b97d826493a422cda18da0af`  
		Last Modified: Fri, 03 May 2024 02:42:38 GMT  
		Size: 2.8 MB (2797544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b45586cbb41fad66dc5f380447df66683aa6c18b6229b52dbc33078176d6652`  
		Last Modified: Fri, 03 May 2024 02:42:37 GMT  
		Size: 61.7 KB (61652 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:91166dedf9d78fc798dc929689ac36904139efe5d69068237b98f90f3a93ad13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64217661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a988a3f9f1314f8c7f8323f52cde6715ce8c8f245d82bb4252bb62f8a076ec85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 23:16:53 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 May 2024 23:16:53 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 May 2024 23:16:53 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 May 2024 23:16:53 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 May 2024 23:16:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_VERSION=3.13.3
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 May 2024 23:16:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 May 2024 23:16:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 May 2024 23:16:53 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 May 2024 23:16:53 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 May 2024 23:16:53 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 May 2024 23:16:53 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 May 2024 23:16:53 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 May 2024 23:16:53 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 May 2024 23:16:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 23:16:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 23:16:53 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 May 2024 23:16:53 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53472ed25a544a2c9730d214f55d7477d8ee092d1bf0575e65e631f5f723cb9e`  
		Last Modified: Mon, 03 Jun 2024 19:07:12 GMT  
		Size: 33.4 MB (33354190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81d2af33ef152852dfb8b63d32ac038dbbc4703e5a6e186a22e49e0d7ae27b6`  
		Last Modified: Mon, 03 Jun 2024 19:07:11 GMT  
		Size: 7.5 MB (7493804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8378d080afb47187f121c808a43cd801cfa2f96698fb90b1c1a348f72ae0c8d`  
		Last Modified: Mon, 03 Jun 2024 19:07:11 GMT  
		Size: 1.4 MB (1404308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfad940a067639142a1f3f6e34ea8e3cf541329532e85f7ae72da6aaac143cc`  
		Last Modified: Mon, 03 Jun 2024 19:07:11 GMT  
		Size: 18.7 MB (18719521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b52dab1b97db73bf3b7ca9d0a735fdaa01c2da23ea118f1340f29457c90c698`  
		Last Modified: Mon, 03 Jun 2024 19:07:11 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1f9e3f8003675c836ed02a363fd0839107ab26c4437a22f3aa653a98f36946`  
		Last Modified: Mon, 03 Jun 2024 19:07:12 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e57411cc62cc7dcbaded2c08390453c0b2be95f853bb0ecbcc0e657987460fa`  
		Last Modified: Mon, 03 Jun 2024 19:07:12 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87a85befad7a6b27a755e0f77b5a7927ba3cf648057128edec0e41ce165cbfb`  
		Last Modified: Mon, 03 Jun 2024 19:07:12 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4fc73e1b8832644b596a0293fe99d74721869beb1992dd48914f085bbcbab530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6721190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b5994cfb0ffe24c2d485273e0b7eabe4b02ec702703e33df1423b08e2f6928`

```dockerfile
```

-	Layers:
	-	`sha256:42a6eb92a784408841cd0e3566a4df1adf9910a5299895416da5620e1aa144c9`  
		Last Modified: Mon, 03 Jun 2024 19:07:11 GMT  
		Size: 994.6 KB (994613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16e3e6060faee0adf09f048248af3122568cc768785cacae65d4ea54b67e8c8d`  
		Last Modified: Mon, 03 Jun 2024 19:07:10 GMT  
		Size: 2.9 MB (2893476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9733ba227a2667fe3cf6c4011adabd4581ab889b7c0314e1d3aa0d4565be4cd3`  
		Last Modified: Mon, 03 Jun 2024 19:07:10 GMT  
		Size: 2.8 MB (2771672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:117bcc203113f29dd035a23d5603f2a7b7048341065352cb7fa9d757ad4add7e`  
		Last Modified: Mon, 03 Jun 2024 19:07:10 GMT  
		Size: 61.4 KB (61429 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:9cb18d920d90e9d3efd7802785097b4b91b3c38c4f36fb204a5f3a37228a32c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65173409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d272831ddcbb1329b5f439b1763d0d44fcf0c092814c017a842b19e018dc6f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 19:07:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 02 May 2024 19:07:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 02 May 2024 19:07:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 02 May 2024 19:07:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 02 May 2024 19:07:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 19:07:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 02 May 2024 19:07:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 02 May 2024 19:07:14 GMT
ENV RABBITMQ_VERSION=3.13.2
# Thu, 02 May 2024 19:07:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 02 May 2024 19:07:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 02 May 2024 19:07:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 19:07:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 02 May 2024 19:07:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 02 May 2024 19:07:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 02 May 2024 19:07:14 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 02 May 2024 19:07:14 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 02 May 2024 19:07:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 02 May 2024 19:07:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 02 May 2024 19:07:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 May 2024 19:07:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 May 2024 19:07:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 02 May 2024 19:07:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ceef9865cd34272590a2110e6313647be4032492b52d578256780578e8aa295`  
		Last Modified: Fri, 03 May 2024 00:37:44 GMT  
		Size: 33.6 MB (33609094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2201192a44ea3615320ba0dc078ef7e6e479967aba6fdc940709320fcdbeb67e`  
		Last Modified: Fri, 03 May 2024 00:37:42 GMT  
		Size: 8.0 MB (7981827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d9765c2cf3f0f21ed63b9d85bd3bdc520bda649ebbe494237c0c4c5eaa963a`  
		Last Modified: Fri, 03 May 2024 00:37:42 GMT  
		Size: 1.5 MB (1515653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7d00daa5f30911b18b0b17ba8f7949835f97b13d3e5578838848fa16d1d011`  
		Last Modified: Fri, 03 May 2024 00:37:43 GMT  
		Size: 18.7 MB (18706732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a454a180738293f6427053c6b31e2a0bbee5bf5a65d1de8b5dacc9bbfd4312`  
		Last Modified: Fri, 03 May 2024 00:37:43 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b8fdd367788818d3a2331910c4679f81b74ec96708b90f0be2c53c925b670c`  
		Last Modified: Fri, 03 May 2024 00:37:44 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8680b7829f83cb50fb42874790d3f27a405c1c9e07638e46a6641e4ee2e68430`  
		Last Modified: Fri, 03 May 2024 00:37:45 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdac70d89d39b8eb7562de2794afdad79f5f70a8b1e63bc36f66e1abdb5e544f`  
		Last Modified: Fri, 03 May 2024 00:37:44 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1bb14c8afeef37651fd3590a43c14420fccb33cc8dd04518f3c3d9c380d5bc59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6713789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01401e0f5d42ac588c1165f2e649339bc5a62a46116135ae7b7e5de064a85ae8`

```dockerfile
```

-	Layers:
	-	`sha256:d55bc4f4eaab854295ba1d826eeb23ead9e540ccb3c923d03c85d2ab2480d50a`  
		Last Modified: Fri, 03 May 2024 00:37:42 GMT  
		Size: 991.8 KB (991752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:439f0c452c55407884e1655ed67ed50788b204bade5b983c043450bfb288c6a1`  
		Last Modified: Fri, 03 May 2024 00:37:42 GMT  
		Size: 2.9 MB (2890454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:723a84148972bcb1cde6826e8689d8d7e89aa65e10878f2a675d857c204e2978`  
		Last Modified: Fri, 03 May 2024 00:37:42 GMT  
		Size: 2.8 MB (2770051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1b8b64c59f5e3277c8b8497b6ee4eecf45707e14b1912a6fbbba43efe3afa96`  
		Last Modified: Fri, 03 May 2024 00:37:42 GMT  
		Size: 61.5 KB (61532 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:5b7c29be882cb06ce838493236ed2efd8b9c1749693c01b081e1ece694d439aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63838821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3d3c884b86f0322b9b5c7b1d18af86950a81984010828dc5ec0920c1de03fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 19:07:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 02 May 2024 19:07:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 02 May 2024 19:07:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 02 May 2024 19:07:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 02 May 2024 19:07:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 19:07:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 02 May 2024 19:07:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 02 May 2024 19:07:14 GMT
ENV RABBITMQ_VERSION=3.13.2
# Thu, 02 May 2024 19:07:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 02 May 2024 19:07:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 02 May 2024 19:07:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 19:07:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 02 May 2024 19:07:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 02 May 2024 19:07:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 02 May 2024 19:07:14 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 02 May 2024 19:07:14 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 02 May 2024 19:07:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 02 May 2024 19:07:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 02 May 2024 19:07:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 May 2024 19:07:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 May 2024 19:07:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 02 May 2024 19:07:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b171ae1b998ab06ec70ad1b55143dc513c163f4039a481861e0866329910f6`  
		Last Modified: Fri, 03 May 2024 00:45:55 GMT  
		Size: 33.7 MB (33684742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7015fd44ec9d29c9e3903af7006a9ed877f23aad3fbbe4b2d64c6b84d610f7`  
		Last Modified: Fri, 03 May 2024 00:45:55 GMT  
		Size: 6.7 MB (6706511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2695f2206d9968a4a860020a840f4722608fd63b011b01f3e69bcfdbe6070a04`  
		Last Modified: Fri, 03 May 2024 00:45:55 GMT  
		Size: 1.5 MB (1496506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d70ed73bc995913dcb9c9099c6c33e7177611bc361f5c8ff105b865e295a9a6`  
		Last Modified: Fri, 03 May 2024 00:45:55 GMT  
		Size: 18.7 MB (18706676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c5a2f031506766bcc7d486e100e7fab84884dd4cc27c3cedebf4b603b11705`  
		Last Modified: Fri, 03 May 2024 00:45:56 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6fd924d86509ac09becfb9cec284555a62205dff0b3eacbbbb9a62b32d24db`  
		Last Modified: Fri, 03 May 2024 00:45:56 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7077dd2809b3644f2bf6ea7a946c580f49138db9ea88e1c10c481bfeeb069f`  
		Last Modified: Fri, 03 May 2024 00:45:56 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49606ee0d2f62b9ade0c594d89c01a0c6797c3db14494ae4bb551ad8196b5c39`  
		Last Modified: Fri, 03 May 2024 00:45:57 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6aa3d276a1df19bc110b291d32b255e211443e86deb4d76fe2df1f1a71a7bc14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6547876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568d619da8eecf488e7a94f7ad6a6d2354afe3c44e6312d128782226f7f071a6`

```dockerfile
```

-	Layers:
	-	`sha256:f0bd8e5db5c83a53965728979afdf41a67b9eac6b98d78e84022e5821daf3cb7`  
		Last Modified: Fri, 03 May 2024 00:45:54 GMT  
		Size: 991.7 KB (991718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4be60db744d79b7b8d845af3cfe748bb64cca7eaa7d626f9f0bdc0e7b903e623`  
		Last Modified: Fri, 03 May 2024 00:45:54 GMT  
		Size: 2.8 MB (2807543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0b58af172da4352f758fa4b6f3b6360ce6af1010406c9f3e553b8eb2c2983a0`  
		Last Modified: Fri, 03 May 2024 00:45:55 GMT  
		Size: 2.7 MB (2687140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6a74d2b32b01c8083a72db26e23a26f8dae2c844d7d271da9a81cb36972471f`  
		Last Modified: Fri, 03 May 2024 00:45:54 GMT  
		Size: 61.5 KB (61475 bytes)  
		MIME: application/vnd.in-toto+json
