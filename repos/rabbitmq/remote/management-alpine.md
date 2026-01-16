## `rabbitmq:management-alpine`

```console
$ docker pull rabbitmq@sha256:52a1120ca9e85e7cc80af73b6c17d42393c78ae32606fffc3ad895adc051e18b
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
$ docker pull rabbitmq@sha256:0c5585d42537d361e4c08bd10fade35d5173bd1ff44855f5a61df973953cc4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88177680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21f395edc678bd9f66e2a4d6aa39cb0126c6a9ce6df5f14b68cc6cf4a50e820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:43:11 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 18 Dec 2025 00:43:11 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 18 Dec 2025 00:43:11 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 18 Dec 2025 00:43:11 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 18 Dec 2025 00:43:11 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:43:11 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 18 Dec 2025 00:43:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 18 Dec 2025 00:43:13 GMT
ENV RABBITMQ_VERSION=4.2.2
# Thu, 18 Dec 2025 00:43:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 18 Dec 2025 00:43:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 18 Dec 2025 00:43:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:43:19 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 18 Dec 2025 00:43:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 18 Dec 2025 00:43:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 18 Dec 2025 00:43:20 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 18 Dec 2025 00:43:20 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 18 Dec 2025 00:43:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Dec 2025 00:43:20 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 18 Dec 2025 00:43:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 18 Dec 2025 00:43:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:43:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:43:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 18 Dec 2025 00:43:20 GMT
CMD ["rabbitmq-server"]
# Wed, 07 Jan 2026 18:27:11 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Wed, 07 Jan 2026 18:27:11 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.21.0/rabbitmqadmin-2.21.0-x86_64-unknown-linux-musl'; digest='88df97a1d5e09ab54d597fc8f064d82166f24f34bf1271fff1855f8048ac8e8f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.21.0/rabbitmqadmin-2.21.0-aarch64-unknown-linux-musl'; digest='b98b0ff166157a047fa3e4b017865fae7f0e48b5cbf350ade443a830db0a3626' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Wed, 07 Jan 2026 18:27:11 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc878640de49edbec879d5501fd914072b22a27bc988871d8846989cb967d32`  
		Last Modified: Thu, 18 Dec 2025 00:43:49 GMT  
		Size: 42.6 MB (42598832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2b3fb0fc24d3f54fb07b659349be29fa94d1bf5d2f103242c7966f5f901937`  
		Last Modified: Thu, 18 Dec 2025 00:43:44 GMT  
		Size: 9.2 MB (9206830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847a9a6aa2c8b01ca151a25685806b7ff775a4655ffe5f9d05edf4104ebc136b`  
		Last Modified: Thu, 18 Dec 2025 00:43:44 GMT  
		Size: 2.5 MB (2465569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d2b8dd6daa8698583e7bf8570a7f0b6eded142331c1b4d143319be80609c4e`  
		Last Modified: Thu, 18 Dec 2025 00:43:45 GMT  
		Size: 25.3 MB (25317128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d901a09e06dcbf509f04cccecba79c8af1530e0c8a43a4e1a484e1ad7c17d202`  
		Last Modified: Thu, 18 Dec 2025 00:43:43 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2dbf81a9b8bf66535a48484356b0e4760267ff27a981acfa18402a87d4efdb`  
		Last Modified: Thu, 18 Dec 2025 00:43:43 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259d35df5296e2123e4b76e0bd939d026f4444420040704f08148f355bb6d922`  
		Last Modified: Thu, 18 Dec 2025 00:43:43 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554988c62edb19856d5c2a5a966a43bc5817b50bdf9556c6bcba8e463c2cc74d`  
		Last Modified: Thu, 18 Dec 2025 00:43:43 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e40239175d96e7149a54a55b9b18e2492a07f77af60fd42d8896ad4ec462f3`  
		Last Modified: Wed, 07 Jan 2026 18:27:23 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4371e8411d251fdd6cb40dcfee4eedfe523f9292b5ef536cf53dd2d868a3cf9a`  
		Last Modified: Wed, 07 Jan 2026 18:27:23 GMT  
		Size: 4.7 MB (4727196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fd38afaf057d7a1e822cbde6c8185ec4c2f49d75609fbd52c38bfedee2c0fd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.0 KB (691024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0688c62609b5fd97070815f27c9f85ea503895e3f9cf3278aae8afed68bf50`

```dockerfile
```

-	Layers:
	-	`sha256:d846c34e598a4d97044a2bf80f5c4c21a2d3ac98a230827f0e32e2b5b5195eb9`  
		Last Modified: Wed, 07 Jan 2026 19:53:07 GMT  
		Size: 675.8 KB (675785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cf1b793610f80089ef6203d60ad4cc61dd89648d2d5b099d4fa18856264c109`  
		Last Modified: Wed, 07 Jan 2026 19:53:08 GMT  
		Size: 15.2 KB (15239 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:dbb4f584230cb22066396a39fe0c23b3b38d30c992641bc2c15d3a25dab0bf1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71653900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0fae157b425493621b229eb78d20158d35eceb2f48dc6f365cea1678110329e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:02:37 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 18 Dec 2025 01:02:37 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 18 Dec 2025 01:02:37 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 18 Dec 2025 01:02:37 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 18 Dec 2025 01:02:37 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:02:37 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 18 Dec 2025 01:02:40 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 18 Dec 2025 01:02:40 GMT
ENV RABBITMQ_VERSION=4.2.2
# Thu, 18 Dec 2025 01:02:40 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 18 Dec 2025 01:02:40 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 18 Dec 2025 01:02:40 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:02:49 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 18 Dec 2025 01:02:50 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 18 Dec 2025 01:02:51 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 18 Dec 2025 01:02:51 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 18 Dec 2025 01:02:51 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 18 Dec 2025 01:02:51 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Dec 2025 01:02:51 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 18 Dec 2025 01:02:51 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 18 Dec 2025 01:02:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:02:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 01:02:51 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 18 Dec 2025 01:02:51 GMT
CMD ["rabbitmq-server"]
# Wed, 07 Jan 2026 18:26:20 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Wed, 07 Jan 2026 18:26:20 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.21.0/rabbitmqadmin-2.21.0-x86_64-unknown-linux-musl'; digest='88df97a1d5e09ab54d597fc8f064d82166f24f34bf1271fff1855f8048ac8e8f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.21.0/rabbitmqadmin-2.21.0-aarch64-unknown-linux-musl'; digest='b98b0ff166157a047fa3e4b017865fae7f0e48b5cbf350ade443a830db0a3626' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Wed, 07 Jan 2026 18:26:20 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbe4c111a2a0433756d159b026e74fe6186b0bfebff4f505a489535b871d757`  
		Last Modified: Thu, 18 Dec 2025 01:03:07 GMT  
		Size: 33.5 MB (33504388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd995c028c236f6dc09cd69589e6dfee828627b7320aea95438debb978b2491`  
		Last Modified: Thu, 18 Dec 2025 01:03:05 GMT  
		Size: 7.9 MB (7857211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f7ba9ead28cee49fcef78fb534d76d258b951ef25f3c801bc159a306811a3b`  
		Last Modified: Thu, 18 Dec 2025 01:03:04 GMT  
		Size: 1.4 MB (1404613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d3fb7b94b744655403ab4e8bc30f4eaa9a14206b21f6d03ebec7ce595be384`  
		Last Modified: Thu, 18 Dec 2025 01:03:09 GMT  
		Size: 25.3 MB (25317196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4755f9994732bb5ccad4a94b33251e0261f906abea736c87f95d2fc5df4ede`  
		Last Modified: Thu, 18 Dec 2025 01:03:05 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c66dbbb7c619ec636df248257b872b2f9a1f405e3fd12b4c7990c1e2ec046d`  
		Last Modified: Thu, 18 Dec 2025 01:03:05 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d17ef2f1e6d3d704f6c2d4da1408c503e8fe340579fcbde1bbf3cad0f68928`  
		Last Modified: Thu, 18 Dec 2025 01:03:05 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b22d99f86c3c1172f3c0e6c584f457df7cd85db9d3439deffbcf339d4e48ccd`  
		Last Modified: Thu, 18 Dec 2025 01:03:05 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b86e9c595e6b017b9e9411739e1160f4d3b6c26d5c6b3200416b5a77c49354`  
		Last Modified: Wed, 07 Jan 2026 18:26:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:62496c26ec4581fcfc3222a6683a2410180029cb4299cf4824b0ac0ae97bfd87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 KB (15112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9772885b795382c3ab57f80cf3827805d7a56c0469fafedd33a30d74d177dc23`

```dockerfile
```

-	Layers:
	-	`sha256:50562b098d2e74465359c686263c75b7ef12225b26b8de4bdda4d589e728f3ce`  
		Last Modified: Wed, 07 Jan 2026 19:55:13 GMT  
		Size: 15.1 KB (15112 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:9532209815f1ba9712ee2d2c79023911b9e70a0d712738d6862a1c9a5a4b87c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70750395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e60e8b805e2c54dfe30926c7c744bd1f6a5559cfd10e2d4351ad03201e3984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:05:18 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 18 Dec 2025 01:05:18 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 18 Dec 2025 01:05:18 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 18 Dec 2025 01:05:19 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 18 Dec 2025 01:05:19 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:05:19 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 18 Dec 2025 01:05:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 18 Dec 2025 01:05:21 GMT
ENV RABBITMQ_VERSION=4.2.2
# Thu, 18 Dec 2025 01:05:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 18 Dec 2025 01:05:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 18 Dec 2025 01:05:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:05:28 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 18 Dec 2025 01:05:29 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 18 Dec 2025 01:05:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 18 Dec 2025 01:05:29 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 18 Dec 2025 01:05:29 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 18 Dec 2025 01:05:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Dec 2025 01:05:29 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 18 Dec 2025 01:05:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 18 Dec 2025 01:05:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 01:05:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 18 Dec 2025 01:05:29 GMT
CMD ["rabbitmq-server"]
# Wed, 07 Jan 2026 18:26:35 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Wed, 07 Jan 2026 18:26:35 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.21.0/rabbitmqadmin-2.21.0-x86_64-unknown-linux-musl'; digest='88df97a1d5e09ab54d597fc8f064d82166f24f34bf1271fff1855f8048ac8e8f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.21.0/rabbitmqadmin-2.21.0-aarch64-unknown-linux-musl'; digest='b98b0ff166157a047fa3e4b017865fae7f0e48b5cbf350ade443a830db0a3626' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Wed, 07 Jan 2026 18:26:35 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97b2ecda41c2e368e455d27a478de5faeb0d4c4756985f2349582efca7e62eb`  
		Last Modified: Thu, 18 Dec 2025 01:06:00 GMT  
		Size: 33.4 MB (33409218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5abe74fdd036b9bea8a728aeba74f66161af86867fe4fec4e04279d38fee397`  
		Last Modified: Thu, 18 Dec 2025 01:05:54 GMT  
		Size: 7.4 MB (7447227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a15d44b8a87df525fd0eb9994ad17101ed81eaea739c93e52c7aa3046070136`  
		Last Modified: Thu, 18 Dec 2025 01:05:53 GMT  
		Size: 1.3 MB (1295842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890aa995edbed8658042813a84a480bafe086fed2a7742f191aca7f436baf663`  
		Last Modified: Thu, 18 Dec 2025 01:05:55 GMT  
		Size: 25.3 MB (25316669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a6fdaac027724e74ab7a4b4d414e1e861d59c3ebe30a713bd1c466e6c65475`  
		Last Modified: Thu, 18 Dec 2025 01:05:52 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7932a0d672b810c9f4c3af95f8baee511970ff01295198051e5c2e090527ced5`  
		Last Modified: Thu, 18 Dec 2025 01:05:53 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4161ca153704d43c7c6c8dffed1567aa7746a6429aadbd197b9c914a1629b62c`  
		Last Modified: Thu, 18 Dec 2025 01:05:53 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a673791c7a0bc7aa9998bce6d08a25b8feac96545ea2e975884b6f75fb3bb`  
		Last Modified: Thu, 18 Dec 2025 01:05:53 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7604360de51db17a1b9b795758a8f0920f31e7193320e396fe0a07edd4a558`  
		Last Modified: Wed, 07 Jan 2026 18:26:46 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:236165e202452e019785aadc21bfec483396b4b73fbe8677c4b70f2b50986b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.3 KB (686255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0c0756e4f229ce6e4d9324bbecaccfe1cf16a1e5c5c4bb9115530a379ca2f5`

```dockerfile
```

-	Layers:
	-	`sha256:e3eabb87ac45dcab768be46de8dcb61495dad06c1ff63abd9042f87894774982`  
		Last Modified: Wed, 07 Jan 2026 19:55:16 GMT  
		Size: 670.9 KB (670928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70948c7562383aa97f40d8aeed1b785f619a1e3c3443bb19bc655d3d04f586b1`  
		Last Modified: Wed, 07 Jan 2026 19:55:17 GMT  
		Size: 15.3 KB (15327 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:7af9b8d35ecb5d035b8dc16f73e2c21eeb24fbe901826eef24312cccf1a796d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86859584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe2d55347da94d7deac5eb505bd41466ec697a3061ccc356ddce26e088504a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:46:51 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 18 Dec 2025 00:46:51 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 18 Dec 2025 00:46:51 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 18 Dec 2025 00:46:51 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 18 Dec 2025 00:46:51 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:46:51 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 18 Dec 2025 00:46:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 18 Dec 2025 00:46:53 GMT
ENV RABBITMQ_VERSION=4.2.2
# Thu, 18 Dec 2025 00:46:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 18 Dec 2025 00:46:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 18 Dec 2025 00:46:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:46:59 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 18 Dec 2025 00:47:00 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 18 Dec 2025 00:47:00 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 18 Dec 2025 00:47:00 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 18 Dec 2025 00:47:00 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 18 Dec 2025 00:47:00 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Dec 2025 00:47:00 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 18 Dec 2025 00:47:00 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 18 Dec 2025 00:47:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:47:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:47:00 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 18 Dec 2025 00:47:00 GMT
CMD ["rabbitmq-server"]
# Wed, 07 Jan 2026 18:26:41 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Wed, 07 Jan 2026 18:26:41 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.21.0/rabbitmqadmin-2.21.0-x86_64-unknown-linux-musl'; digest='88df97a1d5e09ab54d597fc8f064d82166f24f34bf1271fff1855f8048ac8e8f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.21.0/rabbitmqadmin-2.21.0-aarch64-unknown-linux-musl'; digest='b98b0ff166157a047fa3e4b017865fae7f0e48b5cbf350ade443a830db0a3626' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Wed, 07 Jan 2026 18:26:41 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b353084ce0e49f3438c5aca9e4e4aceaf099f1867be377c5c34910cc9133e1`  
		Last Modified: Thu, 18 Dec 2025 00:47:31 GMT  
		Size: 40.5 MB (40454885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9947c134b4924a1d46a2403966d38b1795b60e0f1f74e4ddfd8a821255aa562f`  
		Last Modified: Thu, 18 Dec 2025 00:47:25 GMT  
		Size: 10.0 MB (9987910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd256d04ff3d32922e489612b10aa4b36d85a26c5d167ba48c4c3d1f8e5eb081`  
		Last Modified: Thu, 18 Dec 2025 00:47:25 GMT  
		Size: 2.5 MB (2514383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3824e4a7686b5fe6b72dc544830fff8fb348b498fbb4c1a248f44c61b264ab97`  
		Last Modified: Thu, 18 Dec 2025 00:47:27 GMT  
		Size: 25.3 MB (25317281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275a782d8eff888f9e26b08988ad00eefea48cbfa0e749b4b3e3bb6052f74f24`  
		Last Modified: Thu, 18 Dec 2025 00:47:25 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94c3258c54ba3be1bbc67d5b2b8b5bfc9d1065c509ed70dc0b5e8dd30f2e9cb`  
		Last Modified: Thu, 18 Dec 2025 00:47:25 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a4e04aed125148d178a854fc60ad4c25f7cd0b2152990ce6b5e43bfbf86e5b`  
		Last Modified: Thu, 18 Dec 2025 00:47:25 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6924c2d8b1dcd6984c73ef41ba9dbf2faea78b208e482a0f50f09218c9bd7f85`  
		Last Modified: Thu, 18 Dec 2025 00:47:19 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ea89594dcf01b6cb7b3d5ebb54f8bc8c97763496dc898b72759918a126d5c1`  
		Last Modified: Wed, 07 Jan 2026 18:26:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cb051db25397cd959e6314dfb1c914fee39446b3703f0a681c7cf949cccd49`  
		Last Modified: Wed, 07 Jan 2026 18:26:55 GMT  
		Size: 4.4 MB (4387364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e82ebfbd3b6a26e02e2959ad29a629d9d7a965db3b0b65b4f7762c0d2c515045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.3 KB (691286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05532cd3f309308da48da11ab0643656a7bc999fd794051e3ed8639759200e6`

```dockerfile
```

-	Layers:
	-	`sha256:2c7a5b70a22fd9e8307a42eee7c7b7173c04364075e9a0128b981fb938094739`  
		Last Modified: Wed, 07 Jan 2026 19:55:21 GMT  
		Size: 675.9 KB (675928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fa466f0afb4767a4713b57368de97612c112b59c592b1f698c302c9dbf32386`  
		Last Modified: Wed, 07 Jan 2026 19:55:22 GMT  
		Size: 15.4 KB (15358 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:165139be05e8ccd905e8da7c2b1038f022c5ac0f4a59d8f3511c07e99ada2a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73070210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2011ac0bbfb359e6953e6ac080bf805ae5065a5ac01858d8d1e4d319ffe4289f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:44:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 18 Dec 2025 00:44:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 18 Dec 2025 00:44:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 18 Dec 2025 00:44:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 18 Dec 2025 00:44:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:44:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 18 Dec 2025 00:44:17 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 18 Dec 2025 00:44:17 GMT
ENV RABBITMQ_VERSION=4.2.2
# Thu, 18 Dec 2025 00:44:17 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 18 Dec 2025 00:44:17 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 18 Dec 2025 00:44:17 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:44:22 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 18 Dec 2025 00:44:23 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 18 Dec 2025 00:44:23 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 18 Dec 2025 00:44:23 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 18 Dec 2025 00:44:23 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 18 Dec 2025 00:44:23 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Dec 2025 00:44:23 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 18 Dec 2025 00:44:23 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 18 Dec 2025 00:44:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:44:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:44:23 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 18 Dec 2025 00:44:23 GMT
CMD ["rabbitmq-server"]
# Wed, 07 Jan 2026 18:27:22 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Wed, 07 Jan 2026 18:27:22 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.21.0/rabbitmqadmin-2.21.0-x86_64-unknown-linux-musl'; digest='88df97a1d5e09ab54d597fc8f064d82166f24f34bf1271fff1855f8048ac8e8f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.21.0/rabbitmqadmin-2.21.0-aarch64-unknown-linux-musl'; digest='b98b0ff166157a047fa3e4b017865fae7f0e48b5cbf350ade443a830db0a3626' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Wed, 07 Jan 2026 18:27:22 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d46d10e7d721607dbfda20812f27dd3b0dc50998291210732603d3ab1ef397e`  
		Last Modified: Thu, 18 Dec 2025 00:44:48 GMT  
		Size: 33.5 MB (33458989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6324fac6e6681e6e57e11cad647adc94b8b57496355c0bfcb99845a79fdede71`  
		Last Modified: Thu, 18 Dec 2025 00:44:49 GMT  
		Size: 9.2 MB (9197855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0018b436fdb8ae80b83e087b37b29611caa85bcbdab575ecfa8b0213fcffa4`  
		Last Modified: Thu, 18 Dec 2025 00:44:46 GMT  
		Size: 1.4 MB (1408983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440ef39f99d3001c9eae51fbdda7199a7a5fad4082817d9a1e5b5e8a88875036`  
		Last Modified: Thu, 18 Dec 2025 00:44:47 GMT  
		Size: 25.3 MB (25316227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14042a887ad894e0122e23ffe07b0f5a72fa530d1bf77192f2de5f7d6d46759e`  
		Last Modified: Thu, 18 Dec 2025 00:44:44 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd8522d5e5f524da3f5cebec0cd1714779af0f6c6883ebea2ce46a6389cfd1f`  
		Last Modified: Thu, 18 Dec 2025 00:44:44 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87132d5b08b3de8e63d1c8394a7c6209583af1b2b49153aece757c198efb14c`  
		Last Modified: Thu, 18 Dec 2025 00:44:44 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b89ece089081c30e80f3efcd2b8f67c46278a2057748a6d48a0833503ba9dc`  
		Last Modified: Thu, 18 Dec 2025 00:44:44 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e5542a774cdd46269b9f918978f9a236a35b85d997f03e093e3129552e60cd`  
		Last Modified: Wed, 07 Jan 2026 18:27:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f3ab1433ab77fe72b3decc26bd0a5816d789c4e645971d901e3ca447c22d4fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.0 KB (685980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a80c736b83c32026c05d8d04fa3aceacc314cd62c5462b79d5c850ed1af614b`

```dockerfile
```

-	Layers:
	-	`sha256:16e93087de6869886566f68273188ceb71646cd7baa92fb98d5a8d66c6d74403`  
		Last Modified: Wed, 07 Jan 2026 19:55:37 GMT  
		Size: 670.8 KB (670780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39a1208c075e7921401bd50e6b054df146a2d11e602dffae11745e57573f0038`  
		Last Modified: Wed, 07 Jan 2026 19:55:38 GMT  
		Size: 15.2 KB (15200 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:ea49656aa38736b279372c3a96eedd401ca875718f70fb510b1febae7e66e843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74712924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f9dd4d2e67f0046f86373c0f074f2ee78d79cad43255bf8031fc90a95f2e2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 02:13:51 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 18 Dec 2025 02:13:51 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 18 Dec 2025 02:13:51 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 18 Dec 2025 02:13:51 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 18 Dec 2025 02:13:51 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 02:13:51 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 18 Dec 2025 02:13:55 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 18 Dec 2025 02:13:55 GMT
ENV RABBITMQ_VERSION=4.2.2
# Thu, 18 Dec 2025 02:13:55 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 18 Dec 2025 02:13:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 18 Dec 2025 02:13:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 02:14:06 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 18 Dec 2025 02:14:08 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 18 Dec 2025 02:14:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 18 Dec 2025 02:14:09 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 18 Dec 2025 02:14:09 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 18 Dec 2025 02:14:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Dec 2025 02:14:09 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 18 Dec 2025 02:14:10 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 18 Dec 2025 02:14:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 02:14:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 02:14:10 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 18 Dec 2025 02:14:10 GMT
CMD ["rabbitmq-server"]
# Wed, 07 Jan 2026 18:27:02 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Wed, 07 Jan 2026 18:27:03 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.21.0/rabbitmqadmin-2.21.0-x86_64-unknown-linux-musl'; digest='88df97a1d5e09ab54d597fc8f064d82166f24f34bf1271fff1855f8048ac8e8f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.21.0/rabbitmqadmin-2.21.0-aarch64-unknown-linux-musl'; digest='b98b0ff166157a047fa3e4b017865fae7f0e48b5cbf350ade443a830db0a3626' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Wed, 07 Jan 2026 18:27:03 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d162d3b63753d8d295a891a775d5181faa0d31da719ee5b720c1a12648a955e`  
		Last Modified: Thu, 18 Dec 2025 02:14:59 GMT  
		Size: 34.1 MB (34067297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51eb38d1e95e64f0eaf411ad100f93397b95cb10b0d02a4a39c57a64e8d0ccc`  
		Last Modified: Thu, 18 Dec 2025 02:14:56 GMT  
		Size: 10.0 MB (9956656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881ebbc002c6144a03814927d9bacd35c4563b345650b5f49fe968f7872a4fb1`  
		Last Modified: Thu, 18 Dec 2025 02:14:54 GMT  
		Size: 1.5 MB (1542636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0e5700a7b386c993a0f5080dd07617f5106cd0cd70f793068c945015a3e968`  
		Last Modified: Thu, 18 Dec 2025 02:14:56 GMT  
		Size: 25.3 MB (25316520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e66b218be1d46f74370b204e011480a84660403edcb24abba12b15eb4171b5`  
		Last Modified: Thu, 18 Dec 2025 02:14:54 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab58c33eeecf0e155699dcb35ab8ae344921db14cdb043faa5590356f92699ac`  
		Last Modified: Thu, 18 Dec 2025 02:14:54 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d40f5ff035b589767183847b34f228990fc23bab8c439d4d2f5ec062583d97`  
		Last Modified: Thu, 18 Dec 2025 02:14:54 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd26448c3d1263489a02899d424e4705ab12f68381f6b589b48a870edeae088e`  
		Last Modified: Thu, 18 Dec 2025 02:14:54 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bf0346d022dad1a1958c6c5e9c18cbab0f4f5ad9c7469966386c5067f5b00a`  
		Last Modified: Wed, 07 Jan 2026 18:27:23 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:350b3f0d297740caea3bc4a099b11c0f0e1ed4de0d1c07931ac5324f1c21586c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.2 KB (686205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0935e29f609b0dc31a531b6f896fa70c456f2b44c28742e5f1fddcae01cdead1`

```dockerfile
```

-	Layers:
	-	`sha256:d54ae7cea852fa5b31f2e6c5c884a8d0122620fd21ea5950a8c0fc1a578798e6`  
		Last Modified: Wed, 07 Jan 2026 19:55:41 GMT  
		Size: 670.9 KB (670925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0250a58434eb53ceb767d26a1f648a95222b736b7176454b18a775894e7bf625`  
		Last Modified: Wed, 07 Jan 2026 19:55:42 GMT  
		Size: 15.3 KB (15280 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:4b7b685e3c88ee7cd23d3aa673e5a5dd36c1172b48f65e3d1caf37fb581ff591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78639189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb9b7cb0166ef8a809ade82dfbf1e5cb979b4144d1b81f18defc5374db7049a`
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
# Fri, 19 Dec 2025 10:53:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 10:53:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 10:53:06 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 19 Dec 2025 10:53:06 GMT
CMD ["rabbitmq-server"]
# Wed, 07 Jan 2026 18:58:34 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Wed, 07 Jan 2026 18:58:35 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.21.0/rabbitmqadmin-2.21.0-x86_64-unknown-linux-musl'; digest='88df97a1d5e09ab54d597fc8f064d82166f24f34bf1271fff1855f8048ac8e8f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.21.0/rabbitmqadmin-2.21.0-aarch64-unknown-linux-musl'; digest='b98b0ff166157a047fa3e4b017865fae7f0e48b5cbf350ade443a830db0a3626' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Wed, 07 Jan 2026 18:58:35 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
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
	-	`sha256:73341f048365011751f92cb6e6342f2ed59b16b60085944724ec8ff41cc58ac1`  
		Last Modified: Fri, 19 Dec 2025 10:57:21 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d39690ba62bcd056f3296277ac8c468e2a02b10681f36cc6c29c6d34c87209e`  
		Last Modified: Wed, 07 Jan 2026 18:59:36 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:451f4a8c99d172e36ef87f3ae14348a733bc3c703643e7fe969d9735a99424ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **689.2 KB (689177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12eae3f4bdb8c70b934b254d770e48d44697f0f82dd547d70a6431bc1e88849b`

```dockerfile
```

-	Layers:
	-	`sha256:f561c7873f465dbdf85c99f08df675156f980d94523e91f9884f3d6769408d9f`  
		Last Modified: Wed, 07 Jan 2026 19:55:46 GMT  
		Size: 673.9 KB (673894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0f688c393a704d6d1d70ca95f6086b0744840371e09cc5b43757b480d53af52`  
		Last Modified: Wed, 07 Jan 2026 19:55:47 GMT  
		Size: 15.3 KB (15283 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:017cb5360f9cccfb698219b141fd03d54bcb4e4cab822a3bb6e478cf22a9b7b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72825168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab5079467cabf7ea1632e4820eeb6625ab15be7c36ceb3d67a4ffcdd7e44727`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 03:32:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 18 Dec 2025 03:32:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 18 Dec 2025 03:32:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 18 Dec 2025 03:32:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 18 Dec 2025 03:32:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 03:32:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 18 Dec 2025 03:32:56 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 18 Dec 2025 03:32:56 GMT
ENV RABBITMQ_VERSION=4.2.2
# Thu, 18 Dec 2025 03:32:56 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 18 Dec 2025 03:32:56 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 18 Dec 2025 03:32:56 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 03:33:08 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 18 Dec 2025 03:33:10 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 18 Dec 2025 03:33:11 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 18 Dec 2025 03:33:11 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 18 Dec 2025 03:33:11 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 18 Dec 2025 03:33:11 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Dec 2025 03:33:11 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 18 Dec 2025 03:33:12 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 18 Dec 2025 03:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 03:33:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 03:33:12 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 18 Dec 2025 03:33:12 GMT
CMD ["rabbitmq-server"]
# Wed, 07 Jan 2026 18:25:19 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Wed, 07 Jan 2026 18:25:19 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.21.0/rabbitmqadmin-2.21.0-x86_64-unknown-linux-musl'; digest='88df97a1d5e09ab54d597fc8f064d82166f24f34bf1271fff1855f8048ac8e8f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.21.0/rabbitmqadmin-2.21.0-aarch64-unknown-linux-musl'; digest='b98b0ff166157a047fa3e4b017865fae7f0e48b5cbf350ade443a830db0a3626' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Wed, 07 Jan 2026 18:25:19 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a72ff26a23138cdaa4f0b41bfcc481ade8371719248390c6248e8905289430`  
		Last Modified: Thu, 18 Dec 2025 03:34:02 GMT  
		Size: 33.9 MB (33919488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6924ad8e1ba6e5410a42efe9dcbd3e0096a66790e6ed5f07f6fa89eaf614fd7`  
		Last Modified: Thu, 18 Dec 2025 03:33:50 GMT  
		Size: 8.3 MB (8346912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1210409b7173afd98d184cffda99ceccc0296adf807df7bb7c8066d248a9c0e7`  
		Last Modified: Thu, 18 Dec 2025 03:33:57 GMT  
		Size: 1.5 MB (1515870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28b7694c2744883772a3890c3575001f5611696802768e05cfb8d49a9e8fea6`  
		Last Modified: Thu, 18 Dec 2025 03:34:03 GMT  
		Size: 25.3 MB (25316530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e85f9fe9f47150ba82dba7045fa6911a4f7538e86b809a35497b355185be12`  
		Last Modified: Thu, 18 Dec 2025 03:33:57 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f015b147f83e728ec54cd4540a2dcf3fbbbab8fa86b0d0516bd94b4dd12bdf`  
		Last Modified: Thu, 18 Dec 2025 03:33:57 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4ddabe31ac81772444329627370f3ce7ddeed23b5631f5aef849cdc87a3243`  
		Last Modified: Thu, 18 Dec 2025 03:33:57 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebdd174221fc1d59ab886124ea3124536f2a73653533a642d735e1f76ec9fec`  
		Last Modified: Thu, 18 Dec 2025 03:33:57 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a75a30b5bd9bef4e12cb0f6a12da45c5497bb22efb197eb9f02e12b55208ae`  
		Last Modified: Wed, 07 Jan 2026 18:25:45 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ed973dd2daf0b33871268478dcd4f5f08e3940a79014ae0feef3d373d418baf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.1 KB (686123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d94adfe57c8c3d4c72b7044fda31c8c6b58179558743e05fb305aad805c7c62`

```dockerfile
```

-	Layers:
	-	`sha256:50eb5ba518620259d7d10cfdb95f3a8f49a09687a912edfa506a233dca1e7ccf`  
		Last Modified: Wed, 07 Jan 2026 19:55:50 GMT  
		Size: 670.9 KB (670891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a86a4481dd1b1b5f63c93c7882e2f5447d0249d485f5e2298b8dca6f349cf5ce`  
		Last Modified: Wed, 07 Jan 2026 19:55:54 GMT  
		Size: 15.2 KB (15232 bytes)  
		MIME: application/vnd.in-toto+json
