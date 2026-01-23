## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:76ab3719f2e31631383c7cc5be8a7c25994037f60e141f4d36efc453a5ec3790
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
$ docker pull rabbitmq@sha256:bd28c47a17bc72cd56159d28cb24cb308991751ab8ebfbd030f95be264529334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83511624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914a135a3a7980239f49a8356103f155d4f67448c3af92dbb11c6969157e4bbb`
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

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0c53fef314bf782e51984073f0a071f698fe40fc858a6896cbff23da41bd2e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6963072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edeaa6d946ecd96799fa3e1fd8a981e19c4f4e9a7d6b1e7c6868bed198ca75ac`

```dockerfile
```

-	Layers:
	-	`sha256:c41998b08aa2b9cb0cfac81c6e0490bdbd2d8c229d3c79bb731fe8795de103d1`  
		Last Modified: Thu, 22 Jan 2026 22:57:27 GMT  
		Size: 675.7 KB (675697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0b85a6d81976624636a26cb30b58e2ffcacec9fe183e01784076755bfd521d8`  
		Last Modified: Thu, 22 Jan 2026 22:57:28 GMT  
		Size: 3.2 MB (3190316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581203349af3cc6f84b42a578484fd02d49d3f201620d7bc5d6483e262390595`  
		Last Modified: Thu, 22 Jan 2026 22:57:27 GMT  
		Size: 3.0 MB (3036751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0341be1d0c8929656a274ac237e4bfcb635f6b03cefe531ccfeae319cc283a2`  
		Last Modified: Thu, 22 Jan 2026 22:57:27 GMT  
		Size: 60.3 KB (60308 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:b5280040e291d2b2632e95da0c63d991fd926570d185f01a00e0a09449bd5f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71714702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91580f5d9972bc4ad871a69585bc0461475d5889c0245d9e1ea3234e0d4c144b`
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

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a4a9faa63c613ed89d0f0a503d27c7380a6f6dfefa48e69c9fd689aac449c99d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 KB (60289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2202d015d4a38f31ce7a9cab1d20421cb8a7d70e0fb03c1bab4a591bd4c74c4`

```dockerfile
```

-	Layers:
	-	`sha256:b09344d70ed85a5a82c94c05ab8984f4a9794672f099e06603cef0d7f6e00b96`  
		Last Modified: Thu, 22 Jan 2026 22:58:57 GMT  
		Size: 60.3 KB (60289 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:076bf7c0a6019e0f54d7215e1df1dfca682656f4a1fe9fdac6819f26b67f128a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70811358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c38626b3a2ce2389321a4fb21fbd1df48d7699b7bbda3c0abb77cc9ce6d8a19`
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

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:60328568151a2d5d4fecaaeac564bf4fb20cc642f10a148d9fc89fb828b45e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18ea90391124ab78d3c688bbf7302566c690f00ba2d00d9c3bdbfe0d9ee9e0c`

```dockerfile
```

-	Layers:
	-	`sha256:496cd94fa15d2a8d7ba63e6a9ee543937aa8e58cc83ce88d009ef63669233e20`  
		Last Modified: Thu, 22 Jan 2026 22:57:06 GMT  
		Size: 670.8 KB (670840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04db7bafbb3da04e4a263f3983228886f9d391d14c145b47fa5311f5fabf4822`  
		Last Modified: Thu, 22 Jan 2026 22:57:07 GMT  
		Size: 3.1 MB (3056807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66a25aca52ec5839da9e2bd3cce3c1b8583e26e239fcf5987dd0bde751980e62`  
		Last Modified: Thu, 22 Jan 2026 22:57:07 GMT  
		Size: 2.9 MB (2901913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d52edae12d39e858dd21fcabe33e7fc295f3a80f85b270e27c5791f95828ea3`  
		Last Modified: Thu, 22 Jan 2026 22:57:06 GMT  
		Size: 60.5 KB (60505 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:f239433491ee1652accd9779a3e3a35bffeb36f9b0ec23f37ea9181126224a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82533110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2492950a8e7d96161deb420e0be0fadf6831e6372c3cfe34112360c917792a`
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

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2c952ef867bab2ad9e48d1b2ee12e8493c6414acadd4478701bbd6c301bfbd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7036049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bc5408dfd1c783c01d410c79a486a1b9d0c4da630a163e9d59fb31f40a6ff2`

```dockerfile
```

-	Layers:
	-	`sha256:49b5af7222f59c32c593556a16d4c088e6d6a3169622806798363d0cbd4c3796`  
		Last Modified: Thu, 22 Jan 2026 22:55:37 GMT  
		Size: 675.8 KB (675840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dbf75653b74a52a6ed4b9d2c03549d79a0899ca2116a21d484136c1a8992820`  
		Last Modified: Thu, 22 Jan 2026 22:55:37 GMT  
		Size: 3.2 MB (3227275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1613fbeaf461f94868c50415bab45f1de62296d1b29b2a3461c1b836510fc00e`  
		Last Modified: Thu, 22 Jan 2026 22:55:37 GMT  
		Size: 3.1 MB (3072387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de8552f07a4de1f43509d8e7f0ce2d1a784046eaebcb51c00e64a6419207876`  
		Last Modified: Thu, 22 Jan 2026 22:55:37 GMT  
		Size: 60.5 KB (60547 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:a5890e32bbb15a893e5f836b0680fde5f7960704207116f363f857c1bf92c12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73132043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e1ce671b9b81a0bc4a163467b5a8f5fd30c9ecdafce9ce994223fc76549855`
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

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:919eb30a9bc8937ecf0d1102dd97c968cddcab13e0bbf1e72e5db222884cfce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6914527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13e9dba7fa25541539fe416726df9c2d3b003d359d2b4f923cdb110264084c7`

```dockerfile
```

-	Layers:
	-	`sha256:be3a092cf9eb0d16f246897ed2ddf25053e81507a5af67fcc060310c93f32710`  
		Last Modified: Thu, 22 Jan 2026 22:57:27 GMT  
		Size: 670.7 KB (670692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c104a71533b4df55e9afc7a62b52e1ca03efb90fa40ae6c8381ed897de804721`  
		Last Modified: Thu, 22 Jan 2026 22:57:27 GMT  
		Size: 3.2 MB (3168569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f1d003470a85324e479a4d40f02929881061ff6045b9cf6f2c8ccaa518a01fd`  
		Last Modified: Thu, 22 Jan 2026 22:57:27 GMT  
		Size: 3.0 MB (3015008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c241bd41c0bc0fa5d85eec71f30f95cc413d9f626e2b61feb41d37d9b810338`  
		Last Modified: Thu, 22 Jan 2026 22:57:27 GMT  
		Size: 60.3 KB (60258 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:66693d62fbc0bb504d0f2cb55954d58b5daf130708856fac3edeef557339a072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74774550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60f0e48986694f6d27f99676cc5a4c3910a83b893925977ffb4e964cb988905`
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

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:43c7eb5a5e1b9da7ef16cdd6c8fc12e23fe2435fcca11637ffa3f73e67c2a773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6937727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db68b7394dc130461f0d6c26e5e925548f16a5c666c562db5922e8c79d84be4b`

```dockerfile
```

-	Layers:
	-	`sha256:58b695f78bfcb3e28e3caeea4af54fe52cc8419434132fa9b83847b74f69d18d`  
		Last Modified: Thu, 22 Jan 2026 22:57:29 GMT  
		Size: 670.8 KB (670837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dae117cc6e67d0d0c8a5686b457d1db71c5721b747a497b0163b0657fa5b624d`  
		Last Modified: Thu, 22 Jan 2026 22:57:29 GMT  
		Size: 3.2 MB (3180710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa3e7c7a55b3a8d855aa9236ab1b1cff1e2a2fcd0e572d234a4cc51e291c771e`  
		Last Modified: Thu, 22 Jan 2026 22:57:29 GMT  
		Size: 3.0 MB (3025810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad3e8d4299775e7455e3d1785c39d6f0084e48fd7d21a355c124d00da4a84f24`  
		Last Modified: Thu, 22 Jan 2026 22:57:29 GMT  
		Size: 60.4 KB (60370 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:4577d178c0c724e9640ca11b181bd18164681fc2580c178a0c6a7042eae8f3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78638883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c4704ab7fb6b89d984e02475e61bc59c10825a27f7731bfcb7b29a458f04d6`
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

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:569a1290995087e67a0802b12fa4317bd2390db8ac0c341f1426f1efa23af97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7016945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919133278ccde47002f7a830cb7a9fd63aac110f3b86990c1074ee1db0de9798`

```dockerfile
```

-	Layers:
	-	`sha256:7ccbc6fc9d43de9bb40874376b25ff7d7704435047def9fdae7e9c6348004e69`  
		Last Modified: Mon, 19 Jan 2026 05:55:53 GMT  
		Size: 673.8 KB (673806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44c10f3935b85ea56652d75efd0a563bb040fcfb5613125da2259aae448e902`  
		Last Modified: Mon, 19 Jan 2026 05:55:53 GMT  
		Size: 3.2 MB (3218825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca64c44b0d085fe8305cbaab50e0b04bddedbecfeef89cb24392a606966948ae`  
		Last Modified: Mon, 19 Jan 2026 05:55:53 GMT  
		Size: 3.1 MB (3063937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4c3984dbd143301fbb962d130cc19a29e459378d3408d0718922a4297b68369`  
		Last Modified: Mon, 19 Jan 2026 05:55:52 GMT  
		Size: 60.4 KB (60377 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:35be47865628966944f70c133a4e356b9665b3795bbbe906eae232d52e08ef62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72886446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edba8cb21d40830c728c093cd46c216052b56a4439cf471837c2f189152f15b9`
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

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:eabc975cb8b251fc9d754556074fd1d8eab28a4520b8f720e4458c8635cf64f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6714109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3877795ecb9fcd92b0c32122b781e01c4cdbf00c43415d11059e7afb6f054b3`

```dockerfile
```

-	Layers:
	-	`sha256:0277f296350e8358dd4ba13ae7680bc0b47340cda5ac076a03aadbe14285c9b3`  
		Last Modified: Thu, 22 Jan 2026 22:58:19 GMT  
		Size: 670.8 KB (670803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1a24926c60a225a99a03914d669914c25f0cb220b8b37388fa87b64c9f6c42a`  
		Last Modified: Thu, 22 Jan 2026 22:58:19 GMT  
		Size: 3.1 MB (3068934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3188e12d065b9db187c08087e3c441f846b4d027d898c4bcbba7edc57968eafe`  
		Last Modified: Thu, 22 Jan 2026 22:58:20 GMT  
		Size: 2.9 MB (2914064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76bb08bab31435f2a875ce9a490880bbc7d60ef048e7dbb727b7d3a6a398b5e`  
		Last Modified: Thu, 22 Jan 2026 22:58:19 GMT  
		Size: 60.3 KB (60308 bytes)  
		MIME: application/vnd.in-toto+json
