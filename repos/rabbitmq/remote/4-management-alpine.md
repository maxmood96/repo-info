## `rabbitmq:4-management-alpine`

```console
$ docker pull rabbitmq@sha256:996620e503208c14974432b828241a24b6f12c78a46385590c178a13bfe677e0
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
$ docker pull rabbitmq@sha256:5742aa16b513562e2f473896d67b2fccc03ae68f1f3675412742a487bcc76958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88242982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b4795b25be90edf2a091689e78ff12cc54352719cdd4d015d07dec512861a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 22 Jan 2026 22:57:02 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Jan 2026 22:57:02 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Jan 2026 22:57:02 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Jan 2026 22:57:02 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Jan 2026 22:57:02 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 22:57:02 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Jan 2026 22:57:04 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 22 Jan 2026 22:57:04 GMT
ENV RABBITMQ_VERSION=4.2.3
# Thu, 22 Jan 2026 22:57:04 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Jan 2026 22:57:04 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Jan 2026 22:57:04 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 22:57:10 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Jan 2026 22:57:11 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Jan 2026 22:57:11 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Jan 2026 22:57:11 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Jan 2026 22:57:11 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Jan 2026 22:57:11 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Jan 2026 22:57:11 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 22 Jan 2026 22:57:11 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Jan 2026 22:57:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Jan 2026 22:57:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jan 2026 22:57:11 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Jan 2026 22:57:11 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Jan 2026 23:13:16 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 22 Jan 2026 23:13:17 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-musl'; digest='0dc5e39dac98f38ad50f2aee15cfc5ea53c0ef5e649d79b41c2a7a94376aaf9f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-musl'; digest='fc7ca78e16824a2c77583d067ac1ae4eacbed1516a9a66bec50b5a772530d546' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 22 Jan 2026 23:13:17 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8084eb1728dcd8c3a4d9f9c13958843ce3a78fd9fe0b65e03c268760d4551f4`  
		Last Modified: Thu, 22 Jan 2026 22:57:29 GMT  
		Size: 42.6 MB (42598915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535068400e829c7ae3aa17b021ab43774eaa9c9d531f57a155b8793d72055e12`  
		Last Modified: Thu, 22 Jan 2026 22:57:28 GMT  
		Size: 9.2 MB (9206839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f819a754f61ed6a7bb22980da90a52cbc52fb210e454d255560485ea6ae96fac`  
		Last Modified: Thu, 22 Jan 2026 22:57:28 GMT  
		Size: 2.5 MB (2465562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e841f75f3fc871df3a5bb7aa3487b0747320dc807fa9f7f837ebd1a904658ce9`  
		Last Modified: Thu, 22 Jan 2026 22:57:29 GMT  
		Size: 25.4 MB (25378459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98866a47955342032a20bd22e6784539b2092d3eed86fd429ef3c4995f008f23`  
		Last Modified: Thu, 22 Jan 2026 22:57:29 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfeb6b07e503e1f43a735a193e6511430aa0a9f567fde2a9b3ffa8a41561168`  
		Last Modified: Thu, 22 Jan 2026 22:57:29 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af87f5e6ba43ea955d13da87165c3b6bc1929002037dacc623462b2d7adbdbb`  
		Last Modified: Thu, 22 Jan 2026 22:57:30 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e35172f1f0d05d89c5d3c97fdee55ba3b2237484edc3dc09b29160cb4f3d2c6`  
		Last Modified: Thu, 22 Jan 2026 22:57:30 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d691350eaf26ea56253a8dd4bc779cad2ef7e864e703ffbcae5848da65e104f0`  
		Last Modified: Thu, 22 Jan 2026 23:13:23 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe60f2aeeb8ca53f9fc9623342d82dc4b8eda8ef2de3aede0bbc49b1de6ee3c`  
		Last Modified: Thu, 22 Jan 2026 23:13:23 GMT  
		Size: 4.7 MB (4731085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fe3d898890eb8f19037d32cc1f9281157457c6c8876830fa8dddb3f0f7aacf7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.0 KB (691024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739f2c178f8254d517cb9d5da0b68794d8b6a26b209ae43406ad87a684cc2de2`

```dockerfile
```

-	Layers:
	-	`sha256:116fa1c89fde92f9af02686c035de28ce1c314e7b65cade9fb8e9d573d477cc4`  
		Last Modified: Thu, 22 Jan 2026 23:13:23 GMT  
		Size: 675.8 KB (675785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb01887a6c4fc190a1917f358f118ab1d9f1eb88e999685c21adaef10b8be54b`  
		Last Modified: Thu, 22 Jan 2026 23:13:23 GMT  
		Size: 15.2 KB (15239 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:0af9f4b1571f9f3613fd5fc47eeafb38969e93c765f1060180b2841046a866e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71715009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac635cb8adcde3b1b17db31698e5e1bb5aa8bb96a8bb6525524b913f2ee22ae0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Jan 2026 22:58:36 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Jan 2026 22:58:36 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Jan 2026 22:58:36 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Jan 2026 22:58:36 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Jan 2026 22:58:36 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 22:58:36 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Jan 2026 22:58:39 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 22 Jan 2026 22:58:39 GMT
ENV RABBITMQ_VERSION=4.2.3
# Thu, 22 Jan 2026 22:58:39 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Jan 2026 22:58:39 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Jan 2026 22:58:39 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 22:58:48 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Jan 2026 22:58:50 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Jan 2026 22:58:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Jan 2026 22:58:50 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Jan 2026 22:58:50 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Jan 2026 22:58:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Jan 2026 22:58:50 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 22 Jan 2026 22:58:50 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Jan 2026 22:58:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Jan 2026 22:58:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jan 2026 22:58:50 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Jan 2026 22:58:50 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Jan 2026 23:14:06 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 22 Jan 2026 23:14:06 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-musl'; digest='0dc5e39dac98f38ad50f2aee15cfc5ea53c0ef5e649d79b41c2a7a94376aaf9f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-musl'; digest='fc7ca78e16824a2c77583d067ac1ae4eacbed1516a9a66bec50b5a772530d546' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 22 Jan 2026 23:14:06 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64ef90559c4a94f9a4761c8ef536b144368da93a5fd0baf76d88aa54e998525`  
		Last Modified: Thu, 22 Jan 2026 22:58:58 GMT  
		Size: 33.5 MB (33504434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13d22c804258d56ab430b6863fe0f42e06724f3993714590eea53f9799a56de`  
		Last Modified: Thu, 22 Jan 2026 22:58:58 GMT  
		Size: 7.9 MB (7857215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268f9d73d581796f8148bc91ce2e3c17079edc036c54ae6076faaa9f47ec1d46`  
		Last Modified: Thu, 22 Jan 2026 22:58:57 GMT  
		Size: 1.4 MB (1404645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df125341856c110d1b06fd1d455fc1c0b91bfc6ea9e50cf6517e30b073f140f`  
		Last Modified: Thu, 22 Jan 2026 22:58:58 GMT  
		Size: 25.4 MB (25378228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ace80b3640466fdfb1f93884923c10af79c5a4eb0851c96115ee4800058a906`  
		Last Modified: Thu, 22 Jan 2026 22:58:58 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7da26a763dfa76ed4717afe0262c69463bd4d8980e9a09276d981488ff172c`  
		Last Modified: Thu, 22 Jan 2026 22:58:59 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8373d49de8cdc74650340c566f37cb654fe3e199e2ae6fd680a2aa192e6b101`  
		Last Modified: Thu, 22 Jan 2026 22:58:59 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c360bebdf0273ce4f034334b2367bad538b2bd728ade1da94e81d92b0308cae8`  
		Last Modified: Thu, 22 Jan 2026 22:59:00 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44626b65b5b07b6068396794cd134b103e8b65a40fcc3fbbd327672d95292a1a`  
		Last Modified: Thu, 22 Jan 2026 23:14:10 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:025221048977f74d7b563a6baf7ac89450964a44532255ff95270c401a0ce130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 KB (15112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8382f2f828fa65d0078df11e5203e4f29232526ebc379ef00e89f29db61bada5`

```dockerfile
```

-	Layers:
	-	`sha256:d8dfcd08cb86b53d38a6856a4a5b6daada946dbccba93165424eaa39a2930555`  
		Last Modified: Thu, 22 Jan 2026 23:14:10 GMT  
		Size: 15.1 KB (15112 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:20b423613ede018cf4b3c108c1da04f52bd1ed9c73748820103c119cf2f05d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70811663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1008cc2a4f54fd18877b408545ecaea5bae9e457ecf0ede3993ab4ca8e98479f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 22 Jan 2026 22:56:41 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Jan 2026 22:56:41 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Jan 2026 22:56:41 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Jan 2026 22:56:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Jan 2026 22:56:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 22:56:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Jan 2026 22:56:44 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 22 Jan 2026 22:56:44 GMT
ENV RABBITMQ_VERSION=4.2.3
# Thu, 22 Jan 2026 22:56:44 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Jan 2026 22:56:44 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Jan 2026 22:56:44 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 22:56:50 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Jan 2026 22:56:51 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Jan 2026 22:56:51 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Jan 2026 22:56:51 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Jan 2026 22:56:51 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Jan 2026 22:56:51 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Jan 2026 22:56:51 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 22 Jan 2026 22:56:51 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Jan 2026 22:56:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Jan 2026 22:56:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jan 2026 22:56:51 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Jan 2026 22:56:51 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Jan 2026 23:13:36 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 22 Jan 2026 23:13:36 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-musl'; digest='0dc5e39dac98f38ad50f2aee15cfc5ea53c0ef5e649d79b41c2a7a94376aaf9f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-musl'; digest='fc7ca78e16824a2c77583d067ac1ae4eacbed1516a9a66bec50b5a772530d546' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 22 Jan 2026 23:13:36 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c1c29bbfc534bdb2332c18aca5de0d0e5124edc4bf3cd33c4d5abf68caf192`  
		Last Modified: Thu, 22 Jan 2026 22:57:08 GMT  
		Size: 33.4 MB (33408815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c4f135e530ba71095bbc501a93cc1aefea51200ec4520f807470bf416618f2`  
		Last Modified: Thu, 22 Jan 2026 22:57:07 GMT  
		Size: 7.4 MB (7447274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0c8df31caa52d5097b423f436edf8090c3444e1b87da56d0e884d336d539b1`  
		Last Modified: Thu, 22 Jan 2026 22:57:06 GMT  
		Size: 1.3 MB (1295871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a00f1260e8d71f279228d1e623025bccce76947063756514bb52fbf33739c3b`  
		Last Modified: Thu, 22 Jan 2026 22:57:08 GMT  
		Size: 25.4 MB (25378265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cff304e95dfe1686edbbdbc1f57783bfb46cff75dd81866bedca87d6c5cddb`  
		Last Modified: Thu, 22 Jan 2026 22:57:08 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8170ce806102a6322456abf34ac7cb99d38c8a3ecc01774a2d69822c817d0b2`  
		Last Modified: Thu, 22 Jan 2026 22:57:08 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9714949fca0b589fc5a141007a2b109eb2bb3eea0c0a3edb6ad3a12fb3c945d9`  
		Last Modified: Thu, 22 Jan 2026 22:57:09 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9c7901442abf7ea6d2687910fcbc2a2370877b33fd1d1c7cb81e71a45ace7d`  
		Last Modified: Thu, 22 Jan 2026 22:57:09 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a4254460bcb77efa625ba0311be06b083dfe1d6c54a42dcac0ece5f108d7a6`  
		Last Modified: Thu, 22 Jan 2026 23:13:42 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:54f95d4ee4c67cce7b2e774de6b4aecc946c806697f6bad6b2f529ed68f008d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.3 KB (686255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b660dedce068ce5ef7096f53ef0881b8015d5b04b5ec9803764e530a6c70654`

```dockerfile
```

-	Layers:
	-	`sha256:6d18df581c70f327128613f9326f0da0b54442209b5d55a69204d430bdcf9923`  
		Last Modified: Thu, 22 Jan 2026 23:13:42 GMT  
		Size: 670.9 KB (670928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d48fd0c9f9ec2e5d64d0a067342d92ab98abee3432dbef08d3400f89dd0ba9b`  
		Last Modified: Thu, 22 Jan 2026 23:13:42 GMT  
		Size: 15.3 KB (15327 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:82332c4fa079501973da8d8c01d90be7e860d95ecc5e87da7937ab1cf24b017e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86923906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ee0099e4f06a6eeb2df8911541672dd908578533e2534c9897e68ae8f988b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 22 Jan 2026 22:55:11 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Jan 2026 22:55:11 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Jan 2026 22:55:11 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Jan 2026 22:55:11 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Jan 2026 22:55:11 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 22:55:11 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Jan 2026 22:55:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 22 Jan 2026 22:55:13 GMT
ENV RABBITMQ_VERSION=4.2.3
# Thu, 22 Jan 2026 22:55:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Jan 2026 22:55:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Jan 2026 22:55:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 22:55:20 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Jan 2026 22:55:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Jan 2026 22:55:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Jan 2026 22:55:21 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Jan 2026 22:55:21 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Jan 2026 22:55:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Jan 2026 22:55:21 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 22 Jan 2026 22:55:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Jan 2026 22:55:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Jan 2026 22:55:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jan 2026 22:55:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Jan 2026 22:55:21 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Jan 2026 23:53:22 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 22 Jan 2026 23:53:22 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-musl'; digest='0dc5e39dac98f38ad50f2aee15cfc5ea53c0ef5e649d79b41c2a7a94376aaf9f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-musl'; digest='fc7ca78e16824a2c77583d067ac1ae4eacbed1516a9a66bec50b5a772530d546' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 22 Jan 2026 23:53:22 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b13a74e176a3254250cb92974759505bc10bfe22bdbb2a032df74d155708b93`  
		Last Modified: Thu, 22 Jan 2026 22:55:39 GMT  
		Size: 40.5 MB (40454836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b963f25ef2cd2b387d11ee98f52c2ee00cc861131478c3f7c41d16d59de2895`  
		Last Modified: Thu, 22 Jan 2026 22:55:38 GMT  
		Size: 10.0 MB (9987908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8183f48b820d75c2521034d7814427644eebc021cd3f116f2abdf66ba9f44b`  
		Last Modified: Thu, 22 Jan 2026 22:55:37 GMT  
		Size: 2.5 MB (2514402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b602a4b18e8a13cc2cdf468068534b51c400705a86229c9291e3341928a25a6c`  
		Last Modified: Thu, 22 Jan 2026 22:55:39 GMT  
		Size: 25.4 MB (25378476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaf0f2e07864781e549d7bea8c1cf707b2d8d7adf9486125961052c0ca7d7db`  
		Last Modified: Thu, 22 Jan 2026 22:55:38 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e09fc8091fea877be22ce634ba79f97ac2914f277bc0d12bd0e32b2eb436c86`  
		Last Modified: Thu, 22 Jan 2026 22:55:39 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc1b665b554fd9ebecc9b336e0c684f2d0503b9ca1de3674aa8014a30b06411`  
		Last Modified: Thu, 22 Jan 2026 22:55:40 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcb2382a6fca2db2b826cb2539a6d792fa01741145c4680c1b50a7f529760b8`  
		Last Modified: Thu, 22 Jan 2026 22:55:40 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ffc7962c0ead6932116d3ec4388d8b6fa1ab41dc6b7e2b6075828332d7706a`  
		Last Modified: Thu, 22 Jan 2026 23:53:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64eded500c82966ea356930a51cf2e830e6c20110141e4afa6ac5c216063882`  
		Last Modified: Thu, 22 Jan 2026 23:53:29 GMT  
		Size: 4.4 MB (4390521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:486a5a092b096471c9cabbda45b2582f0b2dcb46cb007853488968449a719e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.3 KB (691286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704fb9e491d8fa1a1b6531b3132cc0c0eb5b7330e73e64c21feb696cf6de675c`

```dockerfile
```

-	Layers:
	-	`sha256:105fd82db5bf36967cec265527782609764f33b02b329c080e97da4c00cb25a4`  
		Last Modified: Thu, 22 Jan 2026 23:53:29 GMT  
		Size: 675.9 KB (675928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f15e0588f0e1563b32a78c79937a6a3f4e438ab9e8645f04216a4a6655cdc599`  
		Last Modified: Thu, 22 Jan 2026 23:53:29 GMT  
		Size: 15.4 KB (15358 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:80c841e82c556d53b9f14cecb04a2522bbf1fbfad8727ac55a6f75433c0abb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73132347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e3a62eb9fcc4784e0001b15d4f8efdda666f75213b2a91dc2ce88600376212`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 22 Jan 2026 22:57:02 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Jan 2026 22:57:02 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Jan 2026 22:57:02 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Jan 2026 22:57:03 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Jan 2026 22:57:03 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 22:57:03 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Jan 2026 22:57:05 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 22 Jan 2026 22:57:05 GMT
ENV RABBITMQ_VERSION=4.2.3
# Thu, 22 Jan 2026 22:57:05 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Jan 2026 22:57:05 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Jan 2026 22:57:05 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 22:57:11 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Jan 2026 22:57:12 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Jan 2026 22:57:12 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Jan 2026 22:57:12 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Jan 2026 22:57:12 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Jan 2026 22:57:12 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Jan 2026 22:57:12 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 22 Jan 2026 22:57:12 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Jan 2026 22:57:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Jan 2026 22:57:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jan 2026 22:57:12 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Jan 2026 22:57:12 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Jan 2026 23:14:57 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 22 Jan 2026 23:14:57 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-musl'; digest='0dc5e39dac98f38ad50f2aee15cfc5ea53c0ef5e649d79b41c2a7a94376aaf9f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-musl'; digest='fc7ca78e16824a2c77583d067ac1ae4eacbed1516a9a66bec50b5a772530d546' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 22 Jan 2026 23:14:57 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:25 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb405e5ffad8c80e754b18463851f53f4da7cbbd486c0dca5c6e0fe068152ce`  
		Last Modified: Thu, 22 Jan 2026 22:57:28 GMT  
		Size: 33.5 MB (33459140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de5b37fbcdec3ca8e757bce63da6abf3c6d2f581cf673484c631f765d98a36d`  
		Last Modified: Thu, 22 Jan 2026 22:57:27 GMT  
		Size: 9.2 MB (9197828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a1222db68efaec4b87e715c40e02ff18fc74af6eaf263f21d28d07e0b021a4`  
		Last Modified: Thu, 22 Jan 2026 22:57:26 GMT  
		Size: 1.4 MB (1409008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37040efa57f41ddf79edde01b4056dd9c189193c4d9ce48dfde8de628695869f`  
		Last Modified: Thu, 22 Jan 2026 22:57:27 GMT  
		Size: 25.4 MB (25378224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87fdfc6e696743ee832952ebee500b699ef5ea6fc1e35c8b3e2772a80beab74`  
		Last Modified: Thu, 22 Jan 2026 22:57:28 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9f3cdd70e8a5f0176df8c4c61a13b6cc3af8970cdd97faeb93ad64f9b6b474`  
		Last Modified: Thu, 22 Jan 2026 22:57:28 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1e4c492bc0e5de3377ce774100ef937895976d9175cc8de80f64961fe993a6`  
		Last Modified: Thu, 22 Jan 2026 22:57:29 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2405d0d3d67d936d41f64777d9edd1782cc2d40a04236717e1d106462e661d33`  
		Last Modified: Thu, 22 Jan 2026 22:57:29 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9e62c498f3489ba6a2892fe7b25c7051beb6acef008f4e011d48d185a7741a`  
		Last Modified: Thu, 22 Jan 2026 23:15:03 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f9ddec617276b7a376d94352019806016057869aa909a3e0d61ec1f2257ea604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.0 KB (685980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7426b7bc4665c629a5064d44d9690e008ce540e6e21c6a4362766db80e5c4a3b`

```dockerfile
```

-	Layers:
	-	`sha256:ac63e2ba94ecbd2b6dc9758fb34b6dd63573dc1e5fedcc84a38e1b95126ecf67`  
		Last Modified: Thu, 22 Jan 2026 23:15:04 GMT  
		Size: 670.8 KB (670780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d64469c55af3f8251d7bbf1006e0b340cb18924b4eecb08ff8e676e18c7ef7fa`  
		Last Modified: Thu, 22 Jan 2026 23:15:04 GMT  
		Size: 15.2 KB (15200 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:d67d26e426c4fb9267343014823d1369122046c40dbce29c9ee0359a46fc5649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74774857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bacce8bbbb030b59d22111691b96521c795e70cece72475874d7a865dd5853`
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
ENV RABBITMQ_VERSION=4.2.3
# Fri, 16 Jan 2026 22:05:00 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 16 Jan 2026 22:05:00 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 16 Jan 2026 22:05:00 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 22:52:42 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Jan 2026 22:52:46 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Jan 2026 22:52:49 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Jan 2026 22:52:49 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Jan 2026 22:52:49 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Jan 2026 22:52:49 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Jan 2026 22:52:49 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 22 Jan 2026 22:52:51 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Jan 2026 22:52:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Jan 2026 22:52:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jan 2026 22:52:52 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Jan 2026 22:52:52 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Jan 2026 23:14:49 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 22 Jan 2026 23:14:49 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-musl'; digest='0dc5e39dac98f38ad50f2aee15cfc5ea53c0ef5e649d79b41c2a7a94376aaf9f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-musl'; digest='fc7ca78e16824a2c77583d067ac1ae4eacbed1516a9a66bec50b5a772530d546' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 22 Jan 2026 23:14:49 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:42 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e8476c5fb2ee33ff8d9e070314e37155747ff62db433260e64f2204af0f548`  
		Last Modified: Fri, 16 Jan 2026 22:06:14 GMT  
		Size: 34.1 MB (34067450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4acb3ea94eb6294cda790a2da6c6caab84dad75807dd9678053e3c6f171e066`  
		Last Modified: Fri, 16 Jan 2026 22:06:12 GMT  
		Size: 10.0 MB (9956659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721090c8af8b0bd3d26f3c79f71d5a6fa60a3c8f94081552584c57fd39b96c92`  
		Last Modified: Fri, 16 Jan 2026 22:06:12 GMT  
		Size: 1.5 MB (1542668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6d568db469a9f9f760e5f9ae5e1b417bdd9e5fd01372818f95aa8dc98772cc`  
		Last Modified: Thu, 22 Jan 2026 22:57:30 GMT  
		Size: 25.4 MB (25378262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4343d511bd9c5af2a25b468a1e83e947a268da7a11bcb2db6a5445e8f2d8031`  
		Last Modified: Thu, 22 Jan 2026 22:57:29 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099e81287403e10771ea56df2652937500af196a4065be8c33036d6686a03f3d`  
		Last Modified: Thu, 22 Jan 2026 22:57:29 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd9ccca46101337f848f7752f83e11ee88f8a45d541cd541b3b42cd2792463b`  
		Last Modified: Thu, 22 Jan 2026 22:57:29 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c82018936015eee380a7b9eeaadac76b88e51c5bb47c97a74c0cd4079db028`  
		Last Modified: Thu, 22 Jan 2026 22:57:30 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8974145efa14e07ece00de02d3d0d33987de858ee706ade2482150526c231c27`  
		Last Modified: Thu, 22 Jan 2026 23:15:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:672dd63e59ee0dbc3a3eb0f95857c8591ebfd2c20b10a914ebd2687fb032598f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.2 KB (686205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f908528e0d0c57af9fa5df7c3f64d8faa72a21cf83586f6d5b4a109161a8c1`

```dockerfile
```

-	Layers:
	-	`sha256:97f66ea2bf4e8c2aca2dc4398980fffc3508327868da929d3184b802ff8c7c1f`  
		Last Modified: Thu, 22 Jan 2026 23:15:07 GMT  
		Size: 670.9 KB (670925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75290b3666235164714bc0d35f9f22ef4f7c7d30ac725da921beee386bbd3f39`  
		Last Modified: Thu, 22 Jan 2026 23:15:07 GMT  
		Size: 15.3 KB (15280 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:cc1e04d542e6d7e004faf7ea1af19dc16f01771593384998e1e4ed767f236462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78639193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e96c7d2b9fcb943c75d3fd3456b6c5a92065da94c29d39f3ef3f1e0bfaee335`
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
# Thu, 22 Jan 2026 12:20:14 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-musl'; digest='0dc5e39dac98f38ad50f2aee15cfc5ea53c0ef5e649d79b41c2a7a94376aaf9f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-musl'; digest='fc7ca78e16824a2c77583d067ac1ae4eacbed1516a9a66bec50b5a772530d546' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 22 Jan 2026 12:20:14 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b16024bea26483c4ecdc60f404c46f57cb84a272c2b594f7f0c40f0b7ca50fb`  
		Last Modified: Fri, 19 Dec 2025 10:57:13 GMT  
		Size: 37.5 MB (37499627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76990ab68bc0fa49949abd7d842d2e3cec338241d21b8d9c5bfb92f2e9746b54`  
		Last Modified: Fri, 19 Dec 2025 10:57:06 GMT  
		Size: 10.8 MB (10786312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff510e29b3470403ce0d3bd1912ea1c8a301f188fadac32a33a5bf6a7940f12f`  
		Last Modified: Fri, 19 Dec 2025 10:57:03 GMT  
		Size: 1.4 MB (1449944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666f4cf3f20e4f9a788134aab3e97c7f6b6824f97c9ae8b231a412121e1b6d08`  
		Last Modified: Fri, 19 Dec 2025 10:57:11 GMT  
		Size: 25.3 MB (25317306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34db82d643b5fb83f1ee2788f9dec1b8d0ce2069d4353f8eec6335713bd0ed9b`  
		Last Modified: Fri, 19 Dec 2025 10:57:05 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b5c0f5d1d4ecba1131ed45747ea34fa1474cb0e4541d511e3c8cc2a4633adf`  
		Last Modified: Fri, 19 Dec 2025 10:57:08 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d9f78729104f576101b211bdac1f9d14473ccc12a8f0bcc0c8e7553f3d99fb`  
		Last Modified: Fri, 19 Dec 2025 10:57:08 GMT  
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
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a6928514ba54a666d73cb1258bad499a1f92622b140eb3527ac5b245188e5582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **689.2 KB (689176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa25234dc51057e8fac324c029d768f64b8669b488c4c98b36d7703239b384c`

```dockerfile
```

-	Layers:
	-	`sha256:588a0c89a1b7528087e95e3e84663a2d5b9b566ef66d47499bcde2f43f1f25c9`  
		Last Modified: Thu, 22 Jan 2026 12:21:09 GMT  
		Size: 673.9 KB (673894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab4b4692e313768b1ce9a365b76118189545fe490f5ec2c66156f68cb885994f`  
		Last Modified: Thu, 22 Jan 2026 12:21:09 GMT  
		Size: 15.3 KB (15282 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:00c04416e43fd2d46604ef583201cf895538e601905e4867ed8c4c89d692a370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72886753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd60e35335176fe40dd18a00c518239adc22118ad6899fe064de012ef253ca52`
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
ENV RABBITMQ_VERSION=4.2.3
# Fri, 16 Jan 2026 21:53:02 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 16 Jan 2026 21:53:02 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 16 Jan 2026 21:53:02 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 22:52:37 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Jan 2026 22:52:37 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Jan 2026 22:52:38 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Jan 2026 22:52:38 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Jan 2026 22:52:38 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Jan 2026 22:52:38 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Jan 2026 22:52:38 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 22 Jan 2026 22:52:38 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Jan 2026 22:52:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Jan 2026 22:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jan 2026 22:52:38 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Jan 2026 22:52:38 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Jan 2026 23:13:23 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 22 Jan 2026 23:13:23 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-musl'; digest='0dc5e39dac98f38ad50f2aee15cfc5ea53c0ef5e649d79b41c2a7a94376aaf9f' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-musl'; digest='fc7ca78e16824a2c77583d067ac1ae4eacbed1516a9a66bec50b5a772530d546' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 22 Jan 2026 23:13:23 GMT
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
		Last Modified: Fri, 16 Jan 2026 21:53:32 GMT  
		Size: 8.3 MB (8346917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7432bfb1d8aedf7ebcc8b43143fb0f854e676924caa12048ca5cdc6446033c33`  
		Last Modified: Fri, 16 Jan 2026 21:53:32 GMT  
		Size: 1.5 MB (1515892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4b6847177db99b7ed52cf516b58bd9c294024e46c1c6b4fb6ed70f16450fc1`  
		Last Modified: Thu, 22 Jan 2026 22:58:20 GMT  
		Size: 25.4 MB (25378188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093cc34362cbf56f297c0f089ac83e9602a3610b9d082e57ae66a126a0b6d52f`  
		Last Modified: Thu, 22 Jan 2026 22:58:19 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e21d3017353a0f0b7e3f0f2f83c4c73405161364dac50e738a310fbed1e732`  
		Last Modified: Thu, 22 Jan 2026 22:58:19 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445bde023368e651516d754c4da7cc392e00c628b72dde38a5feaf08dbd3bb90`  
		Last Modified: Thu, 22 Jan 2026 22:58:19 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b523e6dbb93fa67bbdf2f0418ac8e3f400cc63d79417ee31484353b2c77784`  
		Last Modified: Thu, 22 Jan 2026 22:58:20 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc3dbaccfc345474d998a5a6e42dfc80312b7120b7a881f4bc55722a60e5293`  
		Last Modified: Thu, 22 Jan 2026 23:13:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:df4c3e2b1c1d014858cbdafe9bae274815126a3f0bba8cec55f2925a4828126e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.1 KB (686125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d03b83778d6d7a4c26de728b30fc1219a5eae100df7f8220b26b6147a8afe97`

```dockerfile
```

-	Layers:
	-	`sha256:f87f438789c9656ee2618fe4c36e32042c8fcde51aa0698157d4fe29774545df`  
		Last Modified: Thu, 22 Jan 2026 23:13:34 GMT  
		Size: 670.9 KB (670891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc4490a196ea6c5dcd77107346399ba29eec8c31c4e1dfc68a7d79cdf3bf84b6`  
		Last Modified: Thu, 22 Jan 2026 23:13:34 GMT  
		Size: 15.2 KB (15234 bytes)  
		MIME: application/vnd.in-toto+json
