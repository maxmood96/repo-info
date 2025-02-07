## `rabbitmq:management-alpine`

```console
$ docker pull rabbitmq@sha256:54759523c0b09074814b1233e6985babe9fd34e3462d2fea522361cb83b2fd76
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
$ docker pull rabbitmq@sha256:8cb078c3917bd4ed1e4a93c58265cb6e7662848c8c1e2b4a5bd07702a7c353ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91350923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9027127e44b73f5976961be4754de624bf98312cbb5c25b70f93bf32f5db19fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
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
ENV RABBITMQ_VERSION=4.0.5
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
	-	`sha256:f42bc2c3505a6a68d3e8c9847ef6d7bcfee956e86b5015968e7fd27c4021d3a3`  
		Last Modified: Fri, 07 Feb 2025 01:28:07 GMT  
		Size: 13.8 MB (13767779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7fd47081627b56d3fd3d16cf0090e7e4f32c12bd32e0a3abccd5aa94be3511ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 MB (1522781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bc15ee691f0db4b546b0a9e793f13bbbd40851c171b7a56d1edc44e456e33d`

```dockerfile
```

-	Layers:
	-	`sha256:996fc0c072b9780812b683bb70846553dd3bdfb14193378f1d57216e72ca3f4b`  
		Last Modified: Fri, 07 Feb 2025 01:28:06 GMT  
		Size: 1.5 MB (1511558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1de4c4af6ab903a3a96158a3bf77c3ad78b002fc2934fdfd1eadb47ca0e0aaf`  
		Last Modified: Fri, 07 Feb 2025 01:28:06 GMT  
		Size: 11.2 KB (11223 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:544a68308c48397a60b2ab597ce64daca2256c3de7c182aa5eb9c5a4507d320b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80048963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c60efd2ddc05e28bf126b591bbd27fc42127b24c1d2c39dcdcc96d3d31e906`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
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
ENV RABBITMQ_VERSION=4.0.5
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
	-	`sha256:3394376e1a4f8ce044a6513ea740d774259e72c6aa2eef4d63798a3d5dcd13d7`  
		Last Modified: Fri, 07 Feb 2025 01:27:46 GMT  
		Size: 14.4 MB (14402988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b4948beef595fdd96fc06a0a6970652b153180db0b69ec5d6f378e7d9101cf47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 KB (11083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06fd98f7d99ece30500ea700400d8d6084b4277414a0e668a5177388392474c3`

```dockerfile
```

-	Layers:
	-	`sha256:1a58fb1ad5abcb68378bbc7cd196236de96a7017b87263de0fcfe8385bd312c6`  
		Last Modified: Fri, 07 Feb 2025 01:27:44 GMT  
		Size: 11.1 KB (11083 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:43a5fd070b816747bd18a26bee7669df88e32afd2b2c1df0cb7fc9667da834d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78885055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd6f9d1472ece6ce5f152b71a16891a62afb7256ca4e241fd53ab376098bad5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
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
ENV RABBITMQ_VERSION=4.0.5
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
	-	`sha256:d177546472c40fd24dca20f45b214ce3181d8b207b54a51351c2abf7c3898390`  
		Last Modified: Fri, 07 Feb 2025 04:08:51 GMT  
		Size: 14.0 MB (14042261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e97b6212a6d3451d2286da3b83deb134b25e552ba96832a55d0191b2e5212dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1643435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9429af9a84da48bdc2925f38b4eb41a6568c68bdf3fbb502e2948b53e159c1d4`

```dockerfile
```

-	Layers:
	-	`sha256:4fcdaaf8e19b667196d12c64e0fc58c42c96118a00819e5c03785079f84a0017`  
		Last Modified: Fri, 07 Feb 2025 04:08:50 GMT  
		Size: 1.6 MB (1632137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffe074b375d34c7a1f05123fa510762c1261ab5b35ee17c93db501a594d3c4b6`  
		Last Modified: Fri, 07 Feb 2025 04:08:49 GMT  
		Size: 11.3 KB (11298 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:471dd326b55bda1f1217f9b69be2b873f3230e97cb4c0b8a256e51bef5da1523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.4 MB (90436992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaebc17a8e3bf0c2493249e4d8b11b06561aee721867f166b23bb7a237bb6175`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
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
ENV RABBITMQ_VERSION=4.0.5
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
	-	`sha256:c828a7d3235dca3d62e1d655e3b3871c3800f95a3bbbff825c610917654aa38f`  
		Last Modified: Fri, 07 Feb 2025 03:50:20 GMT  
		Size: 13.7 MB (13728019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:916125dcae3f9bf39a85972c6933580bc738981f23625c52c584726e5aede789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1643312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992f58d8b51c9e430a163e278c891cae386fa631f12fc225e592433e9c4cb4d4`

```dockerfile
```

-	Layers:
	-	`sha256:b8543bcb4fea1e8ee44a484c62d070f2e07549a402b21d2ef96cf3c09b33eded`  
		Last Modified: Fri, 07 Feb 2025 03:50:20 GMT  
		Size: 1.6 MB (1631985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f21d52886b112cf36c2618c2637505beae00c4918c3c3e4938e8b59b6c3064b`  
		Last Modified: Fri, 07 Feb 2025 03:50:19 GMT  
		Size: 11.3 KB (11327 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:a67c5f526df11c1fdfea247974d37f5e544d9a714ddbbc8ae2830c48d7b5eac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82338186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d710ada35389372b670f948630be19a25eb2f4cf7149120a2328d6889d0acc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
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
ENV RABBITMQ_VERSION=4.0.5
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
	-	`sha256:8bbf051bc889e902f1f0ba6fcd12e52f84b2d17d27994fbfb5c0617679da13c8`  
		Last Modified: Fri, 07 Feb 2025 01:28:03 GMT  
		Size: 15.3 MB (15270173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:28dfc5f24d226357511072c68a6ac9cf06949da58c0844c42fffa724fa3d4efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 MB (1522552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187a5ef241066e2e5cc258db616dfceb27659a9aa20325b8ef4cbf39e403b754`

```dockerfile
```

-	Layers:
	-	`sha256:d59cd3e25eb69d38fc68199112c4f3fa95cac105e1dca462945cb8d3747419b2`  
		Last Modified: Fri, 07 Feb 2025 01:28:01 GMT  
		Size: 1.5 MB (1511361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28c65ed26c5de92fa3ea7fee970927e6adc4924c891a33a02bbe687124ea1afc`  
		Last Modified: Fri, 07 Feb 2025 01:28:01 GMT  
		Size: 11.2 KB (11191 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:d404f05def0d7c6f0a98fb67ab9458aa9eff748e4787cfbd185a43643966175d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83488235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63c297cc283448220be9747aebdd80db7827e798a6d119f59a11116f94cb7ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
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
ENV RABBITMQ_VERSION=4.0.5
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
	-	`sha256:64af4ada22729a9a9da0d674eabb35fcddb649eb83154d5fed67fd501f9bc83f`  
		Last Modified: Fri, 07 Feb 2025 03:07:51 GMT  
		Size: 15.3 MB (15278900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a695ff084acfc9c447061b43ed912ebb4f4e8fbad1583463f6337d754814e388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1641623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb89b906ed12f6ee420b4b422351677ac1c30f4326b09edb28832e3339637a6e`

```dockerfile
```

-	Layers:
	-	`sha256:f2a59ed1b4645a98aa69a76ab6e7a96a1751f17ebd8aa4426942970660a47ff3`  
		Last Modified: Fri, 07 Feb 2025 03:07:50 GMT  
		Size: 1.6 MB (1630356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d30825c33dd254ff23c05265f2e73c937a3f4a1f5d18fcca94f6876a43b2e0aa`  
		Last Modified: Fri, 07 Feb 2025 03:07:50 GMT  
		Size: 11.3 KB (11267 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:d8c466120ebbcf339be704694e893c7bcd4626cd67dafb6c26c94ec69e28e217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84670063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766fbf1e3e196c40bb17e386d9a4a35bf412c0b6437efd0ab3daec8e09b04765`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
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
ENV RABBITMQ_VERSION=4.0.5
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
	-	`sha256:fe29c20978c8904adf6c1b09c6a8ca5100eca0c3bb40f7d5e5b2ab2ee43785cc`  
		Last Modified: Fri, 07 Feb 2025 04:16:24 GMT  
		Size: 14.8 MB (14813064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:42619e2f3cbe7cdec7dc134305f8fe58aa3f4b49b5be1f74788cf716474da303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1643055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4c7f388dada8e450fba073f7b88080f5ffbfd290bba5271a2a3e9d7f04ee4b`

```dockerfile
```

-	Layers:
	-	`sha256:14003a1926ebf507e78d4eb5c923e3eff3accb413482feea4ae4ba76a837fffc`  
		Last Modified: Fri, 07 Feb 2025 04:16:21 GMT  
		Size: 1.6 MB (1631788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd81147ede547a824af1e5bc72d6dfeb431d2bda557a5a432ab5090654519f3`  
		Last Modified: Fri, 07 Feb 2025 04:16:21 GMT  
		Size: 11.3 KB (11267 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:a6cc95f47276703cbf6d459a54a7bfb33ae184f6cef5733ab38f96ecb3697d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82068044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefdc6d8f0f6c2d5292752917aa0aaf56b8975e1db2c532bc63dbdc241cbfc9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
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
ENV RABBITMQ_VERSION=4.0.5
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
	-	`sha256:338399ad2c0038d73422d4869768a8472b1ac47597a7439186e945e646a396f2`  
		Last Modified: Fri, 07 Feb 2025 03:10:20 GMT  
		Size: 15.3 MB (15303899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ecb4bb3eae27529bd42f607212b24499dd0f788a0448ff57b2057942f72f0ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1641029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d5d8ea905262e71f9adf77bdb08cff30ed0e2a8891b35a9f3046cc2faecca3`

```dockerfile
```

-	Layers:
	-	`sha256:4e045dee8715a6664ec4785974a38969a616e760c6274f62ce39d1629a999daa`  
		Last Modified: Fri, 07 Feb 2025 03:10:19 GMT  
		Size: 1.6 MB (1629806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e132782d4aa8765d0edd7328961b7fde5442c53c04c9faf965af125487ea775d`  
		Last Modified: Fri, 07 Feb 2025 03:10:18 GMT  
		Size: 11.2 KB (11223 bytes)  
		MIME: application/vnd.in-toto+json
