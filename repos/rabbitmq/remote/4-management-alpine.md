## `rabbitmq:4-management-alpine`

```console
$ docker pull rabbitmq@sha256:906b854143d88adf622b0bb7768b11f5ee509c62b7f368299b260cd712d1ccd5
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
$ docker pull rabbitmq@sha256:b10cafe809521dc26a4593a0ae9ce992772d16f571101a0018ade5c7f35a77c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88504964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5edf76032bc4c7d0c955a0742307621de59a2b3a011997e93ddddde2d954f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2026 17:22:44 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 23 Apr 2026 17:22:44 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 23 Apr 2026 17:22:44 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 23 Apr 2026 17:22:44 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 23 Apr 2026 17:22:44 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:22:44 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 23 Apr 2026 17:22:46 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 23 Apr 2026 17:22:46 GMT
ENV RABBITMQ_VERSION=4.3.0
# Thu, 23 Apr 2026 17:22:46 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 23 Apr 2026 17:22:46 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 23 Apr 2026 17:22:46 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:22:52 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 23 Apr 2026 17:22:53 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 23 Apr 2026 17:22:53 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 23 Apr 2026 17:22:53 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 23 Apr 2026 17:22:53 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 23 Apr 2026 17:22:53 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 23 Apr 2026 17:22:53 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 23 Apr 2026 17:22:53 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 23 Apr 2026 17:22:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 17:22:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 17:22:53 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 23 Apr 2026 17:22:53 GMT
CMD ["rabbitmq-server"]
# Thu, 23 Apr 2026 17:25:24 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 23 Apr 2026 17:25:25 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-x86_64-unknown-linux-musl'; digest='cd5f56199daf7bf66cbe81e69340766fafde493bb46c9170a3bd271bb1967831' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-aarch64-unknown-linux-musl'; digest='3806e34c27de3faa722f7e5eca6def6dd1d4ad0100ee176ba0553bea35ba9801' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 23 Apr 2026 17:25:25 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fb0f2d32b8d08ca47b09e3145a451596603b73347112e134912ba526436709`  
		Last Modified: Thu, 23 Apr 2026 17:23:09 GMT  
		Size: 42.6 MB (42625097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224a6f79a26e6e07ae2a9be498a15c45ddc4fd7121c8e9b8c76d4e03a2ca1117`  
		Last Modified: Thu, 23 Apr 2026 17:23:08 GMT  
		Size: 9.2 MB (9201514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30e79de10863afebaaf510b6d18d8e2631a7d83765402dc8fcd771795503304`  
		Last Modified: Thu, 23 Apr 2026 17:23:07 GMT  
		Size: 2.5 MB (2465324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b107c94ea26cbf045b581a4198b7bb19ba4b7f4215f08216838f3334f68384`  
		Last Modified: Thu, 23 Apr 2026 17:23:09 GMT  
		Size: 25.9 MB (25905737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545ce156c46844fd549dc207ccb0f26ddf3c05f00cba1be9d014e66b1ad382b6`  
		Last Modified: Thu, 23 Apr 2026 17:23:09 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26db462b355331811d3e9387bfdb215ebb4c0e83690317134e55d67556766c23`  
		Last Modified: Thu, 23 Apr 2026 17:23:10 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee7b96b5b882bcd927cf164cb614be3e3bdeb15124e0153ece93f0d146f6c42`  
		Last Modified: Thu, 23 Apr 2026 17:23:10 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cbe6e56f3bf8c39b83f8bec75ac4ebdc9e9a989b1cbe79f030b202cf8e6003`  
		Last Modified: Thu, 23 Apr 2026 17:23:11 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d7e329b362c6747704cd1e3b1a7c49908a963d5b898713a6522505dae3f46c`  
		Last Modified: Thu, 23 Apr 2026 17:25:30 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d961b2b13cc8b376dc7208a02b47a7a61f01deb3e2d307e22a4ae3fd9aab5c26`  
		Last Modified: Thu, 23 Apr 2026 17:25:30 GMT  
		Size: 4.4 MB (4441084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2c5258705d9f951e8f4843389d6361c0b9e102b0eeab13185d4f3d199d0efd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.1 KB (691136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee18a438b35d1c11b62f010d09d94f352d1772b949689bf6010b93dceab1deb`

```dockerfile
```

-	Layers:
	-	`sha256:3a02d18f7b6a634678654cedd8a0d33659a38e286ba14bf284ac0170a37ee52a`  
		Last Modified: Thu, 23 Apr 2026 17:25:30 GMT  
		Size: 675.9 KB (675897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d1d59e9f09d81354837b32a6eaf15e5fac4c318c37b223878d53394ce5bd2dc`  
		Last Modified: Thu, 23 Apr 2026 17:25:30 GMT  
		Size: 15.2 KB (15239 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:5154018c9118d4d4dd059c75647ce93c2edf2a6db9d7276177779668958fa0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71771497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac9c8540f4f14fca00ee18aff8a07dd95f16af52522c7ba97e7067ad2cd5f5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 22:28:03 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 21 Apr 2026 22:28:03 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 21 Apr 2026 22:28:03 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 21 Apr 2026 22:28:03 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 21 Apr 2026 22:28:03 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 22:28:03 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 21 Apr 2026 22:28:06 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 21 Apr 2026 22:28:06 GMT
ENV RABBITMQ_VERSION=4.2.5
# Tue, 21 Apr 2026 22:28:06 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 21 Apr 2026 22:28:06 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 21 Apr 2026 22:28:06 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 22:28:15 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 21 Apr 2026 22:28:17 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 21 Apr 2026 22:28:18 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 21 Apr 2026 22:28:18 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 21 Apr 2026 22:28:18 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 21 Apr 2026 22:28:18 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 21 Apr 2026 22:28:18 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 21 Apr 2026 22:28:18 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 21 Apr 2026 22:28:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 22:28:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 22:28:18 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 21 Apr 2026 22:28:18 GMT
CMD ["rabbitmq-server"]
# Tue, 21 Apr 2026 22:59:47 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 21 Apr 2026 22:59:47 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-x86_64-unknown-linux-musl'; digest='cd5f56199daf7bf66cbe81e69340766fafde493bb46c9170a3bd271bb1967831' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-aarch64-unknown-linux-musl'; digest='3806e34c27de3faa722f7e5eca6def6dd1d4ad0100ee176ba0553bea35ba9801' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 21 Apr 2026 22:59:47 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3345b7636541e872ce2be5df43694154c15dfe0c9b8bef4630a1270791513ab`  
		Last Modified: Tue, 21 Apr 2026 22:28:25 GMT  
		Size: 33.5 MB (33520172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fedec92f331b5601113d87841c500c3c0dc5271705689ab1572298b37a3d8eb`  
		Last Modified: Tue, 21 Apr 2026 22:28:24 GMT  
		Size: 7.9 MB (7856514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac1285dd6c232b87097e983acf7f4046545014555cddc9758728e2acabdac99`  
		Last Modified: Tue, 21 Apr 2026 22:28:24 GMT  
		Size: 1.4 MB (1404372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afa4328a9d7c91722e66684bc518197ff8c79bb5565060ad22d00229f0338c7`  
		Last Modified: Tue, 21 Apr 2026 22:28:25 GMT  
		Size: 25.4 MB (25416519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4cd6b3d33db803835cbd741cf62e4a69359944fe750af460c92c250686f96c`  
		Last Modified: Tue, 21 Apr 2026 22:28:25 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42881cb54e74d8c5be5c881b025cbdfa4c351bb3fc77ba0971f73513e370d9d9`  
		Last Modified: Tue, 21 Apr 2026 22:28:26 GMT  
		Size: 107.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5d8a4fec7e927207d1a9e58278ac472d11a8e254240d5e6983510bb3811468`  
		Last Modified: Tue, 21 Apr 2026 22:28:27 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9fa203ceb388ebc6127638edefcca15929ea1b56995c0a071c833e79497e1c`  
		Last Modified: Tue, 21 Apr 2026 22:28:27 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e6e0bf543e3cf124077df9acdbd93e09ea3fdb2a0165e018e968422c048569`  
		Last Modified: Tue, 21 Apr 2026 22:59:51 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:179edd95f25c4585b83417d3ad353d188d7a35786570861407fe9bdfa0753bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 KB (15112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e5796cf77e445298f2b57d607df7193d5e87146a8f4834c3ab61d13ef49c8f`

```dockerfile
```

-	Layers:
	-	`sha256:83552794bd7e6a508c85abb0bd7a6741fd264ead59563a581e1d05dc38df6156`  
		Last Modified: Tue, 21 Apr 2026 22:59:51 GMT  
		Size: 15.1 KB (15112 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:340f3961c7110606d9f3cb9e3abfe6c16e0301f6e77db32a7208495d3369e0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71353533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a6b146db1d82a12e2d2e295963ee8f1a69a6ee0990846151f4bdd92781229d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2026 17:22:07 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 23 Apr 2026 17:22:07 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 23 Apr 2026 17:22:07 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 23 Apr 2026 17:22:07 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 23 Apr 2026 17:22:07 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:22:07 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 23 Apr 2026 17:22:10 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 23 Apr 2026 17:22:10 GMT
ENV RABBITMQ_VERSION=4.3.0
# Thu, 23 Apr 2026 17:22:10 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 23 Apr 2026 17:22:10 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 23 Apr 2026 17:22:10 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:22:16 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 23 Apr 2026 17:22:17 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 23 Apr 2026 17:22:17 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 23 Apr 2026 17:22:17 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 23 Apr 2026 17:22:17 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 23 Apr 2026 17:22:17 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 23 Apr 2026 17:22:17 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 23 Apr 2026 17:22:17 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 23 Apr 2026 17:22:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 17:22:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 17:22:17 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 23 Apr 2026 17:22:17 GMT
CMD ["rabbitmq-server"]
# Thu, 23 Apr 2026 17:25:43 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 23 Apr 2026 17:25:43 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-x86_64-unknown-linux-musl'; digest='cd5f56199daf7bf66cbe81e69340766fafde493bb46c9170a3bd271bb1967831' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-aarch64-unknown-linux-musl'; digest='3806e34c27de3faa722f7e5eca6def6dd1d4ad0100ee176ba0553bea35ba9801' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 23 Apr 2026 17:25:43 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef2d04aebce00307a48f4c2583035721545245104feac4663fe12c0b05cb534`  
		Last Modified: Thu, 23 Apr 2026 17:22:34 GMT  
		Size: 33.4 MB (33429489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0d0a0ce854b90557407cb514c751cb08887de3dea23ee1d06414f8ca1ab65b`  
		Last Modified: Thu, 23 Apr 2026 17:22:33 GMT  
		Size: 7.4 MB (7437795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7832c92953051110aca5d2c00008fc1840eb639bf1f2e4283bd92d6d264d37f`  
		Last Modified: Thu, 23 Apr 2026 17:22:32 GMT  
		Size: 1.3 MB (1295659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db1a8f3988a0436c3516345bf977b3cd2ec627c6757c6ccffec86ea1a7a19e3`  
		Last Modified: Thu, 23 Apr 2026 17:22:33 GMT  
		Size: 25.9 MB (25905415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca772b2a7302f948501c1eb95a3d9c23571764d74ace594fd3efd35614e56e0`  
		Last Modified: Thu, 23 Apr 2026 17:22:33 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f200abb40121af8e3a4685c051db369f4bbe8b7b0682428fd6db7d7f8618d1f0`  
		Last Modified: Thu, 23 Apr 2026 17:22:34 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeab179b9f388265ae469656e6fb87d6a5555a98bad95328375df0d66ffedd1`  
		Last Modified: Thu, 23 Apr 2026 17:22:35 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107134fdc22ea0d0f4ca8226ffa6561b9584eb6e5ddc1d110c7dfc0941077d70`  
		Last Modified: Thu, 23 Apr 2026 17:22:35 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01f87f493ee289bde98992b9c28223f8272f1cb069fdc26f578d47d8d9730b1`  
		Last Modified: Thu, 23 Apr 2026 17:25:49 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2136b35d80a6c8cb352dcf16f07e3ca5d470c2142b8aaa6f2fba5655a5c92921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.4 KB (686367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b6f04ba24d601d99a5665ad23140f9e4428ba511cc5d8340642fda37a15b63`

```dockerfile
```

-	Layers:
	-	`sha256:4c1fe2b3cccfcde960d5290cc476a641489fbe81794e4daecc05d864774c8a49`  
		Last Modified: Thu, 23 Apr 2026 17:25:49 GMT  
		Size: 671.0 KB (671040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d22a072cd9c40ef6526cdc06ddea9af8bfa2ad69bd0e5b5406f0d99db373b621`  
		Last Modified: Thu, 23 Apr 2026 17:25:49 GMT  
		Size: 15.3 KB (15327 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:95a8b59483e41a0fa5057690b2f4e74451fbf439d8e56306ff617d35474a9b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87216718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c570fe6bcb9a7269884319a294a1bb7f8d1c695b1f5b5861c3291d9aa13e6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2026 17:21:45 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 23 Apr 2026 17:21:45 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 23 Apr 2026 17:21:45 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 23 Apr 2026 17:21:45 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 23 Apr 2026 17:21:45 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:21:45 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 23 Apr 2026 17:21:47 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 23 Apr 2026 17:21:47 GMT
ENV RABBITMQ_VERSION=4.3.0
# Thu, 23 Apr 2026 17:21:47 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 23 Apr 2026 17:21:47 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 23 Apr 2026 17:21:47 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:21:53 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 23 Apr 2026 17:21:54 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 23 Apr 2026 17:21:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 23 Apr 2026 17:21:54 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 23 Apr 2026 17:21:54 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 23 Apr 2026 17:21:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 23 Apr 2026 17:21:54 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 23 Apr 2026 17:21:54 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 23 Apr 2026 17:21:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 17:21:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 17:21:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 23 Apr 2026 17:21:54 GMT
CMD ["rabbitmq-server"]
# Thu, 23 Apr 2026 17:25:29 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 23 Apr 2026 17:25:30 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-x86_64-unknown-linux-musl'; digest='cd5f56199daf7bf66cbe81e69340766fafde493bb46c9170a3bd271bb1967831' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-aarch64-unknown-linux-musl'; digest='3806e34c27de3faa722f7e5eca6def6dd1d4ad0100ee176ba0553bea35ba9801' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 23 Apr 2026 17:25:30 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38b11a5a9977b59af525563265b5171b76be2dae23882662335b4164cea2419`  
		Last Modified: Thu, 23 Apr 2026 17:22:11 GMT  
		Size: 40.5 MB (40485299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6697b371fcb253fe1eecb04534a4ef5feffa2a146fe3798f9cc8f691ef06c3fd`  
		Last Modified: Thu, 23 Apr 2026 17:22:10 GMT  
		Size: 10.0 MB (9984528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec0b528bf2c0c2930d113ca7352f5f489db6432fce04bb88eb5f79b9c839768`  
		Last Modified: Thu, 23 Apr 2026 17:22:09 GMT  
		Size: 2.5 MB (2514179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad8dc3f73353cd80d649e8713ab899c593c23007dca3f7d9bab7f17a189f387`  
		Last Modified: Thu, 23 Apr 2026 17:22:11 GMT  
		Size: 25.9 MB (25905808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92cb9479d0e5c49a0f3bb768e5537a1192ffe38b0bc8d6724c5ed093622f47f`  
		Last Modified: Thu, 23 Apr 2026 17:22:11 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79801872ecfaec5a58e84a0c1cd0b9fc2f0efbca920b97f8cb76ad1242630102`  
		Last Modified: Thu, 23 Apr 2026 17:22:11 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bbbe8943c8f7f91c68f6b74afa93acb355cc3370c8bfe3dc544e0ff475b51a`  
		Last Modified: Thu, 23 Apr 2026 17:22:12 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da069a858fec46591802e4d9caab9b8e383806575a8c5b0354736dd1063589f5`  
		Last Modified: Thu, 23 Apr 2026 17:22:12 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be3d1a80d18abcdddaf48fc28d5bd6e52c18ddc925cee1ec6dd8b35582a77c5`  
		Last Modified: Thu, 23 Apr 2026 17:25:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7784682a3618112a516f50b91007149fda28eb590f04934ad82e64e390763576`  
		Last Modified: Thu, 23 Apr 2026 17:25:35 GMT  
		Size: 4.1 MB (4125015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:cd0f664827bf4f744eadd86137f2368ebdfd3566a1cdbd92864fea91c04fd4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.4 KB (691398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a551a14247047aeabd1eac20b17777c00fb3461ca75818aae2d20e23afabc9a`

```dockerfile
```

-	Layers:
	-	`sha256:af9e989e6d0b493c6d9b05b704c7629122139b990e0b3e2334ef68dc4ba0bcc3`  
		Last Modified: Thu, 23 Apr 2026 17:25:35 GMT  
		Size: 676.0 KB (676040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f03c6df00f997657fdc48227355a1bee18676797d337009a6d36cd962b51f82`  
		Last Modified: Thu, 23 Apr 2026 17:25:35 GMT  
		Size: 15.4 KB (15358 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:5c102c5cede001b93969eef256c2e02d26b4f11a4ba70e7b623e754cffa4e665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73195584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f14386bb5f9e8a3ddf596edddd33888afbcff9f5d03c78c9c5469d7e72ea74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 22:29:19 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 21 Apr 2026 22:29:19 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 21 Apr 2026 22:29:19 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 21 Apr 2026 22:29:19 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 21 Apr 2026 22:29:19 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 22:29:19 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 21 Apr 2026 22:29:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 21 Apr 2026 22:29:22 GMT
ENV RABBITMQ_VERSION=4.2.5
# Tue, 21 Apr 2026 22:29:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 21 Apr 2026 22:29:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 21 Apr 2026 22:29:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 22:29:28 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 21 Apr 2026 22:29:29 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 21 Apr 2026 22:29:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 21 Apr 2026 22:29:29 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 21 Apr 2026 22:29:29 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 21 Apr 2026 22:29:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 21 Apr 2026 22:29:29 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 21 Apr 2026 22:29:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 21 Apr 2026 22:29:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 22:29:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 22:29:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 21 Apr 2026 22:29:29 GMT
CMD ["rabbitmq-server"]
# Tue, 21 Apr 2026 23:02:37 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 21 Apr 2026 23:02:37 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-x86_64-unknown-linux-musl'; digest='cd5f56199daf7bf66cbe81e69340766fafde493bb46c9170a3bd271bb1967831' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-aarch64-unknown-linux-musl'; digest='3806e34c27de3faa722f7e5eca6def6dd1d4ad0100ee176ba0553bea35ba9801' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 21 Apr 2026 23:02:37 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cd82d062ef7b0d94d7f55637909d9593d5434b58cfe02f45673d7cb71e4370`  
		Last Modified: Tue, 21 Apr 2026 22:29:46 GMT  
		Size: 33.5 MB (33485624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b93e459cfc066ddec7cef359839d55fc77c57287d29546d3b7e7e64fc36642c`  
		Last Modified: Tue, 21 Apr 2026 22:29:44 GMT  
		Size: 9.2 MB (9192215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080eec3a39cd77bb4b3f60b2c65d1cd99883f4ccdb53e03ee0867e47af04128e`  
		Last Modified: Tue, 21 Apr 2026 22:29:43 GMT  
		Size: 1.4 MB (1408803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c4de7edd7bc048d226bcffa989f2e7b1ea100ddc2ec0b84f67a7b83922e856`  
		Last Modified: Tue, 21 Apr 2026 22:29:45 GMT  
		Size: 25.4 MB (25416444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9933e29e5be9f6395152163bf5e42e14ec767c46605cd8cb6cbcf329c88b998a`  
		Last Modified: Tue, 21 Apr 2026 22:29:45 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bce6a486dd36d3b2f7d77e25e4e197d0149b6a00a2a0cb10a26547c0bb44a2`  
		Last Modified: Tue, 21 Apr 2026 22:29:46 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48ae3490e21494fb1a76507dcb7b539274e27f43177860933dd7115ea33cb65`  
		Last Modified: Tue, 21 Apr 2026 22:29:46 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0dd08b61ac84cb89f91fbd52f0e56125ddee753de049307a2152b3f87e173b`  
		Last Modified: Tue, 21 Apr 2026 22:29:46 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c6936642723e1ba1e5ab54a6349e792c719ba04a02509d01e85aee68977134`  
		Last Modified: Tue, 21 Apr 2026 23:02:43 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3b07f5ddd3f3f815d09bf1b7807d83ce4ba4666a712b835658062313c36fa236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.0 KB (686028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb68bc17146432e893f8d6f2c93b60d3fae5277795731504f9c7625d157f0e8`

```dockerfile
```

-	Layers:
	-	`sha256:7171537313b7f11254e04801abd87e8f7d633325c343540bdc5fe29bc20a3420`  
		Last Modified: Tue, 21 Apr 2026 23:02:43 GMT  
		Size: 670.8 KB (670828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7961d84ca604004cf9881f5cc820e91a9bb9089d66148283b29cfd011feb1f03`  
		Last Modified: Tue, 21 Apr 2026 23:02:43 GMT  
		Size: 15.2 KB (15200 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:7309a2a30081f699c676bd2c5b1e8cbfa43f115a0d50aa8d3ede6753b039b9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74845325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddcdd8b4b70d1721958a266c8591f3f0d6b08f96affe46db0b551d0dea5bf24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 22:28:23 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 21 Apr 2026 22:28:23 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 21 Apr 2026 22:28:23 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 21 Apr 2026 22:28:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 21 Apr 2026 22:28:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 22:28:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 21 Apr 2026 22:28:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 21 Apr 2026 22:28:29 GMT
ENV RABBITMQ_VERSION=4.2.5
# Tue, 21 Apr 2026 22:28:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 21 Apr 2026 22:28:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 21 Apr 2026 22:28:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 22:32:19 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 21 Apr 2026 22:32:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 21 Apr 2026 22:32:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 21 Apr 2026 22:32:21 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 21 Apr 2026 22:32:21 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 21 Apr 2026 22:32:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 21 Apr 2026 22:32:21 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 21 Apr 2026 22:32:22 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 21 Apr 2026 22:32:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 22:32:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 22:32:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 21 Apr 2026 22:32:22 GMT
CMD ["rabbitmq-server"]
# Tue, 21 Apr 2026 23:00:50 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 21 Apr 2026 23:00:50 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-x86_64-unknown-linux-musl'; digest='cd5f56199daf7bf66cbe81e69340766fafde493bb46c9170a3bd271bb1967831' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-aarch64-unknown-linux-musl'; digest='3806e34c27de3faa722f7e5eca6def6dd1d4ad0100ee176ba0553bea35ba9801' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 21 Apr 2026 23:00:50 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edcfe834f5ce56d9f96aafb64020c446ce3da6c8b49dfd0cc8a6316f3e5ae81`  
		Last Modified: Tue, 21 Apr 2026 22:29:24 GMT  
		Size: 34.1 MB (34093673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7d2cb35068bf3142dd24607e66d95b8a93e65b501a261a52544ee95e618303`  
		Last Modified: Tue, 21 Apr 2026 22:29:23 GMT  
		Size: 10.0 MB (9959826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145516326b769e06bf43d9af6372390e7a743f95362f05aa55e906bec2b8f87d`  
		Last Modified: Tue, 21 Apr 2026 22:29:22 GMT  
		Size: 1.5 MB (1542422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68824d6dcb502ff7df08915ce6fd1e8728fa4732d1da9ec304660bfbd7a665c2`  
		Last Modified: Tue, 21 Apr 2026 22:37:54 GMT  
		Size: 25.4 MB (25416425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a1d779eadea50d3ba767a531a514d6f8a5cf3cb720ada5236b3d7a160a2a60`  
		Last Modified: Tue, 21 Apr 2026 22:37:53 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733c4f567ab3186661719643e8c5d094447936786ecee1b97baf74208eba6a93`  
		Last Modified: Tue, 21 Apr 2026 22:37:53 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a92637da6a757a1db3138f62b7347cf6542564085428066fc1454677543feb`  
		Last Modified: Tue, 21 Apr 2026 22:37:53 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302e274fe3150e428ff5e20940ec8c78a57536eabc414d14ea671e451bd441da`  
		Last Modified: Tue, 21 Apr 2026 22:37:54 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74343b31bba344b1180a6f885ff3f3881688c9f9d186b64696d3c18561b3762`  
		Last Modified: Tue, 21 Apr 2026 23:01:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c0617c36cc24ed5944e953ee6fbc533b9dce710012b67cb53c6ae456897b1094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.3 KB (686252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e528d28a66e6f8de6f8b457f0141ff3d7222a9f4ea54398bc62de2dbed587aa`

```dockerfile
```

-	Layers:
	-	`sha256:30ca9774b2c0412d7b33342473a09be9e7037137caeaf64553a03f659826c770`  
		Last Modified: Tue, 21 Apr 2026 23:01:03 GMT  
		Size: 671.0 KB (670973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8649c023609eaa0cb0f2da5ef787a2b47b306017e055a99b6b3ff3639ebf65`  
		Last Modified: Tue, 21 Apr 2026 23:01:03 GMT  
		Size: 15.3 KB (15279 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:1c98e7d3f1dc2fa26f7007579060057626fec199a68cc01e892999bd12cbdf08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78766173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48528babf0972d0ec5df2896f4215e11286a86390834296f5918cad1554f1be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 23:59:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 16 Apr 2026 23:59:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 16 Apr 2026 23:59:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 16 Apr 2026 23:59:53 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 16 Apr 2026 23:59:53 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 23:59:53 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 17 Apr 2026 00:00:05 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 17 Apr 2026 00:00:05 GMT
ENV RABBITMQ_VERSION=4.2.5
# Fri, 17 Apr 2026 00:00:05 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 17 Apr 2026 00:00:05 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 17 Apr 2026 00:00:05 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:17:00 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 17 Apr 2026 00:17:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 17 Apr 2026 00:17:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 17 Apr 2026 00:17:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 17 Apr 2026 00:17:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 17 Apr 2026 00:17:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 17 Apr 2026 00:17:09 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 17 Apr 2026 00:17:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 17 Apr 2026 00:17:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:17:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 17 Apr 2026 00:17:09 GMT
CMD ["rabbitmq-server"]
# Sat, 18 Apr 2026 02:00:21 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Sat, 18 Apr 2026 02:00:21 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-x86_64-unknown-linux-musl'; digest='cd5f56199daf7bf66cbe81e69340766fafde493bb46c9170a3bd271bb1967831' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-aarch64-unknown-linux-musl'; digest='3806e34c27de3faa722f7e5eca6def6dd1d4ad0100ee176ba0553bea35ba9801' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Sat, 18 Apr 2026 02:00:21 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f381e086b7d46fed97fd0163257024b9eaeca27e568e09fcae61a1f8610894`  
		Last Modified: Fri, 17 Apr 2026 00:04:53 GMT  
		Size: 37.5 MB (37522767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab11e049553f99b2ef54ffdc7f0c070f04083098c7db9d49872eebd13f4730e`  
		Last Modified: Fri, 17 Apr 2026 00:04:47 GMT  
		Size: 10.8 MB (10787543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3890ec1a157d7985c28603b2842fa2448623348b51d26951676226f8bc5a237`  
		Last Modified: Fri, 17 Apr 2026 00:04:42 GMT  
		Size: 1.4 MB (1449750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95baeee9f5122024d241f3300c1d4c075ec42001b88679aaef4ddedaebe735f`  
		Last Modified: Fri, 17 Apr 2026 00:21:22 GMT  
		Size: 25.4 MB (25416396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fde9d67d1cae5cac95be49c4b0c6045e21fe9e6db80a91ade19e6622ef6873`  
		Last Modified: Fri, 17 Apr 2026 00:21:17 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3a1a828e37d191bafa76e2d6135a6b91088c461a29963b7fbbfccbb4ea3bc9`  
		Last Modified: Fri, 17 Apr 2026 00:21:17 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac394302f8e14abaca7f38042173f5abc8d43667b3c6d485e82b586487032813`  
		Last Modified: Fri, 17 Apr 2026 00:21:17 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cc8c017a316afb5d5fc0650fc7792df798d9c598817f6e39f5a7249f0ebc1`  
		Last Modified: Fri, 17 Apr 2026 00:21:19 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dfb926fe6ac9eb8c88758990daf018e3ac4c947aec1e0120be586117ef3fa5`  
		Last Modified: Sat, 18 Apr 2026 02:01:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6698e885db67163a018fd4d340fbada6c85844c81243441f0acfabfee0b1709d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **689.2 KB (689225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e854d21e4042646496a8087250281a861b519c25cbab79a47b6615c884fc49`

```dockerfile
```

-	Layers:
	-	`sha256:adc08d44072530e24ea36f7a058847efc2fd7623f326a5d7e7fe17d728c9d817`  
		Last Modified: Sat, 18 Apr 2026 02:01:16 GMT  
		Size: 673.9 KB (673942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91b29aefe346ece056c7afcc18633e69dffa82d45ce65ad332ed8b73f507d026`  
		Last Modified: Sat, 18 Apr 2026 02:01:16 GMT  
		Size: 15.3 KB (15283 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:17d8c19223b3f82931304cd1cdea24c64f20f15345df00072b49e6ac7b19301c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72954270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d278487fe19cc1aff29a7e6815a76adcf570d5b30c203223297bb524e1cdd46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 22:30:00 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 21 Apr 2026 22:30:00 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 21 Apr 2026 22:30:00 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 21 Apr 2026 22:30:00 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 21 Apr 2026 22:30:00 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 22:30:00 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 21 Apr 2026 22:30:03 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 21 Apr 2026 22:30:03 GMT
ENV RABBITMQ_VERSION=4.2.5
# Tue, 21 Apr 2026 22:30:03 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 21 Apr 2026 22:30:03 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 21 Apr 2026 22:30:03 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 22:30:10 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 21 Apr 2026 22:30:11 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 21 Apr 2026 22:30:11 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 21 Apr 2026 22:30:11 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 21 Apr 2026 22:30:11 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 21 Apr 2026 22:30:11 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 21 Apr 2026 22:30:11 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 21 Apr 2026 22:30:11 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 21 Apr 2026 22:30:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 22:30:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 22:30:11 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 21 Apr 2026 22:30:11 GMT
CMD ["rabbitmq-server"]
# Tue, 21 Apr 2026 23:00:10 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 21 Apr 2026 23:00:10 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 		case "$arch" in 		'x86_64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-x86_64-unknown-linux-musl'; digest='cd5f56199daf7bf66cbe81e69340766fafde493bb46c9170a3bd271bb1967831' ;; 		'aarch64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-aarch64-unknown-linux-musl'; digest='3806e34c27de3faa722f7e5eca6def6dd1d4ad0100ee176ba0553bea35ba9801' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum -c -; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 21 Apr 2026 23:00:10 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b97ca3a7e0b77cd9dd2e046b5509de95a1845f3bef120eaeb1079d05be3b80`  
		Last Modified: Tue, 21 Apr 2026 22:30:37 GMT  
		Size: 33.9 MB (33948924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a0f3196d00a2d3f94ccad32e747d70ce4297d26609ad2b9e075f027555c221`  
		Last Modified: Tue, 21 Apr 2026 22:30:36 GMT  
		Size: 8.3 MB (8344750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bf8d400f42161d9d6f4a6a66b3039f1417bb68e0481acfa2626652d78afdde`  
		Last Modified: Tue, 21 Apr 2026 22:30:36 GMT  
		Size: 1.5 MB (1515698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517603ab680ec6ac00e93ce18f0fbd70751a0263075afd4de1d66c658d1631e7`  
		Last Modified: Tue, 21 Apr 2026 22:30:37 GMT  
		Size: 25.4 MB (25416311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a7edb71fd20f8dc0291cf6bf98f4a384fce1e0edea22d8039e45240f052804`  
		Last Modified: Tue, 21 Apr 2026 22:30:37 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1854d0f223366c33a364ab22b6745ad696a5c6ea43fcdf0156a6695f7bf4646b`  
		Last Modified: Tue, 21 Apr 2026 22:30:37 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61144c6395c099d3d2161c6942a6c2c2c9953cf883b02faae1b215cf3dfebb1d`  
		Last Modified: Tue, 21 Apr 2026 22:30:38 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60133527295bb584c253c48f0c94091cdc69db80a5b44c620f2ad6cdb15d18f0`  
		Last Modified: Tue, 21 Apr 2026 22:30:38 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106d4c27e489e9db8bb03b7aefe6ad9567b9737391432c308a79405956eb1845`  
		Last Modified: Tue, 21 Apr 2026 23:00:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0def5ab63cbe4a3467110b34166a38f8869b814742ceca5c8f53bc223f02f5a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.2 KB (686173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97d8b8f6304a4ae77fd5317740c0dce7a8ca44cb5be91661a75f6740d324231`

```dockerfile
```

-	Layers:
	-	`sha256:fdd77cfefdcf0ec7bd73f30ef2c5b1d289522828a47b56005fa5eefd09152cc1`  
		Last Modified: Tue, 21 Apr 2026 23:00:22 GMT  
		Size: 670.9 KB (670939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:552d2fac9cc781274b71b56e046150f80be475907929ab594db0f89907e3a893`  
		Last Modified: Tue, 21 Apr 2026 23:00:24 GMT  
		Size: 15.2 KB (15234 bytes)  
		MIME: application/vnd.in-toto+json
