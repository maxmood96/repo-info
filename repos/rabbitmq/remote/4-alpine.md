## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:e045b5166b9188a38eee5c99411709aa1f0ffa2ac75664053e64cb69411f7c32
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
$ docker pull rabbitmq@sha256:d720022ec369dcdffada072a19a1a5e9cbec7b997a06a20b3e540271d25ad154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77583144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21da76d58b538715ce6044d1d48492c7a5a6f86e29908905ea682b9246b76d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2025 18:05:23 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 06 Feb 2025 18:05:23 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 06 Feb 2025 18:05:23 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_VERSION=4.0.5
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 18:05:23 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 06 Feb 2025 18:05:23 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 06 Feb 2025 18:05:23 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Feb 2025 18:05:23 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 06 Feb 2025 18:05:23 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fdf3d7a711c8fb5ad8750d45f48c7c210ff2cfce659e3cb79f482ae1c848df`  
		Last Modified: Fri, 07 Feb 2025 00:38:03 GMT  
		Size: 45.0 MB (44993680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f357f21e65066c4e9bce5283490387ae5ffc317a18cd8658bb6c0b462685c10`  
		Last Modified: Fri, 07 Feb 2025 00:38:03 GMT  
		Size: 8.3 MB (8309044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c328e7651cb20959e2453ed9e7feb106e07fdc22934ce4faa80dfb65b6be64`  
		Last Modified: Fri, 07 Feb 2025 00:38:03 GMT  
		Size: 2.3 MB (2277977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10042c984327a08e0e00f0f152239278a343a4d279342535a32d80cd02e03a1`  
		Last Modified: Fri, 07 Feb 2025 00:38:03 GMT  
		Size: 18.4 MB (18358981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079cdd5574712e5a889f5ec5c0c1b25626bac935f99f2381637109105765a3e9`  
		Last Modified: Fri, 07 Feb 2025 00:38:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce17d81ec6346942de25bed18e7b6939cce2b6fa500cf24f57ba5087891f24b`  
		Last Modified: Fri, 07 Feb 2025 00:38:04 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada2ec92324c11ac105483593d95ce538816ce91109ce3b80a348bdaf71b259b`  
		Last Modified: Fri, 07 Feb 2025 00:38:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542e875cf4a119c0117b59cdf9293de329f58a0ce0eb79c19867538086eaa5d8`  
		Last Modified: Fri, 07 Feb 2025 00:38:04 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bbb3908af9198094d16ab171c744996e416cfdba71050645994af55d062a5d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6458424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033fd56ee8c573e3cdd762321391a65dcb7ce82d2e4f1ab86913406ca58680b9`

```dockerfile
```

-	Layers:
	-	`sha256:6cff4a57fd15e868a883a1ded27a87f4b07ed1fb9ecbc61d1d31e9a1553adfcf`  
		Last Modified: Fri, 07 Feb 2025 00:38:03 GMT  
		Size: 538.2 KB (538238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95fb75c8a3ee6f1c87e8769c2ef22fc3e08049330d62ca98aaceebd2a2025a54`  
		Last Modified: Fri, 07 Feb 2025 00:38:03 GMT  
		Size: 2.9 MB (2932253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79f0a7b5a0859f79ab9e29581c69d8f00a78d9d27843d35f57874a1b0d0ce029`  
		Last Modified: Fri, 07 Feb 2025 00:38:03 GMT  
		Size: 2.9 MB (2928075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174aeb91f0010e774eb43358a4403cc5de006ea38529736c195c9d92be21f559`  
		Last Modified: Fri, 07 Feb 2025 00:38:02 GMT  
		Size: 59.9 KB (59858 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:a3d1dc961c7ec19af9412a31c2308e4f91527120e3b0527e119fc0bcaa7860a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65645975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3075e69270b9181604ff48bbfb657f13b84ff09fa1fb51d7ae6e83f5e8823048`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2025 18:05:23 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 06 Feb 2025 18:05:23 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 06 Feb 2025 18:05:23 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_VERSION=4.0.5
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 18:05:23 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 06 Feb 2025 18:05:23 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 06 Feb 2025 18:05:23 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Feb 2025 18:05:23 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 06 Feb 2025 18:05:23 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607174c40719d52624fe8e287bf67d77cc0d725af93f5b6225322b2bcc9081af`  
		Last Modified: Fri, 07 Feb 2025 00:36:31 GMT  
		Size: 35.6 MB (35603999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a98fc17984184c0c471fa30c865753efd2f9a1149ac29b1457e3513796900ec`  
		Last Modified: Fri, 07 Feb 2025 00:36:30 GMT  
		Size: 7.1 MB (7092048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec94fed9f8a3baf5ccdff8570c3de8c1868de02ba2f4708fa9e34905198328f`  
		Last Modified: Fri, 07 Feb 2025 00:36:30 GMT  
		Size: 1.2 MB (1225390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd93ff21efbd6ac1da277463251b4aec1ad3633d9737fe29f8b7045b1d0ea1ce`  
		Last Modified: Fri, 07 Feb 2025 00:36:58 GMT  
		Size: 18.4 MB (18358907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a64a3779f3d838d785ff4785d233f36b552c8ecbbb5031e3e6aca3aab56926d`  
		Last Modified: Fri, 07 Feb 2025 00:36:57 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd41094da70d1ab05cab14dbcd3b5185c492333913e989ec3086108fd7a2da9`  
		Last Modified: Fri, 07 Feb 2025 00:36:57 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c396fcd24f5e20fde3e6635aeb61ebedf0d2dfe9bd05923631a97fc48d3639c`  
		Last Modified: Fri, 07 Feb 2025 00:36:57 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab08cead817839653c5d4a453aadbbe6a0024e8940aa553806bed07606af50a`  
		Last Modified: Fri, 07 Feb 2025 00:36:58 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:788fef7f0ef9452067040535912682e3020197b8f4f24321f54d714f29dc15a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 KB (59836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d713e2bd53e0f8c8a144f0bcae2691f72a452d81a8378bedd205a47b46ba45f`

```dockerfile
```

-	Layers:
	-	`sha256:284de3f2568709ba1b88f4eb7a97e9e4d223c2f2a6f6265273f54f8bb8713f1d`  
		Last Modified: Fri, 07 Feb 2025 00:36:57 GMT  
		Size: 59.8 KB (59836 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:6597a1d9567f2a14fef721fc2f303c35a6b8b97377555e77c95b57f9cd01f9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64842794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd5cd68eb2a4a9932e7eb888a1186bc09ca0551ebbdb2340af07972580f402e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2025 18:05:23 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 06 Feb 2025 18:05:23 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 06 Feb 2025 18:05:23 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_VERSION=4.0.5
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 18:05:23 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 06 Feb 2025 18:05:23 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 06 Feb 2025 18:05:23 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Feb 2025 18:05:23 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 06 Feb 2025 18:05:23 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecdda70ba1d6241978e7959fea459d4efc5114e992af36327c27c2302f7847d`  
		Last Modified: Fri, 07 Feb 2025 03:55:47 GMT  
		Size: 35.5 MB (35520109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057187fc83f492a12b65a7d897b960fe1ca5138fd07472876a50da5cb4da4a8b`  
		Last Modified: Fri, 07 Feb 2025 03:55:46 GMT  
		Size: 6.7 MB (6731641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cb8934ed2831473ef1cb8cc0c103ce6c06a3e9dc437a2910ca5850c86161c9`  
		Last Modified: Fri, 07 Feb 2025 03:55:46 GMT  
		Size: 1.1 MB (1133175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510f81a22f9f7ef0b76b8f68a26b37e964a8221d2179aa9a3d2c3313c6ee6888`  
		Last Modified: Fri, 07 Feb 2025 03:57:48 GMT  
		Size: 18.4 MB (18359015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edc91dd084b53e0613a8e03dbae646efc55c3ad470d664165f249ae06f67de8`  
		Last Modified: Fri, 07 Feb 2025 03:57:47 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc37d09ced11fe7200f7cc3f20702ed6735bd34e8c44d9d5885f8495b16973b7`  
		Last Modified: Fri, 07 Feb 2025 03:57:47 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0b23c8214e6d5c326e9e8f6251ea1e07f002dacc9f0f39dd511593143e47b6`  
		Last Modified: Fri, 07 Feb 2025 03:57:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fa00a43b789a20a6ccc932a4e64dbe82fc51f9863e0b40d8f9e40bb9693f44`  
		Last Modified: Fri, 07 Feb 2025 03:57:48 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:cc121a64b2143e266b61dae948748735ffa8281282b41daee49f74fdaeec054c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6494325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2b19a1dd2dfeba668c1e31e9b84433b60624522c7156b976815dd7b54d2024`

```dockerfile
```

-	Layers:
	-	`sha256:7f33e2a808e3f155bd8f3678dcde1bf8a03031b150187c533efac1a2e5611167`  
		Last Modified: Fri, 07 Feb 2025 03:57:47 GMT  
		Size: 653.9 KB (653933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:497984504949dde579f76b2c01424dd38268ed98e8fdc9634ca23c19122ff540`  
		Last Modified: Fri, 07 Feb 2025 03:57:47 GMT  
		Size: 3.0 MB (2967737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed568ffb7f41fd3d11628baea7cb54b7f94e434982ad906969ce8ea58608023e`  
		Last Modified: Fri, 07 Feb 2025 03:57:47 GMT  
		Size: 2.8 MB (2812604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdc201be5fcca2e11585d8548173da9a4ca84c10bd6be417a5f261deb7a717af`  
		Last Modified: Fri, 07 Feb 2025 03:57:47 GMT  
		Size: 60.1 KB (60051 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:38549e0bacf0cb3310abb2377201b3c590a241b668c257f7813f938b2080859e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76708973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a023d6fb977b635a62f685fb9ab698bb8c6666d29bdc0683134c76989c605de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2025 18:05:23 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 06 Feb 2025 18:05:23 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 06 Feb 2025 18:05:23 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_VERSION=4.0.5
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 18:05:23 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 06 Feb 2025 18:05:23 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 06 Feb 2025 18:05:23 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Feb 2025 18:05:23 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 06 Feb 2025 18:05:23 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb93c8760e0f4fa405f49e9092c117a6a643225c13530bc398832fa4adc80a74`  
		Last Modified: Fri, 07 Feb 2025 02:58:00 GMT  
		Size: 43.0 MB (43001403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9579a134a5f2e3d53c0cecf041e4209773b1f1ed1db42def28c43fbfa2e6fee4`  
		Last Modified: Fri, 07 Feb 2025 02:57:59 GMT  
		Size: 9.0 MB (9031961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9f65fa5cfe7b99e33fa09c464169dbfdc9fb22293fe44f209132870ebb7cf2`  
		Last Modified: Fri, 07 Feb 2025 02:57:59 GMT  
		Size: 2.3 MB (2322572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6014e6366f58d02df15750dcb5dcc812ce697f6f8cdc54d5025d421fe82333`  
		Last Modified: Fri, 07 Feb 2025 03:06:04 GMT  
		Size: 18.4 MB (18358943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e907442080e57226ee988b82fad72b98f8fd1bd27e728cbe3e28919aaed987c8`  
		Last Modified: Fri, 07 Feb 2025 03:06:03 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8557d983b4d8f4e9c87dc9c83381171909ccf8fd88e29f6df05a7f5aee88de6b`  
		Last Modified: Fri, 07 Feb 2025 03:06:03 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189ff428b38958b5d389213aae4422148ca67fdc0eda09e63944b1bdf1d15aaa`  
		Last Modified: Fri, 07 Feb 2025 03:06:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a84304dca0825e9dfe4ec933012581032c8735cd5d3e54ef0f105a8cac26dc`  
		Last Modified: Fri, 07 Feb 2025 03:06:04 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:aa6a021de993cd6cc5ad8ef2e40e450dea1f62e753253c82d63f450dfb5f2702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6836933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2794c5cb3070b460225a2cb234a01e7a8159ae1108cc31f441521e3d5b1e7340`

```dockerfile
```

-	Layers:
	-	`sha256:2e46697492b247990edb5b1512169fd5ab46dc6535f667da15f3707d2f4bb8b8`  
		Last Modified: Fri, 07 Feb 2025 03:06:03 GMT  
		Size: 658.6 KB (658579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f052f3a7894cd570f4c8e638777743f29cc9ac16eabfe3be6ea6550fe074bfb9`  
		Last Modified: Fri, 07 Feb 2025 03:06:03 GMT  
		Size: 3.1 MB (3136692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7690350742fb45ff422f4ecb67c4916a4725a894ee7cca674845046a56483b4`  
		Last Modified: Fri, 07 Feb 2025 03:06:03 GMT  
		Size: 3.0 MB (2981565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25f47a629cc4403708842da0ed80f7d22900a874c0b51fb0c49d12641de10a8a`  
		Last Modified: Fri, 07 Feb 2025 03:06:03 GMT  
		Size: 60.1 KB (60097 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:24598413c82a6636ebc4d7100e95b9922371351d30a7fde2496cf1c14a872c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67068013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f294efce66882c4bea2c167d8a1115b27231cccdd36a0d7dbc3c2e6efd9ee331`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2025 18:05:23 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 06 Feb 2025 18:05:23 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 06 Feb 2025 18:05:23 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_VERSION=4.0.5
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 18:05:23 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 06 Feb 2025 18:05:23 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 06 Feb 2025 18:05:23 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Feb 2025 18:05:23 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 06 Feb 2025 18:05:23 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e331cff379516e21a2a9e9d162587ae6d731d856570873665bfca16900ed860`  
		Last Modified: Fri, 07 Feb 2025 00:37:08 GMT  
		Size: 35.7 MB (35693905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99807e76ee6a9b8a53e6a3135b9d0d225fcfab9d2bedc52e4b82a9f7a508cac2`  
		Last Modified: Fri, 07 Feb 2025 00:37:07 GMT  
		Size: 8.3 MB (8320830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedcd1f4b19a04df36c98904cc8c0f8af251535e2ecdeb79ed1ac58b0a5a40c5`  
		Last Modified: Fri, 07 Feb 2025 00:37:07 GMT  
		Size: 1.2 MB (1229388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc751df527329ec4ec3e9cf48ec6da5de67d4b1c5eb7188d9533d468cf6aa679`  
		Last Modified: Fri, 07 Feb 2025 00:37:07 GMT  
		Size: 18.4 MB (18359016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c12c47a4054d290d7022d3729e057d5e6be22d8d20375cb569da6f0d753679`  
		Last Modified: Fri, 07 Feb 2025 00:37:07 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0f5af02f7b577a22c4c48a12b758906fa65ec29079b444adfa4a523655d857`  
		Last Modified: Fri, 07 Feb 2025 00:37:08 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89e021123a1572dc7ade97ad135dca6e7a33060daa7911fdd403bd1e80d5239`  
		Last Modified: Fri, 07 Feb 2025 00:37:08 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4057dab5ebf3790e066302a73995bf2aa25659faf0e6ff1b202367fbd2e32b`  
		Last Modified: Fri, 07 Feb 2025 00:37:08 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6af4f591462a9826af4f76972c0480c10de16dfe9c15ad8872b71d19e671d735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6431619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec581f0ff81cb9a8eed670ad910d34eaefe2afda79615bae421638d70027cef`

```dockerfile
```

-	Layers:
	-	`sha256:b0d2453591a04474fe26a8d21bba5a292eb3dfc9f1aee7230bc9ae0466639314`  
		Last Modified: Fri, 07 Feb 2025 00:37:07 GMT  
		Size: 533.6 KB (533587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a732ec1b13b75ae8864fef196ec967654c274c21e9c9833178c97f6a69a8fcd4`  
		Last Modified: Fri, 07 Feb 2025 00:37:07 GMT  
		Size: 2.9 MB (2921199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:139e1c3580a8913c7af5a275ca6f8d9602a35ed2a72abc613ad1b74be1aa9a1c`  
		Last Modified: Fri, 07 Feb 2025 00:37:07 GMT  
		Size: 2.9 MB (2917025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2cf5fb5a0255e78aad3eaed6f1e93f8b6965edf5343d30a744ae877ee5cb4be`  
		Last Modified: Fri, 07 Feb 2025 00:37:06 GMT  
		Size: 59.8 KB (59808 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:86b051ecfa3aa6bd1ad79169ead36d1a17221ecf6eab7cff2d7e4a4fdb08600c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68209335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb0ef64bc2ceaac4a35ca72c767bde0aec0fa549d8656546d660fdb7e3d0542`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2025 18:05:23 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 06 Feb 2025 18:05:23 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 06 Feb 2025 18:05:23 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_VERSION=4.0.5
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 18:05:23 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 06 Feb 2025 18:05:23 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 06 Feb 2025 18:05:23 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Feb 2025 18:05:23 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 06 Feb 2025 18:05:23 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50dd96f3aa6d882ea240d85fc4932d9903370df40eff5f1808e2ad7a015fb16`  
		Last Modified: Fri, 07 Feb 2025 01:59:31 GMT  
		Size: 36.1 MB (36085362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf142fa26f75b32739bbab38a7744d38f0da8799eebddd79bcb04ab09e7edbb9`  
		Last Modified: Fri, 07 Feb 2025 01:59:31 GMT  
		Size: 8.8 MB (8844391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2ebe397dbd34444f0625373b79f5286ad1c3b1ee6de7f00ad348a924d91d54`  
		Last Modified: Fri, 07 Feb 2025 01:59:30 GMT  
		Size: 1.3 MB (1345150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2abc72cbfc6f9a5c38d480fd384cd9bee428bbd3ecca2706c26073f3f391a57`  
		Last Modified: Fri, 07 Feb 2025 02:09:53 GMT  
		Size: 18.4 MB (18359083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8f11b494b2f386d8386a46e1f5148a405e62192ebfee50b6b0038daa536e71`  
		Last Modified: Fri, 07 Feb 2025 02:09:52 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adcc9a15b1f2d58e31f841447f45eeaf0e38e8ef44ed496210442323353a46c`  
		Last Modified: Fri, 07 Feb 2025 02:09:52 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0be27cdfd958cf68f24ce129c2d0a7765e8915f7681ce4bb926e126d2b91cd`  
		Last Modified: Fri, 07 Feb 2025 02:09:52 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ca1360953de1a6b53cf3274eda1322156d4555f2622fd4277403573c1731c6`  
		Last Modified: Fri, 07 Feb 2025 02:09:53 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:5dd807481fa4b8fb1b12a524d6e2dc25504280b8f024dc70f3ae1ba57082a4d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6732603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2d36fb9f6a9f894bd4ecc69eeefe563f862bfbf421ab9493e18f18a99671fe`

```dockerfile
```

-	Layers:
	-	`sha256:fc0e61ac6fe60d56de44e16f2329ca2a5597ec9302a0245fbc5c0af1df622f6d`  
		Last Modified: Fri, 07 Feb 2025 02:09:52 GMT  
		Size: 652.0 KB (651980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b6a0b9c7c26f364634d6eafc1f7f303f8afe076a172b8b67b8be7137e145d84`  
		Last Modified: Fri, 07 Feb 2025 02:09:52 GMT  
		Size: 3.1 MB (3087921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:986f98d26483d92cf20d930c872c534e20254dcc8ab19d51656ca263ae20a9da`  
		Last Modified: Fri, 07 Feb 2025 02:09:52 GMT  
		Size: 2.9 MB (2932782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50837491943bb379a39a834b6357b281b13e2f1dbb0094489dc3130193823450`  
		Last Modified: Fri, 07 Feb 2025 02:09:51 GMT  
		Size: 59.9 KB (59920 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:ff1540f120c600983757c3469bace4ddc87417824bc8da7433db9f2989660bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69856999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e08e748b14e91db5c5d79d909acaba26578369e384bc5dd2d71fc02b3a5aaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2025 18:05:23 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 06 Feb 2025 18:05:23 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 06 Feb 2025 18:05:23 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_VERSION=4.0.5
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 18:05:23 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 06 Feb 2025 18:05:23 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 06 Feb 2025 18:05:23 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Feb 2025 18:05:23 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 06 Feb 2025 18:05:23 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c387f6576a25eeb1ca62347bfe594e925229bd04f406ac86cba88a72135f5d6a`  
		Last Modified: Fri, 07 Feb 2025 03:42:27 GMT  
		Size: 37.0 MB (37026843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42330276566789bf0b6f0cc51f4b13c9d01ab0b70d9fa390cd7e5d08edb305d6`  
		Last Modified: Fri, 07 Feb 2025 03:42:22 GMT  
		Size: 9.9 MB (9854308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991b8c4c8fe059ec56c65b40e37d4ee3bb3aa7c242b5f2aaab952279ba63c6c0`  
		Last Modified: Fri, 07 Feb 2025 03:42:21 GMT  
		Size: 1.3 MB (1265039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32de7d49f0fb193ffae2b2ffb18447ef1a3847cd23a459b217f68f3500b0cb5c`  
		Last Modified: Fri, 07 Feb 2025 04:02:14 GMT  
		Size: 18.4 MB (18358807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e583c84d2dc63a507f997810b90d37d0686014d93ba9bcb62ad7e473c047a4`  
		Last Modified: Fri, 07 Feb 2025 04:02:11 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63152e40694c946b95639dcb3e62a0bd6b28480858ba208196bef993012866`  
		Last Modified: Fri, 07 Feb 2025 04:02:11 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5650c6e9f668ca51600861cd79efe542a2a371c953af7247e96c87c3b63ae185`  
		Last Modified: Fri, 07 Feb 2025 04:02:12 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22098f9c71a8ff0dd00b09deefa5589464a2293976d67f6fa71c7a6dd48b061d`  
		Last Modified: Fri, 07 Feb 2025 04:02:12 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:cc2a39b9f27528474569a8597198d9354acd3b8bfc090731ab3be15c8ad87e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6810716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42671d60d3d5dd960624dbff0cfe380ad9af1e8990ff0da8a86ac75931f6a8d5`

```dockerfile
```

-	Layers:
	-	`sha256:3fcc19692b3585a7a87e0886dab4c3c713ca00bcb4faa888f29078e523eab359`  
		Last Modified: Fri, 07 Feb 2025 04:02:12 GMT  
		Size: 654.8 KB (654772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f5e7072b27baa6072232e2657bca5a5859419c0a1e9f669924bcea18eb7ffac`  
		Last Modified: Fri, 07 Feb 2025 04:02:12 GMT  
		Size: 3.1 MB (3125576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e8c3ae906f1bfcc71896d98e9fdf92d2562c7b5aba34220c128ba8aaa4ffb7b`  
		Last Modified: Fri, 07 Feb 2025 04:02:12 GMT  
		Size: 3.0 MB (2970449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:067570f2d315f2bcb0c9d4d48769dcf1e56689266a753785d0f5110ed0757c83`  
		Last Modified: Fri, 07 Feb 2025 04:02:11 GMT  
		Size: 59.9 KB (59919 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:25c5fd266878652cc2d1f8edf0b92f1941b3306e20e0d191b6639f7f0fba51dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66764145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78cec0fe7a93df29dcafb67bbd7403c1ea1c4dd243681ccea6593d3d1fd096c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2025 18:05:23 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 06 Feb 2025 18:05:23 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 06 Feb 2025 18:05:23 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_VERSION=4.0.5
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 06 Feb 2025 18:05:23 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 18:05:23 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 06 Feb 2025 18:05:23 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 06 Feb 2025 18:05:23 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 06 Feb 2025 18:05:23 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 18:05:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Feb 2025 18:05:23 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 06 Feb 2025 18:05:23 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618e0b776ff852eceaa0b60c516c1967ad241624ab035274d5711f5263c4e13e`  
		Last Modified: Fri, 07 Feb 2025 02:17:13 GMT  
		Size: 36.1 MB (36104628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a797d7acd0e66e34f503e7d70130603cb4090b059fca91d081e67ee97fad87`  
		Last Modified: Fri, 07 Feb 2025 02:17:13 GMT  
		Size: 7.5 MB (7508452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919bb27d6a523850e7ca5e5885c2173bf90a686dff8aaedabfa1d2529d7a6bae`  
		Last Modified: Fri, 07 Feb 2025 02:17:13 GMT  
		Size: 1.3 MB (1323353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7984918081bf1dd3c2e63fd499defe3c12de4987d01ebbf6769dcd2ed0a14d4b`  
		Last Modified: Fri, 07 Feb 2025 02:27:58 GMT  
		Size: 18.4 MB (18359095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0ba827054492069591856b10b97d131321d1ac271c159375a0fca01ecaa373`  
		Last Modified: Fri, 07 Feb 2025 02:27:58 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879eef930eece3d1a2e5387794665eb525fd0b007423c4674549d05c4f8b7a2d`  
		Last Modified: Fri, 07 Feb 2025 02:27:58 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db40b3195ba69534f6cf12e055be28da3f8cb156026882974fa0d31fb51dce5a`  
		Last Modified: Fri, 07 Feb 2025 02:27:58 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b481379a34f516f7a6bedb6e6587b1ddae29cac630c3b6646428c5ed557f5371`  
		Last Modified: Fri, 07 Feb 2025 02:27:59 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e52d5fa4fc0595abcbdb1270f34a3e317340391604c23d7d1ed380e0cb0c3f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6512471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a53c2e943c61b27dfabf58cc1729ffb7e6cf39d7fcf9f2468e697bf6ca30b19`

```dockerfile
```

-	Layers:
	-	`sha256:170c779894478f8e84ab0bed33a94992fd489f3b4c16c3312bbbfdb5b88b4e8d`  
		Last Modified: Fri, 07 Feb 2025 02:27:58 GMT  
		Size: 651.9 KB (651946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ff003fe226e5e1bc0f216205d2679bb94b8cdf9f91a2c1a9c86f3f0b77cfa2`  
		Last Modified: Fri, 07 Feb 2025 02:27:58 GMT  
		Size: 3.0 MB (2977888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ce425942dda60f1f80df87ebe3e9ec3f8ec68cbeae561475ebcfa2b5abe875c`  
		Last Modified: Fri, 07 Feb 2025 02:27:58 GMT  
		Size: 2.8 MB (2822779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3087d96e7d0a6481288c36617c5d345d30aa23feb71130b5297a0b87e48e1225`  
		Last Modified: Fri, 07 Feb 2025 02:27:57 GMT  
		Size: 59.9 KB (59858 bytes)  
		MIME: application/vnd.in-toto+json
